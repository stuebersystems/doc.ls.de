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
Datenfeld         | MAGELLAN: Wird beim Export berechnet.
Beschreibung      | Laufende Nummer pro Schüler. die beim Export erzeugt und hochgezählt wird.<br/>***Achtung***: Es handelt sich hierbei nicht um die Schüler.ID aus MAGELLAN.
**Statistikfeld** | **Klasse**
Datenfeld         | MAGELLAN: Klassen > Daten > Statistikkürzel
SF / ST           | Alle
Beschreibung      | Bitte wiederholen Sie hier das Klassenkürzel, um die Klasse und dessen Schüler für die Statistik zu berücksichtigen. Das Statistikkürzel darf nicht mehr als 6 Zeichen betragen.<br/>***Achtung***: Über das Statistikkürzel steuern Sie auch, ob eine Klasse für den Export berücksichtigt wird. Kein Statistikkürzel = Kein Export!
**Statistikfeld** | **Gliederung (Schulgliederung)**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]<br/>Schüler > Daten 3 > Verschiedenes > G8/G9
Beschreibung      | ***ABS***: Gymnasien geben hier im Feld "G8/G9" an, ob es sich um ein G8 oder G9 Bildungsgang handelt. Kein Wert bedeutet = G01 (Aufbaugymnasium).<br/><br/>***BBS***: Da die Schulgliederung von der Fachklasse abhängig ist, wird diese anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Statistikfeld** | **Fachklasse (Fachklassen)**
SF / ST           | BK / ABG, AKT, BAG, NZG, NGS
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung >  Aktuelle Ausbildung > Bildgungsgang [Bildgungsgänge]
Beschreibung      | Die Schulgliederung wird anhand des Bildungsgangs in MAGELLAN ausgelesen. Die ersten drei Zeichen des Schlüssels ergeben die Gliederung, alles danach ergibt die Fachklasse. Wenn die gesamte Klasse für einen Bildungsgang bestimmt ist, dann tragen Sie den Bildungsgang bei der Klasse ein. In Klassen mit gemischten Bildungsgängen, müssen Sie den Bildungsgang beim Schüler erfassen. Es wird Schüler vor Klasse geprüft.
**Statistikfeld** | **Klassenart (Klassenarten)**
SF / ST           | ABS / AKT, BAG, NZG, NGS
Datenfeld         | MAGELLAN: Klassen > Merkmale > Merkmal S3 [Verzeichnisse > Merkmale > Klassen]
Beschreibung      | Bitte erfassen Sie hier pro Klasse die Klassenart.
**Statistikfeld** | **OrgForm (Orgform)**
SF / ST           | Alle / AKT, BAG, NZG, NGS
Datenfeld         | MAGELLAN: Klassen > Daten > Organisation [Organisationen]
Beschreibung      | Wählen Sie die Organisationsform der Klasse aus.
**Statistikfeld** | **AktJahrgang**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Klassen > Zeiträume > Klassenstufe[Klassenstufen]
Beschreibung      | Wählen Sie die Klassenstufe der Klasse aus.
**Statistikfeld** | **Foerderschwerp**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br>>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten
Beschreibung      | Es werden die eingetragenen Förderschwerpunkte der Klasse ausgelesen, wenn keine Einträge beim Schüler gemacht wurden. In der Liste der Fördermaßnahmen beim Schüler wird der erste Datensatz ausgelesen, dessen Von- und Bis- Daten, in den entsprechenden Zeitraum passsen, sortiert nach der eingetragenen Position!! ***WICHTIG***: Die Schlüssel für den 2. Förderschwerpunkt haben im Kürzel den Wert "_2" stehen und nur diese dürfen dafür genutzt werden. Alle anderen sind Schlüssel für den 1. Förderschwerpunkt.
**Statistikfeld** | **Schwerstbeh - Schwerstbehindert**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Förderbedarf[Förderbedarf]
Beschreibung      | In der Liste der Fördermaßnahmen beim Schüler wird der erste Datensatz ausgelesen, sortiert nach der eingetragenen Position!! Wählen Sie im Feld "Förderbedarf" das Merkmal Schwerstbehinderung aus.
**Statistikfeld** | **Reformpdg - Reformpädagogik**
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **JVA - JVA-Klasse**
SF / ST           | BK / Alle
Datenfeld         | MAGELLAN: Klassen > Merkmale > Merkmal S2 [Merkmale]
Beschreibung      | Wählen Sie aus, ob es sich bei der Klasse um eine JVA-Klasse handelt.
**Statistikfeld** | **PLZ**
SF / ST           | Alle
Datenfeld         | MAGELLAN:Schüler > Daten 1 > PLZ[Postleitzahlen]
Beschreibung      | Wenn Sie hier die PLZ eintragen, wird diese ausgespielt. Das Feld ist wird z.Zt. nicht benötigt.
**Statistikfeld** | **Wohnort**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Daten 1 > Land<br/>Schüler > Daten 1 > Ort<br/>Schüler > Daten 1 > Gemeinde
Beschreibung      | Über die Felder Land, Ort und Gemeinde steuern Sie die Ausgabe des Wohnortes. Folgende Kombinationen sind möglich:<br/>Land = LEER und Ort = LEER: Ausgabe = `Übriges Ausland`<br/>Land einer von **D, DEU, 0, 000** und Gemeinde = LEER oder in NRW: Ausgabe = Ort<br/>Gemeinde <> NRW: Ausgabe = Bundesland, z.B. `Rheinland Pfalz`<br/>Land = **B**: Ausgabe = `Belgien`<br/>Land = **L**: Ausgabe = `Luxemburg`<br/> Land =  **NL**: Ausgabe = `Niederlande`
**Statistikfeld** | **Gebdat - Geburtsdatum**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geburtsdatum
Beschreibung      | Geben Sie das Geburtsdatum des Schülers ein.
**Statistikfeld** | **Geschlecht**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie das Geschlecht des Schülers aus. ***WICHTIG***: MAGELLAN 7 unterstützt das neue Geschlecht D = divers. Dieses wird durch die Statistik in diesem Jahr noch nicht offiziell unterstützt. In Absprache mit dem Statistikamt wird der zukünftige Schlüssel 5 ausgespielt und vom Amt nicht beanstandet, sollten sie das neue Geschlecht in MAGELLAN verwenden.
**Statistikfeld** | **Staatsang - Staatsangehörigkeit (Staatsangehörigkeiten)**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Staatsangeh. 1[Staatsangehörigkeiten]
Beschreibung      | Wählen Sie die Staatsangehörigkeit des Schülers aus. Wenn Sie keine Staatsangehörigkeit eingetragen haben, dann wird der Schüler automatisch mit dem Schlüssel der deutschen Staatsangehörigkeit ausgespielt.
**Statistikfeld** | **Religion - Religionszugehörikeit (Religionen)**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Konfession[Konfessionen]
Beschreibung      | Wählen Sie die Konfession des Schülers aus.
**Statistikfeld** | **Relianmeldung**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Rel.-Abmeldung bis
Beschreibung      | Die Anmeldung zum Religionsunterricht ergibt sich anhand des Bis-Datums der Abmeldung vom Religionsunterricht. Eine Anmeldung ist nur erforderlich, wenn es zuvor eine Abmeldung gegeben hat.
**Statistikfeld** | **Reliabmeldung**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Rel.-Abmeldung Von
Beschreibung      | Geben Sie im Vom-Feld die Abmeldung vom Religionsunterricht an.
**Statistikfeld** | **Aufnahmedatum**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > ZugangAm
Beschreibung      | Geben Sie das Zugangsdatum des Schülers an der Schule an.
**Statistikfeld** | **Labk**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Lehrer > Daten 1 > Kürzel<br/>Klassen > Zeiträume > Klassenleiter 1
Beschreibung      | Tragen Sie für jeden Lehrer der Schule das 4-Stellige Lehrerkürzel (Abkürzung des Lehrers in der LID) ein.<br/>Geben Sie für jede Klasse der Statistik den Klassenlehrer an.
**Statistikfeld** | **Ausbildort**
SF / ST           | Alle
Datenfeld         | -
Beschreibung      | Wird nicht erfasst, da es z.zt. nicht von der ASDPC-Schnittstelle statistisch ausgewertet wird<br/>Quelle: [Schnittstellenbeschreibung ASDPC](https://schulverwaltungsprogramme.msb.nrw.de/zbwschul.pdf)
**Statistikfeld** | **Betriebsort**
SF / ST           | BK, SB / Alle
Datenfeld         | MAGELLAN:<br/>Betriebe > Daten 1 > Ort<br/>Betriebe > Daten 1 > Land<br/>Betriebe > Daten 1 > Gemeinde<br/>Schüler > Ausbildung > Aktuelle Ausbildung (mit Ausbildungsbetrieb)
Beschreibung      | Der Schüler muss eine aktuelle Ausbildung eingetragen haben und einen Ausbildungsbetrieb. Diese Betrieb sollte die oben genannten Felder eingetragen haben. Lesen Sie dazu auch die Berechnung des Wohnortes beim Schüler. Die Berechnung der Ausgabe ist identisch.
**Statistikfeld** | **LSSchulform - Schulform der letzten Schule**
SF / ST           | Alle / NZG, NZS
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schule<br/>Zugang/Abgang > Bereits besuchte Schulen > Schulform[Schulformen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wird der Schüler als `Neuzugang` erkannt, dann wird die Schulform der Herkunftsschule ausgegeben.<br/>Wird der Schüler als `Neuzugang an gleicher Schule` erkannt, dann wird die Schulform des Mandanten ausgegeben.
**Statistikfeld** | **LSSchulnummer - Schulnummer der letzten Schule**
SF / ST           | Alle / NZG, NZS
Datenfeld         | MAGELLAN:<br/>Schulen > Daten > Schulnummer<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schule<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wird der Schüler als `Neuzugang` erkannt, dann wird die Schulnummer der Herkunftsschule ausgegeben.<br/>Wird der Schüler als `Neuzugang an gleicher Schule` erkannt, dann wird die Schulnummer des Mandanten ausgegeben.
Tragen Sie bei den Schulen die Herkunftsschulen der Schüler mit deren Schulnummer ein.<br/>Wählen Sie unter Bereits besuchte Schulen die Schule aus.<br/>ählen Sie unter Herkunftsschule die eingetragene Schule aus.
**Statistikfeld** | **LSGliederung - Schulgliederung der letzten Schulen**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang[Bildungsgänge]<br/>
Beschreibung      | Die mitgebrachte Schulgliederung tragen Sie über die dazugehörige Fachklasse über den Höchsten berufsbildenden Bildungsgang ein. Die Berechnung des Schlüssels erfolgt wie bei der Gliederung.
**Statistikfeld** | **LSFachklasse**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Bildungsgang [Bildungsgänge]
Beschreibung      | Die mitgebrachte Fachklasse tragen Sie über den Höchsten berufsbildenden Bildungsgang ein. Die Berechnung des Schlüssels erfolgt wie bei der Fachklasse.
**Statistikfeld** | **LSKlassenart**
SF / ST           | ABS / NZG, NZS
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > Bereits besuchte Schule > Herkunftsart [Herkunftsarten]
Beschreibung      | Tragen Sie die Art der Klasse an der letzten Schule, z.B. Regelklasse ein.
**Statistikfeld** | **LSReformpdg**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **LSSchulentl**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulbesuch bis<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Geben Sie für die Herkunfsschule den Schulbesuch bis an.
**Statistikfeld** | **LSJahrgang**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Letzte Klassenstufe [Klassenstufen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie für die Herkunfsschule die Letzte Klassenstufe aus.
**Statistikfeld** | **LSQual**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss [Abschlüsse (Extern)]
Beschreibung      | Grundsätzlich berechnet ASDPC den Höchsten allgemeinbildenden Abschluss aus dem Statistikfeld LSQual und Zeugnis, wobei LSQual eigentlich den letzten höchsten ABS Abschluss darstellt, z.B. aus einer anderen Schule. In MAGELLAN tragen Sie den höchsten Abschluss ABS nur an einer Stelle ein, auch wenn dieser an Ihrer eigenen Schule erworben wurde.
**Statistikfeld** | **LSVersetz**
SF / ST           | Alle / NZG
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen[ Herkunftsunterlagen]<br/>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung      | Wählen Sie für die Herkunftsschule als Versetzungsart die Unterlagen aus.
**Statistikfeld** | **VOklasse**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Daten > Statistikkürzel
Beschreibung      | Achten Sie bitte darauf, dass für alle aktuellen und auch die Vorjahresklassen ein Statistikkürzel unter `Klassen > Daten > Statistikkürzel` erfasst wurde.
**Statistikfeld** | **VOgliederung**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildungsgang [Bildgungsgänge]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld Gliederung den Bildungsgang ein.
**Statistikfeld** | VOfachklasse
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Aktuelle Ausbildung > Bildgungsgang [Bildungsgänge]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld Fachklasse den Bildungsgang ein.
**Statistikfeld** | **VOOrgForm**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Daten > Organisation [Organisationen]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld OrgForm die Organisation der Klasse ein.
**Statistikfeld** | **VOKlassenart**
SF / ST           | ABS / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Merkmale > Merkmal S3 [Verzeichnisse > Merkmale > Klassen]
Beschreibung      | Es wird die Klassenart der im Vorjahr besuchten Klasse ausgegeben. Bitte erfassen Sie pro Klasse die Klassenart.
**Statistikfeld** | **VOJahrgang**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN: Klassen > Zeiträume > Klassenstufe [Klassenstufen]
Beschreibung      | Wechseln Sie in den Vorjahreszeitraum und tragen Sie analog zum Statistikfeld AktJahrgang die Klassenstufe der Klasse ein.
**Statistikfeld** | **VOfoerderschwerp**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1[Förderschwerpunkte]<br/>Schueler > Daten 4 > Schwerpunkt1[Förderschwerpunkte]
Beschreibung      | Lesen Sie dazu das Statistikfeld "Foerderschwerp" und achten Sie darauf, dass der Eintrag eines evtl. auszugebenden Vorjahreswert mit den Von- und Bis-Daten des Vorjahreszeitraums übereinstimmt. Wenn sich die Schwerpunkte und weitere Eingaben nicht geändert haben, erweitern Sie den Zeitraum einfach entsprechend, dass der aktuelle und der Vorjahreszeitraum mit eingeschlossen wird oder Sie legen entsprechend getrennte Datensätze für die Zeiträume an.
**Statistikfeld** | **VOschwerstbeh**
SF / ST           | Alle / ABG, AKT, BAG
Datenfeld         | MAGELLAN:Schüler > Daten 4 > Förderbedarf[Förderbedarf]
Beschreibung      | Wählen Sie hier das Merkmal Schwerstbehinderung für den Vorjahreszeitraum beim Schüler aus. Lesen Sie dazu auch die Beschreibung zum Feld "Vofoerderschwerp".
**Statistikfeld** | VOReformpdg
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **Entldatum - Datum der Entlassung**
SF / ST           | Alle / ABG
Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > Abgang am
Beschreibung      | Geben Sie das Abgangsdatum des Schülers ein, wenn es sich um einen Abgänger handelt.
**Statistikfeld** | **Zeugnis**
SF / ST           | Alle / ABG
Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Abschluss > Abschluss 1[Abschlüsse (Intern)]<br/>Schüler > Zugang/Abgang > Abgang
Beschreibung      | Wählen Sie für Abgänger den Abschluss bzw. die Abgangsart des Schülers aus. Je nach schulischem Alltag, können Sie die Werte unter Abschlüsse oder Abgang erfassen. Es wird vorrangig der Abschluss gesetzt. Wenn dieser nicht eingetragen ist, wird der Abgang für die Statistik erfasst.
**Statistikfeld** | **Schulpflichterf - Erfüllung der Vollzeitschulpflicht**
SF / ST           | ABS / Alle
Datenfeld         | MAGELLAN: Schüler  > Zeugnis > Details > Schulbesuchsjahr
Beschreibung      | Ist das Schulbesuchsjahr > 9 dann wird der Schüler mit dem Merkmal `Vollzeitschulpflicht erfüllt` ausgegeben.
**Statistikfeld** | **Schulwechselform**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird nicht erfasst.
**Statistikfeld** | **Versetzung**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Allgemein > Versetzungsart [Versetzungsarten]
Beschreibung      | Wählen Sie die Art der Versetzung des Schülers im letzten Schuljahr aus.
**Statistikfeld** | **JahrZuzug**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „zugezogen“ ausgewertet wird.
**Statistikfeld** | **JahrEinschulung**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „zugezogen“ ausgewertet wird.
**Statistikfeld** | **JahrWechselSekI**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „zugezogen“ ausgewertet wird.
**Statistikfeld** | **zugezogen**
SF / ST           | Alle 
Datenfeld         | MAGELLAN:<br/>Schüler > Daten 1 > Geburtsland [Staatsangehörigkeiten]<br/>Schüler > Daten 2 > In Deutschland seit
Beschreibung      | Der Schüler gilt als zugezogen, wenn das Feld „Geburtsland“ nicht einer der Werte D, DE, DEU, 0  oder 000 für Deutschland eingetragen hat; oder das Feld „In Deutschland seit“ ein Zuzugsdatum nach Deutschland enthält.
**Statistikfeld** | **GeburtslandMutter**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „Elternteilzugezogen“ ausgewertet wird.
**Statistikfeld** | **GeburtslandVater**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Wird lt. Statistik nicht benötigt, wenn das Statistikfeld „Elternteilzugezogen“ ausgewertet wird.
**Statistikfeld** | **Elternteilzugezogen**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > NdH
Beschreibung      | Es ist zwar möglich bei den Sorgeberechtigten das Geburtsland anzugeben, der Einfachheit halber, lesen wir das NdH-Feld in MAGELLAN aus. Markieren Sie das Feld „NdH“, wenn mindestens ein Elternteil nach Deutschland zugezogen ist.
**Statistikfeld** | **Verkehrssprache**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Verkehrssprache
Beschreibung      | Geben Sie hier einen Wert ein, wenn in der Familie überwiegend nicht Deutsch gesprochen wird. Anderenfalls können Sie das Feld leer lassen. Für die aktuelle Erhebung ist es ausreichend, einen Wert verschieden zu 000 zu verwenden, um darzustellen, das die Verkehrssprache in der Familie nicht Deutsch ist.
**Statistikfeld** | **Einschulungsart**
SF / ST           | G / Alle
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S1 [Merkmale]
Beschreibung      | Wählen Sie hier die Einschulungsart des Schülers aus.
**Statistikfeld** | **Grundschulempfehlung**
SF / ST           | GE, GY / Alle
Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Zugang > Empfehlung [Empfehlungen (Bewerbung)]
Beschreibung      | Geben Sie hier die Empfehlung der Primarschulen an.
**Statistikfeld** | Massnahmentraeger
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S2 [Merkmale]
Beschreibung      | Wählen Sie aus, ob der Schüler von einem Ausbildungsbetrieb oder einem Träger ausgebildet wird.
**Statistikfeld** | **Betreuung**
SF / ST           | G, GY, GE / Alle
Datenfeld         | MAGELLAN: Schüler > Extras > Betreuungsarten > Innerschulisch 1 [Betreuungen innerschulisch (Schüler)]
Beschreibung      | Wählen Sie die Betreuungsmaßnahme der Nachmittags/Ganztagsbetreuung aus.
**Statistikfeld** | **BKAZVO**
SF / ST           | BK, SB / NZG
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal T1
Beschreibung      | Geben Sie die Anzahl der anzurechnenden Monate bei verkürzter Ausbildung an. Möglich sind 0, 6, 12 oder 18 Monate.
**Statistikfeld** | **Foerderschwerp2**
SF / ST           | Alle
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br>>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten
Beschreibung      | Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse geprüft. Lesen Sie dazu auch die Beschreibung zum Feld "Foerderschwerp".
**Statistikfeld** | **VOfoerderschwerp2**
SF / ST           | Alle / ABG, AKT, BAG, NZS
Datenfeld         | MAGELLAN:<br/>Klassen > Daten > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br/>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Schwerpunkt1 und Schwerpunkt2[Förderungen]<br>>Schueler > Daten 4 > Beinträchtigung und Fördermaßnahmen > Von und Bis-Daten
Beschreibung      | Wählen Sie den 2. Förderschwerpunkt zur Kombination mit dem 1. Förderschwerpunkt aus. Analog zum Förderschwerpunkt geben Sie den Wert bei der Klasse und abweichend beim Schüler an. Es wird Schüler vor Klasse geprüft. Lesen Sie dazu auch die Beschreibung zum Feld "Foerderschwerp".
**Statistikfeld** | **Berufsabschluss**
SF / ST           | BK, SB, WB / Alle
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S1 [Merkmale]
Beschreibung      | Wählen Sie aus, ob bereits eine abgeschlossene Berufsausbildung vorliegt.
**Statistikfeld** | **Produktname**
SF / ST           | Alle
Datenfeld         | -
Beschreibung      | Wir geben hier fest den Wert „MAGELLAN 7“ aus
**Statistikfeld** | **Produktversion**
SF / ST           | Alle
Datenfeld         | -
Beschreibung      | Wir geben hier die aktuell installierte MAGELLAN 7 Version (Registry Wert) aus.
**Statistikfeld** | **Adressenmerkmal**
SF / ST           | -
Datenfeld         | -
Beschreibung      | Die Adressenmerkmale für weitere Standorte erfassen Sie bitte direkt in ASDPC.
**Statistikfeld** | **Internat**
SF / ST           | Alle
Datenfeld         | MAGELLAN: Schüler > Daten 4 > Betreuung > Einrichtung
Beschreibung      | Wenn der Schüler einen Internatsplatz besetzt, wählen Sie bitte Internat aus der Auswahlliste aus.
