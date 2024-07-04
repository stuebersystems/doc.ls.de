# Mecklenburg-Vorpommern

Schülerdaten, Personalangaben von Lehrerinnen und Lehrern: Die Datenerhebung für allgemein bildende und berufliche Schulen erfolgt in Mecklenburg-Vorpommern über das interne Schulinformations- und Planungssystem M-V (SIP M-V).

STÜBER SYSTEMS bietet Ihnen die Möglichkeit, Daten für die SIP-Schnittstelle mit Magellan zu exportieren.

!!! warning "Wichtig"

    Bitte beachten Sie, mit dem Magellan 9 Serviceupdate 9.0.4 stehen überarbeitete Schnittstellen zur Verfügung. Wir stellen mit der Veröffentlichung unser Angebot von der jährlich angebotenen Lizenz (bisher veröffentlicht "LANDESSTATISTIK") auf einen Nutzungsvertrag um. Dieser Vertrag beinhaltet die Nutzung, Pflege, Weiterentwicklung und den Support der Magellan Schnittstelle zu verschiedenen Anbietern. Bitte beachten Sie, dass diese Nutzungsverträge nicht den Magellan Support- und Softwarepflegevertrag ersetzen. 

## Einführung

Die SIP-MV Schnittstelle wird über zwei definierte Schnittstellendateien im XML-Format bedient. Eine für die Richtung Magellan -> SIP, eine weitere für die Richtung SIP -> Magellan.
In den nachfolgenden Abschnitten beschreiben wir die Voraussetzungen und Schritte zur Erstellung der jeweiligen Schnittstellendatei, bzw. zum Import von Daten aus einer Schnittstellendatei.

## Lizenz

Bitte beachten Sie, seit Magellan 7 haben wir unser Angebot von der jährlich angebotenen Lizenz (bisher veröffentlicht "LANDESSTATISTIK") auf einen Nutzungsvertrag um. Dieser Vertrag beinhaltet die Nutzung, Pflege, Weiterentwicklung und den Support der Magellan Schnittstelle zu verschiedenen Anbietern. Bitte beachten Sie, dass diese Nutzungsverträge nicht den Magellan Support- und Softwarepflegevertrag ersetzen.
**Die jährlich neue Lizenz kann mit der jeweils neuesten Ausgabe von Magellan verwendet werden, wir weisen darauf per Newsletter hin. Wenn Sie einen Nutzungsvertrag abgeschlossen haben, senden wir Ihnen die neue Lizenz und weitere Informationen per Mail zu.**

### Das XML-Dateiformat

Die Schnittstelle importiert und exportiert eine Datei im XML-Format. Dies bedeutet Sie erhalten eine strukturierte Textdatei nach vorgegebenem Format.
Allgemeine Informationen zum grundsätzlichen Verständnis von XML-Dateien finden Sie auf z.B. auf [Wikipedia](https://de.wikipedia.org/wiki/Extensible_Markup_Language).

Magellan erzeugt eine XML-Datei nach folgendem Muster:

xxxxx_[DATUM].xml

Hierbei steht xxxxx für Ihre Schulnummer und [DATUM] für das aktuelle Datum.

#### XML-Dateien prüfen

Ein Vorteil von XML-Dateien ist, dass diese über eine weitere Datei, genannt Schemadatei (Dateiformat .XSD) geprüft werden kann. Das Schema gibt vor, wie eine XML-Datei auszusehen hat und z.B. welche Werte grundsätzlich erlaubt sind. Die Schemadatei für die SIP-Schnittstelle finden Sie [hier](https://download.stueber.de/bin/de/magellan/v7/files/SipSchuleTransfer.xsd).
Um die fertige XML-Datei mit der Schemadatei prüfen zu können, benötigen Sie ein entsprechendes Programm, z.B. XML-Spy oder ähnliches. Es gibt auch Online-Prüfungen, in denen Sie den Text der XML-Datei kopieren können und den Link zur Prüfdatei im Netz angeben (**Achten Sie auf den Datenschutz bei Prüfungen im Internet**). Die Prüfungen geben üblicherweise recht gute Fehlerbeschreibungen aus, wenn etwas in der XML-Datei nicht stimmt.

### SIP-MV

Für Sie als Schule bedeutet dies: Sie müssen die exportierte XML-Datei über das [Schulportal Mecklenburg-Vorpommern](https://portal.schule-mv.de) nach SIP-MV übertragen.

## Notwendige Schritte

### Schlüsselpflege

[Schlüsselpflege (Einlesen, kontrollieren und ggfs. anpassen der Statistikschlüssel)](../schluesselverzeichnisse.md)

### Export

Dateiname         | Abkürzung | Kapitel                                 | Lizenz | Inhalt
----------------- | --------- | --------------------------------------- | ------ | ------
xxxxx_[DATUM].xml | SIP       | [Datenpflege zum Export](export_sip.md) | YYYY (aktuelles Jahr)  | Aktuelle und historische Daten des laufenden und davor liegenden Schulhalbjahres

#### Voraussetzungen für den Export

!!! warning "Wichtig"

    SIP benötigt Daten aus dem aktuellen Schulhalbjahr und den vorangegangenen Schulhalbjahr, sofern vorhanden. Diese beiden Zeiträume berechnen sich anhand des Exportdatums. Wenn sich der Export im 1.HJ befindet so werden Sie in der Exportdatei Daten aus dem 1. HJ des aktuellen Schuljahres und dem 2. HJ des vorangehangenen Schuljahres finden. Wenn der Export im 2. HJ ausgeführt wird, so werden Sie in der Exportdatei Daten aus dem aktuellen Schuljahr finden.

Damit die Schnittstellendatei korrekt erstellt und gefüllt werden kann, müssen in Magellan bestimmte Datenfelder immer gefüllt werden. Ist einer der Felder nicht gefüllt erhalten Sie entsprechende Meldungen und der Export wird nicht durchgeführt.

Titel            | Inhalt
---------------- | ------
**Feld**         | Verschiedene
**Beschreibung** |  `Magellan > Mandanten > Daten 1 > Schulformen`<br/>Einige Felder werden nur für ABS oder BBS ausgespielt und schließen sich gegenseitig aus. Sie müssen die für Ihre Schule gültigte Schulform angeben, um dies berechnen zu können.
**Feld**         | Verschiedene im `<Lehrer>` Knoten
**Beschreibung** |  `Magellan > Mandanten > Daten 1 > Rechtsstatus`<br/>Einige Felder werden nur für `Freie Schulen` ausgespielt. Als freie Schule geben Sie im Feld `Rechtsstatus` den Wert `privat` an, alle anderen `öffentlich`. Es wird erwartet, dass Sie dort bewusst einen Eintrag auswählen. Leer lassen führt zu einer Meldung beim Export.

### Import

Dateiname         | Abkürzung | Kapitel                                 | Lizenz | Inhalt
----------------- | --------- | --------------------------------------- | ------ | ------
xxxxx_[DATUM].xml | SIP       | [Import aus SIP](import_sip.md)         | YYYY (aktuelles Jahr) | IDs zum Synchronisieren mit Magellan

#### Voraussetzungen für den Import

Damit die Schnittstellendatei korrekt eingelesen und die Daten nach Magellan importiert werden können, muss die Schnittstellendatei einige Mindestangaben enthalten.
In Magellan müssen bereits die Schlüssel in den Katalogen vorhanden sein, auf die in der Schnittstellendatei verwiesen wird.
Fehlen diese Angaben, wird der Schüler nicht importiert.

!!! warning "Wichtig"

    Wenn die Kataloge nicht die korrekten Schlüssel enthalten, dann können Sie davon ausgehen, dass somit kein Schüler aus der Schnittstellendatei importiert wird.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<schueler extern_id>`
**Beschreibung** | GUID des Schülers.
**Feld**         | `<an_vname>`
**Beschreibung** | Vorname des Schülers.
**Feld**         | `<an_name>`
**Beschreibung** | Nachname des Schülers.
**Feld**         | `<an_gebdat>`
**Beschreibung** | Geburtsdatum des Schülers.

### Besonderheiten

keine
