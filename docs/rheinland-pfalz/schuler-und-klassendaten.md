# Für Schüler und Klassendaten (ABS und BBS)



| Titel             | Inhalt                                   |
|-------------------|------------------------------------------|
| **Statistikfeld** | Pruefungen > AufnahmePruefung > **KlassenStufe** |
| Datenfeld         | MAGELLAN:Klasse > Zeiträume > Zeitraum > Klassenstufe <br />[Klassenstufen] |
| Beschreibung      | Prüfungen: Summen für Aufnahmeprüfungen AufnahmePrüfung:1..3 Nur für Klassenstufen 7, 10, 11; |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Pruefungen > AufnahmePruefung > SummeBestanden<br />Pruefungen > AufnahmePruefung > **SummeNichtBestanden** |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > Aufnahmeprüfung > Aufnahmeprüfung<br />[Aufnahmeprüfungen]<br /><br />Schüler > Laufbahn > Allgemein > Aufnahmeprüfung > Bestanden |
| Beschreibung      | Geben Sie im Feld „Aufnahmeprüfung“ an, ob der Schüler an einer Aufnahmeprüfung für den Eintritt in die <br/>nächste Klassenstufe teilgenommen hat. Markieren Sie im Feld „Bestanden“, ob der Schüler die <br/>Aufnahmeprüfung bestanden hat. <br/>Die Statistiksummen berechnen sich automatisch anhand Ihrer Angaben. |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > **KlassenBez**                      |
| Datenfeld         | MAGELLAN:Klassen > Daten > Statistikkürzel |
| Beschreibung      | Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. |
| Statistikdatei    | ABSBewegung <br /> ABSNeuanlage<br /> BBSBewegung <br />BBSNeuanlage |
| **Statistikfeld** | Klasse > **KlassenArt**                      |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal S2[Klassenmerkmale <br />(Bereich S2)] |
| Beschreibung      | Geben Sie hier die Klassenart ein.       |
| Statistikdatei    | ABSBewegung <br />ABSNeuanlage           |
| **Statistikfeld** | Klasse > **G8GTS**                           |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal B3 |
| Beschreibung      | Tragen Sie hier bitte ein Ja für eine G8-Klasse ein oder ein Nein wenn es sich nicht um eine G8-Klasse handelt. <br />Nur für Gymnasien! |
| Statistikdatei    | ABSNeuanlage<br />ABSBewegung            |
| **Statistikfeld** | Klasse > **Schulform**                       |
| Datenfeld         | MAGELLAN:Klassen > Daten > Schulform<br />[Schulformen] |
| Beschreibung      | Geben Sie hier die Schulform ein.        |
| Statistikdatei    | BBSBewegung <br />BBSNeuanlage           |
| **Statistikfeld** | Klasse > **OrgaForm**                        |
| Datenfeld         | MAGELLAN:Klassen > Daten > Organisation<br />[Organisationen] |
| Beschreibung      | Geben Sie hier die Organisationsform ein. |
| Statistikdatei    | BBSBewegung<br /> BBSNeuanlage           |
| **Statistikfeld** | Klasse > KlassenStufe <br /> Klasse > **SammelKlasse** |
| Datenfeld         | MAGELLAN:Klassen > Zeiträume > Zeitraum > Klassenstufe <br />[Klassenstufen]<br />Schüler > Statistik > Merkmal S6<br />[Schülermerkmale (Bereich S6)] |
| Beschreibung      | Geben Sie hier die Klassenstufe der Klasse ein.<br /><br />BBS: Bei Sammelklassen müssen Sie hier den Schlüssel „99“ Jahrgangssammelklasse eintragen. Sie müssen dann die Klassenstufe pro Schüler eintragen.<br /><br />ABS: Bei Kombiklassen wird automatisch der Schlüssel 99 in die Statistik eingetragen, egal was an dieser Stelle steht, vorausgesetzt Sie haben die Klassenart korrekt eingetragen. |
| Statistikdatei    | ABSNeuanlage <br /> BBSNeuanlage         |
| **Statistikfeld** | Klasse > **BerufsFeld**                      |
| Datenfeld         | MAGELLAN:Klassen > Daten > Berufsfeld[Berufsfelder] |
| Beschreibung      | Geben Sie hier das Berufsfeld ein. Für Berufsschulen Pflichtfeld! |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > **FachKlassenArt**                 |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal S2 |
| Beschreibung      | Geben Sie hier die Fachklassenart ein. Grundlage ist das Schlüsselverzeichnis „Klassenmerkmale“ (Bereich S2).Für Berufsschulen Pflichtfeld! |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > **BerufsKennZiffer**               |
| Datenfeld         | MAGELLAN:Klassen > Daten > Beruf <br/>[Berufe] |
| Beschreibung      | Geben Sie hier die Berufskennziffer ein. Für Berufsschulen Pflichtfeld! |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > **WochenStundenIst**               |
| Datenfeld         | DAVINCI:Stundenplan > Berechneter Wert[D2 – 3 SchuelerIst] |
| Beschreibung      | Das WochenStundenIst für die Schüler wird automatisch in DAVINCI anhand des gesetzten Plans gefüllten Veranstaltungsliste der Klasse berechnet.<br />Dieses Feld ist nur noch für BS einschl. BVJ Pflicht.<br /> <br />Achtung: Möchten Sie Veranstaltungen mit einer Dauer von 0 Stunden verplanen, geben Sie bitte für diese Stunden in der Spalte Bemerkung „/N“ an. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > **KlassenId** |
| Datenfeld         | MAGELLAN:Klassen > ID                    |
| Beschreibung      | Eindeutiger Bezeichner der Klasse aus MAGELLAN. Der Wert wird automatisch hinzugefügt. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > **Flexibilisierung** |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal B2 |
| Beschreibung      | Geben Sie hier die Flexibilisierung ein. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > **AusgelagerteFachpraxis** |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal B4 |
| Beschreibung      | Die "AusgelagerteFachpraxis" einer Klasse ist die Summe der Unterrichtsstunden, die - statt in der Schule - in einem Betrieb als Praktikum absolviert werden. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > **SollAenderungsGrund** |
| Datenfeld         | DAVINCI-Stundenplan:Stundentafel der Klasse |
| Beschreibung      | Der Soll-Änderungsgrund einer Klasse entspricht dem Eintrag in der Spalte „Bemerkung“ in der Stundentafel der Klasse. Es darf maximal einen Eintrag in der Spalte Bemerkung der Stundentafel der Klasse geben. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > Unterricht > **Fach** |
| Datenfeld         | DAVINCI:Stundentafel > Fach              |
| Beschreibung      | [D6 – 4 Fachschlüssel]<br/>Fachschlüssel aus der Stundentafel.Der Wert wird automatisch hinzugefügt. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > Unterricht > **Lehrer** |
| Datenfeld         | DAVINCI:Stundentafel > Lehrer            |
| Beschreibung      | [D6 – 2 LehrerID]<br/>	Eindeutiger Bezeichner des Lehrers aus der Stundentafel.Der Wert wird automatisch hinzugefügt. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > Unterricht > **StundentafelStunden**<br/>(zuvor Soll)</span> |
| Datenfeld         | DAVINCI:Stundentafel > Soll              |
| Beschreibung      | [D6 – 8 Soll]<br/>Sollstunden der Klasse in der Stundentafel. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > Unterricht > **AenderungsStunden** <br/>(zuvor SollAE) |
| Datenfeld         | DAVINCI: Stundenplan > Stundenplan > Stundenplan der Klasse > Stundentafel der Klasse > Angleichung |
| Beschreibung      | [D6 – 9 Soll2]	<br/>Solländerung (Differenz) in der Stundentafel. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | KlassenErgaenzungen > **AenderungsGrund**    |
| Datenfeld         | DAVINCI:Stundenplan > Stundenplan > Stundentafel der Klasse > Kategorie<br />Stundenplan > Stundenplan > Veranstaltung bearbeiten (STRG-Enter) > Kategorie |
| Beschreibung      | [D6 - 20 Veranstaltungskategorie (Veranstaltungskategorien)]<br/>Die Änderungsgründe sind veranstaltungs- und nicht mehr klassenbasiert einzutragen.<br /> <br />Wählen Sie dazu in der Veranstaltungskategorie (```Veranstaltungsliste > Rechtsklick auf die Veranstaltung > Veranstaltung bearbeiten > Kategorie```) den entsprechenden Schlüssel aus. <br /><br />Die Schlüssel (aus der Datei „25_RLP_Veranstaltungskategorien.keys“) können Sie unter ```Extras > Schlüsselverzeichnisse > Veranstaltungskategorien > Import``` in Ihre Plandatei importieren.<br />**Wichtig:** Bitte erfassen Sie die Werte in der Klassenstundentafel. Wenn Sie in den Klassenstundentafeln die Spalte Kategorie [Veranstaltungskategorie] gefüllt haben, wird der Wert geklammert in der Veranstaltungsliste eingeblendet. Wenn Sie die Fachkategorie im Nachhinein in der Veranstaltungsliste ändern wollen, müssen Sie die Änderung in der Stundentafel vornehmen. Die Kategorie wird dann in die Veranstaltungsliste synchronisiert. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > Unterricht > **IstStunden** <br/>(zuvor Ist) |
| Datenfeld         | DAVINCI:Stundenplan > Berechneter Wert   |
| Beschreibung      | [D6 - 11 LehrerIst]	<br/>Lehrer Ist-Stunden aus dem Stundenplan. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > KlassenErgaenzungen > Unterricht > **GekoppeltMit** |
| Datenfeld         | DAVINCI:Stundenplan > Berechneter Wert   |
| Beschreibung      | [D6 - 13 BlockNr]<br/>Ergibt sich aus den Blockungen im Stundenplan. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klassen > Orientierungsstufe > **SchulNrFiktiv** |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal B1 |
| Beschreibung      | Wenn es sich bei der Klasse um eine schulartübergreifende Orientierungsstufe handelt, müssen Sie hier die fiktive Schulnummer eintragen. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > Orientierungsstufe > **KlassenTyp** |
| Datenfeld         | MAGELLAN:Klassen > Merkmale > Merkmal S1<br />[Klassenmerkmale (Bereich S1)] |
| Beschreibung      | Wenn es sich bei der Klasse um eine schulartübergreifende Orientierungsstufe handelt, müssen Sie hier das entsprechende Kürzel auswählen. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > **Kurs**                           |
| Datenfeld         | DAVINCI:KursplanStundentafel der Klasse  |
| Beschreibung      | Kursdaten werden aus dem Kursplan erzeugt. Zusätzliche statistische Angaben müssen über eine Stundentafel pro Klasse erfasst werden.<br />Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > Kurs > **KursBez**                 |
| Datenfeld         | DAVINCI:Kursplan > Kurse > FachKuerzel <br/> [D6 - 3 Fachkürzel]<br/><br/>DAVINCI: [Fächer]Kursplan > Kurse > FachKursNr<br/>[D6 - 7 Fachkursnummer]<br /><br/>Kursplan > Kurse > FachUnterrichtsart<br/>[D6 - 5 Fachunterrichtsart]<br/><br/>MAGELLAN: [Unterrichtsarten]<br/>[D6 - 16 Beifach] |
| Beschreibung      | Jeder Schüler der Oberstufe muss im Kursplan zugeordnete Kurse besitzen. Aus den Angaben berechnet sich entsprechend die Kursbezeichnung. Kursnummern ergeben sich in DAVINCI beim Erstellen der Kurse.<br/>Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > Kurs > **KursArt**                 |
| Datenfeld         | MAGELLAN:Schueler > Zeugnis > Fächer > Unterrichtsart[Unterrichtsarten]<br /><br />DAVINCI: Kursplan > Kurse > FachstatusStundentafel > Bemerkung |
| Beschreibung      | Die Kursart „GK“ und „LK“ müssen in MAGELLAN und DAVINCI übereinstimmen. Beifächer werden im Kursplan den Fachstatus-Schlüssel „Beifach“ gekennzeichnet. <br /> Siehe auch manuelle Statistikkontrolle. <br />Nur Oberstufe!Bilingualer Unterricht und Schulübergreifender Unterricht werden im Feld Bemerkung eingetragen. <br /><br />Bitte tragen Sie entweder „biling“ oder die 5-stellige Schulnummer der unterrichtenden Schule wie im folgenden Beispiel ein. <br /><br />Beispiel 1: biling;SNR12345<br /> Beispiel 2: biling<br /> Beispiel 3: SNR12345 |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > Kurs > **Fach**                    |
| Datenfeld         | DAVINCI:Kursplan > Kurse                 |
| Beschreibung      | Die Fächer der Kurse in DAVINCI Kursplan müssen mit den Fächern der Schüler in der Oberstufe in MAGELLAN übereinstimmen. Siehe auch manuelle Statistikkontrolle. Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > Kurs > **KursNr**                  |
| Datenfeld         | DAVINCI: Kursplan > Automatik <br/>[D6 - 7 Fachkursnummer]<br/>Kursnummern ergeben sich in DAVINCI beim Erstellen der Kurse. Siehe auch manuelle Statistikkontrolle. <br/>Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klassen > Kurs > **WochenStundenIst**        |
| Datenfeld         | DAVINCI: Stundenplan > Berechneter Wert  |
| Beschreibung      | [D6 - 10 KlassenIst]<br />	Die Ist-Wochenstunden für Kurse ergeben sich aus dem erstellten Stundenplan für die Oberstufe. Bei schulübergreifendem Unterricht sind die Ist-Wochenstunden gleich 0. <br />(Eintrag siehe: KursArt)<br/> Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Kurs > **NeuEinsetzende5StdFS**     |
| Datenfeld         | DAVINCI:Kursplan > Kurse > Fachstatus<br/>[Fachstatus] |
| Beschreibung      | [D6 - 6 Fachstatus]	<br/>Geben Sie in DAVINCI für den Kurs den Fachstatus „NeuGK“ im Stundenplan der Klasse ein, um ihn als neu einsetzenden 5-stündigen Grundkurs auszuzeichnen.Dieser Fachstatus muss evtl. zu den bestehenden Fachstatus hinzugefügt werden. Klicken Sie auf Hinzufügen und vergeben Sie als Kürzel und Schlüssel „NeuGK“.<br />Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Kurs > schulÜbergreifend > **UnterrichtendeSchule** |
| Datenfeld         | DAVINCI:Stundentafel > Bemerkung         |
| Beschreibung      | Geben Sie in DAVINCI die Schulnummer der Fremdschule für den Kurs ein, wenn es sich um Schulübergreifenden Unterricht handelt. Bilingualer Unterricht und Schulübergreifender Unterricht werden im Feld Bemerkung eingetragen. <br />Bitte tragen Sie entweder „biling“ oder die 5-stellige Schulnummer der unterrichtenden Schule wie im folgenden Beispiel ein. <br /><br />Beispiel 1: biling;SNR12345<br />Beispiel 2: biling<br />Beispiel 3: SNR12345<br /><br />Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Kurs > AufgestockterGrundkurs > **AnzahlGemeinsamerStd** |
| Datenfeld         | DAVINCI:Kursplan > Kurse > Fachstatus<br/>[Fachstatus] |
| Beschreibung      | [D6 – 6 Fachstatus]	<br />Der 5stündige Leistungskurs muss aufgeteilt (dupliziert) werden. Drei Stunden des Leistungskurses werden als 3stündiger Grundkurs mit den 2 Stunden Leistungskurs geblockt. <br />Der 2stündige Leistungskurs muss als „AufgestGK“ im Fachstatus gekennzeichnet werden. <br />(Zu Ihrer Information können Sie auch den GK als „AufgestGK“ markieren. Dies hat jedoch keine Auswirkungen auf die Statistik.)<br />Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Kurs > **JahrgangsUebergreifend**   |
| Datenfeld         | DAVINCI: Kursplan                        |
| Beschreibung      | Dieser Wert wird automatisch in DAVINCI berechnet und entsprechend für die Statistik eingetragen.<br/> Nur Oberstufe! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **Name**                 |
| Datenfeld         | MAGELLAN: Schüler > Daten 1 > Nachname   |
| Beschreibung      | Geben Sie hier den Nachnamen ein.        |
| Statistikdatei    | ABSBewegung <br/>ABSNeuanlage            |
| **Statistikfeld** | Klasse > Schueler > **Vorname**              |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Vorname     |
| Beschreibung      | Geben Sie hier den Vornamen ein.         |
| Statistikdatei    | ABSBewegung<br />ABSNeuanlage            |
| **Statistikfeld** | Klasse > Schueler > **KlassenStufe**         |
| Datenfeld         | MAGELLAN:Klasse > Zeiträume > Zeitraum > Klassenstufe<br />[Klassenstufen]<br /><br />Schüler > Statistik > Merkmal S6<br />[Schülermerkmale (Bereich S6)] |
| Beschreibung      | Tragen Sie die Klassenstufe grundsätzlich im Feld „Klassenstufe“ ein. Bei Kombiklassen wird die Klassenstufe des Schülers zusätzlich im Feld „Merkmal S6“ des Schülers eingetragen. Tragen sie im Schülermerkmal nichts ein, wird automatisch der Wert des Feldes „Klassenstufe“ für die Statistik eingetragen. |
| Statistikdatei    | ABSBewegung<br /> ABSNeuanlage<br /> BBSBewegung <br />BBSNeuanlage |
| **Statistikfeld** | Klasse > Schueler > **Geschlecht**           |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Geschlecht  |
| Beschreibung      | Geben Sie hier das Geschlecht ein.       |
| Statistikdatei    | ABSBewegung <br/>ABSNeuanlage <br/>BBSBewegung <br/>BBSNeuanlage |
| **Statistikfeld** | Klasse > Schueler > **GeburtsDatum**         |
| Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geboren am |
| Beschreibung      | Geben Sie hier das Geburtsdatum des Schülers ein. |
| Statistikdatei    | ABSBewegung <br/>ABSNeuanlage<br/> BBSBewegung <br/>BBSNeuanlage |
| **Statistikfeld** | Klasse > Schueler > **Nationalitaet**        |
| Datenfeld         | MAGELLAN:Schüler > Daten 2 > Staatsangeh. 1<br/>[Staatsangehörigkeiten] |
| Beschreibung      | Geben Sie hier die Nationalität ein.     |
| Statistikdatei    | ABSBewegung <br/> ABSNeuanlage BBSBewegung <br/>BBSNeuanlage |
| **Statistikfeld** | Klasse > Schueler > **YBildungsGang**        |
| Datenfeld         | MAGELLAN:Schüler > Ausbildung > Bildungsgang |
| Beschreibung      | <br/>[Bildungsgänge]<br/>Geben Sie hier den Bildungsgang des Schülers ein, falls er vom Bildungsgang der Klasse abweicht. |
| Statistikdatei    | BBSNeuanlage<br/>BBSBewegung             |
| **Statistikfeld** | Klasse > Schueler > **AbschlussArt**         |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > Abschluss 1[Abschlüsse (Intern)] |
| Beschreibung      | Geben Sie hier die Abschlussart des Schülers ein. <br/><br/> BBS: Schüler ohne Eintrag in diesem Feld werden nicht in die Bewegungsdatei übergeben. |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **NachPruefung**         |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > NachPruefung [Nachprüfungen] |
| Beschreibung      | Wählen Sie hier „Bestanden“ oder „Nicht bestanden“ aus, wenn der Schüler an einer Nachprüfung teilgenommen hat. <br/>Es reicht aus einen Wert im Feld „Nachprüfung“ auszuwählen, der Haken bei „Bestanden“ hat keine Wirkung. |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **NichtVersetzt**        |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > Versetzungsart[Versetzungsarten] |
| Beschreibung      | Geben Sie hier die Versetzungsart ein    |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **Uebergang**            |
| Datenfeld         | MAGELLAN: Schüler > Zugang/Abgang > Abgang > Übergang[Übergangsarten] |
| Beschreibung      | Geben Sie hier die Übergangsart für den Schüler von der Klassenstufe 4 an. Dieses Feld ist nur für den Übergang der Schüler nach Klassenstufe 4 auszufüllen. Es betrifft nur Grundschulen und verbundene Grund- und Hauptschulen. |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **LaufbahnEmpfehlung**   |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Empfehlung[Empfehlungen] |
| Beschreibung      | Geben Sie hier die Empfehlung der Schule zum Übergang nach Klassenstufe 4 ein.Dieses Feld ist nur für den Übergang der Schüler nach Klassenstufe 4 auszufüllen. Es betrifft nur Grundschulen und verbundene Grund- und Hauptschulen. |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **UEOSVerbleib**         |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > Entscheidung[Entscheidungen] |
| Beschreibung      | Im zweiten Halbjahr wird im Feld „Entscheidung“ der Verbleib aus der Übergeordneten Orientierungs-Stufe angegeben. Nur von federführender Schule in Klassenstufe 6 anzugeben! |
| Statistikdatei    | ABSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **EntlassungsArt**       |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Abschluss > Abschluss 1[Abschlüsse (Intern)] |
| Beschreibung      | Geben Sie hier den erreichten Abschluss ein (Abschlusszeugnis usw.). |
| Statistikdatei    | BBSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > **ZweitAbschluss**       |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Abschluss > Abschluss 2[Abschlüsse (Intern)] |
| Beschreibung      | Geben Sie hier einen zusätzlich erworbenen Abschluss ein. |
| Statistikdatei    | BBSBewegung                              |
| **Statistikfeld** | Klasse > Schueler > Abitur > **AbiturErfolg** |
| Datenfeld         | MAGELLAN:Schüler > Abschluss > Abschluss 1 > Abschlussart[Abschlussarten] |
| Beschreibung      | Geben Sie hier bei Abiturienten die Abschlussart ein (Bestanden, nicht Bestanden). |
| Statistikdatei    | ABSBewegung <br/>BBSBewegung             |
| **Statistikfeld** | Klasse > Schueler > Abitur > **AbiturNote**  |
| Datenfeld         | MAGELLAN:Schüler > Abschluss > bschluss 1 > Abschlussnote |
| Beschreibung      | Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. <br/>Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist. |
| Statistikdatei    | ABSBewegung<br/>BBSBewegung              |
| **Statistikfeld** | Klasse > Schueler > **WohnortRLP**           |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Gemeinde    |
| Beschreibung      | Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein. Der Statistikwert wird automatisch daraus errechnet. |
| Statistikdatei    | ABSNeuanlage<br/> BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > **WohnBundesland**       |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Gemeinde    |
| Beschreibung      | Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein. Der Statistikwert wird automatisch daraus errechnet. |
| Statistikdatei    | ABSNeuanlage <br/>BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > **WohnStaat**            |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Land        |
| Beschreibung      | Geben Sie im Feld „Land“ (das Feld vor PLZ), das Kürzel für den Wohnstaat sein. Ein Statistikwert wird eingetragen, wenn der Schüler in Frankreich (F), Belgien (B) oder Luxemburg (L) wohnt. |
| Statistikdatei    | ABSNeuanlage<br/> BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > **Ortsteil**             |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Ortsteil    |
| Beschreibung      | Gebn Sie hier den Ortsteil ein, indem der Schüler wohnt. <br/>Kann-Feld: Wird nicht statistisch ausgewertet und gilt nur als Untergliederung zum „WohnortRLP“. |
| Statistikdatei    | ABSNeuanlage<br/> BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > **Religion**             |
| Datenfeld         | MAGELLAN:Schüler > Daten 1 > Konfession[Konfessionen] |
| Beschreibung      | Geben Sie hier die Konfession des Schülers ein. Nicht benötigt für Schulkindergarten und Kollegs, ansonsten Pflichtfeld! |
| Statistikdatei    | ABSNeuanlage <br/>BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > **TeilnahmeReligion**    |
| Datenfeld         | MAGELLAN: Schüler > Daten 1 > Rel.-Teilnahme[Religion (Teilnahmen)] |
| Beschreibung      | Geben Sie hier die Teilnahme am Religionsunterricht ein. Nicht benötigt für Schulkindergarten und Kollegs, ansonsten Pflichtfeld! |
| Statistikdatei    | ABSNeuanlage <br/> BBSNeuanlage          |
| **Statistikfeld** | Klasse > Schueler > **SchuelerTyp**          |
| Datenfeld         | MAGELLAN:<br/>Schüler > Laufbahn > Allgemein > WiederholerSchüler > Laufbahn > Allgemein > Wiederholungsart<br/>Schüler > Laufbahn > Allgemein > ÜberspringerSchüler > Laufbahn > Allgemein > Wiederholungsart <br/>[Wiederholungsarten] |
| Beschreibung      | Je nachdem, ob es sich um einen Wiederholer oder Überspringer handelt haken Sie das Feld „Wiederholer“ oder „Überspringer“ an. <br/>Bei einem Wiederholer oder Überspringer geben Sie bitte im Feld „Wiederholer“ die Wiederholungs- oder Überspringungsart an. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **NeuZugang**            |
| Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Herkunftsart<br/>[Herkunftsarten]<br/>Schüler > Zugang/Abgang > Herkunftsschule <br/>Schüler > Zugang/Abgang > Zugang am |
| Beschreibung      | Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. Beachten Sie bitte, dass die „Herkunftsart“ eingetragen sein muss. Das Feld „Zugang am“ muss gefüllt sein, damit der Schüler als Neuzugang erkannt wird. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **GanztagsSchueler**     |
| Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S5 [Schülermerkmale (Bereich S5)] |
| Beschreibung      | Geben Sie für den Ganztagsschüler die Betreuungsform ein. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **BetreuendeGrundschule** |
| Datenfeld         | MAGELLAN: <br/>Schüler > Statistik > Merkmal T1 <br/>Voraussetzungen:<br/>Klassen > Merkmal S2[Klassenmerkmale (Bereich S2)]<br/>Klassen > Daten 1 > Schulart[Schularten] |
| Beschreibung      | Nur von der betreuenden Grundschule anzugeben! <br/>Geben Sie hier ein „J“ ein, wenn der Schüler das Angebot der betreuenden Grundschule in Anspruch nimmt. <br/> Voraussetzungen:<br/>Klasse ist keine „Gruppe im Schul- oder Förderschulkindergarten“ <br/>Nur für Grundschulen |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **EinschulungsJahr**     |
| Datenfeld         | MAGELLAN: Schüler > Daten 2 > Grundschuleintritt > Grundschuleintritt |
| Beschreibung      | Geben Sie hier an, wann der Schüler zum ersten Mal eingeschult wurde, auch, wenn evtl. nochmalige Rückstellung erfolgte.<br/>Aus diesem Wert wird automatisch das ABS2BBS (LMZ Projekt) gebildet.<br/>Nicht für Schulkindergärten! Ansonsten Pflicht! |
| Statistikdatei    | ABSNeuanlage<br/>ABSBewegung             |
| **Statistikfeld** | Klasse > Schueler > MigrationsHintergrund > Herkunft > **GeburtsStaat** |
| Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geburtsland [Staatsangehörigkeiten] |
| Beschreibung      | Geben Sie hier an, in welchem Land der Schüler geboren ist.<br/>Nur Pflicht, wenn Schüler im Ausland geboren! |
| Statistikdatei    | ABSNeuanlage<br/> BBSNeuanlage<br/> ABSBewegung<br/> BBSBewegung |
| **Statistikfeld** | Klasse > Schueler > MigrationsHintergrund > Herkunft > **ZuzugsJahr** |
| Datenfeld         | MAGELLAN: Schüler > Daten 2 > In Deutschland seit |
| Beschreibung      | Geben Sie hier an, seit wann der Schüler in Deutschland lebt. |
| Statistikdatei    | ABSNeuanlage <br/>BBSNeuanlage<br/>ABSBewegung <br/>BBSBewegung |
| **Statistikfeld** | Klasse > Schueler > MigrationsHintergrund > **FamilienSprache** |
| Datenfeld         | MAGELLAN: Schüler > Daten 2 > Sprachgruppe [Sprachgruppen] |
| Beschreibung      | Geben Sie hier an, welche Sprache überwiegend im häuslichen Umfeld des Schülers gesprochen wird (soweit sie nicht Deutsch ist). |
| Statistikdatei    | ABSNeuanlage <br/>BBSNeuanlage<br/>ABSBewegung<br/>BBSBewegung |
| **Statistikfeld** | Klasse > Schueler > MigrationsHintergrund > **Foerderbedarf** [Sprache] |
| Datenfeld         | MAGELLAN: <br/>Schüler > Statistik > Merkmal S1 <br/>Schüler > Statistik > Merkmal S2 |
| Beschreibung      | Geben Sie hier den sprachlichen Förderbedarf an. |
| Statistikdatei    | ABSNeuanlage <br/>BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > **MuttersprachlUnterricht** |
| Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S3[Schülermerkmale“ (Bereich S3] |
| Beschreibung      | Geben Sie hier an, ob der Schüler mit nichtdeutscher Familiensprache "muttersprachlichen" Unterricht erhält. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **FoerderSchwerpunkt**   |
| Datenfeld         | MAGELLAN: Schüler > Daten 4 >  Finanzielle Förderung > Förderung[Förderungen] |
| Beschreibung      | Geben Sie hier an, welchen Förderschwerpunkt dem Schüler zugewiesen wurde. <br/>Pflicht für Förderschulen und Schulen mit integrierter Förderung! |
| Statistikdatei    | ABSNeuanlage <br/>ABSBewegung            |
| **Statistikfeld** | Klasse > Schueler > **BildungsZiel**         |
| Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S4 [Schülermerkmale“ (Bereich S4] |
| Beschreibung      | Geben Sie hier das Bildungsziel des Förderschülers an. <br/>Nur für Förderschulen und Schulen mit integrierter Förderung! |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > FremdSprachen > FremdSprache > **Sprache** |
| Datenfeld         | MAGELLAN: Schüler > Daten 3 > 1. - 4. Fremdsprache[Fächer] mit Eintrag „Fremdsprache“ im Feld „Kategorie“ |
| Beschreibung      | Geben Sie hier die Fremdsprachen des Schülers ein. Sie können bis zu vier Fremdsprachen zuweisen. <br/><br/>Info für allgemeinbildende Schulen: <br/><b>Bitte beachten Sie den Abschnitt "ABS: Wann wird die 2. Fremdsprache ausgegeben?" im oberen Teil der Dokumentation!</b> |
| Statistikdatei    | ABSNeuanlage <br/>BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > FremdSprachen > FremdSprache > **StatusFach** |
| Datenfeld         | MAGELLAN: Schüler > Daten3 > Zusatz<br/>Sammelzuweisung:Schüler > Bearbeiten > Sammelzuweisung |
| Beschreibung      | Geben Sie für die Fremdsprache im Feld „Zusatz“ den Fremdsprachenstatus an. <br/>Folgende Werte stehen zur Auswahl: <br/>Pflicht-/Wahlpflichtfach<br/>Wahlfach (fakultative FS)<br/>Arbeitsgemeinschaft<br/>Förderunterricht<br/>Pflichtfach<br/>Wahlpflichfach |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > FremSprachen > FremdSprache > **StatusErteil** |
| Datenfeld         | MAGELLAN:Schüler > Daten 3 > Status      |
| Beschreibung      | Geben Sie hier den Status der jeweiligen Fremdsprache an. <br/>Die Angabe ist nur erforderlich, wenn er vom Status „Unterrichtserteilung an der berichtenden Schule“ abweicht. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > FremdSprachen > FremdSprache > **Folge** |
| Datenfeld         | MAGELLAN: Schüler > Daten 3 > Fremdsprachenfolge |
| Beschreibung      | Durch die Eingabe der Fremdsprachen 1-4 ergibt sich die Folge. Diese wird dann entsprechend in die Statistik eingetragen. |
| Statistikdatei    | ABSNeuanlage<br/> BBSNeuanlage           |
| **Statistikfeld** | Klasse > Schueler > MSS > LeistungsKurs > KursBez<br/>Klasse > Schueler > MSS > GrundKurs > **KursBez** |
| Datenfeld         | MAGELLAN:<br/>Schüler > Zeugnis > Fächer > Fach<br/>Schüler > Zeugnis > Fächer > Kurs<br/>Schüler > Zeugnis > Fächer > Unterrichtsart<br/><br/>DAVINCI:<br/>Kursplan |
| Beschreibung      | Aus den Angaben berechnet sich entsprechend die Kursbezeichnung. <br/>Beachten Sie, dass diese Daten ursprünglich durch den Datenabgleich aus DAVINCI Kursplan nach MAGELLAN kommen. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > MSS > GrundKurs > **Freiwillig** |
| Datenfeld         | MAGELLAN:Schüler > Zeugnis > Fächer > Fachstatus[Fachstati] |
| Beschreibung      | Geben Sie hier den Schlüssel „Freiw“an, wenn der Schüler den Kurs freiwillig belegt hat. |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > AusbildungsBeruf     |
| Datenfeld         | MAGELLAN:Schüler > Ausbildung > BerufKlassen > Daten 1 > **Beruf**[Berufe] |
| Beschreibung      | Geben Sie hier den Ausbildungsberuf des Schülers ein, falls er vom eingetragenen Beruf der Klasse abweicht.<br/>Pflicht für Berufsschulen! |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **Wiederholer**          |
| Datenfeld         | MAGELLAN:Schüler > Laufbahn > Allgemein > Wiederholungsart[Wiederholungsarten] |
| Beschreibung      | Geben Sie hier an, ob der Schüler im 1. Schulhalbjahr Wiederholer ist oder nicht. <br/>Keine Angabe bedeutet, dass der Schüler kein Wiederholer ist.<br/>Nicht für Berufsschüler! |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **FHRUnterricht**        |
| Datenfeld         | MAGELLAN:Schüler > Statistik > Merkmal T1 |
| Beschreibung      | Geben Sie hier einen der folgenden Werte für die entsprechende zusätzliche Stundenanzahl am Ergänzungsunterricht zum Erwerb der Fachhochschulreife ein, wenn der Schüler daran teilnimmt.<br/>1 = 280 Stunden<br/>2 = 460 Stunden<br/>3 = 600 Stunden<br/>Stundenanzahl ist statistische Vorgabe. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **NeuZugang**<br/>FÜR ABS FÜR FÖRDERSCHULEN |
| Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Zugang am <br/>Schüler > Zugang/Abgang > Klassenstufe |
| Beschreibung      | Regeln, damit der Schüler als Neuzugang erkannt wird:<br/><br/>Zugangsdatum (Zugang am) liegt nach dem letzten Statistiktermin und * Zugangsdatum liegt vor oder gleich auf dem aktuellen Statistikerhebungsdatum <br/><br/>oder<br/><br/>Schüler der Klassenstufe 7, wenn sie in der Klassenstufe 6 einer schulartübergreifenden Orientierungsstufe (UEOS) unterrichtet wurden <br/><br/> oder<br/><br/>Zugang aus einer Förderschule ohne Schwerpunkt <br/><br/>oder<br/><br/> Einschulung nur für Schule SFG (Förderschwerpunkt ganzheitliche Entwicklung): <br/>Einschulung in diese Klasse<br/><br/>oder <br/> <br/>Nur Förderschulen (60): <br/>Beim Zugang aus einer anderen Förderschule. <br/>Mögliche Schwerpunktschulen können sein:<br/>Förderschwerpunkt Lernen<br/>Förderschwerpunkt ganzheitliche Entwicklung<br/>Förderschwerpunkt motorische Entwicklung<br/>Förderschwerpunkt sozial-emotionale Entwicklung<br/>Blinde und Sehbehinderte<br/>Gehörlose und Schwerhörige<br/>Förderschwerpunkt Sprache |
| Statistikdatei    | ABSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > **NeuZugang** <br/>FÜR BBS |
| Datenfeld         | Regeln, damit der Schüler als Neuzugang erkannt wird: <br/> Am Alle Schüler, deren Zugangsdatum nach dem letzten Statistiktermin liegt, werden als Neuzugang markiert. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > NeuZugang > **SchulForm** |
| Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/ Abgang > Bereits besuchte Schulen > Schulform[Schulformen (Herkunft)]<br/>Schüler > Zugang/Abgang > Herkunftsschule |
| Beschreibung      | Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.<br/>Beachten Sie bitte, dass die „Schulform“ eingetragen sein muss. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > NeuZugang > **KlassenStufe** |
| Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Letzte Klassenstufe[Klassenstufen]<br/>Schüler > Zugang/Abgang > Herkunftsschule |
| Beschreibung      | Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.Beachten Sie bitte, dass im Feld „Letzte Klassenstufe“ die Klassenstufe eingetragen sein muss. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > NeuZugang > **EintrittBildungsgang** |
| Datenfeld         | MAGELLAN:<br/>Schüler > Zugang/Abgang > Zugang am<br/>Schüler > Laufbahn > Schulformeintritt<br/>Schüler > Ausbildung > Ausbildung von |
| Beschreibung      | Geben Sie mind. eines der drei möglichen Felder an. Wenn Sie mehrere Datumsangaben eingetragen haben, wird automatisch das höchste Datum als Eintritt für den Bildungsgang verwendet. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > Vorbildung > **SchulischerAbschlussABS** |
| Datenfeld         | MAGELLAN:<br/>Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss<br/>[Abschlüsse (Extern)] |
| Beschreibung      | Geben Sie hier den höchsten erreichten Abschluss an einer ABS ein. |
| Statistikdatei    | BBSNeuanlage                             |
| **Statistikfeld** | Klasse > Schueler > Vorbildung > **BerufsbezAbschlussBBS** |
| Datenfeld         | MAGELLAN:<br/>Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss<br/>[Abschlüsse (Extern)] |
| Beschreibung      | Geben Sie hier den höchsten erreichten berufsbezogenen Abschluss, der ohne den Erwerb eines weiteren allgemeinen Abschlusses erreicht wurde, z.B. Lehrabschluss. |
| Statistikdatei    | BBSNeuanlage                             |

