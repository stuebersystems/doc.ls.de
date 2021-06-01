# Niedersachsen

Das Programm izn-Stabil gestattet für Allgemeinbildende Schulen in Niedersachsen die Übernahme von Daten aus Schulverwaltungsprogrammen und zwar für die Bereiche Klassendaten, Stunden der Lehrkräfte, Kurse aus der gymnasialen Oberstufe (Sekundarbereich II - SEK II) und Daten der Absolventen.

Diese Dokumentation beschreibt die für Niedersächsische Schulen spezifischen Funktionen in MAGELLAN in Ergänzung zur allgemeinen MAGELLAN-Dokumentation.

!!! warning "Wichtig"

    Bitte beachten Sie, die Schnittstelle steht mit der kommenden MAGELLAN 8 Version zur Verfügung. Wir stellen mit der Veröffentlichung unser Angebot von der jährlich angebotenen Lizenz (bisher veröffentlicht "LANDESSTATISTIK") auf einen Nutzungsvertrag um. Dieser Vertrag beinhaltet die Nutzung, Pflege, Weiterentwicklung und den Support der MAGELLAN Schnittstelle zu verschiedenen Anbietern. Bitte beachten Sie, dass diese Nutzungsverträge nicht den MAGELLAN Support- und Softwarepflegevertrag ersetzen. 

## Einführung

Die Schnittstelle zu izn-Stabil wird über definierte Schnittstellendateien im Textformat bedient. Diese Dateien werden aus MAGELLAN heraus exportiert und dienen dem Import nach izn-Stabil. In den nachfolgenden Abschnitten beschreiben wir die Voraussetzungen und Schritte zur Erstellung der jeweiligen Schnittstellendatei.

## Aufbau der Exportdateien

izn-Stabil benutzt ein Textformat in dem die Daten zeilenweise pro Klasse und Jahrgang und Stellenweise pro Informationseinheit gespeichert werden.

## Notwendige Schritte

### Schlüsselpflege

[Schlüsselpflege (Einlesen, kontrollieren und ggfs. anpassen der Statistikschlüssel)](https://doc.ls.stueber.de/schluesselverzeichnisse/)

### Export

Hier erhalten Sie eine Übersicht über die Schnittstellendateien, und welche von MAGELLAN unterstützt werden:

Dateiname   | Abkürzung | Unterstützt | Kapitel                                                | Lizenz | Inhalt
----------- | --------- | ----------- | ------------------------------------------------------ | ------ | ------
KLIMP.TXT   | KLIMP     | X           | [Datenpflege zum Export der KLIMP.TXT](https://doc.ls.stueber.de/niedersachsen/klimp/))   | 2021   | Daten der Klassen
RELIMP.TXT* | RELIMP    | X           | [Datenpflege zum Export der RELIMP.XML](https://doc.ls.stueber.de/niedersachsen/relimp/) | 2021   | Religionsunterricht (Lerngruppen und Stunden), Informationen über die eingerichteten Lerngruppen und die erteilten Stunden Religionsunterricht bzw. Unterricht Werte und Normen
SEK2IMP     | SEK2IMP   | -           | -                                                      | -      | Daten der gymnasialen Oberstufe
LVIMP       | LVIMP     | -           | -                                                      | -      | Informationen über die Unterrichtseinsätze der Lehrkräfte. Die Erfahrungen der Schulen bei den letzten Erhebungen haben gezeigt, dass es günstiger ist, das Lehrkräfteverzeichnis vollständig in izn-Stabil zu bearbeiten.

* Für den Export der RELIMP.TXT wird unser Stundenplanprogramm DAVINCI benötigt.

#### Voraussetzungen für den Export

!!! warning "Wichtig"

    izn-Stabil benötigt Daten aus dem aktuellen Schuljahr. Aus MAGELLAN Sicht können dies max. Daten aus dem 1. HJ und 2. HJ sein. Das aktuelle Schuljahr berechnet sich anhand des Exportdatums und der Von- und Bis-Daten des MAGELLAN-Zeitraums (1. HJ vom 01.08. - 31.01. und 2. HJ vom 01.02. - 31.07.). Wenn sich der Export im 1. HJ befindet, so werden Sie in der Exportdatei auch nur Daten aus dem 1. HJ des aktuellen Schuljahres finden. Wenn der Export im 2. HJ ausgeführt wird, so werden Sie in der Exportdatei Daten aus beiden Halbjahren finden.

Damit die Schnittstellendatei korrekt erstellt und gefüllt werden kann, müssen in MAGELLAN bestimmte Datenfelder immer gefüllt werden. **Ist einer der Felder nicht gefüllt wird der Export nicht durchgeführt.**

Titel            | Inhalt
---------------- | ------
**Feld**         | ``Klassen > Daten > Statistikkürzel``
**Beschreibung** | Bitte geben Sie in diesem Feld das Klassenkürzel ein. Schüler aus Klassen ohne Statistikkürzel werden für den Export nicht berücksichtigt.

### Besonderheiten

#### 2021/2022

keine
