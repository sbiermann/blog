---
title: "Materialflut"
date: 2013-10-15T21:25:00.000+02:00
categories:
    - "Raspberry Pi"
tags:
    ["Internetradio VE301"]
---

Nach dem der VE301 ausgeschlachtet und in Gedanken klar ist wie das ganze umgesetzt werden soll, geht es daran eine Materialliste aufzustellen. Doch das ist gar nicht so ganz einfach, viele Kleinigkeiten müssen bedacht werden.

<!--more-->

### Wissen vergangener Tage

Ich habe viel im Internet recherchiert um die richtigen Komponenten zu finden. Theoretisch könnte man die Taster, LEDs und Drehimpulsgeber direkt an die GPIO des Raspberry Pi anschließen aber das ist nicht so clever. Denn ein Taster kann "prellen" das heißt er sendet beim drücken ein mehrfaches öffnen und schließen bevor das Signal stabil wird. Nun muss man ihn entweder per Hardware oder Software entprellen. Auch muss man beachten wie viel Volt und Ampere die einzelnen Sachen haben und berechnen ob genug vom Raspberry Pi kommt oder extern zuliefern muss. Gut das ich das ganze während meiner Schulzeit schon alles gemacht habe, wenn man sich bloß daran erinnern könnte...


### Schritt für Schritt

Ich benutze den STEC11B um die Wahl der Sender zu ermöglichen. Da dieses Bauteil aber sehr klein ist und nur wenige Grad pro Schritt dreht, ist es nur schwer möglich die Drehscheibe mit der "grafischen" Anzeige der Sender passend mechanisch zu drehen. Daher viel die Entscheidung das ganze per Schrittmotor anzusteuern.


### Laut muss es sein

Da die Soundkarte des Raspberry Pi nicht die optimalste sein soll, werde ich, wie die meisten auch, eine USB Soundkarte verwenden. Neben der Soundkarte kommt ein 100 Watt Breitbandlautsprecher im passenden Format zum Einsatz. Beides wird mittels eines digitalen Verstärkers mit einander verbunden. Ein Röhrenverstärker wär natürlich besser im Klang aber der TDA8920 bietet ein sehr gutes Preis/Leistungs Verhältnis.


### Hardware

Nun zu der Liste mit den Teilen. Ich hab die Liste in Hardware und Bauelemente unterteilt, das macht das ganze übersichtlicher. Zu der Hardware zähle ich auch fertige Schaltungen wie zum Beispiel den Verstärker.

*   Raspberry Pi
*   USB Soundkarte
*   WLAN USB Adapter
*   2 Kanal 5V Relais Module
*   Schaltnezteil, 68W, 8A, 5/24V
*   TDA8920 Class D Verstärker
*   Lautsprecher Beyma 10 AG/N
*   28BYJ48 Schrittmotor mit ULN2003 Driver Board


### Bauelemente

Neben der Hardware benötige ich noch einige Bauelemente, die im folgenden aufgelistet sind.

*   Netzkabel
*   Kabel für Versorgung der Elemente
*   Steckbrücken Drähte
*   Widerstände (10k, 300 und 40 Ohm)
*   LEDs (grün, gelb, rot)
*   logarithmischen Drehpoti 100K Ohm für Lautstärke
*   STEC11B Drehimpulsgeber für die Senderauswahl
*   Kurzhubtaster für Ein- und Ausschalten sowie Reset
*   Stufendrehschalter als Pseudo Ein- und Ausschalter
*   Lochrasterplatinen zum befestigen der Taster
*   GPIO Flachbandkabel
*   Adafruit Half-size Perma-Proto Breadboard um einfacher an die GPIO des Raspberry Pi zu kommen

Da die ganzen Sachen bestellt sind und teilweise sogar aus China direkt versendet werden, wird es wohl ein paar Tage dauern bis ich alle Teile zusammen habe.
