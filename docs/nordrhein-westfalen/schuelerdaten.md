# Schüler- und Klassendaten der SIM.TXTMAGELLAN

[Beachten Sie bitte die Mindesteingaben für die Schnittstelle!](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/#voraussetzungen-fur-alle-statistikdaten)

## Daten in der SIM-Datei

1. Die Ausgabe von Schülerdaten in die SIM.TXT kann gesteuert werden. Das heisst, damit Schüler überhaupt ausgespielt werden können, müssen gewisse Eingaben in MAGELLAN getätigt worden sein. Andererseits können Sie mit diesen Eingaben auch explizit Schüler aus der Datei ausschließen, sei es auf natürlichem Wege, z.B. da Gastschüler nicht statistisch erfasst werden dürfen, oder aus anderen Gründen, ein bestimmter Schülerdatensatz nicht exportiert werden soll.

2. In der Datei werden die zu exportierenden Schülerdaten in typisierte Datensätze eingeteilt. Damit ein Schüler einem Typus entspricht müssen auch hier bestimmte Eingaben in MAGELLAN getätigt sein, bzw. ergeben sich aufgrund der Laufbahn des Schülers. Schülerdatensätze können auch mehrfach in der Exportschnittstelle auftauchen, da sie ggf. mehreren Typen entsprechen.

### Allgemeine Voraussetzungen zum Export

Allgemeine Angaben zum Export von Daten in die SIM.TXT.

MAGELLAN                                          | Beschreibung
------------------------------------------------- | -------------
`Klassen > Daten 1 > Statistikkürzel`             | Damit Schüler einer Klasse zum Export berücksichtigt werden, muss die Klasse ein Statistikkürzel eingetragen haben. Ist dieses Feld leer, wird die komplette Klasse ignoriert.
`Schüler > Statistik > Merkmal S10`               | Wählen Sie im Schülermerkmal S10 ***Kein Export nach ASDPC*** aus, um Schüler explizit aus vom Export auszuschließen.
`Schüler > Daten 3 > Verschiedenes > Gastschüler` | Haken Sie einen Schüler als Gastschüler an, wird dieser nicht in die Datei exportiert.

### Einteilung eines Datensatzes in den entsprechenden Schülertyp

Die Einteilung eines Schülers in einen der vorgegebenen Typen erfolgt aufgrund der Laufbahn und gegebenen Datenmenge in MAGELLAN und in der folgenden Reihenfolge:

#### Abgänger (ABG)

- Schüler werden aus allen drei Schulhalbjahren ausgelesen
- Der Schüler ist in MAGELLAN auf `Ausgeschult` gesetzt oder
- Der Schüler ist in MAGELLAN auf `Eingeschult` gesetzt und
  - `Schüler > Daten 2 > Abgang > Abgangsart` oder
  - `Schüler > Laufbahn > Abschluss > Abschluss 1`  ist auf den Wert ***0A*** gesetzt.

#### Bildungsgang abgeschlossen (BAG)

!!! warning "Sehr wichtig!"

    Diese Datensätze werden für die SIM.TXT nicht mehr ausgelesen. 

- Schüler werden aus allen drei Schulhalbjahren ausgelesen
- Der Schüler ist in MAGELLAN auf `Eingeschult` gesetzt
- `Schüler > Laufbahn > Abschluss > Abschluss 1`  ist gefüllt und darf nicht auf den Wert ***0A*** gesetzt sein.

#### Aktuell eingeschult (AKT), Neuzugang (NZG), Neuzugang an gleicher Schule (NGS)

- Schüler werden nur aus dem aktuellen Schulhalbjahr ausgelesen
- Der Schüler ist in MAGELLAN auf `Eingeschult` gesetzt

Nach dem Auslesen der Daten wird der Typus auf **Neuzugang** gesetzt und dann weitere Bedingungen geprüft:

#### Aktuell eingeschult (AKT)

- Schüler ist Stammschüler und
- Schüler war bereits im letzten Schuljahr an der Schule (es wird die Laufbahn geprüft) und
- Die Gliederung hat sich zum aktuellen Schulhalbjahr nicht verändert

#### Neuzugang an gleicher Schule (NZG)

- Schüler ist ein Nebenschüler oder
- Schüler ist Stammschüler und
  - war bereits im letzten Schuljahr an der Schule (es wird die Laufbahn geprüft) und
  - die Gliederung sich zum aktuellen Schulhalbjahr verändert

##### "Versetzung" für "Neuzugänger an gleicher Schule"

An Berufsschulen wird in der Regel anders als an Allgemeinbildenden Schulen nicht zwischen den Jahrgangsstufen (1. Ausbildungsjahr, 2. Ausbildungsjahr usw.) versetzt, sondern es wird fortgeschrieben. Aus diesem Grund setzen wir den Wert `Versetzung` künstlich auf den Wert `0` (=versetzt). Eine Ausnahme bildet die Situation, dass der Schüler "Neuzugänger an gleicher Schule" (siehe Status-Berechung im vorstehenden Abschnitt) ist, in diesem Fall wird der Wert für `Versetzt` nicht gesetzt. 

## Dateneingabe

***Erläuterung:*** In der nachfolgenden Tabelle finden Sie alle Schnittstellenfeder der SIM.TXT. Entsprechend der Schnittstellenbeschreibung, Ihrer Rückmeldungen und Erfahrungen der letzten Jahre werden nicht alle Felder immer gefüllt. Ob ein Feld gefüllt wird, hängt vom erkannten Schülertyp und der Haupt-Schulform Ihrer Schule ab. Es gibt Felder die lediglich für Berufskollegs oder z.B. nur für Gymnasien zu füllen sind und wiederum andere, die nur gefüllt werden, wenn es ich um den Schülertyp "Neuzugang" oder "Neuzugang an gleicher Schule" handelt.

Die Zeilen- Spaltenkombination **SF / ST** in der Tabelle steht für "Schulform / Schülertyp" und gibt entsprechend Auskunft für das jeweilige Exportfeld.

Titel            | Inhalt
---------------- | ------
Feld             | **Bezugsjahr** (Alle)
Beschreibung     | `Exportmodul > Erhebungsjahr` (Alle)<br/>Geben Sie im Dialogfenster bei der Ausführung des Exports das Erhebungsdatum ein. Das Datum wird auch dazu<br/>benötigt um das Erhebungsjahr auszulesen.
Feld             | **Status - Schülerstatus** (Alle)
Beschreibung     | `Schüler > Laufbahn > Abschluss > Abschluss 1 [Abschlüsse (Intern)]`<br/>`Schüler > Daten2 > Abgang [Abgangsarten]`<br>Der Schülerstatus ergibt sich anhand des Schülertyps un dem angegebenen Abschluss bzw. Abgang des Schülers.<br/>Neuzugang, Neuzugang an gleicher Sxhule, Eingeschult = 2 (Aktiv)<br/>Bildungsgang abgeschlossen = 8 (Abschluss)<br/>Abgänger = 8 (Abgang mit Abschluss) oder wenn kein Abschluss bzw. Abschluss oder Abgang = 0A sind = 9 (Abgang ohne Abschluss)
Feld             | **LfdNr** (Alle)
Beschreibung     | `Wird beim Export berechnet.`<br>Laufende Nummer pro Schüler, die beim Export erzeugt und hochgezählt wird.<br/>***Achtung***: Es handelt sich hierbei nicht um die Schüler.ID aus MAGELLAN.
Feld             | **Klasse** (Alle)
Beschreibung     | `Klassen > Daten > Statistikkürzel`<br>Bitte wiederholen Sie hier das Klassenkürzel, um die Klasse und dessen Schüler für die Statistik zu berücksichtigen. Das Statistikkürzel darf nicht mehr als 6 Zeichen betragen.<br/>**ABS** Max. 4 Stellen. Die ersten beiden Stellen werden als Jahrgang der Klasse übernommen. Die dritte und vierte Stelle werden als Parallelität übernommen. Ist das Feld Klasse nur zwei Zeichen lang, dann bleibt die Parallelität leer. <br>***Achtung***: Über das Statistikkürzel steuern Sie auch, ob eine Klasse für den Export berücksichtigt wird. Kein Statistikkürzel = Kein Export!
Feld             | **Gliederung (Schulgliederung)** (Alle)
Beschreibung     | `Klassen > Daten > Bildungsgang`<br/>`Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]`<br/>`Schüler > Daten 3 > Verschiedenes > G8/G9`<br>***ABS***: Gymnasien geben hier im Feld "G8/G9" an, ob es sich um ein G8 oder G9 Bildungsgang handelt. Kein Wert bedeutet = G01 (Aufbaugymnasium).<br/><br/>***BBS***: Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
Feld             | **Fachklasse (Fachklassen)** (BK / ABG, AKT, BAG, NZG, NGS)
Beschreibung     | `Klassen > Daten > Bildungsgang`<br/>`Schüler > Ausbildung >  Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]`<br>Die Schulgliederung wird anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung, alles danach ergibt die Fachklasse. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
Feld             | **Klassenart (Klassenarten)** (ABS / AKT, BAG, NZG, NGS)
Beschreibung     | `Klassen > Merkmale > Merkmal S3 [Verzeichnisse > Merkmale > Klassen]`<br>Bitte erfassen Sie hier pro Klasse die Klassenart.
Feld             | **OrgForm (Orgform)** (Alle / AKT, BAG, NZG, NGS)
Beschreibung     | `Klassen > Daten > Organisation [Organisationen]`<br>Wählen Sie die Organisationsform der Klasse aus.
Feld             | **AktJahrgang** (Alle)
Beschreibung     | `Klassen > Zeiträume > Klassenstufe [Klassenstufen]`<br>Wählen Sie die Klassenstufe der Klasse aus.
Feld             | **Foerderschwerp** (Alle)
Beschreibung     | `Klassen > Daten > Schwerpunkt1 und Schwerpunkt2 [Förderungen]`<br/>`Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2 [Förderungen]`<br>`Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von-Datum`<br>Es werden die eingetragenen Förderschwerpunkte der Klasse ausgelesen, wenn keine Einträge beim Schüler gemacht wurden. In der Liste der Fördermaßnahmen beim Schüler wird der erste Datensatz ausgelesen, dessen Von- Datum, in den entsprechenden Zeitraum passen, sortiert nach der eingetragenen Position!! <br/><br/>**Folgende Von-Bis-Daten werden ausgegeben:**<br/>Das Fördermaßnahmen-Von-Datum muss kleiner oder gleich dem Zeitraum-Von-Datum sein.<br/><br/>**WICHTIG**: Die Schlüssel für den 2. Förderschwerpunkt haben im Kürzel den Wert "_2" stehen und nur diese dürfen dafür genutzt werden. Alle anderen sind Schlüssel für den 1. Förderschwerpunkt.
Feld             | **Schwerstbeh - Schwerstbehindert** (Alle)
Beschreibung     | `Schüler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Förderbedarf [Förderbedarf]`<br>In der Liste der Fördermaßnahmen beim Schüler wird der erste Datensatz ausgelesen, sortiert nach der eingetragenen Position!! Wählen Sie im Feld "Förderbedarf" das Merkmal Schwerstbehinderung aus.
Feld             | **Reformpdg - Reformpädagogik**
Beschreibung     | Wird nicht erfasst.
Feld             | **JVA - JVA-Klasse** (BK / Alle)
Beschreibung     | `Klassen > Merkmale > Merkmal S2 [Merkmale]`<br>Wählen Sie aus, ob es sich bei der Klasse um eine JVA-Klasse handelt.
Feld             | **PLZ** (Alle)
Beschreibung     | `Schüler > Daten 1 > PLZ [Postleitzahlen]`<br>Wenn Sie hier die PLZ eintragen, wird diese ausgespielt. Das Feld ist wird z.Zt. nicht benötigt.
Feld             | **Wohnort** (Alle)
Beschreibung     | `Schüler > Daten 1 > Land<br/>Schüler > Daten 1 > Ort`<br/>`Schüler > Daten 1 > Gemeinde`<br>Über die Felder Land, Ort und Gemeinde steuern Sie die Ausgabe des Wohnortes. Folgende Kombinationen sind möglich:<br/>Land = LEER und Ort = LEER: Ausgabe = `Übriges Ausland`<br/>Land einer von **D, DEU, 0, 000** und Gemeinde = LEER oder in NRW: Ausgabe = Ort<br/>Gemeinde <> NRW: Ausgabe = Bundesland, z.B. `Rheinland Pfalz`<br/>Land = **B**: Ausgabe = `Belgien`<br/>Land = **L**: Ausgabe = `Luxemburg`<br/> Land =  **NL**: Ausgabe = `Niederlande`
Feld             | **Gebdat - Geburtsdatum** (Alle)
Beschreibung     | `Schüler > Daten 1 > Geburtsdatum`<br>Geben Sie das Geburtsdatum des Schülers ein.
Feld             | **Geschlecht** (Alle)
Beschreibung     | `Schüler > Daten 1 > Geschlecht`<br>Wählen Sie das Geschlecht des Schülers aus. <br>Wenn das Geschlecht keinen Eintrag enthält, wird der Schlüssel 6 = `Ohne Eintrag (im Geburtsregister)` ausgespielt.
Feld             | **Staatsang - Staatsangehörigkeit (Staatsangehörigkeiten)** (Alle)
Beschreibung     | `Schüler > Daten 2 > Staatsangeh. 1 [Staatsangehörigkeiten]`<br>Wählen Sie die Staatsangehörigkeit des Schülers aus. Wenn Sie keine Staatsangehörigkeit eingetragen haben, dann wird der Schüler automatisch mit dem Schlüssel der deutschen Staatsangehörigkeit ausgespielt.
Feld             | **Religion - Religionszugehörikeit (Religionen)** (Alle)
Beschreibung     | `Schüler > Daten 1 > Konfession [Konfessionen]`<br>Wählen Sie die Konfession des Schülers aus.
Feld             | **Relianmeldung** (Alle)
Beschreibung     |  `Schüler > Daten 1 > Rel.-Abmeldung bis`<br>Die Anmeldung zum Religionsunterricht ergibt sich anhand des Bis-Datums der Abmeldung vom Religionsunterricht. Eine Anmeldung ist nur erforderlich, wenn es zuvor eine Abmeldung gegeben hat.
Feld             | **Reliabmeldung** (Alle)
Beschreibung     | `Schüler > Daten 1 > Rel.-Abmeldung Von`<br>Geben Sie im Vom-Feld die Abmeldung vom Religionsunterricht an.
Feld             | **Aufnahmedatum** (Alle)
Beschreibung     | `Schüler > Daten2 > ZugangAm`<br>Geben Sie das Zugangsdatum des Schülers an der Schule an.
Feld             | **Labk** (Alle)
Beschreibung     | `Lehrer > Daten 1 > Kürzel`<br/>`Klassen > Zeiträume > Klassenleiter 1`<br>Tragen Sie für jeden Lehrer der Schule das 4-Stellige Lehrerkürzel (Abkürzung des Lehrers in der LID) ein.<br/>Geben Sie für jede Klasse des Exports den Klassenlehrer an.
Feld             | **Ausbildort** (Alle)
Beschreibung     |  Wird nicht erfasst, da es z.zt. nicht von der ASDPC-Schnittstelle statistisch ausgewertet wird<br/>Quelle: [Schnittstellenbeschreibung ASDPC](https://schulverwaltungsprogramme.msb.nrw.de/zbwschul.pdf)
Feld             | **Betriebsort** (BK, SB / Alle)
Beschreibung     | `Betriebe > Daten 1 > Ort`<br/>`Betriebe > Daten 1 > Land`<br/>`Betriebe > Daten 1 > Gemeinde`<br/>`Schüler > Ausbildung > Aktuelle Ausbildung (mit Ausbildungsbetrieb)`<br>Der Schüler muss eine aktuelle Ausbildung eingetragen haben und einen Ausbildungsbetrieb. Diese Betrieb sollte die oben genannten Felder eingetragen haben. Lesen Sie dazu auch die Berechnung des Wohnortes beim Schüler. Die Berechnung der Ausgabe ist identisch.
Feld             | **LSSchulform - Schulform der letzten Schule** (Alle / NZG, NZS)
Beschreibung     | `Schüler > Daten2 > Bereits besuchte Schulen > Schule`<br/>`Zugang/Abgang > Bereits besuchte Schulen > Schulform [Schulformen]`<br/>`Schüler > Daten2 > Herkunftsschule`<br>Wird der Schüler als `Neuzugang` erkannt, dann wird die Schulform der Herkunftsschule ausgegeben.<br/>Wird der Schüler als `Neuzugang an gleicher Schule` erkannt, dann wird die Schulform des Mandanten ausgegeben. <br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **LSSchulnummer - Schulnummer der letzten Schule** (Alle / NZG, NZS)
Beschreibung     | `Schulen > Daten > Schulnummer`<br/>`Schüler > Daten2 > Bereits besuchte Schulen > Schule`<br/>`Schüler > Daten2 > Herkunftsschule`<br>Wird der Schüler als `Neuzugang` erkannt, dann wird die Schulnummer der Herkunftsschule ausgegeben.<br/>Wird der Schüler als `Neuzugang an gleicher Schule` erkannt, dann wird die Schulnummer des Mandanten ausgegeben.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler mit deren Schulnummer ein.<br/>Wählen Sie unter Bereits besuchte Schulen die Schule aus.<br/>Wählen Sie unter Herkunftsschule die eingetragene Schule aus.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **LSGliederung - Schulgliederung der letzten Schulen** (Alle / NZG)
Beschreibung     | `Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang [Bildungsgänge]`<br/>Die mitgebrachte Schulgliederung tragen Sie über die dazugehörige Fachklasse über den Höchsten berufsbildenden Bildungsgang ein. Die Berechnung des Schlüssels erfolgt wie bei der Gliederung.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **LSFachklasse** (Alle / NZG)
Beschreibung     | `Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang [Bildungsgänge]`<br>Die mitgebrachte Fachklasse tragen Sie über den höchsten berufsbildenden Bildungsgang ein. Die Berechnung des Schlüssels erfolgt wie bei der Fachklasse.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **LSKlassenart** (ABS / NZG, NZS)
Beschreibung     | `Schüler > Daten2 > Bereits besuchte Schule > Herkunftsart [Herkunftsarten]`<br>Tragen Sie die Art der Klasse an der letzten Schule, z.B. Regelklasse ein.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **LSReformpdg**
Beschreibung     | Wird nicht erfasst.
Feld             | **LSSchulentl** (Alle / NZG)
Beschreibung     | `Schüler > Daten2 > Bereits besuchte Schulen > Schulbesuch bis`<br/>`Schüler > Daten2 > Herkunftsschule`<br>Geben Sie für die Herkunfsschule den Schulbesuch bis an.
Feld             | **LSJahrgang** (Alle / NZG)
Beschreibung     | `Schüler > Daten2 > Bereits besuchte Schulen > Letzte Klassenstufe [Klassenstufen]`<br/>`Schüler > Daten2 > Herkunftsschule`<br>Wählen Sie für die Herkunfsschule die Letzte Klassenstufe aus.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **LSQual** (Alle / NZG, NZS)
Beschreibung     | `Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss [Abschlüsse (Extern)]`<br>Grundsätzlich berechnet ASDPC den Höchsten allgemeinbildenden Abschluss aus dem Statistikfeld LSQual und Zeugnis, wobei LSQual eigentlich den letzten höchsten ABS Abschluss darstellt, z.B. aus einer anderen Schule. In MAGELLAN tragen Sie den höchsten Abschluss ABS nur an einer Stelle ein, auch wenn dieser an Ihrer eigenen Schule erworben wurde.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen) ausgegeben.
Feld             | **LSVersetz** (Alle / NZG)
Beschreibung     | `Schüler > Daten2 > Bereits besuchte Schulen > Unterlagen [ Herkunftsunterlagen]`<br/>`Schüler > Daten2 > Herkunftsschule`<br>Wählen Sie für die Herkunftsschule als Versetzungsart die Unterlagen aus.<br/>Für Abgänger wird dieser Wert nicht erneut (wurde bereits für den Schüler als Neuzugang oder Neuzugang an gleicher Schule übertragen)ausgegeben.
Feld             | **VOklasse** (Alle / ABG, AKT, BAGn NZS)
Beschreibung     | `Klassen > Daten > Statistikkürzel`<br>Achten Sie bitte darauf, dass für alle aktuellen und auch die Vorjahresklassen ein Statistikkürzel unter `Klassen > Daten > Statistikkürzel` erfasst wurde.
Feld             | **VOfachklasse** (Alle / ABG, AKT, BAG, NZS)
Beschreibung     | `Klassen > Daten > Bildungsgang`<br/>`Schüler > Ausbildung > Aktuelle Ausbildung > Bildungsgang [Bildungsgänge]`<br>Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld Fachklasse den Bildungsgang ein.
Feld             | **VOOrgForm** (Alle / ABG, AKT, BAG, NZS)
Beschreibung     | `Klassen > Daten > Organisation [Organisationen]`<br>Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld Gliederung den Bildungsgang für die Klasse und die Schüler ein. Zum Zuweisen des Bildungsgangs können Sie die Sammelzuweisung verwenden, es steht eine Option zum Anpassen der aktuellen Ausbildung zur Verfügung.
Feld             | **VOKlassenart** (ABS / ABG, AKT, BAG, NZS)
Beschreibung     | `Klassen > Merkmale > Merkmal S3 [Verzeichnisse > Merkmale > Klassen]`<br>Es wird die Klassenart der im Vorjahr besuchten Klasse ausgegeben. Bitte erfassen Sie pro Klasse die Klassenart.
Feld             | **VOJahrgang** (Alle / ABG, AKT, BAG, NZS)
Beschreibung     | `Klassen > Zeiträume > Klassenstufe [Klassenstufen]`<br>Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld AktJahrgang die Klassenstufe der Klasse ein.
Feld             | **VOfoerderschwerp** (Alle / ABG, AKT, BAG, NZS)
Beschreibung     | `Klassen > Daten > Schwerpunkt1 [Förderschwerpunkte]`<br/>`Schueler > Daten 4 > Schwerpunkt1 [Förderschwerpunkte]`<br>Lesen Sie dazu das Exportfeld "Foerderschwerp" und achten Sie darauf, dass der Eintrag eines evtl. auszugebenden Vorjahreswert mit den Von- und Bis-Daten des Vorjahreszeitraums übereinstimmt. Wenn sich die Schwerpunkte und weitere Eingaben nicht geändert haben, erweitern Sie den Zeitraum einfach entsprechend, dass der aktuelle und der Vorjahreszeitraum mit eingeschlossen wird oder Sie legen entsprechend getrennte Datensätze für die Zeiträume an.
Feld             | **VOschwerstbeh** (Alle / ABG, AKT, BAG, NZS)
Beschreibung     | `Schüler > Daten 4 > Förderbedarf [Förderbedarf]`<br>Wählen Sie hier das Merkmal Schwerstbehinderung für den Vorjahreszeitraum beim Schüler aus. Lesen Sie dazu auch die Beschreibung zum Feld "Vofoerderschwerp".
Feld             | **VOReformpdg**
Beschreibung     | Wird nicht erfasst.
Feld             | **Entldatum - Datum der Entlassung** (Alle / ABG)
Beschreibung     | `Schüler > Daten2 > Abgang am`<br>Geben Sie das Abgangsdatum des Schülers ein, wenn es sich um einen Abgänger handelt.
Feld             | **Zeugnis** (Alle / ABG, BAG, NZS)
Beschreibung     | `Schüler > Laufbahn > Abschluss > Abschluss 1 [Abschlüsse (Intern)]`<br/>`Schüler > Daten2 > Abgang`<br>Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können Sie die Werte unter Abschlüsse oder Abgang erfassen. Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht eingetragen ist, wird der Abgang für den Export erfasst.
Feld             | **Schulpflichterf - Erfüllung der Vollzeitschulpflicht** (ABS / Alle)
Beschreibung     | `Schüler  > Zeugnis > Details > Schulbesuchsjahr`<br>Ist das Schulbesuchsjahr > 9 dann wird der Schüler mit dem Merkmal `Vollzeitschulpflicht erfüllt` ausgegeben.
Feld             | **Schulwechselform**
Beschreibung     | Wird nicht erfasst.
Feld             | **Versetzung** (Alle)
Beschreibung     | `Schüler > Laufbahn > Allgemein > Versetzt`<br/>`Schüler > Laufbahn > Allgemein > Versetzungsart [Versetzungsarten]`<br>Sie können einen Schüler als `Versetzt` oder `Nicht Versetzt` über das Feld `Versetzt` angeben. Ist dieses Feld leer oder Sie haben zusätzlich im Feld `Versetzungsart` einen Wert ausgewählt, dann wird dieses für die Versetzung ausgelesen.<br/><br/>Wo wird ausgelesen:<br/><br/> * Für Neuzugänge von anderen Schulen wird nichts ausgelesen.<br/> * Für Neuzugänge der selben Schule wird das 2.HJ des vergangenen Jahres ausgelesen<br/> * Bei aktuellen Schülern wird der Eintrag im 2.HJ des vergangenen Jahres ausgelesen<br/> * Bei Abgängern aus dem vergangenen Schuljahr wird jeweils aus dem Abgangshalbjahr gelesen<br/> * Bei Abgängern aus dem aktuellen Schuljahr wird das 2.HJ des vergangenen Jahres ausgelesen<br/><br/>TIPP:<br/>Als welcher Schülertyp der Schüler erkannt wird, können Sie im als Hilfsfeld genutzen Feld `Produktversion` sehen.<br/><br/>Für Berufskollegs: Wenn der Schüler nicht Neuzugang von einer anderen Schule oder der eigenen Schule ist und keine Versetzungsart gewählt ist, wird immer eine `0` ausgegeben, auch wenn die Versetzung nicht gefüllt ist.
Feld             | **JahrZuzug**
Beschreibung     | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „zugezogen“ ausgewertet wird.
Feld             | **JahrEinschulung**
Beschreibung     | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „zugezogen“ ausgewertet wird.
Feld             | **JahrWechselSekI**
Beschreibung     | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „zugezogen“ ausgewertet wird.
Feld             | **zugezogen** (Alle)
Beschreibung     | `Schüler > Daten 1 > Geburtsland [Staatsangehörigkeiten]`<br/>`Schüler > Daten 2 > In Deutschland seit`<br>Der Schüler gilt als zugezogen, wenn das Feld „Geburtsland“ nicht einer der Werte D, DE, DEU, 0 oder 000 für Deutschland eingetragen hat; oder das Feld „In Deutschland seit“ ein Zuzugsdatum nach Deutschland enthält.
Feld             | **GeburtslandMutter**
Beschreibung     | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „Elternteilzugezogen“ ausgewertet wird.
Feld             | **GeburtslandVater**
Beschreibung     | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „Elternteilzugezogen“ ausgewertet wird.
Feld             | **Elternteilzugezogen** (Alle)
Beschreibung     | `Schüler > Daten 2 > NdH`<br>Es ist zwar möglich bei den Sorgeberechtigten das Geburtsland anzugeben, der Einfachheit halber, lesen wir das NdH-Feld aus Markieren Sie das Feld „NdH“, wenn mindestens ein Elternteil nach Deutschland zugezogen ist.
Feld             | **Verkehrssprache** (Alle)
Beschreibung     | `Schüler > Daten 2 > Verkehrssprache`<br>Geben Sie hier einen Wert ein, wenn in der Familie überwiegend nicht Deutsch gesprochen wird. Anderenfalls können Sie das Feld leer lassen. Für die aktuelle Erhebung ist es ausreichend, einen Wert verschieden zu 000 zu verwenden, um darzustellen, das die Verkehrssprache in der Familie nicht Deutsch ist.
Feld             | **Einschulungsart** (G / Alle)
Beschreibung     | `Schüler > Statistik > Merkmal S1 [Merkmale]`<br>Wählen Sie hier die Einschulungsart des Schülers aus.
Feld             | **Grundschulempfehlung** (GE, GY / Alle)
Beschreibung     | `Schüler > Daten2 > Zugang > Empfehlung (extern) [Bewerbungsempfehlungen]`<br>Geben Sie hier die Empfehlung der Primarschulen an. Vorausgesetzt wird der Eintrag der Mandantenschulform (GY,GE).
Feld             | **Massnahmentraeger** (Alle)
Beschreibung     | `Schüler > Statistik > Merkmal S2 [Merkmale]`<br>Wählen Sie aus, ob der Schüler von einem Ausbildungsbetrieb oder einem Träger ausgebildet wird.
Feld             | **Betreuung** (G, GY, GE / Alle)
Beschreibung     | `Schüler > Extras > Betreuungsarten > Innerschulisch 1 [Betreuungen innerschulisch (Schüler)]`<br>Wählen Sie die Betreuungsmaßnahme der Nachmittags/Ganztagsbetreuung aus.
Feld             | **BKAZVO** (BK, SB / NZG)
Beschreibung     | `Schüler > Statistik > Merkmal T1`<br>Geben Sie die Anzahl der anzurechnenden Monate bei verkürzter Ausbildung an. Möglich sind 0, 6, 12 oder 18 Monate.
Feld             | **Foerderschwerp2** (Alle)
Beschreibung     | `Klassen > Daten > Schwerpunkt1 und Schwerpunkt2 [Förderungen]`<br/>`Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2 [Förderungen]`<br>`Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten`<br>Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse geprüft. Lesen Sie dazu auch die Beschreibung zum Feld "Foerderschwerp".
Feld             | **VOfoerderschwerp2** (Alle / ABG, AKT, BAG, NZS)
Beschreibung     | `Klassen > Daten > Schwerpunkt1 und Schwerpunkt2 [Förderungen]`<br/>`Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2 [Förderungen]`<br>`Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten`<br>Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse geprüft. Lesen Sie dazu auch die Beschreibung zum Feld "Foerderschwerp".
Feld             | **Berufsabschluss** (BK, SB, WB / Alle)
Beschreibung     | `Schüler > Statistik > Merkmal S1 [Merkmale]`<br>Wählen Sie aus, ob bereits eine abgeschlossene Berufsausbildung vorliegt.
Feld             | **Produktname** (Alle)
Beschreibung     | Das Feld wird für den Import nach ASDPC nicht benötigt, soll aber beim Support helfen. Wir geben hier fest den Wert Ihrer eingesetzten MAGELLAN-Ausgabe entsprechend des Registryeintrages aus.
Feld             | **Produktversion** (Alle)
Beschreibung     | Das Feld wird für für den Import nach ASDPC nicht benötigt, soll aber beim Support helfen. <br/>Wir geben hier die berechnete Datensatzart (z.B. Neuzugang, Eingeschult, etc.) für die Zeile aus.
Feld             | **Adressenmerkmal**
Beschreibung     | Die Adressenmerkmale für weitere Standorte erfassen Sie bitte direkt in ASDPC.
Feld             | **Internat** (Alle)
Beschreibung     | `Schüler > Daten 4 > Betreuung > Einrichtung`<br>Wenn der Schüler einen Internatsplatz besetzt, wählen Sie bitte Internat aus der Auswahlliste aus.
