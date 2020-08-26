# Schüler- und Klassendaten der SIM.TXT

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

## Dateneingabe

***Erläuterung:*** In der nachfolgenden Tabelle finden Sie alle Schnittstellenfeder der SIM.TXT. Entsprechend der Schnittstellenbeschreibung, Ihrer Rückmeldungen und Erfahrungen der letzten Jahre werden nicht alle Felder immer gefüllt. Ob ein Feld gefüllt wird, hängt vom erkannten Schülertyp und der Haupt-Schulform Ihrer Schule ab. Es gibt Felder die lediglich für Berufskollegs oder z.B. nur für Gymnasien zu füllen sind und wiederum andere, die nur gefüllt werden, wenn es ich um den Schülertyp "Neuzugang" oder "Neuzugang an gleicher Schule" handelt.

Die Zeilen- Spaltenkombination **SF / ST** in der Tabelle steht für "Schulform / Schülertyp" und gibt entsprechend Auskunft für das jeweilige Exportfeld.

Art               | Inhalt
----------------- |-------
**Exportfeld**    | **Bezugsjahr**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Exportmodul > Erhebungsjahr
Beschreibung      | Geben Sie im Dialogfenster bei der Ausführung des Exports das Erhebungsdatum ein. Das Datum wird auch dazu<br/>benötigt um das Erhebungsjahr auszulesen.
**Exportfeld**    | **Status - Schülerstatus**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1 [Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang [Abgangsarten]
Beschreibung      | Der Schülerstatus ergibt sich anhand des Schülertyps un dem angegebenen Abschluss bzw. Abgang des Schülers.<br/>Neuzugang, Neuzugang an gleicher Sxhule, Eingeschult = 2 (Aktiv)<br/>Bildungsgang abgeschlossen = 8 (Abschluss)<br/>Abgänger = 8 (Abgang mit Abschluss) oder wenn kein Abschluss bzw. Abschluss oder Abgang = 0A sind = 9 (Abgang ohne Abschluss)
**Exportfeld**    | **LfdNr**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Wird beim Export berechnet.
Beschreibung      | Laufende Nummer pro Schüler. die beim Export erzeugt und hochgezählt wird.<br/>***Achtung***: Es handelt sich hierbei nicht um die Schüler.ID aus MAGELLAN.
**Exportfeld**    | **Klasse**
Datenfeld         | MAGELLAN: Klassen > Daten > Statistikkürzel
SF / ST           | Alle
Beschreibung      | Bitte wiederholen Sie hier das Klassenkürzel, um die Klasse und dessen Schüler für die Statistik zu berücksichtigen. Das Statistikkürzel darf nicht mehr als 6 Zeichen betragen.<br/>**ABS** Max. 4 Stellen. Die ersten beiden Stellen werden als Jahrgang der Klasse übernommen. Die dritte und vierte Stelle werden als Parallelität übernommen. Ist das Feld Klasse nur zwei Zeichen lang, dann bleibt die Parallelität leer. <br>***Achtung***: Über das Statistikkürzel steuern Sie auch, ob eine Klasse für den Export berücksichtigt wird. Kein Statistikkürzel = Kein Export!
**Exportfeld**    | **Gliederung (Schulgliederung)**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]<br/>Schüler > Daten 3 > Verschiedenes > G8/G9
Beschreibung      | ***ABS***: Gymnasien geben hier im Feld "G8/G9" an, ob es sich um ein G8 oder G9 Bildungsgang handelt. Kein Wert bedeutet = G01 (Aufbaugymnasium).<br/><br/>***BBS***: Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Exportfeld**    | **Fachklasse (Fachklassen)**
SF / ST           | BK / ABG, AKT, BAG, NZG, NGS
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung >  Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]
Beschreibung      | Die Schulgliederung wird anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung, alles danach ergibt die Fachklasse. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Exportfeld**    | **Klassenart (Klassenarten)**
SF / ST           | ABS / AKT, BAG, NZG, NGS
Datenfeld         | MAGELLAN: Klassen > Merkmale > Merkmal S3 [Verzeichnisse > Merkmale > Klassen]
Beschreibung      | Bitte erfassen Sie hier pro Klasse die Klassenart.
**Exportfeld**    | **OrgForm (Orgform)**
SF / ST           | Alle / AKT, BAG, NZG, NGS
Datenfeld         | MAGELLAN: Klassen > Daten > Organisation [Organisationen]
Beschreibung      | Wählen Sie die Organisationsform der Klasse aus.
**Exportfeld**    | **AktJahrgang**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Klassen > Zeiträume > Klassenstufe[Klassenstufen]
Beschreibung      | Wählen Sie die Klassenstufe der Klasse aus.
**Exportfeld**    | **Foerderschwerp**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br>>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten
Beschreibung      | Es werden die eingetragenen Förderschwerpunkte der Klasse ausgelesen, wenn keine Einträge beim Schüler gemacht wurden. In der Liste der Fördermaßnahmen beim Schüler wird der erste Datensatz ausgelesen, dessen Von- und Bis- Daten, in den entsprechenden Zeitraum passsen, sortiert nach der eingetragenen Position!! ***WICHTIG***: Die Schlüssel für den 2. Förderschwerpunkt haben im Kürzel den Wert "_2" stehen und nur diese dürfen dafür genutzt werden. Alle anderen sind Schlüssel für den 1. Förderschwerpunkt.
**Exportfeld**    | **Schwerstbeh - Schwerstbehindert**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Förderbedarf[Förderbedarf]
Beschreibung      | In der Liste der Fördermaßnahmen beim Schüler wird der erste Datensatz ausgelesen, sortiert nach der eingetragenen Position!! Wählen Sie im Feld "Förderbedarf" das Merkmal Schwerstbehinderung aus.
**Exportfeld**    | **Reformpdg - Reformpädagogik**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Exportfeld**    | **JVA - JVA-Klasse**
SF / ST           | BK / Alle
Datenfeld         | MAGELLAN: Klassen > Merkmale > Merkmal S2 [Merkmale]
Beschreibung      | Wählen Sie aus, ob es sich bei der Klasse um eine JVA-Klasse handelt.
**Exportfeld**    | **PLZ**
SF / ST           | Alle
Datenfeld         | MAGELLAN:Schüler > Daten 1 > PLZ[Postleitzahlen]
Beschreibung      | Wenn Sie hier die PLZ eintragen, wird diese ausgespielt. Das Feld ist wird z.Zt. nicht benötigt.
**Exportfeld**    | **Wohnort**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Daten 1 > Land<br/>Schüler > Daten 1 > Ort<br/>Schüler > Daten 1 > Gemeinde
Beschreibung      | Über die Felder Land, Ort und Gemeinde steuern Sie die Ausgabe des Wohnortes. Folgende Kombinationen sind möglich:<br/>Land = LEER und Ort = LEER: Ausgabe = `Übriges Ausland`<br/>Land einer von **D, DEU, 0, 000** und Gemeinde = LEER oder in NRW: Ausgabe = Ort<br/>Gemeinde <> NRW: Ausgabe = Bundesland, z.B. `Rheinland Pfalz`<br/>Land = **B**: Ausgabe = `Belgien`<br/>Land = **L**: Ausgabe = `Luxemburg`<br/> Land =  **NL**: Ausgabe = `Niederlande`
**Exportfeld**    | **Gebdat - Geburtsdatum**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geburtsdatum
Beschreibung      | Geben Sie das Geburtsdatum des Schülers ein.
**Exportfeld**    | **Geschlecht**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie das Geschlecht des Schülers aus. ***WICHTIG***: Ab diesem Jahr wird auch offiziell das Geschlecht D = DIVERS vom Amt unterstützt. Zusätzlich ist auch noch der Schlüssel 6 = `Ohne Eintrag (im Geburtsregister)` mit dabei. Dieser Schlüssel wird auch MAGELLAN 7 ausgespielt, wenn das Geschlecht keinen Eintrag enthält.
**Exportfeld**    | **Staatsang - Staatsangehörigkeit (Staatsangehörigkeiten)**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Staatsangeh. 1[Staatsangehörigkeiten]
Beschreibung      | Wählen Sie die Staatsangehörigkeit des Schülers aus. Wenn Sie keine Staatsangehörigkeit eingetragen haben, dann wird der Schüler automatisch mit dem Schlüssel der deutschen Staatsangehörigkeit ausgespielt.
**Exportfeld**    | **Religion - Religionszugehörikeit (Religionen)**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Konfession[Konfessionen]
Beschreibung      | Wählen Sie die Konfession des Schülers aus.
**Exportfeld**    | **Relianmeldung**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Rel.-Abmeldung bis
Beschreibung      | Die Anmeldung zum Religionsunterricht ergibt sich anhand des Bis-Datums der Abmeldung vom Religionsunterricht. Eine Anmeldung ist nur erforderlich, wenn es zuvor eine Abmeldung gegeben hat.
**Exportfeld**    | **Reliabmeldung**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Rel.-Abmeldung Von
Beschreibung      | Geben Sie im Vom-Feld die Abmeldung vom Religionsunterricht an.
**Exportfeld**    | **Aufnahmedatum**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > ZugangAm
Beschreibung      | Geben Sie das Zugangsdatum des Schülers an der Schule an.
**Exportfeld**    | **Labk**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Lehrer > Daten 1 > Kürzel<br/>Klassen > Zeiträume > Klassenleiter 1
Beschreibung      | Tragen Sie für jeden Lehrer der Schule das 4-Stellige Lehrerkürzel (Abkürzung des Lehrers in der LID) ein.<br/>Geben Sie für jede Klasse des Exports den Klassenlehrer an.
**Exportfeld**    | **Ausbildort**
SF / ST           | Alle
Datenfeld         | -
Beschreibung      | Wird nicht erfasst, da es z.zt. nicht von der ASDPC-Schnittstelle statistisch ausgewertet wird<br/>Quelle: [Schnittstellenbeschreibung ASDPC](https://schulverwaltungsprogramme.msb.nrw.de/zbwschul.pdf)
**Exportfeld**    | **Betriebsort**
SF / ST           | BK, SB / Alle
Datenfeld         | MAGELLAN:<br/>Betriebe > Daten 1 > Ort<br/>Betriebe > Daten 1 > Land<br/>Betriebe > Daten 1 > Gemeinde<br/>Schüler > Ausbildung > Aktuelle Ausbildung (mit Ausbildungsbetrieb)
Beschreibung      | Der Schüler muss eine aktuelle Ausbildung eingetragen haben und einen Ausbildungsbetrieb. Diese Betrieb sollte die oben genannten Felder eingetragen haben. Lesen Sie dazu auch die Berechnung des Wohnortes beim Schüler. Die Berechnung der Ausgabe ist identisch.
**Exportfeld**    | **LSSchulform - Schulform der letzten Schule**
SF / ST           | Alle / NZG, NZS
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schule<br/>Zugang/Abgang > Bereits besuchte Schulen > Schulform[Schulformen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wird der Schüler als `Neuzugang` erkannt, dann wird die Schulform der Herkunftsschule ausgegeben.<br/>Wird der Schüler als `Neuzugang an gleicher Schule` erkannt, dann wird die Schulform des Mandanten ausgegeben.
**Exportfeld**    | **LSSchulnummer - Schulnummer der letzten Schule**
SF / ST           | Alle / NZG, NZS
Datenfeld         | MAGELLAN:<br/>Schulen > Daten > Schulnummer<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schule<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wird der Schüler als `Neuzugang` erkannt, dann wird die Schulnummer der Herkunftsschule ausgegeben.<br/>Wird der Schüler als `Neuzugang an gleicher Schule` erkannt, dann wird die Schulnummer des Mandanten ausgegeben.<br/>Tragen Sie bei den Schulen die Herkunftsschulen der Schüler mit deren Schulnummer ein.<br/>Wählen Sie unter Bereits besuchte Schulen die Schule aus.<br/>ählen Sie unter Herkunftsschule die eingetragene Schule aus.
**Exportfeld**    | **LSGliederung - Schulgliederung der letzten Schulen**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang[Bildungsgänge]<br/>
Beschreibung      | Die mitgebrachte Schulgliederung tragen Sie über die dazugehörige Fachklasse über den Höchsten berufsbildenden Bildungsgang ein. Die Berechnung des Schlüssels erfolgt wie bei der Gliederung.
**Exportfeld**    | **LSFachklasse**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang [Bildungsgänge]
Beschreibung      | Die mitgebrachte Fachklasse tragen Sie über den Höchsten berufsbildenden Bildungsgang ein. Die Berechnung des Schlüssels erfolgt wie bei der Fachklasse.
**Exportfeld**    | **LSKlassenart**
SF / ST           | ABS / NZG, NZS
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > Bereits besuchte Schule > Herkunftsart [Herkunftsarten]
Beschreibung      | Tragen Sie die Art der Klasse an der letzten Schule, z.B. Regelklasse ein.
**Exportfeld**    | **LSReformpdg**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Exportfeld**    | **LSSchulentl**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulbesuch bis<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Geben Sie für die Herkunfsschule den Schulbesuch bis an.
**Exportfeld**    | **LSJahrgang**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Letzte Klassenstufe [Klassenstufen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie für die Herkunfsschule die Letzte Klassenstufe aus.
**Exportfeld**    | **LSQual**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss [Abschlüsse (Extern)]
Beschreibung      | Grundsätzlich berechnet ASDPC den Höchsten allgemeinbildenden Abschluss aus dem Statistikfeld LSQual und Zeugnis, wobei LSQual eigentlich den letzten höchsten ABS Abschluss darstellt, z.B. aus einer anderen Schule. In MAGELLAN tragen Sie den höchsten Abschluss ABS nur an einer Stelle ein, auch wenn dieser an Ihrer eigenen Schule erworben wurde.
**Exportfeld**    | **LSVersetz**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen[ Herkunftsunterlagen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie für die Herkunftsschule als Versetzungsart die Unterlagen aus.
**Exportfeld**    | **VOklasse**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Daten > Statistikkürzel
Beschreibung      | Achten Sie bitte darauf, dass für alle aktuellen und auch die Vorjahresklassen ein Statistikkürzel unter `Klassen > Daten > Statistikkürzel` erfasst wurde.
**Exportfeld**    | **VOgliederung**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildungsgang [Bildgungsgänge]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld Gliederung den Bildungsgang für die Klasse und die Schüler ein. Zum Zuweisen des Bildungsgangs können Sie die Sammelzuweisung verwenden, es steht eine Option zum Anpassen der aktuellen Ausbildung zur Verfügung.
**Exportfeld**    | **VOfachklasse**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildungsgänge]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld Fachklasse den Bildungsgang ein.
**Exportfeld**    | **VOOrgForm**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Daten > Organisation [Organisationen]
Beschreibung      |echseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld Gliederung den Bildungsgang für die Klasse und die Schüler ein. Zum Zuweisen des Bildungsgangs können Sie die Sammelzuweisung verwenden, es steht eine Option zum Anpassen der aktuellen Ausbildung zur Verfügung.
**Exportfeld**    | **VOKlassenart**
SF / ST           | ABS / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Merkmale > Merkmal S3 [Verzeichnisse > Merkmale > Klassen]
Beschreibung      | Es wird die Klassenart der im Vorjahr besuchten Klasse ausgegeben. Bitte erfassen Sie pro Klasse die Klassenart.
**Exportfeld**    | **VOJahrgang**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Zeiträume > Klassenstufe [Klassenstufen]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Exportfeld AktJahrgang die Klassenstufe der Klasse ein.
**Exportfeld**    | **VOfoerderschwerp**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1[Förderschwerpunkte]<br/>Schueler > Daten 4 > Schwerpunkt1[Förderschwerpunkte]
Beschreibung      | Lesen Sie dazu das Exportfeld "Foerderschwerp" und achten Sie darauf, dass der Eintrag eines evtl. auszugebenden Vorjahreswert mit den Von- und Bis-Daten des Vorjahreszeitraums übereinstimmt. Wenn sich die Schwerpunkte und weitere Eingaben nicht geändert haben, erweitern Sie den Zeitraum einfach entsprechend, dass der aktuelle und der Vorjahreszeitraum mit eingeschlossen wird oder Sie legen entsprechend getrennte Datensätze für die Zeiträume an.
**Exportfeld**    | **VOschwerstbeh**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:Schüler > Daten 4 > Förderbedarf[Förderbedarf]
Beschreibung      | Wählen Sie hier das Merkmal Schwerstbehinderung für den Vorjahreszeitraum beim Schüler aus. Lesen Sie dazu auch die Beschreibung zum Feld "Vofoerderschwerp".
**Exportfeld**    | VOReformpdg
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Exportfeld**    | **Entldatum - Datum der Entlassung**
SF / ST           | Alle / ABG
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > Abgang am
Beschreibung      | Geben Sie das Abgangsdatum des Schülers ein, wenn es sich um einen Abgänger handelt.
**Exportfeld**    | **Zeugnis**
SF / ST           | Alle / ABG
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1[Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang
Beschreibung      | Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können Sie die Werte unter Abschlüsse oder Abgang erfassen. Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht eingetragen ist, wird der Abgang für den Export erfasst.
**Exportfeld**    | **Schulpflichterf - Erfüllung der Vollzeitschulpflicht**
SF / ST           | ABS / Alle
Datenfeld         | MAGELLAN: Schüler  > Zeugnis > Details > Schulbesuchsjahr
Beschreibung      | Ist das Schulbesuchsjahr > 9 dann wird der Schüler mit dem Merkmal `Vollzeitschulpflicht erfüllt` ausgegeben.
**Exportfeld**    | **Schulwechselform**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Exportfeld**    | **Versetzung**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Allgemein > Versetzt<br/>Schüler > Laufbahn > Allgemein > Versetzungsart [Versetzungsarten]
Beschreibung      | Sie können einen Schüler als `Versetzt` oder `Nicht Versetzt` über das Feld `Versetzt` angeben. Ist diese Feld leer oder Sie haben zusätzlich im Feld `Versetzungsart` einen Wert ausgewählt, dann wird dieses für die Versetzung ausgelesen.<br/><br/>Wo wird ausgelesen:<br/><br/> *  Für Neuzugänge von anderen Schulen wird nichts ausgelesen<br/> *  Für Neuzugänge der selben Schule wird das 2.HJ des vergangenen Jahres ausgelesen<br/> *  Bei aktuellen Schülern wird der Eintrag das 2.HJ des vergangenen Jahres ausgelesen<br/> *  Bei Abgängern aus dem vergangenen Schuljahr wird jeweils aus dem Abgangshalbjahr gelesen<br/> *  Bei Abgängern aus dem aktuellen Schuljahr wird das 2.HJ des vergangenen Jahres ausgelesen<br/><br/>TIPP:<br/>Als welcher Schülertyp der Schüler erkannt wird, können Sie im als Hilfsfeld genutzen Feld `Produktversion` sehen.
**Exportfeld**    | **JahrZuzug**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „zugezogen“ ausgewertet wird.
**Exportfeld**    | **JahrEinschulung**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „zugezogen“ ausgewertet wird.
**Exportfeld**    | **JahrWechselSekI**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „zugezogen“ ausgewertet wird.
**Exportfeld**    | **zugezogen**
SF / ST           | Alle 
Datenfeld         | MAGELLAN:<br/>Schüler > Daten 1 > Geburtsland [Staatsangehörigkeiten]<br/>Schüler > Daten 2 > In Deutschland seit
Beschreibung      | Der Schüler gilt als zugezogen, wenn das Feld „Geburtsland“ nicht einer der Werte D, DE, DEU, 0  oder 000 für Deutschland eingetragen hat; oder das Feld „In Deutschland seit“ ein Zuzugsdatum nach Deutschland enthält.
**Exportfeld**    | **GeburtslandMutter**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „Elternteilzugezogen“ ausgewertet wird.
**Exportfeld**    | **GeburtslandVater**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Schnittstellenbeschreibung nicht benötigt, wenn das Exportfeld „Elternteilzugezogen“ ausgewertet wird.
**Exportfeld**    | **Elternteilzugezogen**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > NdH
Beschreibung      | Es ist zwar möglich bei den Sorgeberechtigten das Geburtsland anzugeben, der Einfachheit halber, lesen wir das NdH-Feld in MAGELLAN aus. Markieren Sie das Feld „NdH“, wenn mindestens ein Elternteil nach Deutschland zugezogen ist.
**Exportfeld**    | **Verkehrssprache**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Verkehrssprache
Beschreibung      | Geben Sie hier einen Wert ein, wenn in der Familie überwiegend nicht Deutsch gesprochen wird. Anderenfalls können Sie das Feld leer lassen. Für die aktuelle Erhebung ist es ausreichend, einen Wert verschieden zu 000 zu verwenden, um darzustellen, das die Verkehrssprache in der Familie nicht Deutsch ist.
**Exportfeld**    | **Einschulungsart**
SF / ST           | G / Alle
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S1 [Merkmale]
Beschreibung      | Wählen Sie hier die Einschulungsart des Schülers aus.
**Exportfeld**    | **Grundschulempfehlung**
SF / ST           | GE, GY / Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Zugang > Empfehlung [Empfehlungen (Bewerbung)]
Beschreibung      | Geben Sie hier die Empfehlung der Primarschulen an.
**Exportfeld**    | Massnahmentraeger
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S2 [Merkmale]
Beschreibung      | Wählen Sie aus, ob der Schüler von einem Ausbildungsbetrieb oder einem Träger ausgebildet wird.
**Exportfeld**    | **Betreuung**
SF / ST           | G, GY, GE / Alle
Datenfeld         | MAGELLAN: Schüler > Extras > Betreuungsarten > Innerschulisch 1 [Betreuungen innerschulisch (Schüler)]
Beschreibung      | Wählen Sie die Betreuungsmaßnahme der Nachmittags/Ganztagsbetreuung aus.
**Exportfeld**    | **BKAZVO**
SF / ST           | BK, SB / NZG
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal T1
Beschreibung      | Geben Sie die Anzahl der anzurechnenden Monate bei verkürzter Ausbildung an. Möglich sind 0, 6, 12 oder 18 Monate.
**Exportfeld**    | **Foerderschwerp2**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br>>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten
Beschreibung      | Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse geprüft. Lesen Sie dazu auch die Beschreibung zum Feld "Foerderschwerp".
**Exportfeld**    | **VOfoerderschwerp2**
SF / ST           | Alle / ABG, AKT, BAG, NZS
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br>>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten
Beschreibung      | Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse geprüft. Lesen Sie dazu auch die Beschreibung zum Feld "Foerderschwerp".
**Exportfeld**    | **Berufsabschluss**
SF / ST           | BK, SB, WB / Alle
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S1 [Merkmale]
Beschreibung      | Wählen Sie aus, ob bereits eine abgeschlossene Berufsausbildung vorliegt.
**Exportfeld**    | **Produktname**
SF / ST           | Alle
Datenfeld         | -
Beschreibung      | Das Feld wird für den Import nach ASDPC nicht benötigt, soll aber beim Support helfen. Wir geben hier fest den Wert „MAGELLAN 7“ und die aktuell installierte MAGELLAN 7 Version (Registry Wert) aus.
**Exportfeld**    | **Produktversion**
SF / ST           | Alle
Datenfeld         | -
Beschreibung      | Das Feld wird für für den Import nach ASDPC nicht benötigt, soll aber beim Support helfen. <br/>Wir geben hier die berechnete Datensatzart (z.B. Neuzugang, Eingeschult, etc.) für die Zeile aus.
**Exportfeld**    | **Adressenmerkmal**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Die Adressenmerkmale für weitere Standorte erfassen Sie bitte direkt in ASDPC.
**Exportfeld**    | **Internat**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 4 > Betreuung > Einrichtung
Beschreibung      | Wenn der Schüler einen Internatsplatz besetzt, wählen Sie bitte Internat aus der Auswahlliste aus.
