# Sachsen

SaxSVS-BBS ist eine Webanwendung für statistische Betrachtungen an sächsischen Berufsbildenden Schulen. Alle schulischen Statistiken werden über diese Webanwendung
erstellt. Da in SaxSVS nicht alle Bereiche abgedeckt werden können, soll eine Schnittstelle eine doppelte Eingabe der Schülerdaten zwischen MAGELLAN und SaxSVS überflüssig machen.
Die Schnittstelle basiert auf festgelegten Schlüsseln, die an die amtliche Schulstatistik Phönix angelehnt sind.

Diese Dokumentation beschreibt die für Sächsische Schulen spezifischen Funktionen in MAGELLAN in Ergänzung zur allgemeinen MAGELLAN-Dokumentation.

!!! warning "Wichtig"

    Zur Nutzung der aktuellsten Version benötigen Sie eine Lizenz für das Modul MAGELLAN Landesstatistik 2020 und mindestens die MAGELLAN Version 7.1.7 - 711 vom XX.XX.2020!

## Einführung

Die SaxSVS-BBS Schnittstelle wird über eine definierte Schnittstellendatei im XML-Format bedient. Diese Datei dient sowohl dem Export- als auch dem Import von und nach MAGELLAN, sowie SaxSVS-BBS.
In den nachfolgenden Abschnitten beschreiben wir die Voraussetzungen und Schritte zur Erstellung der jeweiligen Schnittstellendatei, bzw. zum Import von Daten aus einer Schnittstellendatei.

### Das XML-Dateiformat

Die Schnittstelle importiert und exportiert eine Datei im XML-Format. Dies bedeutet Sie erhalten eine strukturierte Textdatei nach vorgegebenem Format.
Allgemeine Informationen zum grundsätzlichen Verständnis von XML-Dateien finden Sie auf z.B. auf [Wikipedia](https://de.wikipedia.org/wiki/Extensible_Markup_Language).

Hier ein kleiner Ausschnitt aus der SaxSVS-Schnittstelle:

```xml
<saxsvs-bbs xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.3.xsd" zeit="TDateTime Today (2001-12-17T09:30:47-05:00)"  schuljahr="Zeitraeume.Ausdruck2 (2018/2019)" dienststelle="Mandanten.Schulnummer">
  <schueler extern_id="Schueler.ID">
    <an_vname>Schueler.Vorname</an_vname>
    <an_name>Schueler.Nachname</an_name>
    <an_gebdat>Schueler.Geburtsdatum (YYYY-MM-DD)</an_gebdat>
    <an_gebort>x</an_gebort>
    <an_geschlecht schluessel="K101" extern_id="1">männl.</an_geschlecht>
    <al_kennziffer>SchuelerAusbildung.Bildungsgang</al_kennziffer>
    <al_schulart schluessel="S0502" extern_id="110">BS/BS</al_schulart>
    <al_status schluessel="S1920" extern_id="1">Auszubildender/Schüler</al_status>
    <al_zeitform schluessel="S1832" extern_id="1">v</al_zeitform>
    <al_abschl_dat>Schueler.VoraussichtlichesEnde (2016-01-01)</al_abschl_dat>
    <al_laufb_kl>SchuelerLaufbahn.Klasse (BK19A)</al_laufb_kl>
  </schueler>
</saxsvs-bbs>
```

#### XML-Dateien prüfen

Ein Vorteil von XML-Dateien ist, dass diese über eine weitere Datei, genannt Schemadatei (Dateiformat .XSD) geprüft werden kann. Das Schema gibt vor, wie eine XML-Datei auszusehen hat und z.B. welche Werte grundsätzlich erlaubt sind. Die Schemadatei für die SAXSVS-Schnittstelle finden Sie [hier](https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.3.xsd).
Um die fertige XML-Datei mit der Schemadatei prüfen zu können, benötigen Sie ein entsprechendes Programm, z.B. XML-Spy oder ähnliches. Es gibt auch Online-Prüfungen, in denen Sie den Text der XML-Datei kopieren können und den Link zur Prüfdatei im Netz angeben (**Achten Sie auf den Datenschutz bei Prüfungen im Internet**). Die Prüfungen geben üblicherweise recht gute Fehlerbeschreibungen aus, wenn etwas in der XML-Datei nicht stimmt. STÜBER SYSTEMS hat auch eine einfache automatische Prüfung eingebaut, die über den MSXML-Parser angeboten wird. Die Ausgaben der Fehlerbeschreibungen sind allerdings von Hause aus etwas kryptisch und können nur einen Anhaltspunkt geben.

### Lizenz

Die Lizenz zum Ausspielen der Schnittstellendatei aus MAGELLAN wurde erstmalig 2018 vom Kultusministerium für die teilnehmenden Berufsschulen zur Verfügung gestellt und beinhaltet
lediglich das Ausspielen der zum Zeitpunkt 2018 definierten Schnittstelle.

Im Laufe der Entwicklung wurden 2019 weitere Anforderungen an die Schnittstelle gestellt, wie das separate Ausspielen der Abgänger und dem Import der Daten nach MAGELLAN 7.
Für diese und zukünftige Weiterentwicklung der Schnittstelle muss die Lizenz entsprechend erneuert werden. Erfahrungsgemäß sind Änderungen an der Schnittstelle jährlich zu erwarten.
Die Lizenz enthält den entsprechenden Support der Schnittstelle für ein Jahr.

## Notwendige Schritte

### Schlüsselpflege

[Schlüsselpflege (Einlesen, kontrollieren und ggfs. anpassen der Statistikschlüssel)](schluessel.md)

### Export

Dateiname    | Abkürzung | Kapitel                                                     | Lizenz | Inhalt
------------ | --------- | ----------------------------------------------------------- | ------ | ------
SAXSVS.XML   | SAXSVS    | [Datenpflege zum Export der SAXSVS.XML](export_saxsvs.md)   | 2018   | Aktuelle und abgegangene Schüler des laufenden Schuljahres

[comment]: # (SAXSVS-A.XML | SAXSVSA   | [Datenpflege zum Export der SAXSVS-A.XML](export_saxsvs.md) | 2020   | Abgegangene Schüler am Schuljahresende)

#### Voraussetzungen für den Export

Damit die Schnittstellendatei korrekt erstellt und gefüllt werden kann, müssen in MAGELLAN bestimmte Datenfelder immer gefüllt werden. Ist einer der Felder nicht gefüllt erhalten Sie entsprechende Meldungen und der Export wird nicht durchgeführt.

Ohne Angaben zur **Ausbildung** beim Schüler wird der Schüler nicht in die XML-Datei gespielt und Sie erhalten einen entsprechenden Hinweis beim Durchlauf.
Alle folgenden Felder der Ausbildung `müssen` gepflegt sein, sind damit `Pflichtfelder`. Dies gilt auch für Schüler die in SAXSVS zum Löschen markiert werden sollen.

Titel            | Inhalt
---------------- | ------
**Feld**         | -
**Beschreibung** | `Schüler > Ausbildung > Aktuelle Ausbildung`<br/>Sie müssen dem Schüler für den zu exportierenden Zeitraum eine aktuelle Ausbildung zuweisen. Schüler ohne eine aktuelle Ausbildung im ausgewählten Exportzeitraum werden <b>nicht berücksichtigt</b>.
**Feld**         | `<schueler extern_id>`
**Beschreibung** | `Schüler > Ausbildung > GUID`<br/>Wenn Sie  zum ersten mal in MAGELLAN 7 den Export durchlaufen, dann existieren noch keine GUIDs für bestehende aktuelle Ausbildungen. Diese werden dann angelegt und in der Datenbank gespeichert.
**Feld**         |  `<al_kennziffer extern_id>`
**Beschreibung** | `Schüler > Ausbildung > Bildungsgang`<br/>Der Bildungsgang bzw. Beruf des Schülers in der aktuell eingestellten Ausbildung.
**Feld**         | `<al_schulart extern_id>`
**Beschreibung** | `Schüler > Ausbildung > Schulform`<br/>Die Schulart des Schülers in der aktuelle eingestellten Ausbildung.
**Feld**         | `<al_zeitform extern_id>`
**Beschreibung** | `Schüler > Ausbildung > Organisation`<br/>Die Organisationform der aktuell eingestellten Ausbildung.

!!! warning "Wichtig"

    Bildungsgang, Schulform und Organisation können auch per Sammelzuweisung zugewiesen werden.

### Import

Dateiname    | Abkürzung | Kapitel                                 | Lizenz | Inhalt
------------ | --------- | --------------------------------------- | ------ | ------
SAXSVS.XML   | SAXSVS    | [Import SAXSVS.XML](import_saxsvs.md)   | 2020   | Vagabunden

#### Voraussetzungen für den Import

Damit die Schnittstellendatei korrekt eingelesen und die Daten nach MAGELLAN importiert werden können, muss die Schnittstellendatei einige Mindestangaben enthalten.
In MAGELLAN müssen bereits die Schlüssel in den Katalogen vorhanden sein, auf die in der Schnittstellendatei verwiesen wird.
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

Liste der vom Import betroffenen Kataloge:

Katalog               | Feld(er)
--------------------- | --------
Abgangsarten          | `<abbruch extern_id>`
Abschlussarten        | `<absch_art_zusatz extern_id>`
Abschlüsse (Intern)   | `<absch_art extern_id>`
Abschlüsse (Extern)   | `<av_abs_zeugnis extern_id>`<br>`<av_bbs_zeugnis extern_id>`
Behinderungsarten     | `<af_behart extern_id>`
Bildungsgänge         | `<al_kennziffer extern_id>`
Fächer                | `<al_fremd_fs1 extern_id>`<br>`<al_fremd_fs2 extern_id>`<br>`<al_fremd_fs3 extern_id>`
Fehlgründe            | `<an_abw_grund extern_id>`
Förderungen           | `<al_laufb_bgut extern_id>`
FoerderSchwerpunkte   | `<al_mfoerdersw extern_id>`<br>`<af_schwaeche extern_id>`<br>`<af_int extern_id>`
Organisationen        | `<al_zeitform extern_id>`
SchuelerMerkmale      | `<al_status extern_id>`
Schulformen           | `<al_schulart extern_id>`
SchulformenHerkunft   | `<av_abs_schart extern_id>`<br>`<av_bbs_schart extern_id>`
Förderbedarf          | `<migration>`
Staatsangehörigkeiten | `<an_staatsang_1 extern_id>`<br>`<an_staatsang_2 extern_id>`<br>`<as_staat extern_id>`
  
### Besonderheiten

#### 2020/2021

-
