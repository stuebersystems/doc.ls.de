# Landesstatistik 2021/22

Hier finden Sie die jeweils aktuellste Version der Landesstatistik **inklusiver aller kurzfristig veröffentlichten Korrekturen während einer Statistikphase**.

Für die Statistik benötigen Sie mindestens die Versionen MAGELLAN 8.0.X (XX.XX.2021) und DAVINCI 6.X.XX (XX.XX.2021)

## [**Downloadlink**](https://my.hidrive.com/share/)

## aktuelle Änderungen

!!! info "Hinweis"

     Eine Anleitung zum Austausch der einzelnen Dateien finden Sie im Abschnitt ["Wie genau tauscht man die Dateien aus?"](#wie-genau-tauscht-man-die-dateien-aus)!

## Aktuellste Ausgabe ist die 8.0.X (XX.XX.2021)

Diese Ausgabe beinhaltet alle vorangegangenen Änderungen

---

## Wie genau tauscht man die Dateien aus

!!! info "Hinweis"

    Vorausgesetzt wird immer die zuletzt veröffentlichte Programmversion. Liegt das letzte Änderungsdatum vor dem Veröffentlichungsdatum unserer Standardausgabe, sind die Änderungen für die Statistik alle im Standardupdate mit enthalten! Das Ausgabedatum der letzten MAGELLAN-Version sehen Sie in unserer [Changelog-Datei](https://doc.magellan.stueber.de/changelog/changelog/).

Was soll getauscht werden|Anmerkungen

Datei|Anleitung
--|--
**Schlüssel (*.keys) generell**|Dateien mit der Endung \*.keys gehören auf den Serverrechner in den dortigen Unterordner `Importe > Ihr Bundesland`. Wo sich dieser Ordner genau in Ihrem System befindet, sehen Sie über den Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner`. <br/><br/>Diese Datei fügen Sie, einige sind sicherlich davon bereits mit gleichem Namen vorhanden, Sie überschreiben diese. Anschließend lesen Sie die Schlüssel über den Magellan-Administrator auch ein, unter `Datenimporte > Schlüsselverzeichnisse importieren > Ihr Bundesland, Ihre Schulart`. Sie können alle Schlüsseldateien importieren oder auch nur eine Datei, dazu ändern Sie "alle Kataloge" ab und wählen gezielt die gewünschte Importdatei.
**Schlüssel "00_Postleitzahlen.keys" und "00_Gemeinden.keys"**|Dateien mit der Endung *.keys gehören auf den Serverrechner in den dortigen Unterordner `Importe > Deutschland > PLZ`. Wo sich dieser Ordner genau in Ihrem System befindet, sehen Sie über den Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner`.<br/><br/>Diese Datei fügen Sie, einige sind sicherlich davon bereits mit gleichem Namen vorhanden, Sie überschreiben diese. Bitte lesen Sie die Dateien vor der Statistikerstellung ein, eine Anleitung dazu finden Sie in der Dokumentation für die Landesstatistik im Abschnitt [Postleitzahlverzeichnisse aktualisieren](https://doc.ls.stueber.de/schluesselverzeichnisse/#postleitzahlverzeichnisse-aktualisieren).<br>**Bitte beachten Sie die Abschnitte  "Postleitzahlverzeichnis importieren", "Gemeinden synchronisieren" und "Vollständigkeit der Gemeindekennziffern für Schüler überprüfen"!**
**Skripte**| \*.dws oder \*.int: Dateien mit der Endung \*.dws oder *.int  gehören auf den Serverrechner in den dortigen Unterordner Skripte (Achtung: nicht in den Bundeslandunterordner, sondern direkt in den Skripteordner).<br/><br/>*.xml: Dateien mit der Endung *.xml gehören auf den Serverrechner in den dortigen Unterordner `Skripte > Ihr Bundesland`. <br/><br/>Wo sich der Ordner Skripte genau in Ihrem System befindet, sehen Sie über den Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten|Verbindung markieren > Bearbeiten > Unterkarte Datenordner`.
**Magellan.exe**|Das Nutzen dieser Magellan.exe setzt mindestens die aktuellste Version voraus. Nehmen Sie die Statistikarbeiten in der Schule an der aktuellen Datenbank vor oder in einer zweiten Umgebung, also zum Beispiel auf einem Extrarechner, auf den die Datenbank übertragen wird? Wenn Sie es im Schulnetzwerk machen, dann müssten bitte die Rechner alle (erst der Server, dann die Arbeitsplätze) auf die aktuelle Version aktualisiert werden, anschließend fügen Sie diese Magellan.exe auf dem Rechner ins Programmverzeichnis ein, auf dem Sie die Statistik erstellen möchten.<br><br>Nutzen Sie ein Zweitsystem aktualisieren Sie diesen Rechner und ersetzen dann bitte die Magellan.exe mit der neuen Datei.<br/><br/>Die Magellan.exe finden Sie bei 64Bit-Betriebssystem unter `C:\Program Files (x86)\Stueber Systems\MAGELLAN 8`, bei einem 32 Bit Betriebssystem unter `C:\Programme\Stueber Systems\MAGELLAN 8`.

Nehmen Sie die Statistikarbeiten in der Schule an der aktuellen Datenbank vor oder in einer zweiten Umgebung, also zum Beispiel auf einem Extrarechner, auf den die Datenbank übertragen wird? Wenn Sie es im Schulnetzwerk machen, dann müssten bitte die Rechner alle \(erst der Server, dann die Arbeitsplätze\) auf die aktuelle Version aktualisiert werden, anschließend fügen Sie diese Magellan.exe auf dem Rechner ins Programmverzeichnis ein, auf dem Sie die Statistik erstellen möchten.

Nutzen Sie ein Zweitsystem aktualisieren Sie diesen Rechner und ersetzen dann bitte die Magellan.exe mit der neuen Datei.

Die Magellan.exe finden Sie bei  64-Bit Betriebssystemen unter `C:\Program Files \(x86\)\Stueber Systems\MAGELLAN 8`, bei  32 Bit Betriebssystemen unter `C:\Programme\Stueber Systems\MAGELLAN 8`.

---

## Archiv

-
