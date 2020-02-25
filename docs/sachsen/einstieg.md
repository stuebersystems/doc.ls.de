# Sachsen

SaxSVS-BBS ist eine Webanwendung für statistische Betrachtungen an sächsischen Berufsbildenden Schulen. Alle schulischen Statistiken werden über diese Webanwendung
erstellt. Da in SaxSVS nicht alle Bereiche abgedeckt werden können, soll eine Schnittstelle eine doppelte Eingabe der Schülerdaten zwischen MAGELLAN und SaxSVS überflüssig machen.
Die Schnittstelle basiert auf festgelegten Schlüsseln, die an die amtliche Schulstatistik Phönix angelehnt sind.

Diese Dokumentation beschreibt die für Sächsische Schulen spezifischen Funktionen in MAGELLAN in Ergänzung zur allgemeinen MAGELLAN-Dokumentation.

!!! warning "Wichtig"

    Zur Nutzung der aktuellsten Version benötigen Sie eine Lizenz für das Modul MAGELLAN Landesstatistik 2020 und mindestens die MAGELLAN Version 7.1.7 - 711 vom XX.XX.2020!

## Einführung

Die SaxSVS-BBS Schnittstelle wird über eine definierte Schnittstellendatei im XML-Format bedient. Diese Datei dient sowohl dem Export- als auch dem Import von und nach MAGELLAN, sowie SaxSVS-BBS.
In den nachfolgenden Abschnitten beschreiben wir die Voraussetzungen und Schritte zur Erstellung der jeweiligen Schnittstellendateien,
bzw. zum Import von Daten aus einer Schnittstellendatei.

### Lizenz

Die Lizenz zum Ausspielen der Schnittstellendatei aus MAGELLAN wurde erstmalig 2018 vom Kultusministerium für die teilnehmenden Berufsschulen zur Verfügung gestellt und beinhaltet
lediglich das Ausspielen der zum Zeitpunkt 2018 definierten Schnittstelle.

Im Laufe der Entwicklung wurden 2019 weitere Anforderungen an die Schnittstelle gestellt, wie das separate Ausspielen der Abgänger und dem Import der Daten nach MAGELLAN 7.
Für diese und zukünftige Weiterentwicklung der Schnittstelle muss die Lizenz entsprechend erneuert werden. Erfahrungsgemäß sind Änderungen an der Schnittstelle jährlich zu erwarten.
Die Lizenz enthält den entsprechenden Support der Schnittstelle für ein Jahr.

### Export

Dateiname    | Abkürzung | Kapitel                                 | Lizenz | Inhalt
------------ | --------- | --------------------------------------- | ------ | ------
SAXSVS.XML   | SAXSVS    | [Export SAXSVS.XML](export_saxsvs.md)   | 2018   | Aktuelle Schüler und abgegangene Schüler
SAXSVS-A.XML | SAXSVSA   | [Export SAXSVS-A.XML](export_saxsvs.md) | 2020   | Nur Abgegangene Schüler

### Import

Dateiname    | Abkürzung | Kapitel                                 | Lizenz | Inhalt
------------ | --------- | --------------------------------------- | ------ | ------
SAXSVS.XML   | SAXSVS    | [Import SAXSVS.XML](import_saxsvs.md)   | 2020   | Vagabunden

## Notwendige Schritte

1. [Schlüsselpflege (Einlesen, kontrollieren und ggfs. anpassen der Statistikschlüssel)](schluessel.md)
2. [Datenpflege](https://doc.ls.stueber.de/sachsen/datenpflege/)
3. [Daten prüfen und XML-Datei erzeugen](https://doc.ls.stueber.de/sachsen/xml.erzeugen/)
