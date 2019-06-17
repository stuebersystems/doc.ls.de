# Landesstatistik 2018/19

Hier finden Sie die jeweils aktuellste Version der Landesstatistik **inklusiver aller kurzfristig veröffentlichten Korrekturen während einer Statistikphase**.


## [**Downloadlink**](https://my.hidrive.com/share/329e.t1a8q)

## aktuelle Änderungen

FIX: SHL-Statistik DATSA 2018 Skriptfehler REGEL SA9501


> #### primary::Hinweis
>
> Eine Anleitung zum Austausch der einzelnen Dateien finden Sie im Abschnitt ["Wie genau tauscht man die Dateien aus?"](https://doc.ls.stueber.de/nordrhein-westfalen/changelog.html#wie-genau-tauscht-man-die-dateien-aus)!

##**Aktuellste Ausgabe ist die 6.5.28 - 14. September 2018 
Diese Ausgabe beinhaltet alle vorangegangenen Änderungen**
---
## Wie genau tauscht man die Dateien aus?


> #### danger::Achtung!
>
> Vorausgesetzt wird immer die zuletzt veröffentlichte Programmversion. Liegt das letzte Änderungsdatum vor dem Veröffentlichungsdatum unserer Standardausgabe, sind die Änderungen für die Statistik alle im Standardupdate mit enthalten! Das Ausgabedatum der letzten MAGELLAN-Version sehen Sie in unserer [Changelog-Datei](https://doc.magellan6.stueber.de/changelog.html).
 

Was soll getauscht werden|Anmerkungen
---|---
**Pfade in MAGELLAN**|Die entsprechenden Pfade zu Ihren Dokumenten, Skripten und Importdateien können Sie im MAGELLAN-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner` einsehen.
**Schlüssel**| Dateien mit der Endung **\*.keys** sind Ihre Schlüsseldateien für den Import der aktuellen Statistikschlüssel. Diese gehören auf den Serverrechner in den dortigen Unterordner Importe\Rheinland-Pfalz.<br/><br/>Fügen Sie diese Dateien dort ein und überschreiben Sie ggf. bereits existierende Schlüsseldateien. Anschließend lesen Sie die Schlüssel über den MAGELLAN-Administrator unter `Datenimporte > Schlüsselverzeichnisse importieren > Schleswig-Holstein > Ihre Schulart` ein. Sie können alle Schlüsseldateien importieren oder auch nur eine Datei, dazu ändern Sie "alle Kataloge" ab und wählen gezielt die gewünschte Importdatei.
**Skripte**|**\*.dws oder \*.int**<br/>Dateien mit der Endung **\*.dws oder \*.int** gehören auf den Serverrechner in den dortigen Unterordner Skripte \(**Achtung**: Nicht in den Bundesland-Unterordner, sondern direkt in den Skripteordner\).<br/><br/>**\*.xml** Dateien mit der Endung **\*.xml** gehören auf den Serverrechner in den dortigen Unterordner Skripte\Schleswig-Holstein. Bitte beachten Sie, dass die Dateien mit diesem Schritt lediglich hinterlegt sind und erst noch in Ihren Datenbank importiert werden müssen. Eine Anleitung zum Schlüsselimport finden Sie [hier](https://doc.ls.stueber.de/schluesselverzeichnisse.html).
**Magellan.exe**|Das Nutzen einer neuen Magellan.exe setzt mindestens die aktuellste Version voraus. Das letzte und aktuelle Serviceupdate finden Sie in unseren [Downloads.](http://magellan.stueber.de/download.php). <br/><br/>Nehmen Sie die Statistikarbeiten in der Schule an der aktuellen Datenbank vor oder in einer zweiten Umgebung, also zum Beispiel auf einem Extrarechner, auf den die Datenbank übertragen wird? Wenn Sie es im Schulnetzwerk machen, dann müssten bitte die Rechner alle \(erst der Server, dann die Arbeitsplätze\) auf die aktuelle Version aktualisiert werden, anschließend fügen Sie diese Magellan.exe auf dem Rechner ins Programmverzeichnis ein, auf dem Sie die Statistik erstellen möchten.<br/>Nutzen Sie ein Zweitsystem aktualisieren Sie diesen Rechner und ersetzen dann bitte die Magellan.exe mit der neuen Datei.<br/><br/>Die Magellan.exe finden Sie bei  64-Bit Betriebssystemen unter `C:\Program Files \(x86\)\Stueber Systems\Magellan 6`, bei  32 Bit Betriebssystemen unter `C:\Programme\Stueber Systems\Magellan 6`.



---

## Archiv

* FIX: SHL-Statistik DATSA 2017.xml - Hinzufügen der Plausibilität SA3000
* FIX: SHL-Statistik DATSA 2017.xml - Entfernen der Plausibilitäten SA3000-1, SA3000-2
* FIX: SHL-Statistik DATSA 2017.xml - Korrektur der Plausibilitäten SA5900, SA6000, SA7900
* FIX: MAGELLAN - Ausgabe der "IFÖZ" für die Plausiblitätsabfragen
* FIX: SHL-Statistik DATLA 2017.xml - Korrektur verschiedener Plausibilitäten
* FIX: SHL-Statistik DATEA 2017.xml - Korrektur verschiedener Plausibilitäten
* FIX: SHL-Statistik DATSA 2017.xml - Korrektur verschiedener Plausibilitäten
* FIX: SHL-Statistik DATSA 2017.xml - Korrektur der Plausibilität SA1503
* FIX: SHL-Statistik DATSA 2017.xml - Korrektur der Plausibilität SA1498