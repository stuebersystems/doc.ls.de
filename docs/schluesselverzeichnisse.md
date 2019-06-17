# Schlüsselverzeichnisse


Die für die jeweiligen Landesstatistiken oder für die Arbeit in DAVINCI und MAGELLAN notwendigen Schlüssel werden als Dateien mit der Endung .KEYS per Serviceupdate von STÜBER SYSTEMS zur Verfügung gestellt. 

> #### danger::Wichtig
> Stellen Sie bitte vor dem Import der Schlüsselverzeichnisse sicher, dass die aktuellsten Versionen von MAGELLAN oder DAVINCI auf dem Server und den Arbeitsplatzrechnern installiert sind.

## DAVINCI-Import

Per Serviceupdate werden auf Ihrem Rechner importierbare Schlüsseldateien hinterlegt. Um die Inhalte dieser Dateien in DAVINCI nutzen zu können, führen Sie bitte die nachfolgenden Schritte aus:

1. Öffnen Sie DAVINCI und wechseln in die Ansicht `Extras > Schlüsselverzeichnisse`.
2. Rufen Sie per Doppelklick das zu füllende Schlüsselverzeichnis auf, im Beispiel haben wir die "Lehrer-Soll-Änderungsgründe" gewählt.
3. Wählen Sie `Importieren`, verweisen Sie auf die entsprechende Importdatei und bestätigen den Dialog.

![Import der mitgelieferten DAVINCI-Schlüssel](images/davinci.schluessel-importieren.png)

## MAGELLAN-Import

### allgemeine Schlüsselverzeichnisse importieren

Per Serviceupdate werden auf Ihrem Rechner importierbare Schlüsseldateien hinterlegt. Um die Inhalte dieser Dateien in MAGELLAN nutzen zu können, führen Sie bitte die nachfolgenden Schritte aus:

1. Öffnen Sie das Modul MAGELLAN- Administrator und wählen die Ansicht `Datenimporte > Schlüsselverzeichnisse` importieren.
2. Wählen Sie Ihr Bundesland, Ihrer Schulart und Ihren Mandanten aus und importieren einen ausgewählten oder alle mitgelieferten Kataloge.

![Import der mitgelieferten MAGELLAN-Schlüssel](images/magellan.schluessel-importieren.png)

### Postleitzahlverzeichnisse aktualisieren

Einige Werte im Verzeichnis Postleitzahlen können sich durch Gebietsrefomen verändern, ob das für das aktuelle Jahr in Ihrer Region notwendig ist, wird im jeweiligen Regionalabschnitt beschrieben.
daher muss bitte das Postleitzahlverzeichnis (ab Version 6.5.23) neu importiert werden und anschließend die Synchronisierung der Postleitzahlen und Ort der Schüler mit den Inhalten des Postleitzahlverzeichnisses durchgeführt werden.

Folgende Schritt sind notwendig:

1. Postleitzahlverzeichnis importieren
2. Gemeinden synchronisieren
3. Vollständigkeit der Gemeindekennziffern für Schüler überprüfen


#### Postleitzahlverzeichnis importieren

Prüfen Sie bitte, ob in Ihrem Schulnetzwerk mindestens die 6.5.23 eingesetzt wird.
Öffnen Sie anschließend bitte im MAGELLAN Administrator den Punkt `Datenimporte > Postleitzahlverzeichnis importieren`. 
Wählen Sie im Assistenten für `für folgendes Land` den Wert `Deutschland` aus und für `importiere folgenden Katalog` bitte `alle Kataloge`. Starten Sie den Assistenten über die Schaltfläche `Fertigstellen`.

![Importieren des Postleitzahlverzeichnisses](images/RLP_PLZ_importieren.png)

#### Gemeinden synchronisieren

Wenn das Einlesen der Postleitzahlen abgeschlossen ist, müssen die neuen Einträge im Verzeichnis mit den bestehenden Werten der Schüler, Lehrer, Schulen und Betriebe abgeglichen werden. Dabei wird die Postleitzahl und der Ort des jeweiligen Datensatzes (je Schüler, Lehrer usw.) mit den Inhalten des Postleitzahlverzeichnisses verglichen und falls eine Übereinstimmung vorliegt mit der Gemeindekennziffer ergänzt.

![Synchronisieren der Gemeinden](images/RLP_Gemeinden_sync.png)

#### Vollständigkeit der Gemeindekennziffern für Schüler überprüfen

Sollte anhand der Postleitzahl und des Ortes zwischen den Schülern und dem Postleitzahlverzeichnis keine Übereinstimmung festgestellt werden, bekommt der Schüler keine Gemeindekennziffer zugewiesen. In der Regel genügt die Korrektur des Schülerortes oder der Schüler-PLZ und ein erneuter Durchlauf des `Gemeinden synchronisierens`. Damit Sie einen Überblick haben, für welchen Schüler die Zuweisung nicht gelungen ist, finden Sie in `MAGELLAN > Mandanden > Mandant markieren > Drucken ` den Prüfbericht "Mandant (Ausgabe Schueler ohne Gemeindekennziffer).rpt". Rufen Sie pro Halbjahr diesen Bericht auf, es werden nur Schüler gezeigt, denen keine Gemeindekennziffer zugeordnet werden konnte.

## Übersicht der MAGELLAN-Schlüsselverzeichnisse

Nachfolgend finden Sie ein Übersicht alle Magellanschlüsselverzeichnisse tabellarisch aufgeführt.

## Tabellenlegende

In der nachfolgend aufgelisteten Tabelle zur Statistik haben die Spalten folgende Bedeutungen.


| Spaltenname    | Bedeutung                                |
|----------------|------------------------------------------|
| Ort            | Der Pfad in MAGELLAN zum einzugebenden Datenfeld, der auf die entsprechende Schlüsseltabelle verweist |
| Mandantenbezug | Gibt an, ob die Tabelle nur pro Mandant (Mandantenbezug=Ja) oder für alle Mandanten der Datenbank (Mandantenbezug=Nein) gilt. |
| Import         | Gibt an, ob und wie das Schlüsselverzeichnis für einen Import berücksichtigt wird. |
| PLZ            | mport über den Import des Postleitzahlenverzeichnis |
| Katalog        | Import über den Import der Schlüsselverzeichnisse |
| Kein           | Zur Zeit nicht für den Import vorgesehen |
| Beschreibung   | Informationen darüber, wozu das Feld bei Einführung gedacht war und welche Verwendung es im Einsatz eventuell noch hat. |

## Verzeichnisse


| Bezeichnung    | Anmerkung                                |
|----------------|------------------------------------------|
| Verzeichnis    | Abgangsarten                             |
| Ort            | Schüler > Zugang/Abgang > Abgangsart     |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art des Abgangs der aktuellen Schule.    |
| Verzeichnis    | Abordnungsarten                          |
| Ort            | Lehrer > Daten 3 > Abordnung 1 > Art <br/>Lehrer > Daten 3 > Abordnung 2 > Art |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art der Abordnung eines Lehrers an eine Schule. |
| Verzeichnis    | AbschluesseExtern                        |
| Ort            | Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss<br/>Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Bisher höchster erreichter Abschluss an einer Allgemeinbildenden Schule.<br/>Beispiel: Hauptschulabschluss<br/>Bisher höchster erreichter Abschluss an einer Berufsbildenden Schule. <br/>Beispiel: Abschluss der Berufsschule |
| Verzeichnis    | AbschluesseIntern                        |
| Ort            | Schueler > Laufbahn > Abschluss > Abschluss 1<br/>Schueler > Laufbahn > Abschluss > Abschluss 2 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Erreichter Abschluss des Schuljahres. Meistens leer, da Abschlüsse nur nach bestimmten Schuljahren erreicht werden. <br/>Beispiel: 4. Schuljahr - Grundschulabschluss, 9. Schuljahr - Hauptschulabschluss, 10. Schuljahr - Realschulabschluss.An manchen Schulen kann innerhalb eines Schuljahres ein weiterer Abschluss erlangt werden. |
| Verzeichnis    | Abschlussarten                           |
| Ort            | Schueler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart<br/>Schueler > Laufbahn > Abschluss > Abschluss 2 > Abschlussart<br/>[Abschlussarten] |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Jeweils zusätzliche Informationen zum erreichten Abschluss. |
| Verzeichnis    | Amtsbez                                  |
| Ort            | Lehrer > Daten 2 > Amtsbez               |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Offizielle Amtsbezeichnung des Lehrers.  |
| Verzeichnis    | Arbeitsaemter                            |
| Ort            | Betriebe > Daten 1 > Arbeitsamt          |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Zuständiges Arbeitsamt für den Betrieb.  |
| Verzeichnis    | Aufnahmepruefungen                       |
| Ort            | Schueler > Laufbahn > Allgemein > Aufnahmeprüfung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Bestehen einer evtl. Aufnahmeprüfung.    |
| Verzeichnis    | Behinderungsarten                        |
| Ort            | Schueler > Daten 4 > Sonstige Daten > Behinderung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art der Behinderung bei behinderten Schülern. |
| Verzeichnis    | Berufsfelder                             |
| Ort            | Berufe > Berufsfeld<br/>Klassen > Daten > Berufsfeld |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Berufsfeld eines Berufes. Bei Berufschulklassen, das Berufsfeld des Ausbildungsberufes der jeweiligen Klasse.<br/>Beispiel: Metalltechnik |
| Verzeichnis    | Fachrichtungen                           |
| Ort            | Schlüsselverzeichnisse > Fächer > Bildungsgänge > Fachrichtung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Fachrichtung des Bildungsganges.         |
| Verzeichnis    | Berufe                                   |
| Ort            | Betriebe > Daten 2 > Berufe<br/>Schüler > Ausbildung > Beruf<br/>Liste der Berufe > Beruf<br/>Klassen > Daten > Beruf |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Liste der Ausbildungsberufe eines Betriebes. Erlernter bzw. zu Erlernender Ausbildungsberuf des Schülers. |
| Verzeichnis    | Beschaeftigungsverh                      |
| Ort            | Lehrer > Daten 2 > Besch-verh.           |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Das aktuelle Beschäftigungsverhältnis des Lehrers an der Schule,<br/>Beispiel: Teilzeitbeschäftigt |
| Verzeichnis    | Besoldungen                              |
| Ort            | Lehrer > Daten 2 > Besoldung             |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Besoldungsstufe des Lehrers.             |
| Verzeichnis    | BetreuungenAusserschulisch               |
| Ort            | Schueler > Extras > Betreuungsarten > Außerschulisch 1<br/>Schueler > Extras > Betreuungsarten > Außerschulisch 2<br/>Schueler > Extras > Betreuungsarten > Außerschulisch 3 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Evtl. außerschulische Betreuung des Schülers nach Unterrichtsende. |
| Verzeichnis    | BetreuungenInnerschulisch                |
| Ort            | Schueler > Extras > Betreuungsarten > Innerschulisch 1<br/>Schueler > Extras > Betreuungsarten > Innerschulisch 2<br/>Schueler > Extras > Betreuungsarten > Innerschulisch 3 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Evtl. innerschulische Betreuung des Schülers nach Unterrichtsende. |
| Verzeichnis    | Betreuungsformen                         |
| Ort            | Mandanten > Daten 1 > Betreuungsform     |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Betreuungsangebot der Schule.            |
| Verzeichnis    | Bevollmaechtigungen                      |
| Ort            | Lehrer > Daten 2 > Bevollmächt.          |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Bevollmächtigungen des Lehrers.          |
| Verzeichnis    | Bewerbungsziele                          |
| Ort            | Bewerber > Daten 1 > Ziel 1 – Ziel 4     |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Bewerbungsziele des Bewerbers., Abschluss bzw. Bildungsgang. Je nach Angebot der Schule.<br/>Beispiel: Architektur. Abitur, Fachhochschulreife. BWL |
| Verzeichnis    | Bezirke                                  |
| Ort            | Verzeichnisse > Postleitzahlen > Regierungsbezirke |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Regierungsbezirke Deutschlands. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben! |
| Verzeichnis    | Integrationsmerkmale                     |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Klassenstufen                            |
| Ort            | Klassen > Zeiträume > Zeitraum > Klassenstufe |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Klassenstufe der Klasse.Beispiel: 1,2,3,4,5,6,7,8,9 etc. |
| Verzeichnis    | Organisationen                           |
| Ort            | Klassen > Daten > Organsiation           |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Organisation der Klasse. <br/>Beispiel: Teilzeit, Vollzeit, Blockunterricht |
| Verzeichnis    | Schwerpunkte                             |
| Ort            | Verzeichnisse > Bildungsgänge > Schwerpunkt 1<br/>Verzeichnisse > Bildungsgänge > Schwerpunkt 2 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Schwerpunkte des Bildungsganges.         |
| Verzeichnis    | Bildungsgaenge                           |
| Ort            | Schüler > Daten 2 > Höchster Abschluss ABS > Bildungsgang<br/> Höchster Abschluss BBS > Bildungsgang<br/> Schüler > Ausbildung > Liste der Ausbildungsbetriebe > Bildungsgang<br/>Klassen > Daten > Bildungsgang |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Der Bildungsgang zum bisher höchst erreichten Abschluss an einer Allgemeinbildenden Schule.<br/>Der Bildungsgang zum bisher höchst erreichten Abschluss an einer Berufsbildenden Schule.<br/>Der Bildungsgang der Ausbildungen bzw. der aktuellen Ausbildung.<br/>Der Bildungsgang der Klasse. <br/>Beispiel: FO Agrarwirtschaft |
| Verzeichnis    | Bundeslaender                            |
| Ort            | Verzeichnisse > Postleitzahlen > Bundesländer |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Bundesländer Deutschlands. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben! |
| Verzeichnis    | Dienstherren                             |
| Ort            | Lehrer > Daten 2 > Dienstherr            |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Der Dienstherr (Arbeitgeber) des Lehrers. <br/>Beispiel: Land, freier Träger |
| Verzeichnis    | Disziplinen                              |
| Ort            | Sportfeste > Auswahl > Schüler synchronisieren |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | Sportliche Disziplin des Schülers beim Sportfest. Beispiel: Kugelstoßen |
| Verzeichnis    | Empfehlungen                             |
| Ort            | Schüler > Laufbahn > Empfehlung Elternwunsch<br/>Schüler > Laufbahn > Elternwunsch |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Empfehlung der Schule für den Übergang des Schülers aus der Grundschule in eine höhere Schule. <br/>Beispiel: Empfehlung: Realschule<br/>Wunsch der Eltern für den Übergang des Schülers aus der Grundschule in eine höhere Schule. <br/>Beispiel: Wunsch: Gymnasium |
| Verzeichnis    | Fachgruppen                              |
| Ort            | Schlüsselverzeichnisse > Fächer > Gruppe |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Freies Gruppierungsmerkmal für Fächer.   |
| Verzeichnis    | Fachschwerpunkte                         |
| Ort            | Schüler > Zeugnis > Fächer > Schwerpunkt |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Schwerpunkt des Faches. Frei zu vergebenes Merkmal. |
| Verzeichnis    | Fachstati                                |
| Ort            | Schüler > Zeugnis > Fächer > Fachstatus  |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Der Fachstatus wird zum Teil von uns vorgegeben, kann aber durch statistische Schlüssel erweitert werden. Bei gleichen Status wird der Schlüssel für die Statistik im Skript umgesetzt. |
| Verzeichnis    | Faecher                                  |
| Ort            | Schüler > Zeugnis > Fächer               |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | Fächer des Schülers.Beispiel: Deutsch, Mathematik, Religion etc. |
| Verzeichnis    | FaecherThemen                            |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | FaecherUnterpunkte                       |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Fahrkarten                               |
| Ort            | Schüler > Daten 4 > Beförderung > Fahrkarte |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Art des Fahrausweises bei Beförderungsunterstützung des Schülers. Beispiel: Monatskarte, Jahreskarte etc. |
| Verzeichnis    | Foerderungen                             |
| Ort            | Schüler > Daten 4 > Förderung > Förderung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Art der Förderung bei zu fördernden Schülern. Beispiel: Fremdsprachenförderung |
| Verzeichnis    | Gemeinden                                |
| Ort            | Schüler > Daten 1 > Gemeinde<br/>Bewerber > Daten 1 > Gemeinde<br/>Lehrer > Daten 1 > Gemeinde<br/>Mandanten > Daten 1 > Gemeinde<br/>Betriebe > Daten 1 > Gemeinde<br/>Schulen > Daten > Gemeinde |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Deutschlands Gemeinden.. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben |
| Verzeichnis    | Herkunftsarten                           |
| Ort            | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Herkunftsart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Herkunftsunterlagen                      |
| Ort            | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Unterlagen der bereits besuchten Schule. |
| Verzeichnis    | Kammern                                  |
| Ort            | Betriebe > Daten 1 > Kammer              |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Kammern, denen die Betriebe angehören. Beispiel: Handwerkskammer |
| Verzeichnis    | KlassenMerkmale                          |
| Ort            | Klassen > Merkmale > Merkmal A1 – A6<br/>Klassen > Merkmale >Merkmal S1 – S4 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Merkmal A1-A6 sind frei für die Schulen zu vergebende Merkmale.<br/>Merkmal S1-S4 sind spezielle Statistikmerkmale, die zur Eingabe und Auswahl von Statistischen Daten genutzt werden, die in MAGELLAN nicht verwaltet werden. |
| Verzeichnis    | Konfessionen                             |
| Ort            | Schüler > Daten 1 > Konfession           |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Konfession des Schülers. <br/>Beispiel: röm-kath., ev. etc. |
| Verzeichnis    | Krankenkassen                            |
| Ort            | Schüler > Daten 4 > Sonstige Daten > Krankenkasse |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Krankenkasse des Schülers. Beispiel: AOK |
| Verzeichnis    | Kreise                                   |
| Ort            | Verzeichnisse > Postleitzahlen > Kreise  |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Landkreise Deutschlands. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben! |
| Verzeichnis    | Lehraemter                               |
| Ort            | Lehrer > Daten 3 > Lehrämter             |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Lehrämter des Lehrers.               |
| Verzeichnis    | LehrerAbgaenge                           |
| Ort            | Lehrer > Daten 2 > Abgangsart            |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Abgangsarten des Lehrers von einer Schule. Beispiel: Tod, Beurl. aus Erziehungsurlaub |
| Verzeichnis    | LehrerAusbildung                         |
| Ort            | Lehrer > Daten 2 > Ausbildung            |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Ausbildung des Lehrers               |
| Verzeichnis    | LehrerFehlgruende                        |
| Ort            | Lehrer > Auswahlliste > Bearbeiten oder Rechtsklick > Fehlzeiten |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Erfassen der Lehrerfehlzeiten            |
| Verzeichnis    | LehrerFunktionen                         |
| Ort            | Lehrer > Daten 3 > Funktion 1-8          |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Funktionen des Lehrers. Beispiel: Klassenlehrer, Vertrauenslehrer etc. |
| Verzeichnis    | LehrerMerkmale                           |
| Ort            | Lehrer > Merkmale > Merkmal A1-A6<br/>Lehrer > Merkmale > Merkmal S1-S4 |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | Merkmal A1-A6 sind frei für die Schulen zu vergebende Merkmale.<br/>Merkmal S1-S4 sind spezielle Statistikmerkmale, die zur Eingabe und Auswahl von Statistischen Daten genutzt werden, die in MAGELLAN nicht verwaltet werden |
| Verzeichnis    | LehrerPruefungsbezuege                   |
| Ort            | Lehrer > Daten 3 > Prüfungsbezug         |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Prüfungsbezüge des Lehrers.          |
| Verzeichnis    | LehrerZugaenge                           |
| Ort            | Lehrer > Daten 2 > Zugangsart            |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Zugangsarten des Lehrers an die Schule. Beispiel: Zugang aus dem Privatschuldienst |
| Verzeichnis    | LehrerKategorien                         |
| Ort            | Lehrer > Daten 1 > Kategorie             |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Kategorie des Lehrers.                   |
| Verzeichnis    | Mandantenkategorien                      |
| Ort            | Mandanten > Daten 1 > Kategorie          |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Kategorie der Schule                     |
| Verzeichnis    | Kurssprachen                             |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Muttersprachen                           |
| Ort            | Schüler > Daten 2 > Muttersprache        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Muttersprache oder Verkehrssprache des Schülers. Beispiel: Italienisch |
| Verzeichnis    | Verkehrssprache                          |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Muttersprache oder Verkehrssprache des Schülers. Beispiel: Italienisch |
| Verzeichnis    | Nachpruefungen                           |
| Ort            | Schüler > Laufbahn > Allgemein > Nachprüfung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art der Nachprüfung                      |
| Verzeichnis    | Noten                                    |
| Ort            | Schüler > Zeugnis > Leistungen > Schriftl. Note 1-4<br/>Schüler > Zeugnis > Leistungen > Mündl. Note<br/>Schüler > Zeugnis > Leistungen > Endnote<br/>Schüler > Zeugnis > Leistungen > Endnote (Gesamt) |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | Noten der Fächer eines Schülers. Beispiel: Deutsch – Sehr gut (1), Mathematik – Befriedigend (3) |
| Verzeichnis    | Personenkategorien                       |
| Ort            | Personen > Daten > Kategorie             |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Kategorie der Person für sonstiges Personal. Beispiel: Hausmeister, Gärtner, Putzkraft etc. |
| Verzeichnis    | Stadtbezirke                             |
| Ort            | Verzeichnisse > Postleitzahlen > Stadtbezirke |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Stadtbezirke einer Stadt. Gehören zum Postleitzahlenverzeichnis. |
| Verzeichnis    | Postleitzahlen                           |
| Ort            | Schüler > Daten 1 > Postleitzahl<br/>Bewerber > Daten 1 > Postleitzahl<br/>Lehrer > Daten 1 > Postleitzahl<br/>Mandanten > Daten 1 > Postleitzahl<br/>Personen > Daten > Postleitzahl<br/>Sorgeberechtigte > Daten > Postleitzahl<br/>Betriebe > Daten 1 > Postleitzahl<br/>Schulen > Daten 1 > Postleitzahl<br/>Adressen > Daten 1 > Postleitzahl |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Postleitzahlen Deutschlands. Gehören zum Postleitzahlenver-zeichnis und werden von uns vorgegeben! |
| Verzeichnis    | RelGruende                               |
| Ort            | Schüler > Daten 1 > Rel.-Grund           |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Grund der (nicht) Teilnahme am Religionsunterricht. <br/>Beispiel: Mangel an Lehrpersonal, Mangel an Schüler mit entsprechender Konfession |
| Verzeichnis    | RelTeilnahmen                            |
| Ort            | Schüler > Daten 1 > Rel.-Teilnahme       |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Teilnahme des Schülers am Religionsunterricht.<br/>Beispiel: Teilnahme am evangelischen Unterricht |
| Verzeichnis    | RelWuensche                              |
| Ort            | Schüler > Daten 1 > Rel.-Wunsch          |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Wunsch des Schülers zur Teilnahme an bestimmten Religionsunterricht. <br/>Beispiel: Teilnahme am röm-kath. Unterricht. |
| Verzeichnis    | SchuelerArten                            |
| Ort            | Schüler > Extras > Schülerart > Schülerart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art des Schülers.                        |
| Verzeichnis    | SchuelerFehlgruende                      |
| Ort            | Schüler > Bearbeiten > Fehlzeiten > Grund |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Gründe für Fehlzeiten des Schülers. Beispiel: Krankheit |
| Verzeichnis    | SchuelerFunktionen                       |
| Ort            | Schüler > Daten 3 > Funktionen > Funktion 1-8 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Funktionen des Schülers. Beispiel: Klassensprecher, Schülersprecher etc. |
| Verzeichnis    | SchuelerMerkmale                         |
| Ort            | Schüler > Merkmale > Merkmal A1-A6       |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Merkmal A1-A6 sind frei für die Schulen zu vergebende Merkmale.<br/>Merkmal S1-S10 sind spezielle Statistikmerkmale, die zur Eingabe und Auswahl von Statistischen Daten genutzt werden, die in MAGELLAN nicht verwaltet werden. |
| Verzeichnis    | SchuelerProfile                          |
| Ort            | Schüler > Daten 3 > Verschiedenes > Profil |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Profil des Schülers.                     |
| Verzeichnis    | Schularten                               |
| Ort            | Klassen > Daten > Schulart               |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Bei Schulartübergreifenden Schulen, die Schulart pro Klasse. Beispiel: Kolleg, Förderschule etc. |
| Verzeichnis    | Schularten                               |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | SchulartenHerkunft                       |
| Ort            | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Schulart Schülers der zuvor besuchten Schule. <br/>Beispiel: siehe Schularten |
| Verzeichnis    | SchulformenHerkunft                      |
| Ort            | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulform |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Schulform der zuletzt besuchten Schule.Beispiel: siehe Schulformen |
| Verzeichnis    | SchulformenUebergang                     |
| Ort            | Schüler > Zugang/Abgang > Abgang > An Schulform |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Schulform beim Abgang des Schülers an eine andere Schule.Beispiel: siehe Schulformen |
| Verzeichnis    | Schulstati                               |
| Ort            | Mandanten > Daten 1 > Schulstatus        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Status der Schule.                       |
| Verzeichnis    | Schulstellen                             |
| Ort            | Klassen > Daten > Schulstelle            |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Schulstelle der Klasse.                  |
| Verzeichnis    | Schultraeger                             |
| Ort            | Mandanten > Daten 1 > Schulträger        |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Träger der Schule. Beispiel: Freier Träger, Land etc. |
| Verzeichnis    | Schulzweige                              |
| Ort            | Lehrer > Daten 2 > Schulzweig            |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Schulzweig des Lehrers.                  |
| Verzeichnis    | SorgebeFunktionen                        |
| Ort            | Sorgeberechtigte > Daten > Funktion 1-8  |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Funktionen der Sorgeberechtigten. Beispiel: Elternsprecher etc. |
| Verzeichnis    | Sprachgruppen                            |
| Ort            | Schüler > Daten 1 > Staatsangehörigkeit > Sprachgruppe |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Sprachgruppe des Schülers. Zusätzliche Erfassung einer Sprache des Schülers, ähnlich Muttersprache. |
| Verzeichnis    | Staatsangehoerigkeiten                   |
| Ort            | Schüler > Daten 1 > Staatsangehörigkeit > Staatsangeh. 1<br/>Schüler > Daten 1 > Staatsangehörigkeit > Staatsangeh. 2 |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Staatsangehörigkeiten des Schülers. Beispiel: Chinesisch und Britisch,Deutsch etc. |
| Verzeichnis    | Uebergangsarten                          |
| Ort            | Schüler > Zugang/Abgang > Übergang       |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Übergang des Schülers auf eine andere Schule. Beispiel: Abgang auf Grundschule |
| Verzeichnis    | Umschulungsmerkmale                      |
| Ort            | Schüler > Daten 2 > Umschulung > Umschulung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art der Umschulung des Schülers. <br/>Beispiel: Schüler ist Umschüler, oder Umschulung auf XYZ |
| Verzeichnis    | Unterrichtsarten                         |
| Ort            | Schüler > Zeugnis > Fächer > Unterrichtsart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Unterrichtsart des Faches. Beispiel: Arbeitsgemeinschaft, Grundkurs, Lernfeld etc. |
| Verzeichnis    | Unterstuetzungen                         |
| Ort            | Schüler > Daten 3 > Verschiedenes > Unterstützung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Unterstützung für den Schüler.           |
| Verzeichnis    | Verkehrsmittel                           |
| Ort            | Schüler > Daten 4 > Beförderung > Verkehrsmittel |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Verkehrsmittel bei Unterstützung der Beförderung für den Schüler. Beispiel: Bus, Bahn etc. |
| Verzeichnis    | Versetzungsarten                         |
| Ort            | Schüler > Laufbahn > Allgemein > Versetzungsart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Die Versetzungsart des Schülers am Ende des Schuljahres.<br/> Beispiel: Schüler freiwillig zurück, Nachprüfung bestanden |
| Verzeichnis    | Versicherungsarten                       |
| Ort            | Schüler > Daten 4 > Sonstige Daten > Versicherungsart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art der Versicherung des Schülers.       |
| Verzeichnis    | Vertragsarten                            |
| Ort            | Schüler > Ausbildung > Liste der Ausbildungsbetriebe > Vertragsart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Art des Ausbildungsvertrages des Schülers. Beispiel: Praktikant, Auszubildender etc. |
| Verzeichnis    | Verordnungen                             |
| Ort            | Verzeichnisse > Verordnungen<br/>Abitur > Qualififikation |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Wiederholungsarten                       |
| Ort            | Schüler > Laufbahn > Allgemein > Wiederholungsart |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Wiederholungsart des Schülers am Ende des Schuljahres. Beispiel: Freiwillige Wiederholung etc. |
| Verzeichnis    | Wohnformen                               |
| Ort            | Schüler > Daten 1 > Wohnform             |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Wohnform des Schülers.Beispiel: Heim, Betreutes Wohnen, WG etc. |
| Verzeichnis    | Entscheidungen                           |
| Ort            | Schüler > Laufbahn > Allgemein > Entscheidung |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Schullaufbahnentscheidung, z.B. aus Übergeordneter Orientierungsstufe. |
| Verzeichnis    | FachNiveaus                              |
| Ort            | Verzeichnisse > Fachtafeln<br/>Schüler > Zeugnis > Fächer |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | Niveaustufe in der das Fach unterrichtet wird. |
| Verzeichnis    | Banken                                   |
| Ort            | Schüler > Daten 4 > Beförderung > Bank<br/>Mandanten > Daten 2 > Ban |
| Mandantenbezug | Nein                                     |
| Import         | PLZ                                      |
| Beschreibung   | Kontodaten zum Schüler und Mandanten.    |
| Verzeichnis    | Abteilungen                              |
| Ort            | Mandant > Daten<br/>Klasse > Daten1      |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | Abteilungen der Schule                   |
| Verzeichnis    | Fachtafeln                               |
| Ort            | Verzeichnisse > Fachtafeln               |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Lehrer-Soll-Schlüssel                    |
| Ort            | Lehrer >Soll-Berechnung                  |
| Mandantenbezug | Nein                                     |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Raeume                                   |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Katalog                                  |
| Beschreibung   | -                                        |
| Verzeichnis    | Zeitraeume                               |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | ASVArten                                 |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | ASVBewertungen                           |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | ASVKategorien                            |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | ASVTafelKategorien                       |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Zeugnisbemerkungen                       |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Zeugnisbeurteilungen                     |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Zeugnisformulare                         |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Sportfeste                               |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | Wettkämpfe                               |
| Ort            | -                                        |
| Mandantenbezug | Ja                                       |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | MandantenMerkmale                        |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Schulenmerkmale                          |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Sopaedfoerderungen                       |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Adressekategorien                        |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Bewerbungsempfehlungen                   |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |
| Verzeichnis    | Haertefaelle                             |
| Ort            | -                                        |
| Mandantenbezug | Nein                                     |
| Import         | Nein                                     |
| Beschreibung   | -                                        |




   
## Verzeichnisse mit Vorgaben

Einige Schlüsselverzeichnisse enthalten vorgegebene Schlüssel, die eventuell beim Erstellen der Statistik in die entsprechenden Schlüssel des Statistikamtes umgesetzt werden müssen. Da nicht jedes Schlüsselverzeichnis in jedem Bundesland statistisch relevant ist, enthalten viele Schlüsselverzeichnisse allgemeine nicht statistisch relevante Schlüssel, die für die Schulen für die tägliche Arbeit und Verwaltung ihrer Daten von Wichtigkeit sind. Diese Datensätze werden dann ohne das Feld „Schlüssel“ eingetragen.

Folgende Schlüsselverzeichnisse enthalten Vorgaben:


| Schlüsselverzeichnis | Bedeutung                                |
|----------------------|------------------------------------------|
| --                   | --                                       |
| 00_Fachstati         | enthält die Fachstatus zum Austausch mit DAVINCI |
| 00_Noten             | enthält die in Deutschland übliche Noten- und Punktgebung |
| 00_Unterrichtsarten  | enthält die typischen Unterrichtsarten   |




