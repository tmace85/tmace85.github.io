---
title:  Home Assistant auf dem PI 4
description: "Home Automation mit Home Assistant auf dem PI 4"
tags:
    - home assistant
    - howto
    - linux
---

Ich habe seit langem einen Raspberry 4, aus dem Jahr 2018. Was soll ich sagen, ist nicht mehr all zu aktuelle. Jetzt wurde ich von einem [Kumpel](https://sethiele.de/) auf das [Home Assistant](https://www.home-assistant.io/) Projekt aufmerksam gemacht. Davon habe ich natürlich schon mehrfach gehört, aber naja, nie die "Zeit gefunden" das mal anzugehen. Jetzt solls aber los gehen.

<sub>Disclaimer: In diesem Artikel sind [Affiliate Links](https://blog.hubspot.de/marketing/affiliate-links) enthalten. </sub>

## Voraussetzungen

* [Raspberry Pi 4 ModellB](https://amzn.to/3uKBk6E)
* [Raspberry 4596 Pi - offizielles Netzteil für Raspberry Pi 4 Model B](https://amzn.to/4856jZw)
* Eine SD Karte z.b. diese hier von [Sandisk](https://amzn.to/3uS995Q)
* ein [Gehäuse](https://amzn.to/3Ro9dlE)


## Installation

Für das Bespielen des Images auf die SD Karte, benötigt Ihr Ihr den [Raspberry Pi Imager](https://www.raspberrypi.com/software/). Ist eigentlich alles selbserklärend.     l

![raspberrypi_immager](/assets/images/raspberrypi_imager.png)

OS wählen -> "Other specifi-purpose OS" ->  Home assistants and home automation ->  Home Assistant

![raspberrypi_immager](/assets/images/raspberrypi_imager_ha.png)

Nun wird das ganze auf der SD Karte installiert. Bei mir musste ich vorher noch mit der Datenträgerverwaltung die SD Karte mit [FAT32 formatieren](https://www.diskpart.com/de/windows-11/windows-11-festplatte-fat32-formatieren.html).

Ich habe bei mir zu Haus eine [Ubiquiti UniFi Dream Machine](https://amzn.to/3Rybvjh) stehen und dort ist der [Raspberry Pi 4
](https://amzn.to/3uKBk6E) per LAN Kabel angeschlossen. Das erspart mit die WiFi Konifguration. Da daucht er dann auch auf.

![rasbperrypi](/assets/images/raspberrypi_unify.png)

## Einrichtung Home Assistant

Die WUI kann via http://homeassistant.local:8123 aufgerufen werden. Dort wird man nun von dem Onboarding Screen begrüßt.

![ha_setup](/assets/images/ha_setup.png)

Nun soll ich erstmal eine Benutzer anlegen. Nix leichter als das.

![ha_user](/assets/images/ha_user.png)

Und natürlich will man meinen Standort wissen, aber Amsterdam ist es eigentlich nicht.

![ha_location](/assets/images/ha_location.png)

Klar, ein paar Statistiken dürfen auch nicht fehlen.

![ha_stats](/assets/images/ha_stats.png)

Jetzt wurden auch noch ein paar Geräte in meinem Netzwerk erkannt. Viel kann es nicht sein, da ich ein eigenes IOT Netzwerk habe, was per default keinen Zugriff auf das Netzwerk vom [Raspberry Pi 4](https://amzn.to/3uKBk6E) getrennt sind. Ein paar Bluetooth Geräte wurden dann doch gefunden.

![ha_devices](/assets/images/ha_devices.png)

Damit ist das Setup abgeschlossen und es geht die spezielle Konfiguration. Ich werde dort mal etwas rumspielen und dann gegebenfalls mehrer Artikel dazu veröffentlichen.

Quelle der Inspiration war der [Original Artikel]( https://www.home-assistant.io/installation/raspberrypi/#install-home-assistant-operating-system)
