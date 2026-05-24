---
title: "Internetradio VE301 fertig... so gut wie"
date: 2014-03-09T21:20:00.001+01:00
categories:
    - "Raspberry Pi"
tags:
    ["Internetradio VE301"]
---

Es ist ja doch eine Weile vergangen seit meinen letzten Posting. Seit dem mein Sohn Ende Januar auf die Welt gekommen ist, habe ich auch ziemlich wenig Zeit. Daher habe ich die Zeit vor der Geburt nicht zum schreiben von Blogeinträgen genutzt, sondern zum basteln am VE301. Das Ergebnis kann sich sehen lassen, aber lest selbst.

<!--more-->

### Schritt für Schritt

Was noch fehlte war der Anschluss des Drehimpulsgebers an den Pi. Die Schaltung habe ich gemacht und das ganze mit einen Python Skript getestet. Funktionierte auch so ziemlich gleich auf Anhieb, wenn man von der kleinen fehlerhaften Lötstelle absieht die mich einige Zeit gekostet hat. Im Internet habe ich eine gute [Anleitung](http://www.raspberrypi-spy.co.uk/2012/07/stepper-motor-control-in-python/) gefunden wie man einen Schrittmotor ansteuert. Gekoppelt mit dem Drehimpulsgeber dreht sich nun die Senderskala fleißig hin und her.


### Modul

Da mir das Beispielskript aus der Anleitung etwas zu lang war, habe ich ich mich dazu entschlossen ein Modul für Python zu schreiben. Dieses Modul abstrahiert das ganze so, dass es nur noch 2 Methoden gibt, `rotate_clockwise(numberOfSteps)` für drehen im Uhrzeigersinn und `rotate_counterwise(numberOfSteps)` für gegen den Uhrzeiger. Dazu gibt es noch eine Installationsroutine und schon ist das Modul fertig. Python macht es da einen sehr leicht. Das Skript habe ich als neues Projekt auf [GitHub](https://github.com/sbiermann/steppercontrol) veröffentlicht.


### Senderskala

Wie schon weiter oben geschrieben dreht der Schrittmotor die Senderskala. Ich habe lange überlegt wie meine Skala aussehen soll oder wie es umsetze. Am Ende habe ich mich dafür entschieden die original Senderskala zu benutzen. Sieht wie ich finde am besten aus. Zusätzlich habe ich per Suchmaschine des Vertrauens noch herausgefunden, dass es früher wohl zusätzliche [Senderskalen](http://www.radiomuseum.org/forumdata/users/4061/vez10a.jpg) zum aufkleben gab. So etwas werde ich auch machen.


### Sender

Beim Drehen des Schrittmotors wird nicht immer die exakt selbe Position angefahren. Ich nehme an dies liegt daran wie ich die Senderskala befestigt habe. Ein Plastikstab von einen Luftballon ist wohl nicht optimal. Die Senderskala hat immer in 10er Schritten Zahlen, daher habe ich mir überlegt das meine Sender immer im Bereich von 0-10, 11-20, 21-30, usw. liegen. Dann ist es egal ob der Schrittmotor die Skala auf 25 oder 27 dreht.


### Ganz fertig dann doch noch nicht...

Jetzt fehlen nur noch die Sender. Zu Testzwecken habe ich ein paar Sender eingespeichert in der Playlist. Dies muss ich noch überarbeiten und weitere Sender hinzufügen. Die oben genannte zusätzliche Senderskala muss ich ebenfalls noch anfertigen und ausdrucken. Sowie noch die Schaltpläne ergänzen und vervollständigen. Sind aber alles nur Kleinigkeiten. Als nächstes werde ich wohl hier im Blog ein Video und Fotos vom VE301 veröffentlichen.
