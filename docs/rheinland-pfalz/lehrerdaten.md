# Für Lehrerdaten (nur BBS)

!!! warning "Wichtig"

    Lehrer, die nach dem letzten Statistiktermin an Ihre Schule wechselten und vor dem aktuellen Statistiktermin Ihre Schule verlassen haben, werden statistisch nicht an Ihrer Schule ausgewertet, sollen also nicht in Ihrer LehrerNeuanlage.xml erscheinen. Sie werden statistisch an der Herkunftschule als Abgang und an der neuen Schule als Zugang geführt.

| Feld              | Eingabe                                  |
|-------------------|------------------------------------------|
| **Statistikfeld** | Name                                     |
| Eingabe           | Magellan:Lehrer > Daten 1 > Nachname     |
| Beschreibung      | Geben Sie hier den Nachnamen ein.        |
| **Statistikfeld** | Vorname                                  |
| Eingabe           | Magellan:Lehrer > Daten 1 > Vorname      |
| Beschreibung      | Geben Sie hier den Vornamen ein.         |
| **Statistikfeld** | Amtsbezeichnung                          |
| Eingabe           | Magellan:Lehrer > Daten 1 > Amtsbez.     |
| Beschreibung      | Geben Sie hier die Amtsbezeichnung ein. Grundlage ist das Schlüsselverzeichnis „Amtsbezeichnungen“. |
| **Statistikfeld** | Funktion                                 |
| Eingabe           | Magellan:<br/>Mandanten > Daten 1 > Schulleiter<br/>Mandanten > Daten 1 > Stellvertreter |
| Beschreibung      | Geben Sie ein, welcher Lehrer die Funktion des Schulleiters und Stellvertreters Ihrer Schule hat. |
| **Statistikfeld** | KlassenLeitung                           |
| Eingabe           | Magellan:Klassen > Zeiträume > Klassenleiter 1 |
| Beschreibung      | Geben Sie hier den Klassenleiter der Klasse ein.<br/>Nur ABS! |
| **Statistikfeld** | Geschlecht                               |
| Eingabe           | Magellan:Lehrer > Daten 1 > Geschlecht   |
| Beschreibung      | Geben Sie hier das Geschlecht ein.       |
| **Statistikfeld** | GeburtsDatum                             |
| Eingabe           | Magellan:Lehrer > Daten 1 > Geboren am   |
| Beschreibung      | Geben Sie hier das Geburtsdatum ein.     |
| **Statistikfeld** | Nationalitaet                            |
| Eingabe           | Magellan:Lehrer > Daten 1 > Staatsangeh. |
| Beschreibung      | Geben Sie hier die Staatsangehörigkeit ein.Grundlage ist das Schlüsselverzeichnis „Staatsangehörigkeiten“. |
| **Statistikfeld** | DienstVerhaeltnis                        |
| Eingabe           | Magellan:Lehrer > Daten 2 > Dienstverh.  |
| Beschreibung      | Geben Sie hier das Dienstverhältnis ein.Grundlage ist das Schlüsselverzeichnis „Dienstverhältnisse“. |
| **Statistikfeld** | BeschVerhaeltnis                         |
| Eingabe           | Magellan:Lehrer > Daten 2 > Besch-verh.  |
| Beschreibung      | Geben Sie hier das Beschäftigungsverhältnis ein.Grundlage ist das Schlüsselverzeichnis „Beschäftigungsverhältnisse“ |
| **Statistikfeld** | DienstHerr                               |
| Eingabe           | Magellan:Lehrer > Daten 2 > Dienstherr   |
| Beschreibung      | Geben Sie hier den Träger ein.Nur von in privater Trägerschaft anzugeben! |
| **Statistikfeld** | Zugang > ZugangsGrund                    |
| Eingabe           | Magellan:Lehrer > Daten 2 > Zugangsart   |
| Beschreibung      | Geben Sie hier den Zugangsgrund ein.Grundlage ist das Schlüsselverzeichnis „Zugangsarten“. |
| **Statistikfeld** | Zugang > ZugangsDatum                    |
| Eingabe           | Magellan:Lehrer > Daten 2 > Zugang am    |
| Beschreibung      | Geben Sie hier das Zugangsdatum ein.Datum muss nach dem Stichtag der letzten Erhebung liegen:<br/> Wird berechnet! |
| **Statistikfeld** | Abgang > AbgangsGrund                    |
| Eingabe           | Magellan:Lehrer > Daten 2 > Abgangsart   |
| Beschreibung      | Geben Sie hier den Abgangsgrund ein.Grundlage ist das Schlüsselverzeichnis „Abgangsarten“. |
| **Statistikfeld** | Abgang > AbgangsDatum                    |
| Eingabe           | Magellan:Lehrer > Daten 2 > Abgang am    |
| Beschreibung      | Geben Sie hier das Abgangsdatum ein.Datum muss nach dem Stichtag der letzten Erhebung liegen:<br/> Wird berechnet! |
| **Statistikfeld** | RegelStunden                             |
| Eingabe           | DaVinci:<br/>Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]<br/>Stammdaten > Lehrer > Zeitkonto > Stunden |
| Beschreibung      | Geben Sie die Regelstunden für jeden Lehrer in seiner Soll-Berechnung in den Stammdaten an.<br/>Kürzel/Schlüssel ist gleich REGEL. |
| **Statistikfeld** | RSErhoehung                              |
| Eingabe           | DaVinci:<br/>Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]<br/>Stammdaten > Lehrer > Zeitkonto > Stunden |
| Beschreibung      | Geben Sie die Erhöhung des Regelstundenmaßes durch fachpraktischen Unterricht für jeden Lehrer in seiner Soll-Berechnung in den Stammdaten an. <br/>BBS: Kürzel/Schlüssel ist gleich FAPRA.<br/>ABS: Kürzel/Schlüssel ist gleich ZAG.<br/>Nur bei Gym. und IGS: ZAG-Stunden |
| **Statistikfeld** | MehrArbeit                               |
| Eingabe           | DaVinci:<br/>Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]<br/>Stammdaten > Lehrer > Zeitkonto > Stunden |
| Beschreibung      | Geben Sie die Mehrarbeitsstunden für jeden Lehrer in seiner Soll-Berechnung an. <br/>Kürzel/Schlüssel ist gleich MEHR. |
| **Statistikfeld** | PersonalNr                               |
| Eingabe           | Magellan:Lehrer > Daten 1 > Personalnr   |
| Beschreibung      | Geben Sie hier die Personalnummer ein.   |
| **Statistikfeld** | MissioVocation                           |
| Eingabe           | Magellan:Lehrer > Merkmale > Merkmal S1  |
| Beschreibung      | Geben Sie hier ein, ob der Lehrer eine kirchliche Bevollmächtigung hat.<br/>Grundlage ist das Schlüsselverzeichnis „Lehrermerkmale“ <br/>(Bereich S1). |
| **Statistikfeld** | LehrAemter > LehrAmt                     |
| Eingabe           | Magellan:<br/>Lehrer > Daten 3 > Lehrämter > Eintrag aus Liste[Lehrämter]<br/>Lehrer > Daten 3 > Lehrämter > Lehramtstyp |
| Beschreibung      | Geben Sie hier die Liste der Lehrämter ein. Geben Sie bei Lehramtstyp „Lehramt“ an. |
| **Statistikfeld** | LehrAemter > LehrAmtFolge                |
| Eingabe           | Magellan:Lehrer > Daten 3 > Lehrämter    |
| Beschreibung      | Die Folge der Lehrämter ergibt sich aus den eingetragenen Lehrämtern und muss nicht separat eingetragen werden. |
| **Statistikfeld** | LBefaehigungen > LehrBefaehigung         |
| Eingabe           | Magellan:<br/>Lehrer > Daten 3 > Lehrämter > Eintrag aus Liste[Lehrämter]<br/>Lehrer > Daten 3 > Lehrämter > Lehramtstyp |
| Beschreibung      | Geben Sie hier die Liste der Lehrbefähigungen ein. Geben Sie bei Lehramtstyp „Lehrbefähigung“ an. |
| **Statistikfeld** | UBefaehigungen > UnterrichtsBef          |
| Eingabe           | Magellan:<br/>Lehrer > Daten 3 > Lehrämter > Eintrag aus Liste[Lehrämter]<br/>Lehrer > Daten 3 > Lehrämter > Lehramtstyp |
| Beschreibung      | Geben Sie hier die Liste der Unterrichtsbefähigungen ein. Geben Sie bei Lehramtstyp "Unterrichtserlaubnis", "Unterrichtsauftrag" oder "Unterrichtsbefugnis" an. |
| **Statistikfeld** | ZeitAusgleich > AusgleichsGrund          |
| Eingabe           | DaVinci:Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel] |
| Beschreibung      | Geben Sie die Zeitausgleichsstunden für jeden Lehrer in seiner Soll-Berechnung an. Schlüssel beginnen mit ZAS. |
| **Statistikfeld** | ZeitAusgleich > AusgleichsStunden        |
| Eingabe           | DaVinci:Stammdaten > Lehrer > Zeitkonto > Stunden |
| Beschreibung      | Geben Sie zu den eingetragenen Zeitausgleichsgründen die entsprechende Stundenzahl an. |
| **Statistikfeld** | AEF > AEFGrund                           |
| Eingabe           | DaVinci:Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel] |
| Beschreibung      | Geben Sie die Anrechnungs-, Ermäßigungs-, Freistellungsstunden sowie längerfristiger Ausfall des Lehrers in seiner Soll-Berechnung an.<br/>Schlüssel beginnen mit AEF. |
| **Statistikfeld** | AEF > AEFStunden                         |
| Eingabe           | DaVinci:Stammdaten > Lehrer > Zeitkonto > Stunden |
| Beschreibung      | Geben Sie zu den eingetragenen Anrechnungs-, Ermäßigungs- und Freistellungsstunden die entsprechende Stundenzahl an. |
| **Statistikfeld** | AEF > AEFErklaerung                      |
| Eingabe           | DaVinci:Stammdaten > Lehrer > Zeitkonto > Bemerkung |
| Beschreibung      | Geben Sie hier evtl. eine Begründung für eine AEF-Stunde an. Der Begründungstext darf maximal 10 Zeichen lang sein. Er stellt einen Verweis auf ein Zusatzdokument dar, welches erklärend zur Statistik von der Schule mitgeliefert wird. |
| **Statistikfeld** | StundenAbgabe > SchulArtStufe            |
| Eingabe           | DaVinci Stundenplan:<br/>Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]<br/><br/>Magellan:<br/>Klassen > Daten > Organisation Bildungsgang |
| Beschreibung      | Geben Sie hier die Abgabestunden an andere Schulen für jeden Lehrer in seiner Soll-Berechnung an. <br/>Die Schlüssel beginnen mit ART.<br/>Geben Sie in Magellan in den entsprechenden Klassen die Organisation und den Bildungsgang an, da sich aus diesen Werten der statistische Wert berechnet. |
| **Statistikfeld** | StundenAbgabe > AbgabeStunden            |
| Eingabe           | DaVinci:Stammdaten > Lehrer > Zeitkonto > Stunden |
| Beschreibung      | Geben Sie zu den eingetragenen Abgabestunden an die Stundenzahl ein. |
| **Statistikfeld** | Verfuegbar > SchulFormStufe              |
| Eingabe           | Magellan:Klassen > Daten > Organisation[Organisationen]Bildungsgang[Bildungsgänge] |
| Beschreibung      | Die Schulart für die Aufsummierung der Lehrer-Ist-Stunden nach Schulart berechnet sich anhand der eingetragenen Daten in Übereinstimmung mit den Daten in DaVinci, da die Stundendaten aus DaVinci kommen. <br/><b>Diese Schlüssel werden nicht direkt eingetragen, sondern berechnet.</b><br/><br/> Dazu werden folgende Einträge der Klasse ausgewertet:<br/>- Bildungsgang <br/>- Schulform<br/>- Organisation<br/>- Beschäftigungsverhältnis des Lehrers <br/> <br/>Beispiel:<br/> Stunden (Lehrerveranstaltungsliste aus DaVinci), die ein Lehrer mit Beschäftigungsverhältnis 39 (Förderschul-Lehrkraft an Regelschulen) in einer Klasse mit dem Bildungsgang BVJ (8101050) unterrichtet, werden mit der Schulformstufe 73 (Integrationsmaßnahmen Sekundarstufe II/BVJ) gekennzeichnet.<br/><br/>Die Schulformstufenberechnung wurde erweitert:<br/> Für BVJs mit Inklusionsschülern müssen im Gliederungsplan 2017 die verfügbaren Stunden wie folgt differenziert werden: <br/>Der Unterricht in einem BVJ mit Inklusionsschülern (Bildungsgang 8101060) wird im Tag "Verfuegbar" mit zwei unterschiedlichen SchulFomStufen gemeldet. Der Unterricht in Sprachförderung (DAZ = Deutsch als Zusatzsprache, Fach mit Schlüssel 6) wird mit SchulFormStufe 83 gemeldet. Der übrige Unterricht wird mit der SchulFormStufe 59 (BVJ-Vollzeit) gemeldet. |
| **Statistikfeld** | Verfuegbar > VerfuegStunden              |
| Eingabe           | DaVinci:Stundenplan > Berechneter Wert   |
| Beschreibung      | Die verfügbaren Stunden (pro Schulart) ergeben sich aus dem Stundenplan bzw. der Veranstaltungsliste des Lehrers. <br/>Hierbei werden die IST-Stunden der Veranstaltungsliste nach der SchulFormStufe (siehe Erläuterung zur SchulFormStufe) zusammengefasst. |
| **Statistikfeld** | Unterricht > Fach                        |
| Eingabe           | DaVinci:Stundenplan > Berechneter Wert   |
| Beschreibung      | Die Unterrichtsstunden (pro Fach) ergeben sich aus dem Stundenplan bzw. der Veranstaltungsliste des Lehrers. |
| **Statistikfeld** | Unterricht > Stunden                     |
| Eingabe           | DaVinci:Stundenplan > Berechneter Wert   |
| Beschreibung      | Die Unterrichtsstunden (pro Fach) ergeben sich aus dem Stundenplan bzw. der Veranstaltungsliste des Lehrers.<br/><br/>Wichtige Anmerkung:<br/>Wenn der Lehrer geblockt ist, müssen die Lehrerstunden über den Lehrerfaktor verteilt werden. <br/>Die Absprachen lauten, wie im folgenden Beispiel:<br/><br/>Lehrer L1 ist zeitgleich in 7C, 8A, 9B geblockt. Es müssen für das Lehrer-Ist im D6 – Datensatz (DaVinci Export) die Lehrerfaktoren wie folgt gesetzt werden:<br/><br/>L1 7C Lehrerfaktor = 1 ( da „7C“ die alphabetisch erste Klasse ist )<br/>L1 8A Lehrerfaktor = 0 (Nebenklasse)<br/>L1 9B Lehrerfaktor = 0 (Nebenklasse) |
