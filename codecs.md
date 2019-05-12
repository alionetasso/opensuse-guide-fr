---
layout: default
title: 13. Multimedia Codecs - Install Support for restricted codecs including MP3, DVD, WMA, WMV, MOV etc.
permalink: codecs
---

# 13. Multimedia Codecs

This chapter describes two different methods for installing the packages needed to playback most multimedia formats - including MP3, DVDs etc., with the default media players Dragon and VLC. You can use manual 1-click installation or use the command line - whichever method you prefer.

By default only free, open, non-patent encumbered formats such as Ogg Theora, Ogg Vorbis and Flac are supported for legal reasons (US software patents and Digital Millennium Copyright Act (DMCA)).

## 13.1 Codec Installation with 1-Click

1) Click on the button below to add the necessary repositories and install the required packages with 1-click install.

{% include ymp.html icon="codecs" link="http://opensuse-community.org/codecs-kde.ymp" %}

{% include tip.html tip="If a conflict dialog appears, select to install the packages *with* Vendor Change." %}

2) Afterwards make sure all your multimedia packages are coming from the Packman Repository:

<div class="path">Start YaST Software Management => Click on View => Click on Repositories => Select the Packman Repository => Click "Switch system packages" => Click "Accept"</div><p></p>

{% include screenshot.html image="packman-vendorchange" %}

## 13.2 Codec Installation in the Terminal

To install codecs using the terminal instead, do these steps:

{% include tip.html tip="Use Copy/Paste to avoid typos. To paste in Konsole right click mouse => Paste - or use **Ctrl+Shift+V**." %}

1) Add the needed repositories:

<div class="clroot">zypper addrepo -f http://packman.inode.at/suse/openSUSE_Leap_15.0/ packman</div>
<div class="clroot">zypper addrepo -f http://opensuse-guide.org/repo/openSUSE_Leap_15.0/ dvd</div>

2) Then install the necessary packages:

<div class="clroot">zypper install ffmpeg lame gstreamer-plugins-bad gstreamer-plugins-ugly gstreamer-plugins-ugly-orig-addon gstreamer-plugins-libav libdvdcss2 vlc-codecs</div>

You will be asked if you want to allow vendor change for some packages - allow it (usually means picking solution 1 of the offered solutions).

3) Make sure all your multimedia packages are coming from the Packman Repository:

<div class="clroot">zypper dup --from http://packman.inode.at/suse/openSUSE_Leap_15.0/</div>
