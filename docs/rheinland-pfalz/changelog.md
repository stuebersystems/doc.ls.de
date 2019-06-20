# Landesstatistik 2018/19

Hier finden Sie die jeweils aktuellste Version der Landesstatistik **inklusiver aller kurzfristig veröffentlichten Korrekturen während einer Statistikphase**.

## Download

 [**Downloadlink**](https://my.hidrive.com/share/j0wxzj4-v2)

!!! info "Hinweis"

    Eine Anleitung zum Austausch der einzelnen Dateien finden Sie im Abschnitt ["Wie genau tauscht man die Dateien aus?"](https://doc.ls.stueber.de/rheinland-pfalz/changelog/#wie-genau-tauscht-man-die-dateien-aus)!

### Aktuellste Ausgabe ist die 6.5.27 - 671 (28.08.2018). Diese Ausgabe beinhaltet alle vorangegangenen Änderungen.

## Wie genau tauscht man die Dateien aus?

!!! warning "Wichtig"

     Vorausgesetzt wird immer die zuletzt veröffentlichte Programmversion. Liegt das letzte Änderungsdatum vor dem Veröffentlichungsdatum unserer Standardausgabe, sind die Änderungen für die Statistik alle im Standardupdate mit enthalten! Das Ausgabedatum der letzten MAGELLAN-Version sehen Sie in unserer [Changelog-Datei](https://doc.magellan6.stueber.de/changelog/).

Datei|Anleitung
--|--
**Schlüssel (*.keys) generell**|Dateien mit der Endung *.keys gehören auf den Serverrechner in den dortigen Unterordner `Importe > Ihr Bundesland`. Wo sich dieser Ordner genau in Ihrem System befindet, sehen Sie über den Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner`. <br/><br/>Diese Datei fügen Sie, einige sind sicherlich davon bereits mit gleichem Namen vorhanden, Sie überschreiben diese.
Anschließend lesen Sie die Schlüssel über den Magellan-Administrator auch ein, unter `Datenimporte > Schlüsselverzeichnisse importieren > Ihr Bundesland, Ihre Schulart`. Sie können alle Schlüsseldateien importieren oder auch nur eine Datei, dazu ändern Sie "alle Kataloge" ab und wählen gezielt die gewünschte Importdatei.
**Schlüssel "00_Postleitzahlen.keys" und "00_Gemeinden.keys"**|Dateien mit der Endung *.keys gehören auf den Serverrechner in den dortigen Unterordner `Importe > Deutschland > PLZ`. Wo sich dieser Ordner genau in Ihrem System befindet, sehen Sie über den Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner`.<br/><br/>Diese Datei fügen Sie, einige sind sicherlich davon bereits mit gleichem Namen vorhanden, Sie überschreiben diese.
Bitte lesen Sie die Dateien vor der Statistikerstellung ein, eine Anleitung dazu finden Sie in der Dokumentation für die Landesstatistik im Abschnitt "Postleitzahlverzeichnisse aktualisieren" (https://doc.ls.stueber.de/schluesselverzeichnisse/#postleitzahlverzeichnisse-aktualisieren). 
**Bitte beachten Sie die Abschnitte  "Postleitzahlverzeichnis importieren", "Gemeinden synchronisieren" und "Vollständigkeit der Gemeindekennziffern für Schüler überprüfen"!**
**Skripte**|*.dws oder *.int: Dateien mit der Endung *.dws oder *.int  gehören auf den Serverrechner in den dortigen Unterordner Skripte (Achtung: nicht in den Bundeslandunterordner, sondern direkt in den Skripteordner).<br/><br/>*.xml: Dateien mit der Endung *.xml gehören auf den Serverrechner in den dortigen Unterordner `Skripte > Ihr Bundesland`. <br/><br/>Wo sich der Ordner Skripte genau in Ihrem System befindet, sehen Sie über den Magellan-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten|Verbindung markieren > Bearbeiten > Unterkarte Datenordner`.
**Magellan.exe**|Das Nutzen dieser Magellan.exe setzt mindestens die aktuellste Version voraus. Nehmen Sie die Statistikarbeiten in der Schule an der aktuellen Datenbank vor oder in einer zweiten Umgebung, also zum Beispiel auf einem Extrarechner, auf den die Datenbank übertragen wird? Wenn Sie es im Schulnetzwerk machen, dann müssten bitte die Rechner alle (erst der Server, dann die Arbeitsplätze) auf die aktuelle Version aktualisiert werden, anschließend fügen Sie diese Magellan.exe auf dem Rechner ins Programmverzeichnis ein, auf dem Sie die Statistik erstellen möchten.
Nutzen Sie ein Zweitsystem aktualisieren Sie diesen Rechner und ersetzen dann bitte die Magellan.exe mit der neuen Datei.<br/><br/>Die Magellan.exe finden Sie bei 64Bit-Betriebssystem unter `C:\Program Files (x86)\Stueber Systems\Magellan 6`, bei einem 32 Bit Betriebssystem unter `C:\Programme\Stueber Systems\Magellan 6`.

---

## Archiv

### MAGELLAN

* FIX: RLP-BBS-Bewegung: In die Bewegungsdatei werden nur noch Schüler übernommen, für die unter `Schüler > Laufbahn > Abschluss > Abschluss1` eine Eintragung vorgenommen wurde. Damit werden BVJ-Schüler, die nach dem ersten Jahr in eine Klasse mit anderem Bildungsgang (8101050/8101060 ) wechseln nicht mehr für die Bewegungsdatei ausgegeben.

### Skripte

Eine Anleitung für alle unsere Berechnungsskripte finden Sie in der Dokumentation [MAGELLAN Landesanpassungen](https://doc.la.stueber.de).  
Hinweis für angepasste Skriptdateien: Mit der MAGELLAN-Version 6.5 wurde der Skriptingmechanismus auf eine neue Version aktualisiert. Welche Änderungen für von Schulen angepasste Skripte notwendig sind, beschreiben wir hier: [https://doc.magellan-scripting.stueber.de/anderungen/](https://doc.magellan-scripting.stueber.de/anderungen/)

* FIX: RLP-Statistik LehrerNeuanlage BBS 2018.xml
  * STALA-5600 
  * STALA-5160

  * FIX: "RLP-Statistik LehrerNeuanlage BBS 2018.xml":

  * STUEBER-15
  * STUEBER-16
  * STUEBER-17
  * STUEBER-18
  * STUEBER-19
  * STUEBER-20-1
  * STUEBER-20-2
  * MORGEN-170
  * STALA-5550
  * MORGEN-60
  * STUEBER-6
  
### Importe

* FIX: in der Datei "00_Postleitzahlen.keys" (unter `Import > Deutschland > PLZ`) wurde für alle Vorwahlen eine Führungsnull ergänzt. Bitte lesen Sie ggfs. die Datei neu ein, die Möglichkeit finden Sie im MAGELLAN Administrator.

* FIX: Die Dateien "00\_Postleitzahlen.keys" und "00\_Gemeinden.keys" wurden für die Region RLP überarbeitet.


!!! warning "Wichtig"

    Bitte lesen Sie die Dateien vor der Statistikerstellung ein, eine Anleitung dazu finden Sie in der Dokumentation für die Landesstatistik im Abschnitt [Postleitzahlverzeichnisse aktualisieren](https://doc.ls.stueber.de/schluesselverzeichnisse/#postleitzahlverzeichnisse-aktualisieren).
    Bitte beachten Sie die Abschnitte "Postleitzahlverzeichnis importieren", "Gemeinden synchronisieren" und "Vollständigkeit der Gemeindekennziffern für Schüler überprüfen"!