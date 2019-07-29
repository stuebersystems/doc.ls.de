# Schlüsselverzeichnisse

Die für die jeweiligen Landesstatistiken oder für die Arbeit in DAVINCI und MAGELLAN notwendigen Schlüssel werden als Dateien mit der Endung .KEYS per Serviceupdate von STÜBER SYSTEMS zur Verfügung gestellt.
In einigen Bundesländern gibt es darüber hinaus Import für Betriebe und Schulen, die über das MAGELLAN-Importformat eingelesen werden können.

!!! warning "Wichtig"

    Stellen Sie bitte vor dem Import der Schlüsselverzeichnisse sicher, dass die aktuellsten Versionen von MAGELLAN oder DAVINCI auf dem Server und den Arbeitsplatzrechnern installiert sind.

## DAVINCI-Import

Per Serviceupdate werden auf Ihrem Rechner importierbare Schlüsseldateien hinterlegt. Um die Inhalte dieser Dateien in DAVINCI nutzen zu können, führen Sie bitte die nachfolgenden Schritte aus:

1. Öffnen Sie DAVINCI und wechseln in die Ansicht `Extras > Schlüssel**Verzeichnis**  se`.
2. Rufen Sie per Doppelklick das zu füllende Schlüsselverzeichnis auf, im Beispiel haben wir die "Lehrer-Soll-Änderungsgründe" gewählt.
3. Wählen Sie `Importieren`, verweisen Sie auf die entsprechende Importdatei und bestätigen den Dialog.

![Import der mitgelieferten DAVINCI-Schlüssel](/assets/images/davinci.schluessel-importieren.png)

## MAGELLAN-Import

### Allgemeine Schlüsselverzeichnisse importieren

Per Serviceupdate werden auf Ihrem Rechner importierbare Schlüsseldateien hinterlegt. Um die Inhalte dieser Dateien in MAGELLAN nutzen zu können, führen Sie bitte die nachfolgenden Schritte aus:

1. Öffnen Sie das Modul MAGELLAN- Administrator und wählen die Ansicht `Datenimporte > Schlüsselverzeichnisse` importieren.
2. Wählen Sie Ihr Bundesland, Ihre Schulart und Ihren Mandanten aus und importieren einen ausgewählten oder alle mitgelieferten Kataloge.

![Import der mitgelieferten MAGELLAN-Schlüssel](/assets/images/magellan.schluessel-importieren.png)

### Postleitzahlverzeichnisse aktualisieren

Einige Werte im Verzeichnis Postleitzahlen können sich durch Gebietsrefomen verändern, ob das für das aktuelle Jahr in Ihrer Region notwendig ist, wird im jeweiligen Regionalabschnitt beschrieben.
daher muss bitte das Postleitzahlverzeichnis (ab Version 6.5.23) neu importiert werden und anschließend die Synchronisierung der Postleitzahlen und Ort der Schüler mit den Inhalten des Postleitzahlverzeichnisses durchgeführt werden.

Folgende Schritte sind notwendig:

1. Postleitzahlverzeichnis importieren
2. Gemeinden synchronisieren
3. Vollständigkeit der Gemeindekennziffern für Schüler überprüfen

#### Postleitzahlverzeichnis importieren

Prüfen Sie bitte, ob in Ihrem Schulnetzwerk mindestens die 6.5.23 eingesetzt wird.
Öffnen Sie anschließend bitte im MAGELLAN-Administrator den Punkt `Datenimporte > Postleitzahlverzeichnis importieren`.
Wählen Sie im Assistenten für `für folgendes Land` den Wert `Deutschland` aus und für `importiere folgenden Katalog` bitte `alle Kataloge`. Starten Sie den Assistenten über die Schaltfläche `Fertigstellen`.

![Importieren des Postleitzahlverzeichnisses](/assets/images/RLP_PLZ_importieren.png)

#### Gemeinden synchronisieren

Wenn das Einlesen der Postleitzahlen abgeschlossen ist, müssen die neuen Einträge im Verzeichnis mit den bestehenden Werten der Schüler, Lehrer, Schulen und Betriebe abgeglichen werden. Dabei wird die Postleitzahl und der Ort des jeweiligen Datensatzes (je Schüler, Lehrer usw.) mit den Inhalten des Postleitzahlverzeichnisses verglichen und falls eine Übereinstimmung vorliegt mit der Gemeindekennziffer ergänzt.

![Synchronisieren der Gemeinden](/assets/images/RLP_Gemeinden_sync.png)

#### Vollständigkeit der Gemeindekennziffern für Schüler überprüfen

Sollte anhand der Postleitzahl und des Ortes zwischen den Schülern und dem Postleitzahlverzeichnis keine Übereinstimmung festgestellt werden, bekommt der Schüler keine Gemeindekennziffer zugewiesen. In der Regel genügt die Korrektur des Schülerortes oder der Schüler-PLZ und ein erneuter Durchlauf des `Gemeinden synchronisieren`. Damit Sie einen Überblick haben, für welchen Schüler die Zuweisung nicht gelungen ist, finden Sie in `MAGELLAN > Mandanten > Mandant markieren > Drucken` den Prüfbericht "Mandant (Ausgabe Schueler ohne Gemeindekennziffer).rpt". Rufen Sie pro Halbjahr diesen Bericht auf, es werden nur Schüler gezeigt, denen keine Gemeindekennziffer zugeordnet werden konnte.

## Übersicht der MAGELLAN-Schlüsselverzeichnisse

Nachfolgend finden Sie ein Übersicht alle MAGELLAN Schlüsselverzeichnisse tabellarisch aufgeführt.

## Tabellenlegende

In der nachfolgend aufgelisteten Tabelle zur Statistik haben die Spalten folgende Bedeutungen.

Spaltenname    | Bedeutung
-------------- | --------
Wegweiser      | Der Pfad in MAGELLAN zum einzugebenden Datenfeld, der auf die entsprechende Schlüsseltabelle verweist
Mandantenbezug | Gibt an, ob die Tabelle nur pro Mandant (Mandantenbezug = Ja) oder für alle Mandanten der Datenbank (Mandantenbezug = Nein) gilt
Import         | Gibt an, ob und wie das Schlüsselverzeichnis für einen Import berücksichtigt wird<br>* PLZ= Import über den Import des Postleitzahlenverzeichnis<br>* Katalog = Import über den Import der Schlüsselverzeichnisse<br>* Kein = Aktuell nicht für den Import vorgesehen
Beschreibung   | Informationen darüber, wozu das Feld bei Einführung gedacht war und welche Verwendung es im Einsatz eventuell noch hat.

## Verzeichnisse

Spalte          | Beschreibung
--------------- | ------------
**Verzeichnis** | **Abgangsarten**
Wegweiser       | Schüler > Zugang/Abgang > Abgangsart
Beschreibung    | Art des Abgangs der aktuellen Schule
Mandantenbezug  | Kein
Import          | Katalog
**Verzeichnis** | **Abordnungsarten**
Wegweiser       | Lehrer > Daten 3 > Abordnung 1 > Art <br/>Lehrer > Daten 3 > Abordnung 2 > Art
Beschreibung    | Art der Abordnung eines Lehrers an eine Schule
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **AbschluesseExtern**
Wegweiser       | Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss<br/>Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss
Beschreibung    | Bisher höchster erreichter Abschluss an einer Allgemeinbildenden Schule.<br/>Beispiel: Hauptschulabschluss<br/>Bisher höchster erreichter Abschluss an einer Berufsbildenden Schule.<br/>Beispiel: Abschluss der Berufsschule
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **AbschluesseIntern**
Wegweiser       | Schueler > Laufbahn > Abschluss > Abschluss 1<br/>Schueler > Laufbahn > Abschluss > Abschluss 2
Beschreibung    | Erreichter Abschluss des Schuljahres. Meistens leer, da Abschlüsse nur nach bestimmten Schuljahren erreicht werden.<br/>Beispiel: 4. Schuljahr - Grundschulabschluss, 9. Schuljahr - Hauptschulabschluss, 10. Schuljahr - Realschulabschluss. An manchen Schulen kann innerhalb eines Schuljahres ein weiterer Abschluss erlangt werden.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Abschlussarten**
Wegweiser       | Schueler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart<br/>Schueler > Laufbahn > Abschluss > Abschluss 2 > Abschlussart<br/>[Abschlussarten]
Beschreibung    | Jeweils zusätzliche Informationen zum erreichten Abschluss.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Amtsbez**
Wegweiser       | Lehrer > Daten 2 > Amtsbez
Beschreibung    | Offizielle Amtsbezeichnung des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Arbeitsaemter**
Wegweiser       | Betriebe > Daten 1 > Arbeitsamt
Beschreibung    | Zuständiges Arbeitsamt für den Betrieb.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Aufnahmepruefungen**
Wegweiser       | Schueler > Laufbahn > Allgemein > Aufnahmeprüfung
Beschreibung    | Bestehen einer evtl. Aufnahmeprüfung.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Behinderungsarten**
Wegweiser       | Schueler > Daten 4 > Sonstige Daten > Behinderung
Beschreibung    | Art der Behinderung bei behinderten Schülern.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Berufsfelder**
Wegweiser       | Berufe > Berufsfeld<br>Klassen > Daten > Berufsfeld
Beschreibung    | Berufsfeld eines Berufes. Bei Berufschulklassen, das Berufsfeld des Ausbildungsberufes der jeweiligen Klasse.<br/>Beispiel: Metalltechnik
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Fachrichtungen**
Wegweiser       | Schlüsselverzeichnisse > Fächer > Bildungsgänge > Fachrichtung
Beschreibung    | Fachrichtung des Bildungsganges.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Berufe**
Wegweiser       | Betriebe > Daten 2 > Berufe<br>Schüler > Ausbildung > Beruf<br>Liste der Berufe > Beruf<b/>Klassen > Daten > Beruf
Beschreibung    | Liste der Ausbildungsberufe eines Betriebes. Erlernter bzw. zu Erlernender Ausbildungsberuf des Schülers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Beschaeftigungsverh**
Wegweiser       | Lehrer > Daten 2 > Besch-verh.
Beschreibung    | Das aktuelle Beschäftigungsverhältnis des Lehrers an der Schule,<br>Beispiel: Teilzeitbeschäftigt
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Besoldungen**
Wegweiser       | Lehrer > Daten 2 > Besoldung
Beschreibung    | Besoldungsstufe des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **BetreuungenAusserschulisch**
Wegweiser       | Schueler > Extras > Betreuungsarten > Außerschulisch 1<br>Schueler > Extras > Betreuungsarten > Außerschulisch 2<br>Schueler > Extras > Betreuungsarten > Außerschulisch 3
Beschreibung    | Evtl. außerschulische Betreuung des Schülers nach Unterrichtsende.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **BetreuungenInnerschulisch**
Wegweiser       | Schueler > Extras > Betreuungsarten > Innerschulisch 1<br>Schueler > Extras > Betreuungsarten > Innerschulisch 2<br>Schueler > Extras > Betreuungsarten > Innerschulisch 3
Beschreibung    | Evtl. innerschulische Betreuung des Schülers nach Unterrichtsende.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Betreuungsformen**
Wegweiser       | Mandanten > Daten 1 > Betreuungsform
Beschreibung    | Betreuungsangebot der Schule.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Bevollmaechtigungen**
Wegweiser       | Lehrer > Daten 2 > Bevollmächt.
Beschreibung    | Bevollmächtigungen des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Bewerbungsziele**
Wegweiser       | Bewerber > Daten 1 > Ziel 1 – Ziel 4
Beschreibung    | Bewerbungsziele des Bewerbers., Abschluss bzw. Bildungsgang. Je nach Angebot der Schule.<br>Beispiel: Architektur. Abitur, Fachhochschulreife. BWL
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Bezirke**
Wegweiser       | Verzeichnisse > Postleitzahlen > Regierungsbezirke
Beschreibung    | Regierungsbezirke Deutschlands. Gehören zum Postleitzahlenverzeichnis   und werden von uns vorgegeben!
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | **Integrationsmerkmale**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Klassenstufen**
Wegweiser       | Klassen > Zeiträume > Zeitraum > Klassenstufe
Beschreibung    | Die Klassenstufe der Klasse.Beispiel: 1,2,3,4,5,6,7,8,9 etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Organisationen**
Wegweiser       | Klassen > Daten > Organsiation
Beschreibung    | Organisation der Klasse.<br>Beispiel: Teilzeit, Vollzeit, Blockunterricht
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schwerpunkte**
Wegweiser       | Verzeichnisse > Bildungsgänge > Schwerpunkt 1<br>Verzeichnisse > Bildungsgänge > Schwerpunkt 2
Beschreibung    | Schwerpunkte des Bildungsganges.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Bildungsgaenge**
Wegweiser       | Schüler > Daten 2 > Höchster Abschluss ABS > Bildungsgang<br> Höchster Abschluss BBS > Bildungsgang<br> Schüler > Ausbildung > Liste der Ausbildungsbetriebe > Bildungsgang<br>Klassen > Daten > Bildungsgang
Beschreibung    | Der Bildungsgang zum bisher höchst erreichten Abschluss an einer Allgemeinbildenden Schule.<br>Der Bildungsgang zum bisher höchst erreichten Abschluss an einer Berufsbildenden Schule.<br>Der Bildungsgang der Ausbildungen bzw. der aktuellen Ausbildung.<br>Der Bildungsgang der Klasse. <br>Beispiel: FO Agrarwirtschaft
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Bundeslaender**
Wegweiser       | Verzeichnisse > Postleitzahlen > Bundesländer
Beschreibung    | Bundesländer Deutschlands. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben!
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | **Dienstherren**
Wegweiser       | Lehrer > Daten 2 > Dienstherr
Beschreibung    | Der Dienstherr (Arbeitgeber) des Lehrers. <br>Beispiel: Land, freier Träger
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Disziplinen**
Wegweiser       | Sportfeste > Auswahl > Schüler synchronisieren
Beschreibung    | Sportliche Disziplin des Schülers beim Sportfest. Beispiel: Kugelstoßen
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **Empfehlungen**
Wegweiser       | Schüler > Laufbahn > Empfehlung Elternwunsch<br>Schüler > Laufbahn > Elternwunsch
Beschreibung    | Empfehlung der Schule für den Übergang des Schülers aus der Grundschule in eine höhere Schule.<br>Beispiel: Empfehlung: Realschule<br/>Wunsch der Eltern für den Übergang des Schülers aus der Grundschule in eine höhere Schule.<br/>Beispiel: Wunsch: Gymnasium
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Fachgruppen**
Wegweiser       | Schlüsselverzeichnisse > Fächer > Gruppe
Beschreibung    | Freies Gruppierungsmerkmal für Fächer.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Fachschwerpunkt**
Wegweiser       | Schüler > Zeugnis > Fächer > Schwerpunkt
Beschreibung    | Schwerpunkt des Faches. Frei zu vergebenes Merkmal.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Fachstati**
Wegweiser    | Schüler > Zeugnis > Fächer > Fachstatus
Mandantenbezug | Nein
Import | Katalog
Beschreibung   | Der Fachstatus wird zum Teil von uns vorgegeben, kann aber durch statistische Schlüssel erweitert werden. Bei gleichen Status wird der Schlüssel für die Statistik im Skript umgesetzt.
**Verzeichnis** | **Faecher**
Wegweiser       | Schüler > Zeugnis > Fächer
Beschreibung    | Fächer des Schülers.Beispiel: Deutsch, Mathematik, Religion etc.
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **FaecherThemen**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **FaecherUnterpunkte**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **Fahrkarten**
Wegweiser       | Schüler > Daten 4 > Beförderung > Fahrkarte
Beschreibung    | Die Art des Fahrausweises bei Beförderungsunterstützung des Schülers. Beispiel: Monatskarte, Jahreskarte etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Foerderungen**
Wegweiser       | Schüler > Daten 4 > Förderung > Förderung
Beschreibung    | Die Art der Förderung bei zu fördernden Schülern. Beispiel: Fremdsprachenförderung
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Gemeinden**
Wegweiser       | Schüler > Daten 1 > Gemeinde<br>Bewerber > Daten 1 > Gemeinde<br>Lehrer > Daten 1 > Gemeinde<br>Mandanten > Daten 1 > Gemeinde<br>Betriebe > Daten 1 > Gemeinde<br>Schulen > Daten > Gemeinde
Beschreibung    | Deutschlands Gemeinden. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | ****Herkunftsarten**
Wegweiser       | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Herkunftsart
Beschreibung    | -
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Herkunftsunterlagen**
Wegweiser       | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen
Beschreibung   | Unterlagen der bereits besuchten Schule.
Mandantenbezug  | Nein
Import         | Katalog
**Verzeichnis** | **Kammern**
Wegweiser       | Betriebe > Daten 1 > Kammer
Beschreibung    | Die Kammern, denen die Betriebe angehören. Beispiel: Handwerkskammer
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **KlassenMerkmale**
Wegweiser       | Klassen > Merkmale > Merkmal A1 – A6<br>Klassen > Merkmale > Merkmal S1 – S4
Beschreibung    | Merkmal A1-A6 sind frei für die Schulen zu vergebende Merkmale.<br>Merkmal S1-S4 sind spezielle Statistikmerkmale, die zur Eingabe und Auswahl von Statistischen Daten genutzt werden, die in MAGELLAN nicht verwaltet werden.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Konfessionen**
Wegweiser       | Schüler > Daten 1 > Konfession
Beschreibung    | Die Konfession des Schülers. <br>Beispiel: röm-kath., ev. etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Krankenkassen**
Wegweiser       | Schüler > Daten 4 > Sonstige Daten > Krankenkasse
Beschreibung    | Die Krankenkasse des Schülers. Beispiel: AOK
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Kreise**
Wegweiser       | Verzeichnisse > Postleitzahlen > Kreise
Beschreibung    | Landkreise Deutschlands. Gehören zum Postleitzahlenverzeichnis und werden von uns vorgegeben!
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | **Lehraemter**
Wegweiser       | Lehrer > Daten 3 > Lehrämter
Beschreibung    | Die Lehrämter des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerAbgaenge**
Wegweiser       | Lehrer > Daten 2 > Abgangsart
Beschreibung    | Die Abgangsarten des Lehrers von einer Schule. Beispiel: Tod, Beurl. aus Erziehungsurlaub
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerAusbildung**
Wegweiser       | Lehrer > Daten 2 > Ausbildung
Beschreibung    | Die Ausbildung des Lehrers
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerFehlgruende**
Wegweiser       | Lehrer > Auswahlliste > Bearbeiten oder Rechtsklick > Fehlzeiten
Beschreibung    | Erfassen der Lehrerfehlzeiten
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerFunktionen**
Wegweiser       | Lehrer > Daten 3 > Funktion 1-8
Beschreibung    | Die Funktionen des Lehrers. Beispiel: Klassenlehrer, Vertrauenslehrer etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerMerkmale**
Wegweiser       | Lehrer > Merkmale > Merkmal A1-A6<br>Lehrer > Merkmale > Merkmal S1-S4
Beschreibung    | Merkmal A1-A6 sind frei für die Schulen zu vergebende Merkmale.<br>Merkmal S1-S4 sind spezielle Statistikmerkmale, die zur Eingabe und Auswahl von Statistischen Daten genutzt werden, die in MAGELLAN nicht verwaltet werden
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **LehrerPruefungsbezuege**
Wegweiser       | Lehrer > Daten 3 > Prüfungsbezug
Beschreibung    | Die Prüfungsbezüge des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerZugaenge**
Wegweiser       | Lehrer > Daten 2 > Zugangsart
Beschreibung    | Die Zugangsarten des Lehrers an die Schule. Beispiel: Zugang aus dem Privatschuldienst
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **LehrerKategorien**
Wegweiser       | Lehrer > Daten 1 > Kategorie
Beschreibung    | Kategorie des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Mandantenkategorien**
Wegweiser       | Mandanten > Daten 1 > Kategorie
Beschreibung    | Kategorie der Schule
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Kurssprachen**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Muttersprachen**
Wegweiser       | Schüler > Daten 2 > Muttersprache
Beschreibung    | Muttersprache oder Verkehrssprache des Schülers. Beispiel: Italienisch
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Verkehrssprache**
Wegweiser       | Schüler > Daten 2 > Verkehrssprache
Beschreibung    | Muttersprache oder Verkehrssprache des Schülers. Beispiel: Italienisch
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Nachpruefungen**
Wegweiser       | Schüler > Laufbahn > Allgemein > Nachprüfung
Beschreibung    | Art der Nachprüfung
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Noten**
Wegweiser       | Schüler > Zeugnis > Leistungen > Schriftl. Note 1-4<br>Schüler > Zeugnis > Leistungen > Mündl. Note<br>Schüler > Zeugnis > Leistungen > Endnote<br>Schüler > Zeugnis > Leistungen > Endnote (Gesamt)
Beschreibung    | Noten der Fächer eines Schülers. Beispiel: Deutsch – Sehr gut (1), Mathematik – Befriedigend (3)
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **Personenkategorien**
Wegweiser       | Personen > Daten > Kategorie
Beschreibung    | Kategorie der Person für sonstiges Personal. Beispiel: Hausmeister, Gärtner, Putzkraft etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Stadtbezirke**
Wegweiser       | Verzeichnisse > Postleitzahlen > Stadtbezirke
Beschreibung    | Stadtbezirke einer Stadt. Gehören zum Postleitzahlenverzeichnis.
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | **Postleitzahlen**
Wegweiser       | Schüler > Daten 1 > Postleitzahl<br>Bewerber > Daten 1 > Postleitzahl<br>Lehrer > Daten 1 > Postleitzahl<br>Mandanten > Daten 1 > Postleitzahl<br>Personen > Daten > Postleitzahl<br>Sorgeberechtigte > Daten > Postleitzahl<br>Betriebe > Daten 1 > Postleitzahl<br>Schulen > Daten 1 > Postleitzahl<br>Adressen > Daten 1 > Postleitzahl
Beschreibung    | Postleitzahlen Deutschlands. Gehören zum Postleitzahlenver-zeichnis und werden von uns vorgegeben!
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | **RelGruende**
Wegweiser       | Schüler > Daten 1 > Rel.-Grund
Beschreibung    | Grund der (nicht) Teilnahme am Religionsunterricht.<br>Beispiel: Mangel an Lehrpersonal, Mangel an Schüler mit entsprechender Konfession
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **RelTeilnahmen**
Wegweiser       | Schüler > Daten 1 > Rel.-Teilnahme
Beschreibung    | Teilnahme des Schülers am Religionsunterricht.<br>Beispiel: Teilnahme am evangelischen Unterricht
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **RelWuensche**
Wegweiser       | Schüler > Daten 1 > Rel.-Wunsch
Beschreibung    | Wunsch des Schülers zur Teilnahme an bestimmten Religionsunterricht. <br>Beispiel: Teilnahme am röm-kath. Unterricht.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchuelerArten**
Wegweiser       | Schüler > Extras > Schülerart > Schülerart
Beschreibung    | Art des Schülers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchuelerFehlgruende**
Wegweiser       | Schüler > Bearbeiten > Fehlzeiten > Grund
Beschreibung    | Gründe für Fehlzeiten des Schülers. Beispiel: Krankheit
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchuelerFunktionen**
Wegweiser       | Schüler > Daten 3 > Funktionen > Funktion 1-8
Beschreibung    | Die Funktionen des Schülers. Beispiel: Klassensprecher, Schülersprecher etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchuelerMerkmale**
Wegweiser       | Schüler > Merkmale > Merkmal A1-A6
Beschreibung    | Merkmal A1-A6 sind frei für die Schulen zu vergebende Merkmale.<br>Merkmal S1-S10 sind spezielle Statistikmerkmale, die zur Eingabe und Auswahl von Statistischen Daten genutzt werden, die in MAGELLAN nicht verwaltet werden.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchuelerProfile**
Wegweiser       | Schüler > Daten 3 > Verschiedenes > Profil
Beschreibung    | Profil des Schülers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schularten**
Wegweiser       | Klassen > Daten > Schulart
Beschreibung    | Bei Schulartübergreifenden Schulen, die Schulart pro Klasse. Beispiel: Kolleg, Förderschule etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schularten**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchulartenHerkunft**
Wegweiser       | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulart
Beschreibung    | Schulart Schülers der zuvor besuchten Schule. <br>Beispiel: siehe Schularten
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchulformenHerkunft**
Wegweiser       | Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulform
Beschreibung    | Die Schulform der zuletzt besuchten Schule.Beispiel: siehe Schulformen
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SchulformenUebergang**
Wegweiser       | Schüler > Zugang/Abgang > Abgang > An Schulform
Beschreibung    | Die Schulform beim Abgang des Schülers an eine andere Schule.Beispiel: siehe Schulformen
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schulstati**
Wegweiser       | Mandanten > Daten 1 > Schulstatus
Beschreibung    | Status der Schule.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schulstellen**
Wegweiser       | Klassen > Daten > Schulstelle
Beschreibung    | Schulstelle der Klasse.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schultraeger**
Wegweiser       | Mandanten > Daten 1 > Schulträger
Beschreibung    | Träger der Schule. Beispiel: Freier Träger, Land etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Schulzweige**
Wegweiser       | Lehrer > Daten 2 > Schulzweig
Beschreibung    | Schulzweig des Lehrers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **SorgebeFunktionen**
Wegweiser       | Sorgeberechtigte > Daten > Funktion 1-8
Beschreibung    | Die Funktionen der Sorgeberechtigten. Beispiel: Elternsprecher etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Sprachgruppen**
Wegweiser       | Schüler > Daten 1 > Staatsangehörigkeit > Sprachgruppe
Beschreibung    | Sprachgruppe des Schülers. Zusätzliche Erfassung einer Sprache des Schülers, ähnlich Muttersprache.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Staatsangehoerigkeiten**
Wegweiser       | Schüler > Daten 1 > Staatsangehörigkeit > Staatsangeh. 1<br>Schüler > Daten 1 > Staatsangehörigkeit > Staatsangeh. 2
Beschreibung    | Staatsangehörigkeiten des Schülers. Beispiel: Chinesisch und Britisch,Deutsch etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Uebergangsarten**
Wegweiser       | Schüler > Zugang/Abgang > Übergang
Beschreibung    | Übergang des Schülers auf eine andere Schule. Beispiel: Abgang auf Grundschule
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Umschulungsmerkmale**
Wegweiser       | Schüler > Daten 2 > Umschulung > Umschulung
Beschreibung    | Art der Umschulung des Schülers. <br>Beispiel: Schüler ist Umschüler, oder Umschulung auf XYZ
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Unterrichtsarten**
Wegweiser       | Schüler > Zeugnis > Fächer > Unterrichtsart
Beschreibung    | Unterrichtsart des Faches. Beispiel: Arbeitsgemeinschaft, Grundkurs, Lernfeld etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Unterstuetzungen**
Wegweiser       | Schüler > Daten 3 > Verschiedenes > Unterstützung
Beschreibung    | Unterstützung für den Schüler.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Verkehrsmittel**
Wegweiser       | Schüler > Daten 4 > Beförderung > Verkehrsmittel
Beschreibung    | Verkehrsmittel bei Unterstützung der Beförderung für den Schüler. Beispiel: Bus, Bahn etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Versetzungsarten**
Wegweiser       | Schüler > Laufbahn > Allgemein > Versetzungsart
Beschreibung    | Die Versetzungsart des Schülers am Ende des Schuljahres.<br>Beispiel: Schüler freiwillig zurück, Nachprüfung bestanden
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Versicherungsarten**
Wegweiser       | Schüler > Daten 4 > Sonstige Daten > Versicherungsart
Beschreibung    | Art der Versicherung des Schülers.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Vertragsarten**
Wegweiser       | Schüler > Ausbildung > Liste der Ausbildungsbetriebe > Vertragsart
Beschreibung    | Art des Ausbildungsvertrages des Schülers. Beispiel: Praktikant, Auszubildender etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Verordnungen**
Wegweiser       | Verzeichnisse > Verordnungen<br>Abitur > Qualififikation
Beschreibung    | Angabe des Skriptes zur Berechnung verschiedenster Qualifikationen, z.B. Mittelstufe, Abitur oder BBS
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Wiederholungsarten**
Wegweiser       | Schüler > Laufbahn > Allgemein > Wiederholungsart
Beschreibung    | Wiederholungsart des Schülers am Ende des Schuljahres. Beispiel: Freiwillige Wiederholung etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Wohnformen**
Wegweiser       | Schüler > Daten 1 > Wohnform
Beschreibung    | Wohnform des Schülers. Beispiel: Heim, Betreutes Wohnen, WG etc.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Entscheidungen**
Wegweiser       | Schüler > Laufbahn > Allgemein > Entscheidung
Beschreibung    | Schullaufbahnentscheidung, z.B. aus Übergeordneter Orientierungsstufe.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **FachNiveaus**
Wegweiser       | Verzeichnisse > Fachtafeln<br>Schüler > Zeugnis > Fächer
Beschreibung    | Niveaustufe in der das Fach unterrichtet wird.
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Banken**
Wegweiser       | Schüler > Daten 4 > Beförderung > Bank<br>Mandanten > Daten 2 > Bank
Beschreibung    | Kontodaten zum Schüler und Mandanten.
Mandantenbezug  | Nein
Import          | PLZ
**Verzeichnis** | **Abteilungen**
Wegweiser       | Mandant > Daten<br>Klasse > Daten1
Beschreibung    | Abteilungen der Schule
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **Fachtafeln**
Wegweiser       | Verzeichnisse > Fachtafeln
Beschreibung    | Vorlage Fächerkanon zur Zuweisung an Schüler in die Fachdaten
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Lehrer-Soll-Schlüssel**
Wegweiser       | Lehrer > Soll-Berechnung
Beschreibung    | -
Mandantenbezug  | Nein
Import          | Katalog
**Verzeichnis** | **Raeume**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Ja
Import          | Katalog
**Verzeichnis** | **Zeitraeume**
Wegweiser       | Verzeichnisse > Zeiträume
Beschreibung    | Angabe der Schulhalbjahre als Rahmen der zeitlichen Abgrenzung zum Speichern Zeitraumbezogener Daten
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **ASVArten**
Wegweiser       | Verzeichnisse > Arten (ASV)<br>Schüler > Zeugnis > Arbeits- und Sozialverhalten
Beschreibung    | Einordnungarten für Arbeits- und Sozialverhalten
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **ASVBewertungen**
Wegweiser       | Verzeichnisse > Bewertungen (ASV)<br>Schüler > Zeugnis > Arbeits- und Sozialverhalten
Beschreibung    | Bewertungsart für Arbeits- und Sozialverhalten
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **ASVKategorien**
Wegweiser       | Verzeichnisse > Kategorien (ASV)<br>Schüler > Zeugnis > Arbeits- und Sozialverhalten
Beschreibung    | Kategoriesierungsarten für Arbeits- und Sozialverhalten
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **ASVTafelKategorien**
Wegweiser       | Verzeichnisse > Tafeln (ASV) > Tafel-Kategorien<br>Schüler > Zeugnis > Arbeits- und Sozialverhalten
Beschreibung    | Tafeln- und Tafel-Kategorien gehören zusammen. Es können ASV-Tafeln in Kategorien angelegt werden.
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **Zeugnisbemerkungen**
Wegweiser       | Verzeichnisse > Zeugnisbemerkungen<br>Schüler > Zeugnis > Bemerkungen / Formulare
Beschreibung    | Vorformulierte personalisierbare Zeugnisbemerkungen, die den Schülern für die Zeugnisse zugewiesen werden können.
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **Zeugnisbeurteilungen**
Wegweiser       | Verzeichnisse > Zeugnisbeurteilungen<br>Schüler > Zeugnis > Leistungen
Beschreibung    | Vorformulierte Beurteilungstexte, die den Schülern für die Zeugnisse zugewiesen werden können.
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **Zeugnisformulare**
Wegweiser       | Verzeichnisse > Zeugnisformulare<br>Schüler > Zeugnis > Bemerkungen / Formulare
Beschreibung    | Zeugnisformulare (Crystal Reports Dateien), die den Schülern als mögliche Zeugnisse zum Druck zugewiesen werden können.
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **Sportfeste**
Wegweiser       | Verzeichnisse > Sportfeste<br>Sportfeste
Beschreibung    | Ein auszurichtendes Sportfest mit jeweils eigenen Regualieren, z.B Schul-Sportfest oder Bundesjugendspiele
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **Wettkaempfe**
Wegweiser       | Verzeichnisse > Wettkämpfe
Beschreibung    | Wettkämpfe als Gruppierung für Wettkampf-Disziplinen, z.B. Geräteturnen, Schwimmen, Leichtathletik
Mandantenbezug  | Ja
Import          | Nein
**Verzeichnis** | **MandantenMerkmale**
Wegweiser       | Verzeichnisse > Merkmale (Mandanten)<br>Mandanten > Merkmale A1-A6
Beschreibung    | Freie Merkmale für die es sonst keine Abbildung in MAGELLAN gibt.
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **Schulenmerkmale**
Wegweiser       | Verzeichnisse > Merkmale (Schulen)<br>Schulen > Daten > Merkmale A1-A6
Beschreibung    | Freie Merkmale für die es sonst keine Abbildung in MAGELLAN gibt.
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **Sopaedfoerderungen**
Wegweiser       | Verzeichnisse > Förderbedarf<br>Schüler > Daten 4 > Beeinträchtigung und Fördermaßnahmen
Beschreibung    | Benötigter Förderbedarf bei Schülern
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **Adressekategorien**
Wegweiser       | Verzeichnisse > Kategorien (Adressen)<br>Adressen > Daten > Kategorie
Beschreibung    | Kategorisierung von Adressen zur Filterung und Sortierung
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **Bewerbungsempfehlungen**
Wegweiser       | Verzeichnisse > Bewerbungsempfehlungen<br>Schüler > Daten 2 > Ext. Empfehlung
Beschreibung    | Die mitgebrachte Empfehlung, z.B. Gymnasiumsempfehlung der Grundschule
Mandantenbezug  | Nein
Import          | Nein
**Verzeichnis** | **Haertefaelle**
Wegweiser       | -
Beschreibung    | -
Mandantenbezug  | Nein
Import          | Nein

## Verzeichnisse mit Vorgaben

Einige Schlüsselverzeichnisse enthalten vorgegebene Schlüssel, die eventuell beim Erstellen der Statistik in die entsprechenden Schlüssel des Statistikamtes umgesetzt werden müssen. Da nicht jedes Schlüsselverzeichnis in jedem Bundesland statistisch relevant ist, enthalten viele SchlüsselVerzeichnisse allgemeine nicht statistisch relevante Schlüssel, die für die Schulen für die tägliche Arbeit und Verwaltung ihrer Daten von Wichtigkeit sind. Diese Datensätze werden dann ohne das Feld „Schlüssel“ eingetragen.

Folgende Schlüsselverzeichnisse enthalten Vorgaben:

Verzeichnis         | Bedeutung
------------------- | ---------
00_Fachstati        | enthält die Fachstatus zum Austausch mit DAVINCI
00_Noten            | enthält die in Deutschland übliche Noten- und Punktgebung
00_Unterrichtsarten | enthält die typischen Unterrichtsarten
