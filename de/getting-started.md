---
title: "Erste Schritte"
description: "Konto anlegen, Vythea installieren, anmelden und die erste Frage stellen."
---

Vythea ist ein KI-Agent, der bereitsteht, während du arbeitest: ein Fenster und derselbe Agent im Terminal. Er liest und schreibt Dateien, führt Befehle aus (nach Rückfrage), macht sich auf deiner Festplatte Notizen über dich und spricht mit den Modellen, die du auswählst.

## 1. Konto anlegen

[Registriere dich](https://vythea.com/signup) auf vythea.com. Solange Vythea in der Alpha ist, ist der Download an ein Konto gebunden; das Konto trägt außerdem dein Guthaben für die von Vythea gehosteten Modelle, deinen Tarif und deine Teams.

## 2. Installieren

Öffne [Download](https://vythea.com/dashboard/download) im Dashboard. Die Seite bietet zuerst dein eigenes System an:

- **macOS** (13 oder neuer, Apple Silicon): Kopier den einzeiligen Befehl und füg ihn ins Terminal ein. Er installiert Fenster und Terminal und öffnet Vythea, ohne Warnung, die du wegklicken musst. Oder öffne die .dmg und zieh Vythea in den Ordner „Programme“; beim ersten Mal sagt macOS vielleicht, es könne Vythea nicht überprüfen: Schließ die Meldung, öffne Systemeinstellungen › Datenschutz & Sicherheit, klick neben Vythea auf **Dennoch öffnen** und bestätige. Das ist nur einmal nötig.
- **Windows** (11, x64): Lade die .zip herunter, entpacke sie und führe `vythea.exe setup` aus – oder kopiere den Einzeiler und füge ihn in PowerShell ein; er erledigt beides.
- **Linux** (x64, glibc 2.31 oder neuer): Lade die .tar.gz herunter, entpacke sie und führe `./vythea setup` aus – oder füge den Einzeiler in ein Terminal ein.

Nichts braucht Administratorrechte, und außer der App im Ordner „Programme“ auf einem Mac landet nichts außerhalb deines eigenen Benutzerkontos auf dem Rechner.

## 3. Einrichten

`vythea setup` fragt, wie es dich nennen soll, meldet dich an, wählt ein Gateway und ein Modell und installiert das Fenster, das Terminal oder beides dort, wo du willst. Führe es jederzeit erneut aus, um die Antworten zu ändern. Unter Windows und Linux erscheint die App danach im Startmenü bzw. im Anwendungsmenü.

## 4. Anmelden

Die Anmeldung läuft über vythea.com: Die App öffnet die Seite für dich, oder du führst `/login` im Terminal aus. Der Rechner erscheint danach unter [Geräte](https://vythea.com/dashboard/devices).

## 5. Etwas fragen

Schreib eine Nachricht. Vythea antwortet mit dem Modell, das du gewählt hast, und fragt, bevor es einen Befehl ausführt oder eine Datei ändert. Die Kosten gehosteter Modelle werden von deinem Guthaben abgebucht; wie du stattdessen deine eigenen API-Schlüssel nutzt, steht unter [Gateways](gateways.md).
