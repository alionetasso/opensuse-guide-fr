---
layout: default
title: 16. Installation des pilotes sans-fil - Faire fonctionner votre matériel Wifi Broadcom, Ralink, etc.
permalink: wlan
---

# 16. Installation des pilotes Wifi

La plupart du temps, le Wifi fonctionnera sans action de votre part. Dans ce cas, vous pourrez configurer votre carte wifi en utilisant l'appliquette NetworkManager que vous trouverez dans votre barre des tâches.

{% include screenshot.html image="pnm" %}

## 16.1 Trouvez le modèle de la carte Wifi

Si votre carte Wifi ne fonctionne pas directement, il est fort probable que vous parveniez à corriger cela facilement.

La première étape est de lancer la commande suivante afin d'identifier la puce présente sur la carte. C'est bien le modèle de puce qui importe, le fabriquant et le modèle de la carte elle-même importe peu.

<div class="clroot">hwinfo --wlan --short</div><p></p>

{% include screenshot.html image="hwinfo" %}

Maintenant que vous connaissez le type de puce présente sur la carte Wifi, il est temps de découvrir ce qui manque pour la faire fonctionner sous openSUSE ; généralement vous avez juste besoin d'installer un pilote et/ou des firmwares.

## 16.2 Les puces Broadcom récentes

Le noyau Linux embarque le pilote [brcm80211 driver](http://linuxwireless.org/en/users/Drivers/brcm80211) par défaut. Ce pilote prend en charge les puces **bcm4313, bcm43224, bcm43224, bcm43225, bcm4329, bcm4330, bcm4334, bcm43241, bcm43235 (>= rev 3), bcm43236 (>= rev 3), bcm43238 (>= rev 3), bcm43143, bcm43242**.

Si vous rencontrez des problèmes avec le pilote ci-dessus et que vous avec l'une des puces suviantes : **bcm4312, bcm4313, bcm4321, bcm4322, bcm43224, bcm43225, bcm43227, bcm43228** il vous faut installer le pilote propriétaire [broadcom-wl driver](https://www.broadcom.com/support/802.11) (paquet: *broadcom-wl*) présent dans le dépôt Packman.

## 16.3 Ancienne puce Broadcom

Si vous avez un puce Broadcom plus ancienne, [prise en charge par le pilote libre, développé par rétro-ingéniérie, b43](http://linuxwireless.org/en/users/Drivers/b43#Supported_chip_types), à savoir : **bcm4303, bcm4306, bcm4309, bcm4311, bcm4318**, il vous faudra seulement installer ce firmware. Cela peut se faire automatiquement en exécuter simplement cette commande suivie d'un redémarrage (assurez-vous que le paquet *b43-fwcutter* est bien installé et que vous disposez d'une connexion réseau active en lançant la commande) :

<div class="clroot">install_bcm43xx_firmware</div>

## 16.4 Puces Atheros

Atheros travaille avec les développeurs du noyau Linux afin de fournir une prise en charge de leurs puces Wifi par le noyau Linux standard, via les pilotes [ath5k](http://linuxwireless.org/en/users/Drivers/ath5k#supported_chips) et [ath9k](http://linuxwireless.org/en/users/Drivers/ath9k#supported_chipsets), en conséquence la plupart des cartes Atheros devraient fonctionner sans encombres.

## 16.5 Puces Intel

Intel coopére bien avec les développeurs Linux et l'ensemble de leurs puces Wifi fonctionnent sans soucis.
