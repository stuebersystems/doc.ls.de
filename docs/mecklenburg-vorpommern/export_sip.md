# Export von Daten für SIP aus MAGELLAN

1. [Beachten Sie bitte die Mindesteingaben für den Export](https://doc.ls.stueber.de/mecklenburg-vorpommern/einstieg/#voraussetzungen-fur-den-export)
2. Lesen Sie dieses Kapitel gut durch, die meisten Probleme berufen sich auf fehlende oder falsche Eingaben in MAGELLAN.
3. Lesen Sie im Kapitel [Schnittstellendatei aus MAGELLAN erzeugen](sip_xml.erzeugen.md), wie Sie den Export durchführen.

Nachstehend finden Sie eine Auflistung der relevanten Felder und der jeweiligen Stelle, an der Sie in MAGELLAN eingepflegt werden.
Ggf. haben wir nach XML-Elementen (Knoten) aufgeteilt.

!!! warning "Wichtig"

    Die XML-Knoten werden in der Dokumentation wie folgt benannt: `<Knotenname>`. Unterknoten können dann z.B. so aussehen `<Schule><Schueler>`

## Legende

Erklärung zu einigen wenigen Abkürzungen bzw. erwähnenswerten Anmerkungen die in der Beschreibung verwendet werden.

Benennung      | Beschreibung
-------------- | ------------
Werte          | Die Schnittstelle erwartet zumeist einen der folgenden Wertetypen:<br/>* Ein Wert aus einem Katalog, z.B. 20, 60 etc. meistens eine Zahl die im Kontext der Werteliste eine entsprechende Bedeutung hat<br/>* „Ja“/“Nein“ – Trifft, oder trifft nicht zu<br/>* Freitextfeld<br/>* Datum im Format YYYY-MM-DD<br/>* Zahlwert
MI             | *Mindestvoraussetzung.* Diese Felder müssen gefüllt sein, da ansonsten der Import in SIP grundsätzlich aufgrund von XML-Schemafehlern nicht durgeführt werden kann.
OP             | *Optional Pflicht.* Wenn grundsätzliche Aussagen zutreffen und Sie Felder in MAGELLAN mit Werten füllen, dann sind die Felder mit OP für diesen Bereich als Pflichtfelder zu sehen und müssen eingetragen werden. Beispiel: Abwesenheiten. Wenn Sie eine Abwesenheit mit Grund eintragen, muss auch das Von-Datum gefüllt werden, da ansonsten auch wieder ein XML-Schemafehler vorliegt.
MI/OP          | Diese sind zwar Pflichtfelder für die Schnittstelle, müssen aber nur von Ihnen logisch bedient werden, wenn sie zutreffen. Im Falle dass diese Felder in MAGELLAN leer bleiben, werden vom Export automatisch die Standardwerte gefüllt (meistens 0 oder -1).

## Aufbau der Schnittstelle

Die Schnittstelle fängt mit einem Kopfteil und einigen informativen Knoten an, der Teil mit den Daten fängt dann im Unterknoten `<Schule>` an, unter dem dann alle exportierten Daten entsprechend organisiert sind.

```xml
<kopf><schule><...>
```

### Datensätze vom Export ausschließen

Datensätze können aufgrund von Eingaben in MAGELLAN automatisch ausgeschlossen sein, z.B. Gastschüler. Sie haben darüber hinaus die Möglichkeit grundsätzlich Schüler von der Schnittstelle auszuschließen.

#### Gastschüler ausschließen

Schüler, die von einer anderen Schule (die Stammschule) an SIP übergeben werden, aber in Ihrem System aufgrund eines Gastaufenthaltes in MAGELLAN eingepflegt sind,
können als Gastschüler markiert und somit aus dem Export ausgeschlossen werden.
Einen Gastschüler markieren Sie mit dem gleichnamigen Häkchen unter `Schüler > Daten 3 > Verschiedenes > Gastschüler`.

#### Schüler ausschließen

Schüler, die aus anderen Gründen nicht nach SIP übergeben werden sollen. Beispielsweise, weil Sie mitten in der Erfassung der Daten stecken und erst einmal einen Teil der bereits gepflegten Schüler übertragen möchten, können unter `Schüler > Statistik > Merkmal S10` entsprechend mit "Kein Export" markiert werden.

Steht Ihnen in dem Feld keine Auswahl zur Verfügung, importieren Sie bitte das Verzeichnis `00_SchuelerMerkmale.keys` erneut oder legen unter `Extras > Schlüsselverzeichnisse > Merkmale (Schüler)` eine Schlüsselzeile entsprechend der nachfolgenden Abbildung an. Der Wert kann auch per Sammelzuweisung verteilt werden.

![MAGELLAN 7 > Extras > Schlüsselverzeichnisse > Merkmale (Schüler)](/assets/images/mvp/kein_export.png)

### Kopfbereich  

`<Kopf>` - MI

Der Haupteinstiegsknoten ist `<Kopf>` und enthält Kopfdaten für die Schnittstelle,
wie die Versionsnummer der adressierten SIP-Schnittstelle, Umfang der Lieferung und das Exportdatum.

In der XML-Datei sieht das wie folgt aus:

```xml
<Kopf>
  <Version>2.05.001</Version>
  <ExportSystem>SIP</ExportSystem>
  <Umfang>GESAMT</Umfang>
  <ErstelltAm>15.04.2020</ErstelltAm>
  <Schule>Hier kommen dann die exportierten Daten...</Schule>
</Kopf>
```

Feld in Schnittstelle  | Beschreibung
---------------------- | ------------
`<Kopf><Version>`      | Die von MAGELLAN unterstützte SIP-Version, derzeit die aktuellste Version 2.05.001
`<Kopf><ExportSystem>` | Ein fester einzutragender Wert `SIP`
`<Kopf><Umfang>`       | Umfang des Exports. Möglich sind<br>GESAMT = Gesamtdatenlieferungen und<br>TEIL = Teildatenlieferungen.<br>MAGELLAN unterstützt aktuell lediglich die Gesamtdatenlieferung.
`<Kopf><ErstelltAm>`   | Für dieses Feld wird automatisch das aktuelle Datum beim Export eingefügt.

### Schule  

`<Kopf><Schule>` - MI

Ab hier beginnen die Schuldaten.

Es werden alle eingetragenen Daten ausgelesen und entsprechend auf die `<Knoten>` verteilt.
Ab hier werden die weiteren Unterknoten in dieser Dokumentation nicht weiter mit den Elternknoten benannt.

Die Schuldaten sind in weitere Knoten aufgeteilt:

```xml
<Kopf>
  ...
  <Schule>
    <SchuleId>Diensstellennummer Ihrer Schule</SchuleId>
    <SchulTeil>Schularten an Ihrer Schule: Ausgelesen aus den Klassen</SchulTeil>
    <Klasse>Klassen an Ihrer Schule</Klasse>
    <Ue>Unterrichtseinheiten werden nicht unterstützt!</Ue>
    <Schueler>Schüler Ihrer Schule</Schueler>
    <Lehrer>Lehrer Ihrer Schule</Lehrer>
    <Schulwerkstatt>Schulwerkstatt wird nicht unterstützt!</Schulwerkstatt>
  </Schule>
</Kopf>
```

Titel            | Inhalt
---------------- | ------
**Feld**         | `<SchuleId>` - MI
**Beschreibung** | `MAGELLAN > Mandanten > Daten 1 > Schulnummer`<br/>Die Dienststellennummer Ihrer Schule

### SchulTeil

`<Schule><SchulTeil>` - MI

SchulTeil umfasst die im aktuellen Zeitraum beschulten Schularten. Diese hängen in MAGELLAN an der Klasse.
Der Export durchläuft alle Klassen im aktuellen Schulhalbjahr und liest die Schularten für den Export aus.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<SchulArtId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Daten 1 > Schulart`<br/>Die Schulart der Klasse.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

### Klasse

`<Schule><Klasse>` - OP

Klasse umfasst die im aktuellen Zeitraum beschulten Klassen.
Der Export durchläuft alle Klassen im aktuellen Schulhalbjahr und liest die Werte für den Export aus.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<KlasseId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Auswahl > ID` / `MAGELLAN > Klassen > Auswahl > GUIDExtern`<br/>Eindeutiger Wert zur Identifizierung der Klasse. Beim ersten Export wird die MAGELLAN ID verwendet. Beim Übertrag von Daten SIP -> MAGELLAN erhalten die Klassen den Identifikator von SIP für zukünftige Übertragungen.
**Feld**         | `<Bezeichnung>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Daten > Kürzel`<br/>Das Kürzel der Klasse.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

#### Schulart

`<Klasse><Schulart>` - MI

Titel            | Inhalt
---------------- | ------
**Feld**         | `<SchulartId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Daten > Schulart`<br/>Die Schulart der Klasse.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

#### JahrgangsStufe

`<Klasse><JahrgangsStufe>` - MI

Titel            | Inhalt
---------------- | ------
**Feld**         | `<JahrgangsStufeId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Zeiträume > Klassenstufe`<br/>Die Klassenstufe der Klasse.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

#### Bildungsgang

`<Klasse><Bildungsgang>` - MI

Titel            | Inhalt
---------------- | ------
**Feld**         | `<BildungsgangId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Daten > Bildungsgang`<br/>Der Bildungsgang der Klasse.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

#### KlasseBesonderheit

`<Klasse><KlasseBesonderheit>` - OP

Besonderheiten der Klassen werden aktuell nicht unterstützt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<BesonderheitId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Die Besonderheit der Klasse.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

### Ue

`<Schule><Ue>` - OP

Unterrichtseinheiten der Schule. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### Schueler

`<Schule><Schueler>` - OP

Alle Schüler der Schule, die sich im aktuellen Schulhalbjahr befinden,  ungeachtet dessen Status (Eingeschult, Ausgeschult, Abwesend). Es werden keine Bewerber berücksichtigt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<SchuelerId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Auswahl > ID` / `MAGELLAN > Schüler > Auswahl > GUIDExtern`<br/>Eindeutiger Wert zur Identifizierung der Schüler. Beim ersten Export wird die MAGELLAN ID verwendet. Beim Übertrag von Daten SIP -> MAGELLAN erhalten die Schüler den Identifikator von SIP für zukünftige Übertragungen.
**Feld**         | `<GeschlechtId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geschlecht`<br/>Geschlecht. Mögliche Werte sind:<br>Männlich, Weiblich, Divers = Wählen Sie diesen Wert einfach aus.<br>Ohne Angabe im Geburtenregister = Lassen Sie das Feld in MAGELLAN leer.
**Feld**         | `<StaatsangehoerigkeitId>` - MI/OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Staatsangeh. 1`<br/>1. Staatsangehörigkeit. Standardwert ist 0 = Deutsche Staatsangehörigkeit
**Feld**         | `<Staatsangehoerigkeit2Id>` - MI/OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Staatsangeh. 2`<br/>2. Staatsangehörigkeit. Standardwert ist -1 = Keine Angabe zu  Staatsangehörigkeit
**Feld**         | `<VerkehrsSpracheId>` - MI/OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Verkehrssprache`<br/>Verkehrssprache. Standardwert ist -1 = Keine Angabe zu Verkehrssprache
**Feld**         | `<Vorname>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Vorname`<br/>Vorname.
**Feld**         | `<Nachname>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Nachname`<br/>Nachname.
**Feld**         | `<GebDatum>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geburtsdatum`<br/>Geburtsdatum.
**Feld**         | `<GebLandId>` - MI/OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geburtsland`<br/>Geburtsland. Standardwert ist 0 = Deutschland.
**Feld**         | `<GebOrtId>` - OP
**Beschreibung** | `Nicht unterstützt`<br/>Geburtsort als Katalog veschlüsselt.
**Feld**         | `<GebOrtPlz>` - OP
**Beschreibung** | `Nicht unterstützt`<br/>PLZ des Geburtsortes.
**Feld**         | `<GebOrtsteil>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geburtsort`<br/>Geburtsort als Freitext.
**Feld**         | `<EinschulDatum>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Einschulung`<br/>`MAGELLAN > Schüler > Daten 2 > Grundschuleintritt`<br>Nur **ABS**, und nur bei Gesetztem `Einschulung` Feld, wird das  Datum des Grundschuleintritts ausgespielt.
**Feld**         | `<ZuzugsDatum>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Merkmale > Merkmal U2`<br/>Zuzugsdatum nach MVP.
**Feld**         | `<WohnOrtId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Wohnort als Katalog verschlüsselt.
**Feld**         | `<WohnOrtPlz>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > PLZ`<br/>PLZ des Wohnortes.
**Feld**         | `<WohnOrtsteil>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ort`<br/>Wohnort als Freitext.
**Feld**         | `<StrasseNr>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Strasse`<br/>Strasse des Wohnortes als Freitext.

#### AnAbmeldung

`<Schueler><AnAbmeldung>` - OP

An- bzw. Abmeldungen der eigenen Schule werden aktuell nicht unterstützt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<GrundId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>An- bzw. Abmeldegrund.
**Feld**         | `<StatusId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Der Endstatus der An- oder Abmeldung, z.B. (angemeldet, abgelehnt, etc.).
**Feld**         | `<ZumDatum>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Zugangs- bzw. Abgangsdatum an/von Schule.
**Feld**         | `<Freigabe>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Freigabe (Ja/Nein).

##### Schulwunsch

`<AnAbmeldung><Schulwunsch>` - MI

Liste von Schulwünschen. Bei Angabe von An- Abmeldung ist der Schulwunsch mit mindestens einer Schule zu befüllen.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<SchuleId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Identifikator der Wunschschule, wenn Schule in MVP. Keine Angabe = -1, Schule nicht in MVP.
**Feld**         | `<BildungsGangId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Bildungsgang an der Wunschschule.
**Feld**         | `<JahrgangsStufeId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Klassenstufe der Wunschschule.
**Feld**         | `<OertlichZustaendigeSchule>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Ist die Wunschschule örtlich zuständig (Ja/Nein).
**Feld**         | `<LfdNr>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Laufende Nummer = Positionierung des Schulwunsches.

### Angabe

`<Schueler><Angabe>` - OP

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AngabeId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Identifikator der Angabe. Es wird die `SchuelerId` ausgespielt, da MAGELLAN diese Daten logisch anders verwaltet.
**Feld**         | `<LaufbahnEmpfehlungId>` - MI/OP
**Beschreibung** | `Nicht unterstützt`<br/>Es wird der Standardwert -1 ausgespielt.
**Feld**         | `<ImAuslandId>` - MI/OP
**Beschreibung** | `Nicht unterstützt`<br/>Es wird der Standardwert -1 ausgespielt.
**Feld**         | `<AustauschPrgId>` - MI/OP
**Beschreibung** | `Nicht unterstützt`<br/>Es wird der Standardwert -1 ausgespielt.
**Feld**         | `<VomAuslandId>` - MI/OP
**Beschreibung** | `Nicht unterstützt`<br/>Es wird der Standardwert -1 ausgespielt.

Folgende Felder setzen die Angabe einer Ausbildung mit gefülltem Ausbildungsbetriebs in MAGELLAN voraus. Der Ausbildungsbetrieb ist ein Datensatz unter `MAGELLAN > Betriebe`.

1. In `MAGELLAN > Schüler > Ausbildung > Liste der Ausbildungen` muss eine Ausbildung mit Ausbildungsbetrieb angelegt werden.
2. Unter `MAGELLAN > Schüler > Ausbildung > Aktuelle Ausbildung` muss der Eintrag aus der Liste ausgewählt sein.

Die folgenden Feldbeschreibungen zeigen der Einfachheit auf das zu füllende Feld in `Betriebe`.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<BetrBez>` - MI/OP
**Beschreibung** | `MAGELLAN >  Betriebe > Daten > Name 1`<br/>Name 1 des Betriebes. Standardwert ist -1.
**Feld**         | `<BetrOrtId>` - MI/OP
**Beschreibung** | `Nicht unterstützt`<br/>Betriebsort als Katalog verschlüsselt. Standardwert ist -1.
**Feld**         | `<BetrPlz>` - MI/OP
**Beschreibung** | `MAGELLAN >  Betriebe > Daten > PLZ`<br/>PLZ des Betriebes. Standardwert ist -1.
**Feld**         | `<BetrOrtsteil>` - MI/OP
**Beschreibung** | `MAGELLAN >  Betriebe > Daten > Ort`<br/>Ort des Betriebes. Standardwert ist -1.
**Feld**         | `<BetrStrasseNr>` - MI/OP
**Beschreibung** | `MAGELLAN >  Betriebe > Daten > Strasse`<br/>Strasse des Betriebes. Standardwert ist -1.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

### Besonderheit

`<schueler><Besonderheit>` - OP

Besonderheiten der Schüler werden aktuell nicht unterstützt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<BesonderheitId>` - MI
**Beschreibung** | `Nicht unterstützt`<br/>Die Besonderheit des Schülers.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

### Vorjahr

`<schueler><Vorjahr>` - OP

Vorjahresinformationen werden nur für Berufsbildende Schulen oder im Falle eines Zuzuges nach MVP ausgespielt.

Voraussetzungen zum Export aus MAGELLAN Sicht. Es muss nur eine von beiden Voraussetzungen erfüllt sein.

* Eintrag einer BBS Schulform unter  `MAGELLAN > Mandanten > Daten 1 > Schulformen`
* Eintrag eines Zuzugsdatums unter `MAGELLAN > Schüler > Merkmale > Merkmal U2`

Titel            | Inhalt
---------------- | ------
**Feld**         | `<BetaetigungVorjahrId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Unterlagen`<br/>Betätigung des Schülers im Vorjahr.
**Feld**         | `<JahrgangsStufeVorjahrId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Klassenstufe`<br/>Besuchte Klassenstufe des Schülers im Vorjahr.

### Fremdsprache

`<Schueler><Fremdsprache>` - OP

Gewählte Fremdsprachen des Schülers.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<FremdSpracheId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Fremdsprachen > 1. - 4. Fremdsprache`<br/>Die gewählte Fremdsprache.
**Feld**         | `<FremdSpracheArtId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Fremdsprachen > 1. - 4. Fremdsprache > Status`<br/> `MAGELLAN > Schüler > Daten 1 > Fremdsprachen > 1. - 4. Fremdsprache > Zusatz`<br/>Die Art der Fremdsprache berechnet sich aus der Kombination der Felder `Status` und `Zusatz`.
**Feld**         | `<VonJahrgangsStufeId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Fremdsprachen > 1. - 4. Fremdsprache > Von`<br>Anfängliche Jahrgangsstufe der Fremdsprache.
**Feld**         | `<VonJahrgangsStufeId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Fremdsprachen > 1. - 4. Fremdsprache > Bis`<br>Letzte Jahrgangsstufe der Fremdsprache.
**Feld**         | `<Reihenfolge>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Fremdsprachen > 1. - 4. Fremdsprache > Bis`<br>MAGELLAN kennt genau vier Fremdsprachen, die Reihenfolge ergibt sich daraus.

#### Berechnung der Fremdsprachenart

Status           | Zusatz                    | Ausgabewert
---------------- | ------------------------- | -----------
Ergänzend        | Muttersprachl. Unterricht |  3 = muttersprachl. Unterricht als Ergänzungsunterricht
                 | Muttersprachl. Unterricht |  4 = muttersprachl. Unterricht als Fremdsprache
                 | Neigungsunterricht        |  5 = Neigungsunterricht
                 | Pflichtfach               |  6 = Pflichtfach
                 | Wahlpflichtfach           |  7 = Wahlpflichtfach
abgewählt        | -                         |  8 = abgewählt
                 | Basiskurs                 |  9 = Basiskurs
                 | Erweiterungskurs          | 10 = Erweiterungskurs
                 | Gymnasialkurs             | 11 = Gymnasialkurs Sek I (IGS)
Fach             | Wahlpflichtfach           | 12 = Fach als Wahlpflichtfach
Hauptfach        | Pflichtfach               | 13 = Hauptfach als Pflichtfach
Hauptfach        | Wahlpflichtfach           | 14 = Hauptfach als Wahlpflichtfach
Fach             | Wahlfach (fakultative FS) | 15 = Fach als Wahlfach
Hauptfach        | Wahlfach (fakultative FS) | 16 = Fach als Wahlfach

### Foerderung

`<Schueler><Foerderung>` - OP

Liste von pädagogischen und sonderpädagogischen Förderungen.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<FoerderungArtId>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Beinträchtigungen und Fördermaßnahmen > Diagnose/Behinderung`<br/>Die Art der Beeinträchtigung.
**Feld**         | `<Bedarf>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Beinträchtigungen und Fördermaßnahmen > Bedarf`<br/>Wurde ein Förderbedarf festgestellt (Ja/Nein).
**Feld**         | `<Foerderung>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Beinträchtigungen und Fördermaßnahmen >`<br/>Wurde (oder wird aktuell) eine Förderung durchgeführt (Ja/Nein).
**Feld**         | `<Schwerpunkt>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Beinträchtigungen und Fördermaßnahmen > Schwerpunkt 1`<br/>Ist der festgestellte Förderbedarf = Förderschwerpunkt? Wenn ja, wiederholen Sie bitte die Eingabe aus `Diagnose/Behinderung` (Ja/Nein).
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Beinträchtigungen und Fördermaßnahmen > Von`<br/>`MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP. Wenn Sie bei der Förderung `Von` angegeben haben, wird dieser Wert genutzt, ansonsten, die vorige Eingabe aus dem Assistenten.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Beinträchtigungen und Fördermaßnahmen > Bis`<br/>`MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP. Wenn Sie bei der Förderung `Bis` angegeben haben, wird dieser Wert genutzt, ansonsten, die vorige Eingabe aus dem Assistenten.

### SchuelerKlasse

`<Schueler><SchuelerKlasse>` - OP

Die Liste der SchuelerKlassen sind die Klassen, in denen die Schüler tatsächlich eingeschult sind. Diese Klassen müssen auch Bestandteil der zuvor durchlaufenen Liste der Klassen im Zeitraum sein. Ein Teil der Dokumentation wiederholt sich hier, da einige Felder bereits im Abschnitt [Klasse](#klasse) beschrieben wurden.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<KlasseId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Auswahl > ID` / `MAGELLAN > Klassen > Auswahl > GUIDExtern`<br/>Eindeutiger Wert zur Identifizierung der Klasse. Dieser wird entsprechend ausgelesen.
**Feld**         | `<BildungsgangId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Daten > Bildungsgang`<br/>Der Bildungsgang der Klasse.
**Feld**         | `<FachRichtungId>` - MI
**Beschreibung** | `MAGELLAN > Extras > Verzeichnisse > Bildungsgaenge > Fachrichtung`<br/>`MAGELLAN > Klassen > Daten > Bildungsgang`<br/>**Nur BBS**: Jeder Bildungsgang im Verzeichnis der Bildungsgänge hält einen Verweis auf die Fachrichtung (Verzeichnis der Fachrichtungen). Durch die Auwahl des Bildungsgang der Klasse, wählt man somit indirekt auch die Fachrichtung aus.
**Feld**         | `<JahrgangsStufeId>` - MI
**Beschreibung** | `MAGELLAN > Klassen > Zeiträume > Klassenstufe`<br/>Die Klassenstufe der Klasse.
**Feld**         | `<StatusId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Auswahl > Status`<br/>`MAGELLAN > Schueler > Laufbahn > Allgemein > Versetzt`<br/>`MAGELLAN > Schueler > Laufbahn > Allgemein > Versetzungsart`<br/>`MAGELLAN > Schueler > Daten 2 > Abgang > Abgangsart`<br/>Der Status des Schülers berechnet sich aus der Kombination der MAGELLAN Felder.
**Feld**         | `<IstOertlichZustaendigeSchule>` - MI
**Beschreibung** | `MAGELLAN > Schueler > ?? > ??`<br/>Ist die Schule die örtlich zutändige Schule? (Ja/Nein). Aktuell wird immer Ja ausgespielt.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

#### Berechnung der StatusId

Folgende Werte werden nicht unterstützt:

Ausgabewert                        | ABS/BBS
---------------------------------- | -------  
4 = angemeldet                     | ABS/BBS
5 = zurückgezogen                  | ABS/BBS
6 = angenommen                     | ABS/BBS
7 = abgelehnt                      | ABS/BBS
8 = zurückgestellt                 | ABS/BBS

Folgende Werte berechnen sich aus:

* Versetzungsart wird nur bei Status `eingeschult` ausgewertet
* Abgangsart wird nur bei Status `ausgeschult` ausgewertet

Ausgabewert                        | ABS/BBS | Status           | Versetzt         | Versetzungsart/Abgangsart
---------------------------------- | ------- | ---------------- | ---------------- | -------------------------
9 = Schüler                        | ABS/BBS | eingeschult      | keine Auswertung | keine Auswertung
10 = versetzt                      | ABS/BBS | ein- ausgeschult | versetzt         | keine Auswertung
11 = aufgestiegen                  | ABS/BBS | eingeschult      | versetzt         | aufgestiegen
12 = überspringt freiw. JgSt       | ABS/BBS | eingeschult      | versetzt         | überspringt freiw. JgSt
13 = nicht versetzt                | ABS/BBS | eingeschult      | nicht versetzt   | keine Auswertung
14 = tritt freiwillig zurück       | ABS/BBS | eingeschult      | nicht versetzt   | tritt freiwillig zurück
15 = wechselt Klasse               | ABS/BBS | eingeschult      | keine Auswertung | wechselt Klasse
16 = Wegzug aus MV                 | ABS/BBS | ausgeschult      | keine Auswertung | Wegzug aus MV
17 = Absolvent verbleibt ABS       | ABS     | ausgeschult      | keine Auswertung | Absolvent verbleibt ABS
18 = Absolvent verbleibt BBS       | BBS     | ausgeschult      | keine Auswertung | Absolvent verlässt ABS
19 = Absolvent verlässt ABS        | ABS     | ausgeschult      | keine Auswertung | Absolvent verbleibt BBS
20 = Absolvent verlässt BLS        | BBS     | ausgeschult      | keine Auswertung | Absolvent verlässt BLS
21 = Abgänger                      | ABS/BBS | ausgeschult      | keine Auswertung | Abgänger
22 = Abbrecher                     | ABS/BBS | ausgeschult      | keine Auswertung | Abbrecher
23 = verstorben                    | ABS/BBS | ausgeschult      | keine Auswertung | verstorben
24 = wechselt Schule               | ABS/BBS | ausgeschult      | keine Auswertung | wechselt Schule
25 = Abo beendet                   | ABS     | ?                | ?                | ?
26 = abgeordnet (an Krankenschule) | ABS     | ausgeschult      | keine Auswertung | abgeordnet (an Krankenschule)
27 = im Ausland                    | ABS     | ?                | ?                | ?
28 = Frühförderung beendet         | ABS     | ?                | ?                | ?
29 = verbleibt PL (JgSt-Pl)        | ABS     | ?                | ?                | ?

### SchuelerUe

`<Schueler><SchuelerUe>` - OP

Unterrichtseinheiten des Schülers, basierend auf den Unterrichteinheiten der Schule [Ue](#ue). Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### Schulbefreiung

`<Schueler><Schulbefreiung>` - OP

Liste von Befreiungen der Schulpflicht aus gegebenen Gründen.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<GrundId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abwesenheiten > Grund`<br/>Grund der Schulbefreiung.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abwesenheiten > Von`<br/>`MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP. Wenn Sie bei der Abwesenheit `Von` angegeben haben, wird dieser Wert genutzt, ansonsten, die vorige Eingabe aus dem Assistenten.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abwesenheiten > Bis`<br/>`MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP. Wenn Sie bei der Abwesenheit `Bis` angegeben haben, wird dieser Wert genutzt, ansonsten, die vorige Eingabe aus dem Assistenten.

### SchulischeVorbildungAllgemeinbildend

`<Schueler><SchulischeVorbildungAllgemeinbildend>` - OP

Der höchste allgemeinbildende Abschluss.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AbschlussId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Daten 2 > Höchster Abschluss ABS > Abschluss`<br/>Der höchste allgemeinbildende Abschluss.
**Feld**         | `<AbschlussDatum>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Daten 2 > Höchster Abschluss ABS > Erreicht am`<br/>Das Datum des höchsten allgemeinbildenden Abschluss.

### SchulischeVorbildungBerufsbezogenSchulisch

`<Schueler><SchulischeVorbildungBerufsbezogenSchulisch>` - OP

Der höchste berufsbezogene schulische Abschluss.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AbschlussId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Daten 2 > Höchster Abschluss BBS > Abschluss`<br/>Der höchste berufsbezogene schulische Abschluss.
**Feld**         | `<AbschlussDatum>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Daten 2 > Höchster Abschluss BBS > Abschluss - Erreicht am`<br/>Das Datum des höchsten berufsbezogenen schulischen Abschluss.

### SchulischeVorbildungBerufsbezogenBeruflich

`<Schueler><SchulischeVorbildungBerufsbezogenBeruflich>` - OP

Der höchste berufsbezogene beruflische Abschluss.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AbschlussId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Daten 2 > Höchster Abschluss BBS > Beruf`<br/>Der höchste berufsbezogene beruflische Abschluss.
**Feld**         | `<AbschlussDatum>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Daten 2 > Höchster Abschluss BBS > Beruf - Erreicht am`<br/>Das Datum des höchsten berufsbezogenen beruflischen Abschluss.

### AbschlussAllgemeinbildend

`<Schueler><AbschlussAllgemeinbildend>` - OP - **NUR ABS**

Erreichter allgemeinbildender Abschluss im Schulhalbjahr an Ihrer Schule.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AbschlussId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 1`<br/>`MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 2`<br/>Ein an Ihrer Schule erreichter Abschluss. Es werden die Felder  `Abschluss 1` vor `Abschluss 2` ausgegeben, falls beide oder nur einer gefunden wird.
**Feld**         | `<AbschlussDatum>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 1 - Abschlussdatum`<br/>`MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 2 - Abschlussdatum`<br>Es wird das jeweilige Abschlussdatum ausgegeben.

### AbschlussBerufsbezogendSchulisch

`<Schueler><AbschlussBerufsbezogendSchulisch>` - OP - **NUR BBS**

Erreichter berufsbezogener schulischer Abschluss im Schulhalbjahr an Ihrer Schule.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AbschlussId>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 1`<br/>`MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 2`<br/>Ein an Ihrer Schule erreichter Abschluss. Es werden die Felder  `Abschluss 1` vor `Abschluss 2` ausgegeben, falls beide oder nur einer gefunden wird.
**Feld**         | `<AbschlussDatum>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 1 - Abschlussdatum`<br/>`MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 2 - Abschlussdatum`<br>Es wird das jeweilige Abschlussdatum ausgegeben.
**Feld**         | `<Zeugnis>` - MI
**Beschreibung** | `MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 1 - Abschlussart`<br/>`MAGELLAN > Schueler > Laufbahn > Abschluss > Abschluss 2 - Abschlussart`<br>Es wird die jeweilige Abschlussart ausgegeben.

### Lehrer

`<Lehrer>` - OP

Die Liste der Lehrer.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<LehrerId>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Auswahl > ID` / `MAGELLAN > Lehrer > Auswahl > GUIDExtern`<br/>Eindeutiger Wert zur Identifizierung der Lehrer. Beim ersten Export wird die MAGELLAN ID verwendet. Beim Übertrag von Daten SIP -> MAGELLAN erhalten die Schüler den Identifikator von SIP für zukünftige Übertragungen.
**Feld**         | `<GeschlechtId>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 1 > Geschlecht`<br/>Geschlecht. Mögliche Werte sind:<br>Männlich, Weiblich, Divers = Wählen Sie diesen Wert einfach aus.<br>Ohne Angabe im Geburtenregister = Lassen Sie das Feld in MAGELLAN leer.
**Feld**         | `<LehrAmtId>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 3 > Lehrämter > Lehramt`<br/>**Nur Freie Schulen**: Es wird das erste eingetragene Lehramt ausgelesen.
**Feld**         | `<StaatsangehoerigkeitId>` - MI/OP
**Beschreibung** | `MAGELLAN > Lehrer > Daten 1 > Staatsangeh. 1`<br/>1. Staatsangehörigkeit. Standardwert ist 0 = Deutsche Staatsangehörigkeit
**Feld**         | `<TaetigkeitArtId>` - MI/OP
**Beschreibung** | `MAGELLAN > Lehrer > Daten 2 > Dienstbez.`<br/>**Nur Freie Schulen**: Dienstbezeichnung. Standardwert ist -1.
**Feld**         | `<PersonenGruppeId>` - MI/OP
**Beschreibung** | `MAGELLAN > Lehrer > Daten 2 > Besch-verh.`<br/>**Nur Freie Schulen**: Beschäftigungsverhältnis. Standardwert ist -1.
**Feld**         | `<Titel>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 1 > Anrede`<br/>Anrede.
**Feld**         | `<Vorname>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 1 > Vorname`<br/>Vorname.
**Feld**         | `<Nachname>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 1 > Nachname`<br/>Nachname.
**Feld**         | `<GebDatum>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 1 > Geburtsdatum`<br/>Geburtsdatum.

### FachLehrBefaehigung

`<Lehrer><FachLehrBefaehigung>` - OP

Die Lehrbefähigungen des Lehrers.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<FachId>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 3 > Lehrämter > Lehramt`<br/>Es werden die Lehrämter vom Typ `Lehrbefähigung` des Lehrers ausgelesen.

### Ausbildung

`<Lehrer><Ausbildung>` - OP

Ausbildungen der Lehrer werden aktuell nicht unterstützt. - **Nur Freie Schulen**

### Beschaeftigung

`<Lehrer><Beschaeftigung>` - OP

Beschäftigungsinformationen der Lehrer. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### LehrerUe

`<Lehrer><LehrerUe>` - OP

Unterrichtseinheiten des Lehrers, basierend auf den Unterrichteinheiten der Schule [Ue](#ue). Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### Alterszeilzeit

`<Lehrer><Alterszeilzeit>` - OP

Studeninformationen der Lehrer. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt. - **Nur Freie Schulen**

### Arbeitszeitkonto

`<Lehrer><Arbeitszeitkonto>` - OP

Studeninformationen der Lehrer. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt. - **Nur Freie Schulen**

### Rolle

`<Lehrer><Rolle>` - OP

Spezielle Rollen, die ein Lehrer an der Schule ausüben kann.
Entsprechend Ihrer Auswahl wie in `RolleId` beschrieben, wird für jeden Lehrer nachgeschaut und der Eintrag ausgewertet. Ist also ein Lehrer als Klassenlehrer für eine Klasse angegeben, wird ein Eintrag zur Ausgabe bei Rolle gemacht und zusätzlich die `KlasseId` ausgespielt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<RolleId>` - MI
**Beschreibung** | `MAGELLAN > Klasse > Zeiträume > Klassenleiter 1` = Rolle `Klassenleiter`<br>`MAGELLAN > Mandanten > Daten 1 > Schulleiter` = Rolle `Schulleiter`<br>>`MAGELLAN > Mandanten > Daten 1 > Stellvertreter` = Rolle `Ständiger Vertreter des Schulleiters`
**Feld**         | `<KlasseId>` - OP
**Beschreibung** | `MAGELLAN > Klassen > Auswahl > ID` / `MAGELLAN > Klassen > Auswahl > GUIDExtern`<br/>Eindeutiger Wert zur Identifizierung der Klasse. Beim ersten Export wird die MAGELLAN ID verwendet. Beim Übertrag von Daten SIP -> MAGELLAN erhalten die Klassen den Identifikator von SIP für zukünftige Übertragungen.
**Feld**         | `<GueltigAb>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig von`<br/>Gültigkeitsangabe der Daten für SIP.
**Feld**         | `<GueltigBis>` - MI
**Beschreibung** | `MAGELLAN > Export > SIP > Gültig bis`<br/>Gültigkeitsangabe der Daten für SIP.

### Anrechnung

`<Lehrer><Anrechnung>` - OP

Studeninformationen der Lehrer. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### PmsAEinsatz

`<Lehrer><PmsAEinsatz>` - OP

Studeninformationen der Lehrer. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### StundenAbgabe

`<Lehrer><StundenAbgabe>` - OP

Studeninformationen der Lehrer. Da es sich bei diesen Daten weitestgehend um Stundenplandaten handelt, sind diese in MAGELLAN nicht untersützt.

### Abgang

`<Lehrer><Abgang>` - OP

Informationen über den Abgang des Lehrers von der Schule.
Wird nur ausgespielt, wenn der Lehrer ein Abgang und Abgangsdatum innerhalb des angegebenen Gültigkeitszeitraum gesetzt hat.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<AbgangsArtId>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 2 > Zugang/Abgang > Abgangsart`<br>Grund des Abgangs.
**Feld**         | `<AbgangsDatum>` - MI
**Beschreibung** | `MAGELLAN > Lehrer > Daten 2 > Zugang/Abgang > Abgang am`<br>Datum des Abgangs.

### Schulwerkstatt

`<Schule><Schulwerkstatt>` - OP

Schulwerkstätten werden aktuell nicht unterstützt.
