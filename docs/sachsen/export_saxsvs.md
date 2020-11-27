# Export von Daten für SaxSVS aus MAGELLAN

1. [Beachten Sie bitte die Mindesteingaben für den Export](https://doc.ls.stueber.de/sachsen/einstieg/#voraussetzungen-fur-den-export))
2. Lesen Sie dieses Kapitel gut durch, die meisten Probleme berufen sich auf fehlende oder falsche Eingaben in MAGELLAN.
3. Lesen Sie im Kapitel [Schnittstellendatei aus MAGELLAN erzeugen](saxsvs_xml.erzeugen.md), wie Sie den Export durchführen.

Nachstehend finden Sie eine Auflistung der relevanten Felder und der jeweiligen Stelle, an der Sie in MAGELLAN eingepflegt werden.
Ggf. haben wir nach XML-Elementen (Knoten) aufgeteilt.

!!! warning "Wichtig"

    Die XML-Knoten werden in der Dokumentation wie folgt benannt: `<Knotenname>`. Unterknoten können dann z.B. so aussehen `<saxsvs-bbs><schueler>`

## Abgänger in SAXSVS-A

SAXSVS möchte zu unterschiedlichen Zeiten unterschiedlich gefilterte Datensätze. Neben der *SAXSVS.xml* Datei, die aktuelle und abgegangene Schüler des laufenden Schuljahres berücksichtigt, kann die Schnittstelle auch die *SAXSVS-A.XML* Datei erzeugen, die abgegangene Schüler und/oder Schüler mit Abschluss zum Schuljahresende des vorigen Schuljahres berücksichtigt.

Wenn eine der beiden folgenden Vorgaben erfüllt ist, dann wird ein Schüler in der SAXSVS-A Datei berücksichtigt:

Feld in MAGELLAN                             | Art       | Beschreibung
-------------------------------------------- | --------- | ------------
Schüler > Daten 2 > Abgang > **Abgangsart**<br>Schüler Daten 2 > Abgang > **Abgang am** | Abgänger  | Schüler ist ausgeschult und beide Felder müssen gefüllt sein.
 | **ODER** |  
Schüler > Laufbahn > Abschluss > **Abschluss 1**<br>Schüler > Laufbahn > Abschluss > **Abschlussdatum1** | Abschluss | Schüler ist ausgeschult und beide Felder müssen gefüllt sein - auch bei Schülern ohne Abschluss (Abgangszeugnis)!

!!! danger "Achtung"

    Zwei Bedingungen müssen für die Datumswerte erfüllt werden:
    
    1. Sollten Sie beide Datumsfelder befüllen, müssen beide Datumswerte aus `AbgangAm` oder `Abschlussdatum1` im selben Zeitraum des vergangenen Schuljahres liegen.
    2. Die Von- und Bis-Daten der Zeiträume (`Extras > Schlüsselverzeichnisse > Zeiträume`) müssen 01.08-31.01 oder 01.02-31.07 sein.

!!! tip "Tipp"

    Um die Felder `Abschluss1` und `Abschlussdatum1` unter `Schüler > Laufbahn > Abschluss`zu füllen, steht Ihnen eine Sammelzuweisung zur Verfügung.

## Aktuelle Schüler in SAXSVS

## Legende

Erklärung zu einigen wenigen Abkürzungen bzw. erwähnenswerten Anmerkungen die in der Beschreibung verwendet werden.

Benennung      | Beschreibung
-------------- | ------------
Werte          | Die Schnittstelle erwartet zumeist einen der folgenden Wertetypen:<br/>- Ein Wert aus einem Katalog, z.B. 20, 60 etc. meistens eine Zahl die im Kontext der Werteliste eine entsprechende Bedeutung hat<br/>- „Ja“/“Nein“ – Trifft, oder trifft nicht zu<br/>- Freitextfeld<br/>-Datum im Format YYYY-MM-DD<br/>- Zahlwert
MI             | *Mindestvoraussetzung.* Diese Felder müssen gefüllt sein, da ansonsten der Import in SAXSVS grundsätzlich aufgrund von XML-Schemafehlern nicht durgeführt werden kann.
OP             | *Optional Pflicht.* Wenn grundsätzliche Aussagen zutreffen und Sie Felder in MAGELLAN mit Werten füllen, dann sind die Felder mit OP für diesen Bereich als Pflichtfelder zu sehen und müssen eingetragen werden. Beispiel: Abwesenheiten. Wenn Sie eine Abwesenheit mit Grund eintragen, muss auch das Von-Datum gefüllt werden, da ansonsten auch wieder ein XML-Schemafehler vorliegt.
GUID           | Ein *Globally Unique Identifier* ist eine Zahl mit 128 Bit (16 Bytes). Die GUID stellt eine Implementierung des Universally-Unique-Identifier-Standards (UUID) dar. Die Absicht hinter GUIDs ist, Informationen in verteilten Systemen ohne zentrale Koordination eindeutig kennzeichnen zu können. Zusammenfassend, ein starker eindeutiger Wert, über Systemgrenzen hinweg.

## Aufbau der Schnittstelle

Es gibt in der Schnittstelle zwei Stränge für die Angabe von Daten:

```xml
1. <saxsvs-bbs><schueler>
2. <saxsvs-bbs><schueler_loeschen>
```

Wenn sich Datensätze innerhalb dieser Stränge wiederfinden, dann werden sie entweder in SAXSVS eingepflegt oder gelöscht.
Wie Sie verhindern können, bzw. wann automatisch Datensätze nicht exportiert werden und wie Sie Datensätze für die Löschung vorsehen,
erfahren Sie im folgenden Unterabschnitt.

### Datensätze vom Export ausschließen, für die Löschung in SAXSVS vorsehen

Sie haben die Möglichkeit grundsätzlich Schüler von der Schnittstelle auszuschließen, Gastschüler auszuschließen und Schüler zur Löschung vorzusehen.

#### Gastschüler ausschließen

Schüler, die von einer anderen Schule (die Stammschule) an SAXSVS übergeben werden, aber in Ihrem System aufgrund eines Gastaufenthaltes in MAGELLAN eingepflegt sind,
können als Gastschüler markiert und somit aus dem Export ausgeschlossen werden.
Einen Gastschüler markieren Sie mit dem gleichnamigen Häkchen unter `Schüler > Daten 3 > Verschiedenes > Gastschüler`.

#### Schüler ausschließen

Schüler, die aus anderen Gründen nicht nach SAXSVS übergeben werden sollen. Beispielsweise, weil Sie mitten in der Erfassung der Daten stecken und erst einmal einen Teil der bereits gepflegten Schüler übertragen möchten, können unter `Schüler > Statistik > Merkmal S10` entsprechend mit "Kein Export" markiert werden.

Steht Ihnen in dem Feld keine Auswahl zur Verfügung, importieren Sie bitte das Verzeichnis `BS_SchuelerMerkmale.keys` erneut oder legen unter `Extras > Schlüsselverzeichnisse > Merkmale (Schüler)` eine Schlüsselzeile entsprechend der nachfolgenden Abbildung an. Der Wert kann auch per Sammelzuweisung verteilt werden.

![MAGELLAN 7 > Extras > Schlüsselverzeichnisse > Merkmale (Schüler)](/assets/images/sachsen/kein.saxsvs.png)

#### Schüler zum Löschen vorsehen

`<saxsvs-bbs><schueler_loeschen>`

In der XML-Datei sieht das wie folgt aus:

```xml
<saxsvs-bbs ...>
    <schueler_loeschen extern_id="{A0EA16FB-724E-4345-A3EF-62F3E08C6827}"/>
    <schueler_loeschen extern_id="{A0EA16FB-724E-4345-A3EF-62F3E08C6828}"/>
    <schueler_loeschen extern_id="{A0EA16FB-724E-4345-A3EF-62F3E08C6829}"/>  
```

Schüler die in SAXSVS zum Löschen vorgemerkt werden sollen, können unter `Schüler > Statistik > Merkmal S10` mit dem entsprechenden Schlüssel markiert werden.
Der Wert kann auch per Sammelzuweisung verteilt werden.

### Kopfbereich  

`<saxsvs-bbs>`

Der Haupteinstiegsknoten ist `<saxsvs-bbs>` und enthält Kopfdaten für die Schnittstelle,
wie die Versionsnummer der adressierten SAXSVS-Schnittstelle oder auch Ihre Dienststellennummer.

In der XML-Datei sieht das wie folgt aus:

```xml
<saxsvs-bbs xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:noNamespaceSchemaLocation="https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.3.xsd"
zeit="TDateTime Today (2020-03-17T09:30:47-05:00)"
schuljahr="Zeitraeume.Von (2019/2020)"
dienststelle="Mandanten.Schulnummer">
```

Feld in Schnittstelle       | Beschreibung
--------------------------- | ------------
`<saxsvs-bbs zeit>`         | Für dieses Feld wird automatisch ein aktueller Datums-/Zeitstempel beim Export eingefügt.
`<saxsvs-bbs schuljahr>`    | `MAGELLAN > Verzeichnisse > Zeitraeume > Von`<br/> Aus dem Eintrag wird der geforderte Wert im Format `JJJJ/JJJJ` gebildet, als Beispiel: 2019/2020
`<saxsvs-bbs dienststelle>` | `MAGELLAN > Mandanten > Daten 1 > Schulnummer`<br/>7-stellige Dienststellennummer vom Amt

#### Schüler  

`<saxsvs-bbs><schueler>`

Ab hier beginnen die Schülerdaten. Schüler die nicht von der Schnittstelle ausgeschlossen und valide sind,
erscheinen als Datensatz mit einem `<schueler>` Knoten in der XML-Datei. Ab hier werden die weiteren Unterknoten in dieser Dokumentation nicht weiter
mit den Elternknoten benannt.

Ein Schülerknoten enthält alle Informationen die zum Schüler gehören und wird erzeugt, wenn der Schülerdatensatz Bestandteil des Exportes ist.
Dies ergibt sich aus folgenden Regeln:

1. Ein Schüler in MAGELLAN ist nicht gleich ein Schüler in SAXSVS. Der Schüler in MAGELLAN macht sich anhand seiner MAGELLAN-ID und dem Mandanten in dem er sich befindet eindeutig.
   Dies ist in SAXSVS nicht so. Dort kann ein Schüler aufgrund seiner sich ändernden Ausbildungsumstände mehrfach vorhanden sein.
   Dazu nutzt SAXSVS eine GUID für jeden Schülerdatensatz, die sich ändert, wenn sich die Ausbildungsumstände entsprechend ändern, dass ein weiterer Datensatz nach SAXSVS gespielt werden muss.

!!! danger "Achtung"

    Wann wird die GUID erzeugt: 
    1. Bei Ausbildungsdatensätzen, die aus MAGELLAN 6 nach MAGELLAN 7 übernommen wurden, gibt es noch keine GUID. Beim ersten Export nach SAXSVS wird für diese Datensätze die GUID angelegt.
    2.  Für einen neu in Magellan 7 angelegten ersten Ausbildungsdatensatz wird automatisch eine GUID vergeben.
    3.  Wird für eine bestehenden Schüler eine weitere Ausbildung vergeben, muss entschieden werden, ob dieselbe GUID weiterverwendet werden soll oder eine neue GUID vergeben werden soll.
    4.  Wann eine neue GUID benötigt wird, muss der Kunde über Schulungen von den SAXSVS Verantwortlichen beantwortet bekommen.

Ein Schüler ohne GUID wird vom Export ausgeschlossen!

1. Der Schüler wird durch ein Merkmal explizit vom Export ausgeschlossen!
2. Der Schüler ist als Gastschüler gekennzeichnet und somit nur von der Stammschule nach SAXSVS einzuspielen. Der Schüler wird vom Export ausgeschlossen!
3. Der Schüler enthält einige Minimalvoraussetzungen. Wie in Punkt 1 erwähnt sind Ausbildungsinformationen für SAXSVS wichtig, neben der GUID müssen mindestens Bildungsgang,
   Organisationsform und Schulform angegeben werden. Fehlen diese Werte, wird der Schüler vom Export ausgeschlossen!

##### Sammelzuweisung für Bildungsgang, Schulform und Organisation

1. Die Sammelzuweisung rufen Sie unter `Menüpunkt Schüler > Registerkarte Schüler > Sammelzuweisung` auf.
2. Markieren Sie die Gruppe von Schülern, für die die gleichen Eigenschaften vergeben werden sollen.
3. Klicken Sie `Weiter` bis zur dritten Karte, hier können Ausbildungsinformationen neu oder ergänzend zugewiesen werden.<br/>Wichtig: bitte wählen Sie `Neue Ausbildung anlegen` oder `ggfs. aktuelle Ausbildung bearbeiten`!

![MAGELLAN 7 > Menü Schüler > Tab Schüler> Sammelzuweisung](/assets/images/sachsen/sammelzuweisung01.png)

##### Berufliches Gymnasium - Oberstufenschüler

Auch Schüler des beruflichen Gymnasiums müssen einen Bildungsgang zugewiesen bekommen. Diesen können Sie auch über die Sammelzuweisung vergeben.
Folgende Bildungsgänge sind für BGY gedacht:

Kennziffer | Bildungsgang                                  |Schulart | Zeitform
---------  | --------------------------------------------- |-------- | --------
83000002   | Ernährungswissenschaft                        | BGY     | v
82000003   | Gesundheit und Sozialwesen                    | BGY     | v
43000001   | Informations- und Kommunikationstechnologie   | BGY     | v
43000002   | Technikwissenschaft                           | BGY     | v
32000001   | Technikwissenschaft/Bautechnik                | BGY     | v
43000003   | Technikwissenschaft/Datenverarbeitungstechnik | BGY     | v
26000001   | Technikwissenschaft/Elektrotechnik            | BGY     | v
25000001   | Technikwissenschaft/Maschinenbautechnik       | BGY     | v
71000002   | Wirtschaftswissenschaft                       | BGY     | v

### Allgemeine Angaben

Hier stehen alle Werte die nicht in besonderen XML-Knoten untergliedert sind.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<schueler extern_id>` - MI
**Beschreibung** | `MAGELLAN > Schüler > ID`<br/>Die ID des Schülers.
**Feld**         | `<an_vname>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Vorname`<br/>Vorname des Schülers.
**Feld**         | `<an_name>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Nachname`<br/>Nachname des Schülers.
**Feld**         | `<an_gebname>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geburtsname`<br/>Geburtsname des Schülers.
**Feld**         | `<an_gebdat>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geburtsdatum`<br/>Geburtsdatum des Schülers.
**Feld**         | `<an_gebort>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geburtsort`<br/>Geburtsort des Schülers.
**Feld**         | `<an_geschlecht>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Geschlecht`<br/>Geschlecht des Schülers.
**Feld**         | `<an_staatsang_1>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Staatsangeh. 1`<br/>1. Staatsangehörigkeit des Schülers.
**Feld**         | `<an_staatsang_2>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Staatsangeh. 2`<br/>2. Staatsangehörigkeit des Schülers.
**Feld**         | `<al_kennziffer>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Ausbildung > Bildungsgang`<br/>Bildungsgang des Schülers.<br />Lesen Sie dazu den obigen Abschnitt [Mindestvoraussetzung für den Export](einstieg.md#voraussetzungen-fur-den-export).
**Feld**         | `<al_schulart>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Ausbildung > Schulform`<br/>Schulform des Schülers im Bildungsgang.<br />Lesen Sie dazu den obigen Abschnitt [Mindestvoraussetzung für den Export](einstieg.md#voraussetzungen-fur-den-export).
**Feld**         | `<al_status>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Statistik > Merkmale > Merkmal S1`<br/>Status des Schüler lt. Schnittstelle.<br />Wenn kein Wert angegeben, dann wird der Status automatisch als 1 = Schüler in der Schnittstelle ausgegeben.
**Feld**         | `<al_zeitform>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Ausbildung > Organisation`<br/>Die Zeitform des Schülers im Bildungsgang.<br />Lesen Sie dazu den obigen Abschnitt [Mindestvoraussetzung für den Export](einstieg.md#voraussetzungen-fur-den-export).
**Feld**         | `<al_abschl_dat>` - MI
**Beschreibung** | `MAGELLAN > Schüler > Ausbildung > Ausbildung editieren > Ausbildung bis`<br/>Das voraussichtliche Enddatum der Ausbildung.
**Feld**         | `<al_laufb_kl>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Klasse`<br/>Die aktuelle Klasse des Schülers. Eine Klasse hat der Schüler sobald die Einschulung erfolgt ist. Das Klassenkürzel wird für die aktuelle Klasse  aus dem Feld `Statistikkürzel` ausgelesen.
**Feld**         | `<al_laufb_von>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Allgemein > Zugang`<br/>Das Zugangsdatum der Laufbahn, damit Zugang zur Klasse.
**Feld**         | `<al_laufb_bis>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Allgemein > Abgang`<br/>Das Abgangsdatum der Laufbahn, damit Abang aus Klasse.
**Feld**         | `<al_laufb_bem>`
**Beschreibung** | `Nicht unterstützt`<br/>Ein Freitextfeld zur Laufbahn.
**Feld**         | `<al_laufb_neuanf>`
**Beschreibung** | `MAGELLAN > Schüler > Ausbildung > Neuanfänger`<br/>Neuanfänger im Bildungsgang. Neuanfänger ist:<br />* ein Schüler im AJ1, wenn er die Ausbildung beginnt (Normalfall)<br />* ein Schüler im AJ2, wenn er sofort in das 2. AJ einsteigt (die Klasse ist aber schon ein Jahr in Beschulung) -> das trifft bspw. zu, wenn ein Schüler vorher Gym gemacht hat und da wird manchmal (Antrag bei der Kammer) das erste AJ erlassen<br />* ein Schüler im AJ3, wenn er eine artähnliche Ausbildung macht (sicher ein Sonderfall) -> ein Schüler lernt Restaurantkaufmann und macht eine zusätzliche Ausbildung als Hotelkaufmann (dieser Sachverhalt ist keine Stufenausbildung)<br />* ein Schüler, der eine Ausbildung fertig hat (bspw. BVJ) und nun eine Ausbildung macht<br /><br />Neuanfänger ist nicht:<br />* ein Schüler im AJ1, wenn er die Ausbildung ein 2. Mal beginnt -> Ausbildung beginnt, Schülerin macht Erziehungsurlaub ab Oktober und fängt im Folgejahr noch einmal mit AJ1 an, eigentlich keine neue UUID erforderlich<br />* ein Schüler im AJ2, wenn er artähnlich wechselt<br/> -> Neue Kennziffer -> das trifft bspw. zu, wenn ein Schüler von Fleischer auf Fleischfachverkäufer wechselt (keine neue UUID)<br />* ein Schüler, der im AJ1 Schulpflichterfüller war und innerhalb des Jahres nichts gefunden hat und noch ein Jahr Schulpflichterfüller ist (der bekommt aber auch eine neue Kennziffer) (keine neue UUID)<br />* ein Schüler im AJ3, der eine aufgesetzte Ausbildung macht -> ein Schüler lernt Verkäufer (2 Jahre) und macht anschließend die Ausbildung zum Einzelhandelskaufmann im AJ3 -> er bekommt eine neue Kennziffer, der erste Abschluss muss gezählt werden, deshalb eine neue UUID, aber er darf das Merkmal Neuanfänger nicht bekommen (Festlegung vom SMK)<br />* ein Schüler im AJ2, der innerhalb von Dubas (Beruf mit Abitur) lernt -> im ersten Jahr ist er Schüler des BGY, ab dem 2. AJ ist er Schüler der Schulart BS/BS, hat eine neue Kennziffer, aber keine neue UUID und der Abschluss des AJ1 wird nicht gezählt<br /><br />Und dann gibt es noch einen besonderen Sonderfall:<br />Ein Schüler soll verkürzt lernen. Er macht<br />* das AJ1 komplett<br />* das AJ2 und AJ3 parallel<br />Der Schüler hat im AJ1 einen Datensatz. Damit er gleichzeitig in AJ2 und AJ3 gezählt wird, muss er mit Beginn des AJ2 geklont werden. Damit ist der eine Schüler aus dem AJ1 jetzt zweimal da (auch namentlich, da er ja in beiden Klassen gezählt werden muss) -> Schüler ist beide Male kein Neuanfänger, obwohl er einmal neu angelegt wird.<br /><br />Sie haben die Möglichkeit die Option direkt auf der Karte unter `Schüler > Ausbildung` für den jeweiligen Ausbildungsdatensatz zu aktivieren oder zu deaktivieren. Alternativ können Sie hierfür auf die Sammelzuweisung für eine Gruppe von Schülern verwenden.
**Abbildung**    | <img src=/assets/images/sachsen/neuanf.png>
**Feld**         | `<al_laufb_bgut>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Finanzielle Förderung > Förderung`<br/>Innanspruchnahme des Bildungsgutschein vom Arbeitsamt.
**Feld**         | `<al_fremd_fs1>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 3 > 1. Fremdsprache`<br/>1. Fremdsprache des Schülers.
**Feld**         | `<al_fremd_fs2>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 3 > 2. Fremdsprache`<br/>2. Fremdsprache des Schülers.
**Feld**         | `<al_fremd_fs3>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 3 > 3. Fremdsprache`<br/>3. Fremdsprache des Schülers.
**Feld**         | `<al_ausgen>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Überweisung > Einschulantrag/Ausnahme`<br/>Ausnahmegenehmigung zum Besuch einer anderen Schule, als die vom Amt vorgesehene.
**Feld**         | `<al_mfoerdersw>`
**Beschreibung** | `MAGELLAN > Klassen > Daten > Einzelintegration / Förderklasse`<br/>`MAGELLAN > Schüler > Daten 4 > Förderungen > Förderschwerpunkt 1`<br/>Bei der Förderung wird zwischen Schülern unterschieden, die in einer Förderklasse eingeschult sind und damit speziellen rechtlichen Vorgaben unterliegen (Förderstunden, Gelder etc.) und allen anderen Schülern mit Förderbedarf. Die Ausgabe für die Schnittstelle ändert sich dementsprechend. Bei Schülern die in einer Förderklasse eingeschult sind, geben Sie bei der Klasse an, dass es sich um eine Förderklasse handelt. Der Förderschwerpunkt hingegen wird wie auch bei allen anderen Schülern direkt beim Schüler eingetragen und entsprechend ausgewertet.<br/><br/>**Wichtig**:<br/><br/>Förderklasse<br/>--------<br/>Ist der Schüler in einer Förderklasse (Häkchen gesetzt unter `MAGELLAN > Klassen > Daten > Einzelintegration/Förderklasse`) dürfen unter `Daten4 > Förderungen` **keine Förderstundenwerte** erfasst werden. <br/><br/>Keine Förderklasse<br/>--------<br/> Bei Schülern, die nicht in einer speziellen Förderklasse sind (kein Häkchen unter `MAGELLAN > Klassen > Daten > Einzelintegration/Förderklasse`) **müssen die Förderstundenwerte gefüllt** werden.
**Feld**         | `<af_behart>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Behinderung`<br/>Behinderungsart des Schülers. Dabei wird die Liste der Förderungen sortiert nach Position durchlaufen und der erste gefüllte Eintrag unter `Behinderung` ausgelesen.

### Abwesenheiten

`<saxsvs-bbs><schueler><abw>`

Werden angegeben, wenn ein Schüler längerfristig nicht anwesend ist, z.B. wg. Mutterschutz oder Aufenthalt im Ausland.

Eine Abwesenheit wird eingetragen, in dem Sie den Status des Schülers auf Abwesend setzen.
Dazu markieren Sie den Schüler und klicken im `Kontextmenü (Rechte Maustaste) > Status zuweisen...`. Sie können im Dialogfenster den Status Abwesend wählen und den Grund und Abwesenheitsdatum eintragen.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<an_abw_grund>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Abwesenheiten > Grund`<br/>Grund der Abwesenheit, z.B. 60 = Elternzeit.
**Feld**         | `<an_abw_dat>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Abwesenheiten > Von`<br/>Abwesend seit Datum.

### Migration  

`<saxsvs-bbs><schueler><migration>`

Wird angegeben, wenn ein Schüler nicht deutscher Herkunft ist.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<an_migr_grund>` - OP|
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > NdH`<br/>Es handelt sich um ein Ja/Nein Wert. Ja, wenn der Schüler nicht deutscher Herkunft ist, und somit einen Migrationshintergrund hat.
**Feld**         | `<an_migr_dat>`
**Beschreibung** | `MAGELLAN > Schüler > Statistik > Merkmal U2`<br/>Datum des Migrationsgespräches, also nicht des Zuzugs nach Deutschland.
**Feld**         | `<an_migr_daz>`
**Beschreibung** | `MAGELLAN > Schüler > Förderung > Bedarf`<br/>Es handelt sich um ein Ja/Nein Wert. Ja, wenn es sich um einen Schüler mit besonderer Bildungsempfehlung handelt und Deutsch als Zweitsprache, da nicht Muttersprache, unterrichtet bekommt. In MAGELLAN müssen Sie dazu im Förderbedarf den Wert `DAZ-3` auswählen.

### Adresse  

`<saxsvs-bbs><schueler><adresse>`

Die Adresse ist ein Pflichtknoten für die Mindestimplementation. Hier wird die Adresse des Wohnortes erwartet.
Die Schnittstelle unterscheidet dabei, ob der Schüler den Wohnsitz in Sachsen, außerhalb Sachsens in Deutschland oder im Ausland hat.
Lesen Sie bitte auch die Unterabschnitte der Adresse an, da je nach Wohnsitz andere Felder Pflicht sind. Z.B. ist der Eintrag von `Land` für im Ausland lebende Schüler zwingend erforderlich, um den Knoten `<an_staat>` mit dem entsprechenden Land zu füllen.

Zur Unterscheidung in MAGELLAN werden die Einträge in `Gemeinde` und `Land` wie folgt bewertet.

Eintrag                                                        | Bedeutung
-------------------------------------------------------------- | ---------
`Gemeinde` eingetragen<br />Schlüssel entspricht Sachsen       | Wohnsitz in Sachsen
`Gemeinde` eingetragen<br />Schlüssel entspricht nicht Sachsen | Wohnsitz in Deutschland
`Gemeinde` nicht eingetragen<br />`Land` <> "D", "DE", "DEU"   | Wohnsitz im Ausland
`Gemeinde` nicht eingetragen<br />`Land` = "D", "DE", "DEU"    | Keine Ausgabe, führt zu Fehler

#### Adresse Sachsen  

`<adresse_sachsen>`

Wird ausgegeben, wenn der Schüler im Bundesland Sachsen wohnt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<an_plz>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > PLZ`<br/>Postleitzahl des Wohnortes.
**Feld**         | `<an_ort>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ort`<br/>Wohnort.
**Feld**         | `<an_ortsteil>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ortsteil`<br/>Ortsteil des Wohnortes.
**Feld**         | `<an_strasse>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Straße`<br/>Straße des Wohnortes.

#### Adresse Deutschland  

`<adresse_deutschland>`

Wird ausgegeben, wenn der Schüler in Deutschland wohnt, aber nicht im Bundesland Sachsen.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<an_land>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Gemeinde`<br/>Bundesland des Wohnortes. Wird anhand des Gemeindeschlüssels ermittelt.
**Feld**         | `<an_plz>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > PLZ`<br/>Postleitzahl des Wohnortes.
**Feld**         | `<an_ort>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ort`<br/>Wohnort.
**Feld**         | `<an_ortsteil>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ortsteil`<br/>Ortsteil des Wohnortes.
**Feld**         | `<an_strasse>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Straße`<br/>Straße des Wohnortes.

#### Adresse Ausland  

`<adresse_ausland>`

Wird ausgegeben, wenn der Schüler im Ausland wohnt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<an_staat>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Land`<br/>Länderkürzel des Landes. <br/>MAGELLAN setzt aus den folgenden Länderkürzeln die Schlüsselnummer für die Übergabe in die XML-Datei um.<br/><br/>Mögliche Einträge:<br/>D/De/Deu=Deutschland (000)<br/>PL=Polen (152)<br/>CZ=Tschechische Republik (164)<br/>CH=Schweiz (158)<br/><br/>Sollten Sie weitere Werte benötigen, wird um entsprechende Rückmeldung im Support gebeten.
**Feld**         | `<an_plz>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > PLZ`<br/>Postleitzahl des Wohnortes.
**Feld**         | `<an_ort>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ort`<br/>Wohnort.
**Feld**         | `<an_ortsteil>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Ortsteil`<br/>Ortsteil des Wohnortes.
**Feld**         | `<an_strasse>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Straße`<br/>Straße des Wohnortes.

### Sorgeberechtigte  

`<saxsvs-bbs><schueler><sorgeberechtigte>`

Wird ausgegeben, wenn der Schüler Sorgeberechtigte eingetragen hat und der Schüler noch nicht volljährig ist. Wir berechnen die Volljährigkeit anhand des Geburtsdatums und Ihrer Angabe des Stichtages im Statistikassitenten.
SAXSVS erlaubt die Angabe von bis zu vier Sorgeberechtigten.
In MAGELLAN verwalten wir Familienmitglieder. Diese können `Schüler`, `Lehrer`, `Personen` und `Sorgeberechtigte` sein. Die Personendaten
werden in den jeweils einzelnen Ansichten eingetragen. Die Verbindung zum Schüler wird unter `Schüler > Daten 1 > Familie` angegeben.

!!! warning "Wichtig"

    Für den Export nach SAXSVS setzen wir die MAGELLAN-Sorgeberechtigten-Verhältnisse in Schlüssel um. 
    Für einige unserer Verhältnisse gibt es Entsprechungen als Schlüssel, für einige leider nicht. 
    Diese Verhältnisse (Eltern, Erziehungsberechtigte(r), Sorgeberechtigte(r), Ansprechpartner(in), Eheleute, Verhältnis1 - Verhältnis10) dürfen nicht verwendet werden.

Schlüssel in SAXSVS | Verhältnis in MAGELLAN
--------------------|-----------------------
20                  | Mutter
10                  | Vater
30                  | Vormund/Betreuer
50                  | Großmutter
40                  | Großvater
110                 | Pflegeeltern
60                  | Onkel
70                  | Tante
80                  | Bruder
90                  | Schwester
120                 | Erzieher
140                 | Notfall
150                 | Gasteltern
keine Entsprechung  | Eltern
keine Entsprechung  | Erziehungsberechtigte(r)
keine Entsprechung  | Sorgeberechtigte(r)
keine Entsprechung  | Ansprechpartner(in)
keine Entsprechung  | Eheleute
keine Entsprechung  | Verhältnis1 - Verhältnis10

Wenn Sie in der folgenden Auflistung **Person > ...** lesen, dann ist damit die entsprechende Ansicht `Schüler`, `Lehrer`, `Personen` oder `Sorgeberechtigte` gemeint, je nachdem welchen Personentyp Sie in MAGELLAN als Familienmitglied angegeben haben.

Wenn wir im folgenden die MAGELLAN Personenangaben zur Ansicht "Sorgeberechtigte" machen, dann kann damit auch Lehrer oder Personen gemeint sein.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<sorgeberechtigter id>` - OP
**Beschreibung** | `Schüler > Daten 1 > Familie > Position`<br/>Rangfolge der Sorgeberechtigten.
**Feld**         | `<sorgeberechtigter><as_berechtigt>` - OP
**Beschreibung** | `Schüler > Daten 1 > Familie > Sorgerecht`<br/>Gibt an, ob das Familienmitglied das Sorgerecht ausübt.
**Feld**         | `<sorgeberechtigter><as_beziehung>` - OP
**Beschreibung** | `Schüler > Daten 1 > Familie > Verhältnis`<br/>Gibt die Beziehung des Familienmitglieds zum Schüler an, z.B. Vater, Mutter etc.
**Feld**         | `<sorgeberechtigter><as_einrichtung>`
**Beschreibung** | Wird aktuell nicht unterstützt.
**Feld**         | `<sorgeberechtigter><as_anrede>` - OP
**Beschreibung** | `Sorgeberechtigte > Anrede`<br/>Anrede des Sorgeberechtigten.
**Feld**         | `<sorgeberechtigter><as_vname>` - OP
**Beschreibung** | `Sorgeberechtigte > Vorname`<br/>Vorname des Sorgeberechtigten.
**Feld**         | `<sorgeberechtigte><as_name>` - OP
**Beschreibung** | `Sorgeberechtigte > Nachname`<br/>Nachname des Sorgeberechtigten.
**Feld**         | `<sorgeberechtigter><as_staat>` - OP
**Beschreibung** | `Sorgeberechtigte > Land`<br/>Wohnland des Sorgeberechtigten. <br/>MAGELLAN setzt aus den folgenden Länderkürzeln die Schlüsselnummer für die Übergabe in die XML-Datei um.<br/><br/>Mögliche Einträge:<br/>D/De/Deu=Deutschland (000)<br/>PL=Polen (152)<br/>CZ=Tschechische Republik (164)<br/>AT=Österreich (151)<br/>CH=Schweiz (158)<br/><br/>Sollten Sie weitere Werte benötigen, wird um entsprechende Rückmeldung im Support gebeten.Sollten weitere Einträge erforderlich sein, wenden Sie sich bitte an den Support.
**Feld**         | `<sorgeberechtigter><as_land>`
**Beschreibung** | `Sorgeberechtigte > Gemeindekennziffer`<br/>Das Wohnbundesland des Sorgeberechtigten (wenn in Deutschland lebend wird aus der Gemeindekennziffer errechnet.
**Feld**         | `<sorgeberechtigter><as_plz>`
**Beschreibung** | `Sorgeberechtigte > PLZ`<br/>Postleitzahl des Sorgeberechtigten.
**Feld**         | `<sorgeberechtigter><as_ort>`
**Beschreibung** | `Sorgeberechtigte > Ort`<br/>Wohnort des Sorgeberechtigten.
**Feld**         | `<sorgeberechtigter><as_ortsteil>`
**Beschreibung** | `Sorgeberechtigte > Ortsteil`<br/>Ortsteil des Sorgeberechtigten.
**Feld**         | `<sorgeberechtigter><as_strasse>`
**Beschreibung** | `Sorgeberechtigte > Straße`<br/>Straße des Sorgeberechtigten.

### Schwächen  

`<saxsvs-bbs><schueler><schwaechen>`

Die Schwächen sind ein gesonderter Teil der Förderungen und werden für bestimmte Aspekte der Förderung/Teilleistungsschwächen der Schüler ausgegeben.

* Lese-Rechtschreib-Schwäche
* Autistisches Verhalten

Titel            | Inhalt
---------------- | ------
**Feld**         | `<schwaeche id>` - OP
**Beschreibung** | `Schüler > Daten 4 > Förderungen > Position`<br/>Rangfolge der Schwäche
**Feld**         |  `<af_schwaeche>` - OP
**Beschreibung** | `Schüler > Daten 4 > Förderungen > Förderschwerpunkt 2`<br/>Schwäche des Schülers
**Feld**         | `<af_schwaeche_dat>` - OP
**Beschreibung** | `Schüler > Daten 4 > Förderungen > Von`<br/>Schwäche seit Datum

### Förderung  

`<saxsvs-bbs><schueler><foerderung>`

Wird ausgegeben, wenn der Schüler eine Integrationsform eingetragen hat.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<af_int>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Maßnahme/Bedarf`<br/>Integrationsform des Schülers, z.B. 50 = Inkl.
**Feld**         | `<af_int_von>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Von`<br/>Anfangsdatum der Förderung.
**Feld**         | `<af_int_bis>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Bis`<br/>Enddatum der Förderung.
**Feld**         | `<af_int_rs_std>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Stunden 1`<br/>Die Förderstunden in der Regelschule, gemäß Bescheid des Schülers.
**Feld**         | `<af_int_fs_std>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Stunden 2`<br/>Die Förderstunden in der Förderschule, gemäß Bescheid des Schülers.
**Feld**         | `<af_int_foerdersw>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 4 > Förderungen > Förderschwerpunkt 1`<br/>Hauptförderschwerpunkt, z.B. 16 = geistige Entwicklung
**Feld**         | `<af_int_zlk>`
**Beschreibung** | `Nicht unterstützt`<br/>Freitext - Angabe einer zusätzlichen Lehrkraft.
**Feld**         | `<af_int_raum>`
**Beschreibung** | `Nicht unterstützt`<br/>Freitext - Raumbedingungen.

### Vorbildung ABS

`<saxsvs-bbs><schueler><abs>`

Wird ausgegeben, wenn beim Schüler der Höchste allgemeinbildende Abschluss angegeben ist.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<av_abs_schart>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Höchster Abschluss ABS > Schulform`<br/>Schulform der Schule, an dem der höchste Abschluss erworben wurde, z.B. 062 = Abendgymnasium.
**Feld**         | `<av_abs_zeugnis>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss`<br/>Höchster allgemeinbildender Abschluss, z.B. 06 = Allgemeine Hochschulreife.

### Vorbildung BBS  

`<saxsvs-bbs><schueler><bbs>`

Wird ausgegeben, wenn beim Schüler der Höchste berufsbildenden Abschluss angegeben ist.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<av_bbs_schart>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Höchster Abschluss BBS > Schulform`<br/>Schulform der Schule, an dem der höchste Abschluss erworben wurde, z.B. 115 = Berufsvorbereitungsjahr.
**Feld**         | `<av_bbs_zeugnis>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss`<br/>Höchster berufsbildender Abschluss, z.B. 00 = noch kein Abschluss an einer berufsbildenden Schule.

### Ende der Ausbildung  

`<saxsvs-bbs><schueler><aab_ende>`

Wird ausgegeben, wenn der Schüler die Schullaufbahn beendet. Dabei wird zwischen regulärem Abschluss oder Abbruch der Laufbahn unterschieden und jeweils nur ein Weg gefüllt.

#### Abschluss  

`<absch>`

Im Falle eines Abschlusses wird der Knoten `<absch>` gefüllt.

!!! danger "Achtung"

    Der Abschluss wird an dem Eintrag unter `Schüler > Laufbahn > Abschluss > Abschluss 1` erkannt, weitere Prüfungen werden dann ausgelöst. Wird für Ihren Schüler kein Abschluss erkannt, prüfen Sie bitte, ob in diese Feld ein korrekter Eintrag vorgenommen wurde.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<absch_art>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Abschluss > Abschluss 1`<br/>Beendigungsart bei Abschluss der Ausbildung, z.B. 030 = Abschlusszeugnis.
**Feld**         | `<absch_art_dat>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Abschluss > Abschluss 1 Datum`<br/>Abschlussdatum.
**Feld**         | `<absch_art_zusatz>`
**Beschreibung** | `MAGELLAN > Schüler > Laufbahn > Abschluss 1 > Abschlussart`<br/>Zusätzliche erworbener Schulabschluss, z.B. 030 = Fachhochschulreife.

#### Abbruch  

`<abbruch>`

Im Falle eines Abbruches wird der Knoten `<abbruch>` gefüllt.

!!! danger "Achtung"

    Wird kein Abschluss gefunden, der Schüler ist ausgeschult und eine Abgangsart ist eingetragen, wird der Knoten Abbruch gefüllt.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<abbruch>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Abgang > Abgangsart`<br/>Beendigungsart bei Abbruch der Ausbildung, z.B. 110 = Schulwechsel in Sachsen (an öffentliche Schule).
**Feld**         | `<abbruch_dat>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Abgang > Abgang am`<br/>Abbruchsdatum.
**Feld**         | `<bzsort_neu>`
**Beschreibung** | `MAGELLAN > Schüler > Daten 2 > Abgang > Übergang an Schule`<br/>`MAGELLAN > Schulen > Daten > Schulnummer`<br/>Bei Wechsel auf eine andere Schule, wird hier die vom Amt vergebene 7-stellige Dienststellennummer der neuen Schule erwartet. In MAGELLAN geben Sie die Schule an, an die der Schüler wechselt. In der Ansicht `Schulen` muss für die entsprechende Schule die Schulnummer eingetragen sein.

### Einstellungsbetrieb (MAGELLAN Ausbildungsbetrieb)  

`<saxsvs-bbs><schueler><aau_einbetr>`

Im Falle einer betrieblichen Ausbildung wird hier der Betrieb angegeben, bei dem der Vertrag abgeschlossen wird. In MAGELLAN ist dies der Ausbildungsbetrieb.
Wie beim Wohnort des Schülers wird die Adresse unterschieden in Adresse in Sachsen, restliches Deutschland und Ausland.

Titel                  | Inhalt
---------------------- | ------
**Ausbildungsbetrieb** | `MAGELLAN > Schüler > Ausbildung > Betrieb [Ausbildungsbetrieb]`
**Beschreibung**       | Wählen Sie bei der aktuellen Ausbildung den Betrieb aus, der als Einstellungsbetrieb gelten soll.<br/>Alle weiteren Informationen berufen sich auf den ausgewählten Betrieb.


!!! info "Hinweis"

    In SAXSVS wird jeweils der Eintrag des Einstellungsbetriebs (MAGELLAN-Ausbildungsbetrieb) UND der Ausbildungsbetriebs (MAGELLAN-Praxisbetrieb) erwartet. Ist einer der beiden Betriebe nicht erfasst, wird alternativ immer der jeweils andere Betrieb ausgegeben. Sie müssten also, wenn der Einstellungs- und der Ausbildungsbetrieb identisch sind, nur einen der beiden Betriebe erfassen.  

#### Adresse Sachsen

`<adresse_sachsen>`

Wird ausgegeben, wenn sich der Einstellungsbetrieb im Bundesland Sachsen befindet.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<bez>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Name 1`<br/>Name des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).
**Feld**         | `<plz>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > PLZ`<br/>Postleitzahl des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).
**Feld**         | `<ort>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Ort`<br/>Ort des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).
**Feld**         | `<str>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Straße`<br/>Straße des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).

### Adresse Deutschland  

`<adresse_deutschland>`

Wird ausgegeben, wenn sich der Einstellungsbetrieb (MAGELLAN Ausbildungsbetrieb) in Deutschland, aber nicht im Bundesland Sachsen befindet.

!!! danger "Achtung"

    Wenn die Gemeindekennziffer des Betriebes gefüllt ist, füllen wir automatisch das Feld Land mit `De`. Ist das Feld `Land` und das Feld 'Gemeinde' leer, wird in der Prüfung eine Fehlermeldung ausgegeben.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<bez>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Name 1`<br/>Name des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).
**Feld**         | `<land>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Gemeinde`<br/>Bundesland des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb). Wird anhand des Gemeindeschlüssels ermittelt.
**Feld**         | `<plz>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > PLZ`<br/>Postleitzahl des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).
**Feld**         | `<ort>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Ort`<br/>Ort des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).
**Feld**         | `<str>`
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Straße`<br/>Straße des Einstellungsbetriebes (MAGELLAN Ausbildungsbetrieb).

### Adresse Ausland  

`<adresse_ausland>`

Wird ausgegeben, wenn sich der Einstellungsbetrieb (MAGELLAN Ausbildungsbetrieb) im Ausland befindet.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<bez>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Name 1`<br/>Name des Einstellungsbetriebes.
**Feld**         | `<an_staat>` - OP
**Beschreibung** | `MAGELLAN > Schüler > Daten 1 > Land`<br/>Länderkürzel des Landes, z.B. PL = Polen.<br /> Der auszugebende Wert wird berechnet. Aktuell berechnen wir nur Polen, sollten Sie weitere Werte benötigen, wird um entsprechende Rückmeldung im Support gebeten.
**Feld**         | `<plz>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > PLZ`<br/>Postleitzahl des Einstellungsbetriebes.
**Feld**         | `<ort>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Ort`<br/>Ort des Einstellungsbetriebes.
**Feld**         | `<str>`
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Straße`<br/>Straße des Einstellungsbetriebes.

## Ausbildungsbetrieb (MAGELLAN Praxisbetrieb)  

`<saxsvs-bbs><schueler><aau_ausbetr>`

Im Falle einer betrieblichen Ausbildung wird hier der Betrieb angegeben, bei dem der Schüler ausgebildet wird. Dies ist überwiegend gleich dem Einstellungsbetrieb, aber in einigen Fällen, kann dies abweichen. In MAGELLAN ist dies der Praxisbetrieb.
Wie beim Wohnort des Schülers wird die Adresse unterschieden in Adresse in Sachsen, restliches Deutschland und Ausland.

Titel             | Inhalt
----------------- | ------
**Praxisbetrieb** | `MAGELLAN > Schüler > Ausbildung > Praxisbetrieb`
**Beschreibung**  | Wählen Sie bei der aktuellen Ausbildung den Betrieb aus, der als Praxisbetrieb gelten soll.<br/>Alle weiteren Informationen berufen sich auf den ausgewählten Betrieb.

!!! info "Hinweis"

    In SAXSVS wird jeweils der Eintrag des Einstellungsbetriebs (MAGELLAN-Ausbildungsbetrieb) UND der Ausbildungsbetriebs (MAGELLAN-Praxisbetrieb) erwartet. Ist einer der beiden Betriebe nicht erfasst, wird alternativ immer der jeweils andere Betrieb ausgegeben. Sie müssten also, wenn der Einstellungs- und der Ausbildungsbetrieb identisch sind, nur einen der beiden Betriebe erfassen.  

### Adresse Sachsen

`<adresse_sachsen>`

Wird ausgegeben, wenn sich der Ausbildungsbetrieb im Bundesland Sachsen befindet.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<bez>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Name 1`<br/>Name des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<plz>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > PLZ`<br/>Postleitzahl des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<ort>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Ort`<br/>Ort des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<str>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Straße`<br/>Straße des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).

### Adresse Deutschland

`<adresse_deutschland>`

Wird ausgegeben, wenn sich der Ausbildungsbetrieb (MAGELLAN Praxisbetrieb) in Deutschland, aber nicht im Bundesland Sachsen befindet.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<bez>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Name 1`<br/>Name des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<land>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Gemeinde`<br/>Bundesland des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb). Wird anhand des Gemeindeschlüssels ermittelt.
**Feld**         | `<plz>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > PLZ`<br/>Postleitzahl des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<ort>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Ort`<br/>Ort des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<str>`
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Straße`<br/>Straße des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).

### Adresse Ausland

`<adresse_ausland>`

Wird ausgegeben, wenn sich der Ausbildungsbetrieb (MAGELLAN Praxisbetrieb) im Ausland befindet.

Titel            | Inhalt
---------------- | ------
**Feld**         | `<bez>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Name 1`<br/>Name des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<an_staat>` - OP
**Beschreibung** || `MAGELLAN > Schüler > Daten 1 > Land`<br/>Länderkürzel des Landes, z.B. PL = Polen.<br /> Der auszugebende Wert wird berechnet. Aktuell berechnen wir nur Polen, sollten Sie weitere Werte benötigen, wird um entsprechende Rückmeldung im Support gebeten.
**Feld**         | `<plz>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > PLZ`<br/>Postleitzahl des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<ort>` - OP
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Ort`<br/>Ort des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
**Feld**         | `<str>`
**Beschreibung** | `MAGELLAN > Betriebe > Daten 1 > Straße`<br/>Straße des Ausbildungsbetriebes (MAGELLAN Praxisbetrieb).
