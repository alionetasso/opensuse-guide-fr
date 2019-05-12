---
layout: default
title: 7. Segurança e root - segurança básica e trabalhando como o usuário root
permalink: seguranca
---

# 7. Segurança e root

O openSUSE (e o GNU/Linux em geral) é um sistema operacional bastante seguro. Mas ao usar qualquer computador conectado à Internet, você deve sempre ser cuidadoso.

## 7.1 O usuário root

Um dos motivos pelos quais o GNU/Linux é tão seguro é que normalmente você não usa o sistema com permissões de administrador — apenas o usuário *root* tem permissões de administrador completas.

A senha do usuário *root* será perguntada a você sempre que for instalar pacotes ou executar outras tarefas administrativas fora da sua pasta pessoal (/home/seunomedeusuario/). A menos que você tenha desmarcado aquela opção durante a instalação, a senha do usuário *root* é igual à senha do seu usuário comum.

{% include note.html note="Apenas trabalhe como *root* quando for absolutamente necessário." %}

### 7.1.1 Gerenciador de arquivos modo root

Para trabalhar graficamente com arquivos do sistema que requerem permissões de administrador, você pode iniciar o gerenciador de arquivos Dolphin em modo *root*.

{% include screenshot.html image="super-user-dolphin" %}

### 7.1.2 Trabalhando como usuário root no terminal

O comando a seguir é usado para alternar para o usuário *root* em um terminal:

<div class="cl">su -</div><p></p>

{% include tip.html tip="Nada aparecerá na tela enquanto você digita a senha. Isso é intencional." %}

Para parar de trabalhar como *root*, execute o seguinte comando:

<div class="clroot">exit</div>

Para executar apenas um único comando como *root*, você pode usar:

<div class="cl">su -c "[command]"</div>

Você pode ler mais sobre como usar o terminal no próximo capítulo.

## 7.2 Atualizações de segurança

Quando houver novas atualizações disponíveis, você será notificado pelo miniaplicativo de atualização, que fica na área de notificação:

{% include screenshot.html image="pk-updater" %}

### 7.2.1 Instalando atualizações pelo terminal

Para instalar apenas atualizações oficiais de segurança e correções de falhas, execute:

<div class="clroot">zypper patch</div>

Para instalar atualizações oficiais e também atualizações de repositórios de terceiros, execute:

<div class="clroot">zypper update</div>

## 7.3 Firewall

A instalação padrão do openSUSE inclui um *firewall* ('firewalld'). Por padrão, ele permite todas as conexões de saída e bloqueia qualquer conexão de entrada. Portanto, você só precisará mudar a configuração se desejar executar servidores. O *firewall* pode ser configurado pelo YaST, leia sobre o YaST em um capítulo mais adiante.

## 7.4 Vírus e spyware

Não há necessidade de rodar um antivírus ou varrer o sistema em busca de *spyware*. *Malwares* que se espalham pela Internet e afetam usuários normais de computadores domésticos praticamente não existem para GNU/Linux. Apenas se certifique de não instalar e executar *softwares* ou *scripts* de desconhecidos e estará seguro.
