# ASDPC-Schnittstelle 2020/21

Hier finden Sie die jeweils aktuellste Version zur ASDPC-Schnittstelle **inklusiver aller kurzfristig veröffentlichten Korrekturen während einer Statistikphase**.

## Download der aktuellen Schnittstelle

Sollte die aktuelle Schnittstelle bereits in einem Serviceupdate veröffentlicht sein, dann zeigt der Link des Schnittstellenpakets auf unsere Downloadseite.

### Schnittstellenpaket - 31.08.2021

[Downloadlink](https://my.hidrive.com/share/neqlm8tqnv)

!!! info "Hinweis"

    Eine Anleitung zum Austausch der einzelnen Dateien finden Sie im Abschnitt ["Wie Dateien ausgetauscht werden"](#wie-dateien-ausgetauscht-werden)!

#### Aktuelle Änderungen

* FIX: SIM.TXT - Ausgabe der VOfachklasse
* CHANGE: [NRW]: Geschwindigkeitsverbesserung SIM.TXT, ABI.TXT, LEHRER.TXT
* FIX: [NRW]: Ausgabe von ABG, BAG, AKT, NZG, NGS, AKT, NZG
---

#### Letztes Serviceupdate - 8.0.11 802 (12.08.2021)

* FIX: -

---

## Wie Dateien ausgetauscht werden

!!! warning "Wichtig"

    Vorausgesetzt wird immer die zuletzt veröffentlichte Programmversion. Liegt das letzte Änderungsdatum vor dem Veröffentlichungsdatum unserer Standardausgabe, sind die Änderungen für die Schnittstelle alle im Standardupdate mit enthalten! Das Ausgabedatum der letzten MAGELLAN-Version sehen Sie in unserer [Changelog-Datei](https://doc.magellan.stueber.de/changelog/changelog/).

Was soll getauscht werden | Anmerkungen
------------------------- | -----------
**Pfade in MAGELLAN**     | Die entsprechenden Pfade zu Ihren Dokumenten, Skripten und Importdateien können Sie im MAGELLAN-Administrator unter `Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner` einsehen.
**Schlüssel**             | Dateien mit der Endung **\*.keys** sind Ihre Schlüsseldateien für den Import der aktuellen Statistikschlüssel. Diese gehören auf den Serverrechner in den dortigen Unterordner Importe\Nordrhein-Westfalen.<br><br>Fügen Sie diese Dateien dort ein und überschreiben Sie ggf. bereits existierende Schlüsseldateien. Anschließend lesen Sie die Schlüssel über den MAGELLAN-Administrator unter `Datenimporte > Schlüsselverzeichnisse importieren > Nordrhein-Westfalen > Ihre Schulart` ein. Sie können alle Schlüsseldateien importieren oder auch nur eine Datei, dazu ändern Sie "alle Kataloge" ab und wählen gezielt die gewünschte Importdatei.
**Skripte**               | **\*.dws oder \*.int**  Dateien mit der Endung **\*.dws oder \*.int** gehören auf den Serverrechner in den dortigen Unterordner Skripte \(**Achtung**: Nicht in den Bundesland-Unterordner, sondern direkt in den Skripteordner\).<br/><br/>**\*.xml** Dateien mit der Endung **\*.xml** gehören auf den Serverrechner in den dortigen Unterordner Skripte\Nordrhein-Westfalen. Bitte beachten Sie, dass die Dateien mit diesem Schritt lediglich hinterlegt sind und erst noch in Ihren Datenbank importiert werden müssen. Eine Anleitung zum Schlüsselimport finden Sie [hier](https://doc.ls.stueber.de/schluesselverzeichnisse/).
**Magellan.exe**          | Das Nutzen einer neuen Magellan.exe setzt mindestens die aktuellste Version voraus. Das letzte und aktuelle Serviceupdate finden Sie in unseren [Downloads](http://magellan.stueber.de/download.php).<b/r><br/>Nehmen Sie die Arbeiten mit der Schnittstelle in der Schule an der aktuellen Datenbank vor oder in einer zweiten Umgebung, also zum Beispiel auf einem Extrarechner, auf den die Datenbank übertragen wird? Wenn Sie es im Schulnetzwerk machen, dann müssten bitte die Rechner alle \(erst der Server, dann die Arbeitsplätze\) auf die aktuelle Version aktualisiert werden, anschließend fügen Sie diese Magellan.exe auf dem Rechner ins Programmverzeichnis ein, auf dem Sie die Schnittstelle ausführen möchten. Nutzen Sie ein Zweitsystem aktualisieren Sie diesen Rechner und ersetzen dann bitte die Magellan.exe mit der neuen Datei.<br/><br/>Die Magellan.exe finden Sie bei 64-Bit Betriebssystemen unter `C:\Program Files \(x86\)\Stueber Systems\MAGELLAN 8`, bei 32 Bit Betriebssystemen unter `C:\Programme\Stueber Systems\MAGELLAN 8`.

---

## Archiv

---

### Schnittstellenpaket ABS/BBS 2019 - 19-09-2019

* FIX: ABI.TXT - Ausgabe der Abiturnote im Format n.n (Punkt)
* FIX: ABI.TXT - Zeugnis wird jetzt korrekt, entsprechend der Dokumentation ausgespielt.

---

### Serviceupdate - 17.09.2019

* FIX: SIM.TXT - LSSchulform wurde nicht korrekt ausgelesen. Das führte zu Leereinträgen in der Spalte.
* FIX: SIM.TXT - LSKlassenart wurde nicht ausgespielt, sondern nur ausgelesen. Das führte bei den Datensatzsarten: "Neuzugang" und "Neuzugang an gleicher Schule" dazu, dass eine Spalte in der Zeile fehlte.
* FIX: SIM.TXT - Adressmerkmal wird zwar nicht benötigt wurde aber auch nicht als Leerfeld (Nur Trennzeichen) ausgespielt.
* FIX: SIM.TXT - Die Kopfzeilen für Adressmerkmal und Internat am Ende der SIM.TXT haben gefehlt
* CHANGE: SIM.TXT - Die beiden Spalten `Produktname` und `Produktversion` dienen lediglich Supportzwecken. Beide Informationen wurden in die Spalte Produktname verschoben. In der Spalte `Produktversion` geben wir jetzt die Datensatzart aus, dies hilft dem Support bei der Suche nach Problemlösungen.
* CHANGE: Kein Fehler aber eine Eingabehilfe. Einige Kunden geben keine Versetzungart ein, sondern setzen lediglich das Merkmal Versetzt. Wir tragen dem Folge und berechnen entsprechend die Versetzung anders als zuvor. Nachzulesen in der Dokumentation unter [SIM.TXT - Dateneingabe - Feld "Versetzung"](https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/#dateneingabe).
