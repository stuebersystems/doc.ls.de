# Schüler- und Klassendaten der SIM.TXT

[Beachten Sie bitte die Mindesteingaben für die Statistik!](https://doc.ls.stueber.de/nordrhein-westfalen/abs-bbs/#voraussetzungen-für-alle-statistikdaten)

## Daten in der SIM-Datei

1. Die Ausgabe von Schülerdaten in die Statistikdatei kann gesteuert werden. Das heisst, damit Schüler überhaupt ausgespielt werden können, müssen gewisse Eingaben in MAGELLAN getätigt worden sein. Andererseits können Sie mit diesen Eingaben auch explizit Schüler aus der Statistik ausschließen, sei es auf natürlichem Wege, z.B. da Gastschüler nicht statistisch erfasst werden dürfen, oder aus anderen Gründen, ein bestimmter Schülerdatensatz nicht exportiert werden soll.

2. In der Datei werden die zu exportierenden Schülerdaten in typisierte Datensätze eingeteilt. Damit ein Schüler einem Typus entspricht müssen auch hier bestimmte Eingaben in MAGELLAN getätigt sein, bzw. ergeben sich aufgrund der Laufbahn des Schülers. Schülerdatensätze können auch mehrfach in der Statistikdatei auftauchen, da sie ggf. mehreren Typen entsprechen.

### Allgemeine Voraussetzungen zum Export

Allgemeine Angaben zum Export von Daten in die Statistikdatei.

MAGELLAN                                          | Beschreibung
------------------------------------------------- | -------------
`Klassen > Daten 1 > Statistikkürzel`             | Damit Schüler einer Klasse zur Statistik berücksichtigt werden, muss die Klasse ein Statistikkürzel eingetragen haben. Ist dieses Feld leer, wird die komplette Klasse ignoriert.
`Schüler > Statistik > Merkmal S10`               | Wählen Sie im Schülermerkmal S10 ***Kein Export nach ASDPC*** aus, um Schüler explizit aus der Statistik zu nehmen.
`Schüler > Daten 3 > Verschiedenes > Gastschüler` | Haken Sie einen Schüler als Gastschüler an, wird dieser nicht in die Statistikdatei exportiert.

### Einteilung eines Datensatzes in den entsprechenden Schülertyp

Die Einteilung eines Schülers in einen der vorgegebenen Typen erfolgt aufgrund der Laufbahn und gegebenen Datenmenge in MAGELLAN und in der folgenden Reihenfolge:

#### Abgänger

- Schüler werden aus allen drei Schulhalbjahren ausgelesen
- Der Schüler ist in MAGELLAN auf `Ausgeschult` gesetzt oder
- Der Schüler ist in MAGELLAN auf `Eingeschult` gesetzt und
    - `Schüler > Daten 2 > Abgang > Abgangsart` oder
    - `Schüler > Laufbahn > Abschluss > Abschluss 1`  ist auf den Wert ***0A*** gesetzt.

#### Bildungsgang abgeschlossen

- Schüler werden aus allen drei Schulhalbjahren ausgelesen
- Der Schüler ist in MAGELLAN auf `Eingeschult` gesetzt
- `Schüler > Laufbahn > Abschluss > Abschluss 1`  ist gefüllt und darf nicht auf den Wert ***0A*** gesetzt sein.

#### Aktuell eingeschult, Neuzugang, Neuzugang an gleicher Schule

- Schüler werden nur aus dem aktuellen Schulhalbjahr ausgelesen
- Der Schüler ist in MAGELLAN auf `Eingeschult` gesetzt

Nach dem Auslesen der Daten wird der Typus auf **Neuzugang** gesetzt und dann weitere Bedingungen geprüft:

#### Aktuell eingeschult

- Schüler ist Stammschüler und
- Schüler war bereits im letzten Schuljahr an der Schule (es wird die Laufbahn geprüft) und
- Die Gliederung hat sich zum aktuellen Schulhalbjahr nicht verändert

#### Neuzugang an gleicher Schule

- Schüler ist ein Nebenschüler oder
- Schüler ist Stammschüler und
    - war bereits im letzten Schuljahr an der Schule (es wird die Laufbahn geprüft) und
    - die Gliederung sich zum aktuellen Schulhalbjahr verändert

## Dateneingabe

***Erläuterung:*** In der nachfolgenden Tabelle finden Sie alle Statistikfelder der SIM.TXT. Entsprechend der Schnittstellenbeschreibung, Ihrer Rückmeldungen und Erfahrungen der letzten Jahre werden nicht alle Felder immer gefüllt. Ob ein Feld gefüllt wird, hängt vom erkannten Schülertyp und der Haupt-Schulform Ihrer Schule ab. Es gibt Felder die lediglich für Berufskollegs oder z.B. nur für Gymnasien zu füllen sind und wiederum andere, die nur gefüllt werden, wenn es ich um den Schülertyp "Neuzugang" oder "Neuzugang an gleicher Schule" handelt.

Die Zeilen- Spaltenkombination **SF / ST** in der Tabelle steht für "Schulform / Schülertyp" und gibt entsprechend Auskunft für das jeweilige Statistikfeld.

Art               | Inhalt
----------------- |-------
**Statistikfeld** | **Bezugsjahr**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Statistikmodul > Erhebungsjahr
Beschreibung      | Geben Sie im Statistikmodul bei der Ausführung der Statistik das Ergebungsdatum ein. Das Datum wird auch dazu<br/>benötigt um das Erhebungsjahr auszulesen.
**Statistikfeld** | **Status - Schülerstatus**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 [Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang [Abgangsarten]
Beschreibung      | Der Schülerstatus ergibt sich anhand des Schülertyps un dem angegebenen Abschluss bzw. Abgang des Schülers.<br/>Neuzugang, Neuzugang an gleicher Sxhule, Eingeschult = 2 (Aktiv)<br/>Bildungsgang abgeschlossen = 8 (Abschluss)<br/>Abgänger = 8 (Abgang mit Abschluss) oder wenn kein Abschluss bzw. Abschluss oder Abgang = 0A sind = 9 (Abgang ohne Abschluss)
**Statistikfeld** | **LfdNr**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Wird beim Export berechnet.
Beschreibung      | Laufende Nummer pro Schüler. die beim Export erzeugt und hochgezählt wird.<br/>***Achtung***: Es handelt sich hierbei nicht um die Schüler.ID aus MAGELLAN.
**Statistikfeld** | **Klasse**
Datenfeld         | MAGELLAN: Klassen > Daten > Statistikkürzel
SF / ST           | Alle
Beschreibung      | Bitte wiederholen Sie hier das Klassenkürzel, um die Klasse und dessen Schüler für die Statistik zu berücksichtigen. Das Statistikkürzel darf nicht mehr als 6 Zeichen betragen.<br/>***Achtung***: Über das Statistikkürzel steuern Sie auch, ob eine Klasse für den Export berücksichtigt wird. Kein Statistikkürzel = Kein Export!
**Statistikfeld** | **Gliederung**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildgungsgang [Bildgungsgänge] und [Berufsfelder] (Aktuelle Ausbildung)<br/>Schüler > Daten 3 > Verschiedenes > G8/G9
Beschreibung      | ***ABS***: Gymnasien geben hier im Feld "G8/G9" an, ob es sich um ein G8 oder G9 Bildungsgang handelt. Kein Wert bedeutet = G01 (Aufbaugymnasium).<br/><br/>***BBS***: Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in MAGELLAN<br/>ausgelesen. Lesen Sie dazu die Beschreibung des nächsten Feldes `Fachklasse`.<br/>Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein.<br/>In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor<br/>Klasse geprüft.
**Statistikfeld** | **Fachklasse**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildgungsgang[Bildungsgänge]<br/>Schüler > Ausbildung > Von<br/>Schüler > Ausbildung > Bis
Beschreibung      | Nur für BBS!<br/>
**Statistikfeld** | **Klassenart**
Datenfeld         | Klassen > Merkmale > MerkmalS3 [Verzeichnisse > Merkmale > Klassen]
Beschreibung      | Nur für ABS<br/>Bitte erfassen Sie hier pro Klasse die Klassenart. Das Feld wird durch den Import der Schlüsseldatei<br/>`AS_Klassenmerkmale.keys` befüllt.
**Statistikfeld** | **OrgForm**
Datenfeld         | MAGELLAN:Klassen > Daten > Organisation [Organisationen]
Beschreibung      | Wählen Sie die Organisationsform der Klasse aus.
**Statistikfeld** | **AktJahrgang**
Datenfeld         | MAGELLAN: Klassen > Zeiträume > Klassenstufe[Klassenstufen]
Beschreibung      | Wählen Sie die Klassenstufe der Klasse aus.
**Statistikfeld** | **Foerderschwerp**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Schwerpunkt1 und Schwerpunkt2[Förderungen]
Beschreibung      | Wählen Sie den Förderschwerpunkt der Klasse aus, bei abweichenden Förderschwerpunkten für einzelne Schüler<br/>wählen Sie zusätzlich den Förderschwerpunkt beim Schüler aus. Es wird Schüler vor Klasse geprüft.
**Statistikfeld** | **Schwerstbeh**
Datenfeld         | MAGELLAN:Schüler > Daten 4 > Förderbedarf[Förderbedarf]
Beschreibung      | Wählen Sie hier das Merkmal Schwerstbehinderung beim Schüler aus.
**Statistikfeld** | **Reformpdg**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **JVA**
Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal S2 [Merkmale]
Beschreibung      | Wählen Sie aus, ob es sich bei der Klasse um eine JVA-Klasse handelt.
**Statistikfeld** | **PLZ**
Datenfeld         | MAGELLAN:Schüler > Daten 1 > PLZ[Postleitzahlen]
Beschreibung      | Wenn Sie hier die PLZ eintragen, wird diese ausgespielt. Das Feld ist wird z.Zt. nicht benötigt.
**Statistikfeld** | **Wohnort**
Datenfeld         | MAGELLAN:<br/>Schüler > Daten 1 > Land<br/>Schüler > Daten 1 > Ort<br/>
Beschreibung      | Über das Land und den Ort steuern Sie die Ausgabe des Wohnortes. Folgende Kombinationen sind möglich:<br/>Land = LEER und Ort = LEER: Keine Ausgabe<br/>Land = **D** und Ort &lt; LEER: Ausgabe = siehe Liste unten<br/>Land = LEER und Ort = LEER: Ausgabe = siehe Liste unten<br/>Land = **B**: Ausgabe = `Belgien`<br/>Land = **L**: Ausgabe = `Luxemburg`<br/> Land =  **NL**: Ausgabe = `Niederlande`<br/>Land = Sonstige Einträge: Ausgabe = `Übriges Ausland`<br/>Gemeinde = LEER: Ausgabe = Ort<br/>Gemeinde in NRW: Ausgabe = Ort<br/>Gemeinde <> NRW: Ausgabe = Bundesland, z.B. `Rheinland Pfalz`<br/>
**Statistikfeld** | **Gebdat**
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geburtsdatum
Beschreibung      | Geben Sie das Geburtsdatum des Schülers ein.
**Statistikfeld** | **Geschlecht**
Datenfeld         | MAGELLAN: Klassen > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie das Geschlecht des Schülers aus.
**Statistikfeld** | **Staatsang**
Datenfeld         | MAGELLAN:Schüler > Daten 2 > Staatsangeh. 1[Staatsangehörigkeiten]
Beschreibung      | Wählen Sie die Staatsangehörigkeit des Schülers aus.
**Statistikfeld** | **Aussiedler**
Datenfeld         | MAGELLAN:Schüler > Daten 2 > Aussiedler
Beschreibung      | Setzen Sie entsprechend den Haken, um den Schüler als Aussiedler zu markieren.
**Statistikfeld** | **Religion**
Datenfeld         | MAGELLAN:Schüler > Daten 1 > Konfession[Konfessionen]
Beschreibung      | Wählen Sie die Konfession des Schülers aus.
**Statistikfeld** | **Relianmeldung**
Datenfeld         | MAGELLAN:Schüler > Daten 1 > Rel.-Abmeldung bis
Beschreibung      | Die Anmeldung zum Religionsunterricht ergibt sich anhand des Bis-Datums der Abmeldung vom Religionsunterricht. Eine<br/>Anmeldung ist nur erforderlich, wenn es zuvor eine Abmeldung gegeben hat.
**Statistikfeld** | **Reliabmeldung**
Datenfeld         | MAGELLAN:Schüler > Daten 1 > Rel.-Abmeldung Von
Beschreibung      | Geben Sie im Vom-Feld die Abmeldung vom Religionsunterricht an.
**Statistikfeld** | **Aufnahmedatum**
Datenfeld         | MAGELLAN:Schüler > Zugang/Abgang > ZugangAm
Beschreibung      | Geben Sie das Zugangsdatum des Schülers an der Schule an. Dieses Datum ist u.a. wichtig zur Feststellung von<br/>Neuzugängen an der Schule.
**Statistikfeld** | **Labk**
Datenfeld         | MAGELLAN:<br/>Lehrer > Daten 1 > Kürzel<br/>Klassen > Zeiträume > Klassenleiter 1
Beschreibung      | Tragen Sie für jeden Lehrer der Schule das 4-Stellige Lehrerkürzel (identisch zur LID 123) ein.<br/>Geben Sie für jede Klasse der Statistik den Klassenlehrer an.
**Statistikfeld** | **Ausbildort**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst, da es z.zt. nicht von der ASDPC-Schnittstelle statistisch ausgewertet wird<br/>Quelle: [Schnittstellenbeschreibung ASDPC](https://schulverwaltungsprogramme.msb.nrw.de/zbwschul.pdf)
**Statistikfeld** | **Betriebsort**
Datenfeld         | Der Betriebsort ist nicht 1:1 die Ausgabe des Eintrages im Feld `Ort` des Betriebes. Es wird unterschieden zwischen der Schulform, den Ländern Belgien, den Niederlanden, Luxemburg oder dem weiteren Ausland. Innerhalb von Deutschland wird differenziert zwischen NRW und weiteren Bundesländern. Daher müssen zum Auswerten die nachfolgenden Felder korrekt gefüllt sein.<br/> MAGELLAN:<br/>[Mandant > Daten2 > Schulformen (BK oder SB, jeweils als erstes in der Liste der Mandantenschulformen)](https://doc.ls.stueber.de/nordrhein-westfalen/abs-bbs/#voraussetzungen-für-alle-statistikdaten)<br/>Betriebe > Daten 1 > Ort<br/>Betriebe > Daten 1 > Land (D,L,B,NL oder abweichende Länderkürzel)<br/>Betriebe > Daten 1 > Gemeinde (nur fürs Inland zu füllen)<br/>Schüler > Ausbildung > Ausbildungsbetrieb <br/>[eine aktuelle Ausbildung wird anhand der Von-Bis-Daten der Ausbildung und dem Zeitraum-Von-Bis-Daten identifiziert]
Beschreibung      | Nur für BBS:<br/>Tragen Sie zu jedem Betrieb die vollständige Adresse ein.<br/>Wählen Sie für den Schüler einen Ausbildungsbetrieb aus.
**Statistikfeld** | **LSSchulform**
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schule<br/>Zugang/Abgang > Bereits besuchte Schulen > Schulform[Schulformen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie unter `Bereits besuchte Schulen` die Schule aus.<br/>Wählen Sie unter `Bereits besuchte Schulen` die Schule und die Schulform aus.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler ein.<br/>Achtung: Die folgenden Werte beziehen sich auf die zuletzt besuchte Schule, bevor der Schüler an Ihre Schule<br/>gewechselt ist.<br/>Diese werden nur benötigt, wenn der Schüler zum Schuljahreswechsel erstmalig an Ihrer Schule ist oder an Ihrer<br/>Schule einen neuen Bildungsgang (verglichen wird der aktuelle Bildungsgang mit dem Vorjahresbildungsgang) belegt.
**Statistikfeld** | **LSSchulnummer**
Datenfeld         | MAGELLAN:<br/>Schulen > Daten > Schulnummer<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schule<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Tragen Sie bei den Schulen die Herkunftsschulen der Schüler mit deren Schulnummer ein.<br/>Wählen Sie unter Bereits besuchte Schulen die Schule aus.<br/>ählen Sie unter Herkunftsschule die eingetragene Schule aus.
**Statistikfeld** | **LSGliederung**
Datenfeld         | MAGELLAN:Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang[Bildungsgänge] und [Berufsfelder]
Beschreibung      | Die mitgebrachte Schulgliederung tragen Sie über die dazugehörige Fachklasse über den Höchsten berufsbildenden<br/>Bildungsgang ein. Es wird das MAGELLAN-Feld „Berufsfeld“ aus dem Bildungsgang ausgelesen.<br/><br/>**Hinweis:** LSGliederung wird nur benötigt, wenn der neue Schüler zuletzt einen berufsbildenden Bildungsgang an<br/>einem Berufskolleg besucht hat, bei Schülern, die von allgemeinbildenden Schulen kommen, bleibt das Feld leer.
**Statistikfeld** | **LSFachklasse**
Datenfeld         | MAGELLAN:Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang [Bildungsgänge]
Beschreibung      | Nur für BBS:<br/>Die mitgebrachte Fachklasse tragen Sie über den Höchsten berufsbildenden Bildungsgang ein. **Hinweis:**<br/>LSFachklasse wird nur benötigt, wenn der neue Schüler zuletzt einen berufsbildenden Bildungsgang an einem Berufskolleg<br/>besucht hat, bei Schülern, die von allgemeinbildenden Schulen kommen, bleibt das Feld leer.
**Statistikfeld** | **LSKlassenart**
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > Bereits besuchte Schule > Herkunftsart [Herkunftsarten]
Beschreibung      | Nur für ABS:<br/>Tragen Sie die Art der Klasse an der letzten Schule, z.B. Regelklasse ein. Das hinerlegte Verzeichnis wird befüllt<br/>durch den Import des Katalogs `AS_Herkunftsarten`.
**Statistikfeld** | **LSReformpdg**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **LSSchulentl**
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulbesuch bis<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie unter Bereits besuchte Schulen die Schule aus und geben den Schulbesuch bis an.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler ein.
**Statistikfeld** | **LSJahrgang**
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Letzte Klassenstufe [Klassenstufen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie unter Bereits besuchte Schulen die Schule und die Letzte Klassenstufe aus.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler ein.
**Statistikfeld** | **LSQual**
Datenfeld         | MAGELLAN:Schüler > Zugang/Abgang > Bereits besuchte Schulen > Abschluss[Abschlüsse (Extern)]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie unter Bereits besuchte Schulen die Schule und den Abschluss aus.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler ein.
**Statistikfeld** | **LSVersetz**
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen[Herkunftsunterlagen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie unter Bereits besuchte Schulen die Schule und bei Unterlagen die Versetzungsart aus.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler ein.
**Statistikfeld** | **VOklasse**
Datenfeld         | MAGELLAN:Klassen > Daten > Statistikkürzel
Beschreibung      | Achten Sie bitte darauf, dass für alle aktuellen und auch die Vorjahresklassen ein Statistikkürzel unter `Klassen > Daten > Statistikkürzel` erfasst wurde.
**Statistikfeld** | **VOgliederung**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildungsgang<br/>[Bildgungsgänge] und [Berufsfelder]
Beschreibung      | Nur BBS:<br/>Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld Gliederung den Bildungsgang ein.
**Statistikfeld** | VOfachklasse
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildgungsgang<br/>[Bildungsgänge]
Beschreibung      | Nur BBS:<br/>Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld Fachklasse den Bildungsgang ein.
**Statistikfeld** | **VOOrgForm**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Organisation [Organisationen]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld OrgForm die Organisation der Klasse<br/>ein.
**Statistikfeld** | **VOKlassenart**
Datenfeld         | MAGELLAN:<br/>Klassen > Merkmale > MerkmalS3<br/>[Verzeichnisse > Merkmale > Klassen]
Beschreibung      | <br/>**Nur für ABS:**<br/>Es wird die Klassenart der im Vorjahr besuchten Klasse ausgegeben. Bitte erfassen Sie pro Klasse die Klassenart.<br/>Das Feld wird durch den Import der Schlüsseldatei `AS_Klassenmerkmale.keys` befüllt.
**Statistikfeld** | **VOJahrgang**
Datenfeld         | MAGELLAN:Klassen > Zeiträume > Klassenstufe [Klassenstufen]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld AktJahrgang die Klassenstufe der Klasse<br/>ein.
**Statistikfeld** | **VOfoerderschwerp**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1[Förderschwerpunkte]<br/>Schueler > Daten 4 > Schwerpunkt1[Förderschwerpunkte]
Beschreibung      | Wählen Sie den Förderschwerpunkt der Klasse aus, bei abweichenden Förderschwerpunkten für einzelne Schüler<br/>wählen Sie zusätzlich den Förderschwerpunkt beim Schüler aus. Es wird Schüler vor Klasse geprüft.
**Statistikfeld** | **VOschwerstbeh**
Datenfeld         | MAGELLAN:Schüler > Daten 4 > Förderbedarf[Förderbedarf]
Beschreibung      | Wählen Sie hier das Merkmal Schwerstbehinderung beim Schüler aus.
**Statistikfeld** | VOReformpdg
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **Entldatum**
Datenfeld         | MAGELLAN:Schüler > Zugang/Abgang > Abgang am
Beschreibung      | Geben Sie das Abgangsdatum des Schülers ein, wenn es sich um einen Abgänger handelt.
**Statistikfeld** | **Zeugnis**
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1[Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang
Beschreibung      | Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können<br/>Sie die Werte unter Abschlüsse oder Abgang erfassen. Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht<br/>eingetragen ist, wird der Abgang für die Statistik erfasst.
**Statistikfeld** | **Schulpflichterf**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **Schulwechselform**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **Versetzung**
Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > Versetzungsart[Versetzungsarten]
Beschreibung      | Wählen Sie die Art der Versetzung des Schülers aus.
**Statistikfeld** | JahrZuzug
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „zugezogen“ ausgewertet wird.
**Statistikfeld** | **JahrEinschulung**
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „zugezogen“ ausgewertet wird.
**Statistikfeld** | **JahrWechselSekI**
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „zugezogen“ ausgewertet wird.
**Statistikfeld** | **zugezogen**
Datenfeld         | MAGELLAN:<br/>Schüler > Daten 1 > Geburtsland [Staatsangehörigkeiten]<br/>Schüler > Daten 2 > In Deutschland seit
Beschreibung      | Der Schüler gilt als zugezogen, wenn das Feld „Geburtsland“ nicht leer, den Wert 0, oder 000 für Deutschland<br/>eingetragen hat; oder das Feld „In Deutschland seit“ ein Zuzugsdatum nach Deutschland enthält.
**Statistikfeld** | **GeburtslandMutter**
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „Elternteilzugezogen“ ausgewertet wird.
**Statistikfeld** | **GeburtslandVater**
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „Elternteilzugezogen“ ausgewertet wird.
**Statistikfeld** | **Elternteilzugezogen**
Datenfeld         | MAGELLAN:Schüler > Daten 2 > NdH
Beschreibung      | Markieren Sie das Feld „NdH“, wenn mindestens ein Elternteil nach Deutschland zugezogen ist.
**Statistikfeld** | **Verkehrssprache**
Datenfeld         | MAGELLAN:Schüler > Daten 2 > Verkehrssprache
Beschreibung      | Geben Sie hier einen Wert ein, wenn in der Familie überwiegend nicht Deutsch gesprochen wird. Anderenfalls können<br/>Sie das Feld leer lassen.<br/>Für die aktuelle Erhebung ist es ausreichend, einen Wert verschieden zu 000 zu verwenden, um darzustellen, das die<br/>Verkehrssprache in der Familie nicht Deutsch ist.
**Statistikfeld** | **Einschulungsart**
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S1 [Merkmale]
Beschreibung      | Wählen Sie hier die Einschulungsart des Schülers aus.
**Statistikfeld** | **Grundschulempfehlung**
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Zugang > Empfehlung [Empfehlungen (Bewerbung)]
Beschreibung      | <br/>**Nur für ABS**<br/>Geben Sie hier die Empfehlung der Primarschulen an.
**Statistikfeld** | Massnahmentraeger
Datenfeld         | MAGELLAN:Schüler > Statistik > Merkmal S2[Merkmale]
Beschreibung      | Wählen Sie aus, ob der Schüler von einem Ausbildungsbetrieb oder einem Träger ausgebildet wird.
**Statistikfeld** | **Betreuung**
Datenfeld         | MAGELLAN: Schüler > Extras > Betreuungsarten > Innerschulisch 1 [Betreuungen innerschulisch<br/>(Schüler)]
Beschreibung      | Wählen Sie die Betreuungsmaßnahme der Nachmittags/Ganztagsbetreuung aus.
**Statistikfeld** | **BKAZVO**
Datenfeld         | MAGELLAN:Schüler > Statistik > Merkmal T1
Beschreibung      | Geben Sie die Anzahl der anzurechnenden Monate bei verkürzter Ausbildung an. Möglich sind 0, 6,12 oder 18<br/>Monate.
**Statistikfeld** | **Foerderschwerp2**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt2[Förderschwerpunkte]<br/>Schüler > Daten 4 > Schwerpunkt2 [Förderschwerpunkte]
Beschreibung      | Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum<br/>Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse<br/>geprüft.
**Statistikfeld** | **VOfoerderschwerp2**
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt2[Förderschwerpunkte]<br/>Schüler > Daten 4 > Schwerpunkt2[Förderschwerpunkte]
Beschreibung      | Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum<br/>Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse<br/>geprüft.
**Statistikfeld** | **Berufsabschluss**
Datenfeld         | MAGELLAN:Schüler > Statistik > Merkmal S1[Merkmale]
Beschreibung      | Wählen Sie aus, ob bereits eine abgeschlossene Berufsausbildung vorliegt.
**Statistikfeld** | **Produktname**
Datenfeld         | -
Beschreibung      | Wir geben hier fest den Wert „MAGELLAN 6“ aus
**Statistikfeld** | **Produktversion**
Datenfeld         | -
Beschreibung      | Wir geben hier die aktuell installierte MAGELLAN 6 Version (Registry Wert) aus.
**Statistikfeld** | **Adressenmerkmal**
Datenfeld         | -
Beschreibung      | Die Adressenmerkmale für weitere Standorte erfassen Sie bitte direkt in ASDPC.
**Statistikfeld** | **Internat**
Datenfeld         | MAGELLAN:Schüler > Daten 4 > Betreuung > Einrichtung
Beschreibung      | Wenn der Schüler einen Internatsplatz besetzt, wählen Sie bitte Internat aus der Auswahlliste aus.
