# Schleswig-Holstein

Dieses Kapitel beschreibt für Allgemeinbildende Schulen in Schleswig-Holstein die benötigten Schritte zum Erstellen der Schnittstellendateien zur elektronischen Landesstatistik im Statistik-Online-Verfahren für das Schuljahr 2021/2022.

!!! warning "Wichtig"

    Bitte beachten Sie, mit dem kommenden MAGELLAN 8 Serviceupdate 8.0.6 steht die überarbeitete Schnittstelle zur Verfügung.

!!! info "Hinweis"
     Sollten **Berufsbildende Schulen** Schulen an der Umsetzung der elektronischen Landesstatistik in Schleswig-Holstein interessiert sein, bitten wir Sie sich unter office@stueber.de bei STÜBER SYSTEMS zu melden.

## Einführung

Auf Basis der erfassten Daten in MAGELLAN und DAVINCI können Sie die Herbststatistik für das Statistikamt bzw. das Ministerium vollständig elektronisch erstellen. Voraussetzung dafür ist eine Lizenz für das jeweilige Statistikjahr.
Hier erhalten Sie eine Übersicht über die Schnittstellendateien, und welche von MAGELLAN 8 unterstützt werden:

 Datei                  | Kürzel | Unterstützt   | Schulart  | Inhalt
 ---------------------- | ------ | ------------- | --------- | ------
 XXX_DATLD_JJJJMMTT.TXT | LD     | X             | ABS / BBS | Die Leitdatei enthält Daten zu Ihrer Schule.
 XXX_DATLE_JJJJMMTT.TXT | LE     | X             | ABS / BBS | Die Lehrerdatei enthält Daten zum Lehrer im aktuellen Schuljahr.
 XXX_DATSA_JJJJMMTT.TXT | SA     | X             | ABS       | Die Schülerdatei enthält Daten der Schüler und gegebenen Fächer im aktuellen Schuljahr.
 XXX_DATEA_JJJJMMTT.TXT | EA     | X             | ABS       | Die Entlassenendatei entält Daten der entlassenen Schüler im vorangegangenen und aktuellen Schuljahr.
 XXX_DATSB_JJJJMMTT.TXT | SB     | -             | BBS       | Die Schülerdatei enthält Daten der Schüler im aktuellen Schuljahr.
 XXX_DATEB_JJJJMMTT.TXT | EB     | -             | BBS       | Die Entlassenendatei entält Daten der entlassenen Schüler im vorangegangenen und aktuellen Schuljahr.
 XXX_DATFB_JJJJMMTT.TXT | FB     | -             | BBS       | Die Fächerdatei entält Daten der gegebenen Fächer aktuellen Schuljahr.
 XXX_DATOS_JJJJMMTT.TXT | OS     | -             | BBS       | Die Oberstufendatei enthält Daten zu den Kursen in der Oberstufe.

!!! info "Hinweis"
    Die Angabe `XXX` steht für die Schulnummer der Schule und `JJJJMMTT` für das Erstellungsdatum z.B. 20210904.

    Ist beispielsweise die Lehrerdatei am 05.09.2021 von der Schule 12345 erstellt worden, so erhält sie den Dateinamen 12345_LE_20210905.TXT.

Wie Sie diese Dateien an das Statistikamt versenden, wird Ihnen direkt durch das Statistikamt mitgeteilt.

Notwendige Schritte:

1. Schritt: [Statistikschlüssel bereinigen und aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Statistisch relevante Daten in DAVINCI bzw. MAGELLAN eingeben
3. Schritt: Kurswahlen (nur für Gymnasien/Gesamtschulen mit Oberstufe)
4. Schritt: Lehrer (Soll-Ist-Berechnung) von DAVINCI nach MAGELLAN übertragen
5. Schritt: [Statistikdaten aus DAVINCI exportieren](../dav.statistikdaten-exportieren.md)
6. Schritt: [Datenprüfung](../datenpruefung.md)
7. Schritt: [Statistikdateien erzeugen](../statistikdaten.erstellen.md)

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistisch relevante Daten eingeben

Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang, in einer tabellarischen Übersicht.

!!! warning "Wichtig"
    **Statistikkürzel**: Voraussetzung für das Ausspielen der Daten in das Statistikformat ist die Angabe des Feldes ```Klassen > Daten 1 > Statistikkürzel```. Das Feld kann beliebig eingetragen werden und sollte eindeutig benannt sein. Üblicherweise wird hier einfach das Klassenkürzel wiederholt. Schüler, für deren Klasse kein Statistikkürzel eingetragen ist, werden statistisch nicht berücksichtigt.

Statistikfeld | Datenfeld in MAGELLAN/DAVINCI  | Beschreibung
------------- | ------------------------------ | ------------
--            | MAGELLAN:<br>`Klassen > Daten > Statistikkürzel` | Über das Statistikkürzel steuern Sie, ob diese Klasse und dessen Schüler statistisch relevant sind und in den Statistikdateien berücksichtigt werden sollen.
--            | MAGELLAN:<br>`Schüler > Daten 3 > Verschiedenes > Gastschüler` | Wenn Sie den Haken beim Gastschüler setzen, wird der Schüler nicht mit in der Statistik berücksichtigt.

## Eingaben in DAVINCI

!!! info "Hinweis"
    Sie müssen zusätzliche Eingaben im Kurs- und Stundenplanmodul von DAVINCI vornehmen.
    Genauere Informationen zu den Eingaben für DAVINCI finden Sie in der nachfolgenden tabellarischen Übersicht.

Überprüfen Sie in DAVINCI (bei Gymnasien/Gesamtschulen) bitte folgende Punkte:

Wo                                | Was
--------------------------------- | ---
Stammdaten > Klassen              | Bitte erfassen Sie in der Spalte ID für alle Oberstufen Klassen die MAGELLAN-ID.
Stammdaten > Fächer               | Für alle Fächer muss in der Spalte „Schlüssel“ der vom Statistikamt vorgeschriebene Schlüssel erfasst werden, z.B. „014“ für das Fach Deutsch.
Veranstaltungsübersicht > Klassen | Achten Sie darauf alle Leistungs- und Grundkurse eingetragen zu haben.

Wir empfehlen Ihnen beim Abgleich der IDs der Schüler, Klassen, Lehrer und Fächer sicherheitshalber wie folgt vorzugehen:

1. Öffnen Sie MAGELLAN und wechseln Sie in die entsprechende Ansicht „Schüler“, „Klassen“ oder „Lehrer“. Die Fächerliste finden unter „Verzeichnisse“, „Fächer“.
2. Exportieren Sie die Auswahlliste nach Excel und drucken Sie diese zur Vorlage aus.
3. Öffnen Sie DAVINCI und wechseln Sie in die entsprechende Ansicht.
4. Vergleichen Sie die IDs und Kürzel Ihrer Vorlage mit den IDs und Kürzel in der DAVINCI Ansicht und korrigieren Sie ggf. in DAVINCI.

## Kurswahldaten und Lehrerdaten von DAVINCI nach MAGELLAN übertragen

### Kurswahl

Schulen mit Oberstufe müssen ihre Kurswahldaten für die Statistik in DAVINCI mit MAGELLAN abgleichen. Nachdem die IDs in beiden Programmen übereinstimmen, sollten sie die Kurswahldaten (Schülerkurswahl) übernehmen, wie im DAVINCI Handbuch im Kapitel „Spezielles“ unter „Datenaustausch mit MAGELLAN“, „Daten nach MAGELLAN übergeben“ beschrieben.

### Lehrerdaten

Nachdem in DAVINCI unter `Stammdaten > Lehrer` die Solländerungsgründe erfasst wurden, müssen diese Informationen von DAVINCI nach MAGELLAN abgeglichen werden. Der Übertrag erfolgt beim Abgleich des Punktes „Lehrer“.

!!! info "Hinweis"
     Bitte beachten Sie, dass Sie nur mit Kopien der DAVINCI Datei und MAGELLAN Datenbank arbeiten!

## Statistikdaten aus DAVINCI exportieren

Als Schule mit Oberstufe müssen Sie aus DAVINCI statistikrelevante Daten exportieren. Diese exportierten Daten werden dann zur eigentlichen Statistikerstellung in MAGELLAN verwendet.
So exportieren Sie Daten aus DAVINCI:

1. Wählen Sie unter `Plan > Importieren und Exportieren > Statistikdaten exportieren` aus und dann mit `Statistik Schleswig-Holstein exportieren`
2. Geben Sie eine Exportdatei an. Klicken Sie auf `OK`.
3. Die Daten werden jetzt in die angegebene Datei exportiert.

## Besonderheiten

Es kann vorkommen, dass für den aktuellen Statistikzeitraum bestimmte Besonderheiten aufgrund von Schlüsseländerungen oder speziellen Schnittstellenänderungen ihre besondere Aufmerksamkeit benötigen. In einem solchen Falle stehen alle verfügbaren Informationen dazu in diesem Kapitel.

### Zur Statistik 2021/2022

-

### Zur Statistik 2020/2021

#### 15.06.2020

Das Amt hat fälschlicherweise einen Schlüssel aus der Tabelle "GTB" für die Ganztagsbetreuung entfernt. Dieser fehlt ggf. auch in Ihrer MAGELLAN Installation im Schlüsselverzeichnis "Betreuungsformen" und müsste, sofern dieser für Sie relevant ist, manuell nachgetragen werden:

Kürzel     | Schlüssel | Bezeichnung                        | Gültig von
---------- | --------- | ---------------------------------- | ----------
Teilg. GTS | 4         | teilweise gebundene Ganztagsschule | 01.08.2012

## Statistikdateien

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Alle Statistikdateien enthalten folgende Statistikfelder und werden hier einmalig dargestellt.

**Statistikfeld** | **Beschreibung**
----------------- | ----------------
STATNR            | Statistiknummer - Fester Wert (0211) für die Statistikdatei. Wird vorbelegt.
DATSA             | Datensatzbezeichnung - Jede Statistikdatei enthält einen Kürzel der vorbelegt wird.<br>LD = Leitdatei<br>LE = Lehrerdatei<br>OS = Oberstufendatei<br>SA = Schülerdatei ABS<br>EA = Entlassenendatei ABS.
JAHR              | Jahr des Stichtages. Berechnet sich aus dem angegeben Stichtag.

### Schuldaten

Die Leitdatei enthält Daten zur Schule. Alle Daten der Datei kommen aus MAGELLAN.

**Spalte**        | **Beschreibung**
----------------- | ----------------
**Statistikfeld** | **GKZ - Gemeindekennziffer (GKZ)**
Datenfeld         | Mandanten > Daten 1 > Land<br>Mandanten > Daten 1 > Gemeinde (Verzeichnisse > Gemeinden)
Beschreibung      | Geben Sie im Feld `Land` (das Feld vor „PLZ“) die möglichen Länderkürzel ein. Möglich sind D für Deutschland (oder leer), oder DK für Dänemark.<br>Im Feld `Gemeinde` geben Sie die Gemeindekennziffer an. Der korrekte Schlüssel wird aus diesen Angaben berechnet.
**Statistikfeld** | **DSTNR - Dienststellennummer**
Datenfeld         | Mandanten > Daten 1 > Schulnummer.
Beschreibung      | Geben Sie die vom Land vergebene Schulnummer an.
**Statistikfeld** | **SFORM - Schulform (SFORM)**
Datenfeld         | Mandanten > Daten 2 > Schulformen (Verzeichnisse > Schulformen)
Beschreibung      | Es wird die erste Schulform aus der Liste der Schulformen berücksichtigt. Geben Sie Ihre Hauptschulform entsprechend der Statistikvorgaben hier an.
**Statistikfeld** | **SNAME1 - Schulname 1**
Datenfeld         | Mandanten > Daten 1 > Name 1
Beschreibung      | Name 1 der Schule
**Statistikfeld** | **SNAME2 - Schulname 2**
Datenfeld         | Mandanten > Daten 1 > Name 2
Beschreibung      | Name 2 der Schule
**Statistikfeld** | **RSTA - Rechtsstatus**
Datenfeld         | Mandanten > Daten 1 > Rechtsstatus
Beschreibung      | Wählen Sie hier den Rechtsstatus der Schule aus.
**Statistikfeld** | **TRAEG - Schulträger (TRAEG)**
Datenfeld         | Mandanten > Daten 1 > Schulträger (Verzeichnisse > Schulträger)
Beschreibung      | Wählen Sie hier den Rechtsstatus der Schule aus.
**Statistikfeld** | **TNAM - Name des Schulträgers**
Datenfeld         | -
Beschreibung      | Dieses Statistikfeld wird aktuell nicht unterstützt.
**Statistikfeld** | **STRHSN - Straße und Hausnummer**
Datenfeld         | Mandanten > Daten 1 > Straße
Beschreibung      | Geben Sie die Straße der Schule ein.
**Statistikfeld** | **PLZ - Postleitzahl**
Datenfeld         | Mandanten > Daten 1 > PLZ
Beschreibung      | Geben Sie die Postleitzahl der Schule ein.
**Statistikfeld** | **ORT**
Datenfeld         | Mandanten > Daten 1 > Ort
Beschreibung      | Geben Sie den Ort der Schule ein.
**Statistikfeld** | **VORW - Telefonvorwahl**
Datenfeld         | -
Beschreibung      | Dieses Statistikfeld wird aktuell nicht unterstützt.
**Statistikfeld** | **TEL - Telefon**
Datenfeld         | Mandanten > Daten 1 > Telefon
Beschreibung      | Geben Sie die Telefonnummer der Schule ein.
**Statistikfeld** | **FAX - Telefax**
Datenfeld         | Mandanten > Daten 1 > Telefax
Beschreibung      | Geben Sie die Faxnummer der Schule ein.
**Statistikfeld** | **EMAIL**
Datenfeld         | Mandanten > Daten 1 > E-Mail
Beschreibung      | Geben Sie die Email-Adresse der Schule ein.
**Statistikfeld** | **SLEIT - Schulleitung**
Datenfeld         | Mandanten > Daten 1 > Schulleiter<br>Lehrer > Daten 1 > Vorname<br>Lehrer > Daten 1 > Nachname
Beschreibung      | Wählen Sie den Schulleiter der Schule aus. Der Schulleiter muss zuvor als Lehrer mit Vor- und Nachnamen eingetragen worden sein.
**Statistikfeld** | **SLGS - Geschlecht der Schulleitung**
Datenfeld         | Mandanten > Daten 1 > Schulleiter<br>Lehrer > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie den Schulleiter der Schule aus. Der Schulleiter muss zuvor als Lehrer mit seinem Geschlecht eingetragen worden sein.
**Statistikfeld** | **GTB - Ganztagsbetrieb** (GTB)
Datenfeld         | Mandanten > Daten 1 > Betreuungsform (Verzeichnisse > Betreuungsformen)
Beschreibung      | Geben Sie die Betreuungsform der Schule ein.
**Statistikfeld** | **VORWFAX - Faxvorwahl**
Datenfeld         | -
Beschreibung      | Dieses Statistikfeld wird aktuell nicht unterstützt.
**Statistikfeld** | **URL**
Datenfeld         | Mandanten > Daten 1 > Internet
Beschreibung      | Geben Sie die Internetpräsenz der Schule ein.
**Statistikfeld** | **SVP**
Datenfeld         | -
Beschreibung      | Wir geben hier fest den Wert „MAGELLAN 7“ aus
**Statistikfeld** | **VERSION**
Datenfeld         | -
Beschreibung      | Wir geben hier die aktuell installierte MAGELLAN 7 Version (Registry Wert) aus.

### Schüler- und Klassendaten

Folgende Statistikfelder können in mehreren Statistikdateien ausgegeben werden. Die Eingabe in MAGELLAN erfolgt aber stets an der gleichen Stelle, weshalb wir hier die Felder lediglich einmal erläutern und angeben in welchen Statistikdateien diese ausgespielt werden. Einige der Daten können aus der Stundenverwaltung DAVINCI stammen. Aus diesem Grunde unterscheiden wir in der Spalte `Datenfeld` zwischen MAGELLAN: und DAVINCI: Angaben.

**Spalte**        | **Beschreibung**  
----------------- | ----------------
**Statistikfeld** | **SNR - Schülernummer**
Statistikdateien  | SA, EA, SB, EB
Datenfeld         | MAGELLAN: Schüler > Liste der Schüler > ID
Beschreibung      | Die ID des Schülers wird beim Anlegen des Schülers automatisch erzeugt und ist eindeutig. Sie wird beim Erstellen der Statistikdateien automatisch gesetzt.
**Statistikfeld** | **SART - Schulart (SART)**  
Statistikdateien  | SA, EA, FB
Datenfeld         | MAGELLAN: Klassen > Daten > Schulart (Verzeichnisse > Schularten)
Beschreibung      | Geben Sie hier die Schulart ein.
**Statistikfeld** | **KLNM - Name der Klasse**
Statistikdateien  | SA, SB
Datenfeld         | MAGELLAN: Klassen > Daten > Statistikkürzel
Beschreibung      | Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie das Feld leer lassen.
**Statistikfeld** | **KLK - Klassentyp (Klasse, Lerngruppe, Kurs)**
Statistikdateien  | SA
Datenfeld         | <span style="color:blue">Klassen > Zeiträume > Klassenstufe<br>Klassen > Zeiträume > Jahrgang</span>
Beschreibung      | Der Statistikwert wird entweder direkt aus der Klassenstufe gelesen, oder berechnet sich anhand der Kombination aus Klassenstufe und Jahrgang.<br>Der Jahrgang wird für  Klassenstufenübergreifende Klassen in Primarstufe (Jahrgang 1-4), Sekundarstufe I (Jahrgang 5-9) und Sekundarstufe II (Jahrgang 10-13) in Kombination mit der Klassenstufe `ÜGR` genutzt.
**Statistikfeld** | **GS - Geschlecht**
Statistikdateien  | SA
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geschlecht  
Beschreibung      | Geben Sie hier das Geschlecht des Schülers ein. Kein Eintrag ergibt Schlüssel 5 = Kein Eintrag ins Geburtsregister
**Statistikfeld** | **GBDAT - Geburtsdatum**
Statistikdateien  | SA, EA, SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geboren am  
Beschreibung      | Geben Sie hier das Geburtsdatum des Schülers ein.
**Statistikfeld** | **STAAT - Staatsangehörigkeit (STAAT)**
Statistikdateien  | SA, EA, SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Staatsangeh. 1 (Verzeichnisse > Staatsangehörigkeiten)
Beschreibung      | Geben Sie hier die Nationalität des Schülers ein.
**Statistikfeld** | **DAZ - Deutsch als Zweitsprache**
Statistikdateien  | SA, EA
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S6 (Verzeichnisse > Merkmale (Schüler) - Bereich S6)  
Beschreibung      | Geben Sie die Teilnahme am Unterricht „Deutsch als Zweitsprache“ an.<br>Keine Eingabe = Leine Teilnahme am DaZ.
**Statistikfeld** | **GEBLAND - Geburtsland (STAAT)**
Statistikdateien  | SA, EA, SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Geburtsland (Verzeichnisse > Staatsangehörigkeiten)
Beschreibung      | Geben Sie hier das Geburtsland des Schülers an.
**Statistikfeld** | **ZUZD - Jahr des Zuzugs nach Deutschland**  
Statistikdateien  | SA, EA, SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > In Deutschland seit
Beschreibung      | Geben Sie hier das das Zuzugsdatum nach Deutschland ein.
**Statistikfeld** | **VERKSPR - Verkehrssprache (VERKSPR)**
Statistikdateien  | SA, EA, SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Sprachgruppe (Verzeichnisse > Sprachgruppen)
Beschreibung      | Geben Sie hier die überwiegend in der Familie gesprochene Sprache ein.
**Statistikfeld** | **KONF Konfession (KONF)**
Statistikdateien  | SA, EA
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Konfession (Verzeichnisse > Konfessionen)
Beschreibung      | Geben Sie hier die Konfession des Schülers ein.
**Statistikfeld** | **GTBU - Ganztagbetrieb**
Statistikdateien  | SA
Datenfeld         | MAGELLAN: Schüler > Extras > Betreuung > Ganztagbetrieb<br>Schüler > Extras > Betreuung > Ganztagbetrieb > Gebunden<br>Schüler > Extras > Betreuung > Ganztagbetrieb > Offen
Beschreibung      | Geben Sie hier mit dem Haken bei `Ganztagbetrieb` an, ob ein Schüler grundsätzlich am Ganztagsbetrieb teilnimmt. Wenn ja, muss ein Wert im Feld `Gebunden` oder `Offen` ausgewählt werden. Die Art der Werte ist egal. Je nachdem welches Feld gefüllt ist, wird folgender Wert ausgespielt:<br>Gebunden = 1 voll gebundene Ganztagsschule<br>Offen = 2 offene Ganztagsschule mit Genehmigung
**Statistikfeld** | **JGSTUF - Jahrgangsstufe (JGSTUF)**
Statistikdateien  | SA, EA, SB, EB, FB, OA
Datenfeld         | MAGELLAN: Klassen > Zeiträume > Klassenstufe (Verzeichnisse > Klassenstufen)
Beschreibung      | Wählen Sie hier die Klassenstufe der Klasse aus.
**Statistikfeld** | **SCHHERK (1 von 3) - Schulische Herkunft (SCHHERK)**
Statistikdateien  | SA
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Bereits besuchte Schulen > Schulform (Verzeichnisse > Schulformen)<br>Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule
Beschreibung      | Geben Sie für neu an die Schule gekommene Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.<br>Beachten Sie bitte dass die „Schulform“ eingetragen sein muss.<br>Ein Schüler wird als Neuzugang erkannt, wenn unter `Schüler > Daten 2 > Zugang > Zugang am` ein Datum erfasst wurde, dass nach dem letzten und vor dem aktuellen Statistiktermin liegt.<br>Für Schüler mit der Klassenstufe 1 (Klassen > Zeiträume > Klassenstufe) geben wir automatisch den Wert für den Schlüssel „Neuaufnahme (in die 1. Jahrgangsstufe)“ aus.
**Statistikfeld** | **SCHHERK (2 von 3) - Schulische Herkunft (SCHHERK)**
Statistikdateien  | SA
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Wiederholer (Häckchen)<br>MAGELLAN > Schüler > Laufbahn > Wiederholungsart (Verzeichnisse > Wiederholungsarten)
Beschreibung      | Setzen Sie bitte für die Schüler im aktuellen Zeitraum das Häkchen für Wiederholer.<br>Wählen Sie im Feld Wiederholungsart einen Wert aus.
**Statistikfeld** | **SCHHERK (3 von 3) - Schulische Herkunft (SCHHERK)**
Statistikdateien  | SA
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Allgemein > Überspringer (Häckchen)
Beschreibung      | Setzen Sie bitte für die Schüler im aktuellen Zeitraum das Häkchen für Überspringer.
**Statistikfeld** | **HWS - Hauptwohnsitz (GKZ)**
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Land<br>Schüler > Daten 1 > Gemeinde
Statistikdateien  | SA, EA, SB, EB
Beschreibung      | Geben Sie im Feld `Land` (das Feld vor „PLZ“) die möglichen Länderkürzel ein. Möglich sind D für Deutschland (oder leer), oder DK für Dänemark.<br>Im Feld `Gemeinde` geben Sie die Gemeindekennziffer an. Der korrekte Schlüssel wird aus diesen Angaben berechnet.
**Statistikfeld** | **G8**
Statistikdateien  | SA, EA
Datenfeld         | MAGELLAN: Klassen > Daten > Schulart<br>Schüler > Daten 3 > Verschiedenes > G8/G9
Beschreibung      | Geben Sie hier die Teilnahme des Schülers am Schulversuch G8 ein.<br>G8 = JA<br>G9 = NEIN<br>Wenn dieses Feld bei Gymnasien nicht gefüllt wird, erhalten die Schüler automatisch den Eintrag „G9“ für Nein.<br>Nur für Gymnasien, wenn Teilnahme am Schulversuch G8. Dazu prüfen wir die Schulart der Klasse, die eingetragen werden muss.
**Statistikfeld** | **FSWP - Förderschwerpunkt (FSWP)**
Statistikdateien  | SA, EA  
Datenfeld         | MAGELLAN: Schüler > Daten 4 > Beeinträchtigung und Fördermaßnahmen > Position<br>Schüler > Daten 4 > Beeinträchtigung und Fördermaßnahmen > Förderschwerpunkt 1 (Verzeichnisse > Förderschwerpunkte)
Beschreibung      | In MAGELLAN können Sie eine Liste der Förderungen angeben. Für die Statistik wird ein Eintrag benötigt. Es wird der Datensatz mit der niedrigsten Position und eingetragenem Förderschwerpunkt 1 ausgewählt. Stellen Sie sicher, dass sich bei mehreren Listeneinträgen, die Werten im Feld Position voneinander unterscheiden.
**Statistikfeld** | **IFÖZ - Zuständiges Förderzentrum (IFÖZ)**  
Statistikdateien  | SA, SB
Datenfeld         | MAGELLAN: Schüler > Daten 4 > Beeinträchtigung und Fördermaßnahmen > Förderzentrum (Schulen)
Beschreibung      | Geben Sie hier das zuständige Förderzentrum an.
**Statistikfeld** | **JERST - Jahr der Ersteinschulung**  
Statistikdateien  | SA, EA
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Grundschuleintritt
Beschreibung      | Geben Sie hier das Datum der Ersteinschulung ein. Wichtig ist lediglich das Jahr.
**Statistikfeld** | **FACH01-20**<br>**KURS (FACH/KURS)**
Statistikdateien  | SA, FB
Datenfeld         | MAGELLAN: Schüler > Zeugnis > Fächer > Fach (Verzeichnisse > Fächer)
Beschreibung      | Geben Sie die Fächer des Schülers ein.
**Statistikfeld** | **UART01-20 - Unterrichtsart (UART)**
Statistikdateien  | SA
Datenfeld         | MAGELLAN: Schüler > Zeugnis > Fächer > Fach (Verzeichnisse > Fächer)<br>Schüler > Zeugnis > Fächer > Unterrichtsart (Verzeichnisse > Unterrichtsarten)<br>Schüler > Zeugnis > Fächer > Fachstatus (Verzeichnisse > Fachstati)
Beschreibung      | Geben Sie die Fächer des Schülers ein.<br>Für die Statistik werden einige besondere Fächer mit deren Fachstatus und der Schüleranzahl erfasst.<br><br>Unterrichtsfach ABS:<br>Fremdsprache, Fach wg. Nichtteilnahme am Religionsunterricht und Wahlpflichtfächer.
**Statistikfeld** | **USPR01-20 - Unterrichtssprache (FACH)**
Statistikdateien  | SA
Datenfeld         | MAGELLAN:Schüler > Zeugnis > Fächer > Sprache (Verzeichnisse Kurssprachen)
Beschreibung      | Geben Sie die mündl. und schriftl. Unterrichtssprache für ein genehmigtes bilinguales Bildungsangebot für fremdsprachlichen Fachunterricht ein.
**Statistikfeld** | **KSNM01-20 - Kursname**
Statistikdateien  | SA
Datenfeld         | -
Beschreibung      | Dieser Wert setzt sich aus den Feldern:<br>FachKuerzel<br>FachKursNr<br>zusammen und wird automatisch berechnet.  
**Statistikfeld** | **STD01-20STD - WochenStunden**
Statistikdateien  | SA, FB
Datenfeld         | -
Beschreibung      | Anzahl der Wochen-Ist-Stunden (pro Fach) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird. Dieser Statistikwert wird aus der Exportdatei [D6, Klassenist] berechnet. Voraussetzung dafür sind identische Einträge in MAGELLAN und DAVINC.<br>Bitte überprüfen Sie in MAGELLAN und DAVINCI:<br>- die Fachkürzel und Fachschlüssel<br>- das Kürzel der verwendeten Unterrichtsart (muss gefüllt sein!)<br>- das Klassenkürzel und die KlassenID
**Statistikfeld** | **MASS - Bildungsgang (MASS)**
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Klassen > Daten > Bildungsgang (Verzeichnisse > Bildungsgänge)
Beschreibung      | Geben Sie hier die Maßnahme/Bildungsgang ein.
**Statistikfeld** | **UFBL - Organisationsform (UFBL)**
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Klassen > Daten > Organisation (Verzeichnisse > Organisationen)
Beschreibung      | Geben Sie hier Unterrichtsform/Blockunterricht ein.
**Statistikfeld** | **NSCH - Nichtschüler**  
Statistikdateien  | EA, EB
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S1 (Verzeichnisse > Merkmale (Schüler) - Bereich S1)
Beschreibung      | Geben Sie hier ein, ob der Schüler ein Nichtschüler ist.<br>Kein Eintrag bedeutet „Nein“.
**Statistikfeld** | **ABSF - Abgebende Schulform (ABSF)**
Statistikdateien  | SB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Bereits besuchte Schulen > Schulform (Verzeichnisse > Schulformen (Herkunft))<br>Schüler > Daten 2 > Herkunftsschule  
Beschreibung      | Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. Beachten Sie bitte, dass die „Schulform“ eingetragen sein muss.
**Statistikfeld** | **LKLST - Letzte Jahrgangsstufe (JGSTUF)**  
Statistikdateien  | SB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Bereits besuchte Schulen > Letzte Klassenstufe (Verzeichnisse > Klassenstufen)<br>Schüler > Daten 2 > Herkunftsschule
Beschreibung      | Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. Beachten Sie bitte, dass die „Letzte Klassenstufe“ eingetragen sein muss.
**Statistikfeld** | **AABS - Letzter Abschluss ABS**  
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss (Verzeichnisse > Abschlüsse (Extern))
Beschreibung      | Geben Sie hier den höchsten erreichten Abschluss an einer Allgemeinbildenden Schule ein.
**Statistikfeld** | **LABS - Letzter Abschluss BBS**
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss (Verzeichnisse > Abschlüsse (Extern))
Beschreibung      | Geben Sie hier den höchsten erreichten berufsbezogenen Abschluss ein.
**Statistikfeld** | **WIEDH - Wiederholer**
Statistikdateien  | SB
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Allgemein > Wiederholer<br> Schüler > Laufbahn > Allgemein > Wiederholungsart
Beschreibung      | Haken Sie das Feld „Wiederholer“ an, wenn der Schüler ein Wiederholer ist. **2021/22-NEU: Geben Sie eine "Freiwillige Wiederholung aufgrund der Coronapandemie" in der Wiederholungsart an.
**Statistikfeld** | **ZUSKURS - Zusatzkurs (ZUSKURS)**
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S2 (Verzeichnisse > Merkmale (Schüler) - Bereich S2)
Beschreibung      | Geben Sie an, ob der Schüler Zusatzkurse für weitere Abschlüsse absolviert.
**Statistikfeld** | **BFKLBS - Bezirksfachklasse / Landesberufsschule**
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Klasse > Merkmale > Merkmal S3 (Verzeichnisse > Merkmale (Klasse) - Bereich S3)<br>Schueler > Statistik > Merkmal S3 (Verzeichnisse > Merkmale (Schüler) - Bereich S3)
Beschreibung      | Geben Sie an, ob sich der Schüler oder alle/viele Schüler der Klasse in einer Bezirksfach- oder Landesklasse befinden. Die Angabe beim Schülermerkmal hat vorrang zur Angabe des Klassenmerkmals, wenn beide eingetragen wurden.
**Statistikfeld** | **ENTL -Endgültiges verlassen des allgemeinbildenden Schulsystems**
Statistikdateien  | EA
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal S4 (Verzeichnisse > Merkmale (Schüler) - Bereich S4)
Beschreibung      | Tragen Sie hier bitte für Abgänger ein, ob der Schüler das allgemeinbildende Schulsystem verlässt oder nicht. Achtung: Wenn der Schüler in einer Klasse < Jahrgang 9 ist, geben wir automatisch den Wert für „Nein, Schüler verbleibt im allgemeinbildenden Schulsystem“ aus. Abiturienten mit Abschluss hingegen erhalten automatisch den Wert "Ja, Schüler verlässt das allgemeinbildende Schulsystem".
**Statistikfeld** | **ABSCHL - Abschluss (ABSCHL)**
Statistikdateien  | EA, EB
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Abschluss > Abschluss 1 Abschluss (Verzeichnisse > Abschlüsse (Intern))
Beschreibung      | Der Statistikwert errechnet sich anhand des Eintrags im Feld „Abschluss 1“ aus dem vorangegangenen Schuljahr. Hinweis: Für alle Abgänger (inaktive Schüler mit Abgangsdatum zwischen dem aktuellen und dem vergangenen Statistiktermin unter `Daten 2 > AbgangAm`), die noch nicht die Schulpflicht erfüllt haben, wird automatisch der Schlüssel für „ohne Abschluss“ in die Statistikdatei übernommen. Schulbesuchsjahre werden am aktuellen Datum und dem Grundschuleintritt errechnet.
**Statistikfeld** | **ABSCHLBS - neu erworbeneder berufsbezogener Abschluss (ABSCHLBS)**
Statistikdateien  | EB
Datenfeld         | MAGELLAN: Schüler > Laufbahn > Abschluss 2 > Abschlussart (Verzeichnisse > Abschlussarten)
Beschreibung      | Geben Sie hier den Erfolg des Bildungsgangs ein.
**Statistikfeld** | **ABINOTE - Abiturnote**
Statistikdateien  | EA, EB
Datenfeld         | MAGELLAN: Schüler > Abschluss > Abschluss 1 > Abschlussnote
Beschreibung      | Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist.
**Statistikfeld** | **INSG - Anzahl der Schüler**
Statistikdateien  | FB
Datenfeld         | -
Beschreibung      | Anzahl der Schüler bestimmter Fächer, siehe UART.Statistikwert wird berechnet.
**Statistikfeld** | **WEIBL - Anzahl weiblicher Schüler**
Statistikdateien  | FB
Datenfeld         | -
Beschreibung      | Anzahl der weiblichen Schüler bestimmter Fächer, siehe UART.Statistikwert wird berechnet.
**Statistikfeld** | **PROFIL**
Statistikdateien  | OB
Datenfeld         | MAGELLAN: Schueler > Daten 3 > ProfilSchueler > Zeugnis > Faecher > Unterrichtsart  
Beschreibung      | Tragen Sie das Profil des Schülers ein. Anhand der Eingabe und des gewählten 3. Prüfungsfach berechnet sich beim entsprechenden Fach der Profilschlüssel.
**Statistikfeld** | **SCHINSG - Anzahl der Schüler**
Statistikdateien  | OB
Datenfeld         | -
Beschreibung      | Anzahl der Schüler (pro Kurs).Statistikwert wird berechnet.
**Statistikfeld** | **SCHWEIBL- Anzahl weiblicher Schüler**
Statistikdateien  | OB
Datenfeld         | -
Beschreibung      | Anzahl der weiblichen Schüler (pro Kurs).Statistikwert wird berechnet.  
**Statistikfeld** | **SCHANDS - Anzahl Schüler anderer Schulen**
Statistikdateien  | FB, OB
Datenfeld         | MAGELLAN: Schüler > Statistik > Merkmal T3
Beschreibung      | Geben Sie im Feld „Merkmal T3“ ein „J“ ein, wenn der Schüler einer anderen Schule den Unterricht besucht. Es wird die Anzahl der Schüler (pro Kurs), die von einer anderen Schule kommen automatisch berechnet.
**Statistikfeld** | **SCHSTD - WochenStunden**
Statistikdateien  | SB
Datenfeld         | -
Beschreibung      | Anzahl der Wochen-Ist-Stunden (pro Schüler) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird. Statistikwert wird berechnet.
**Statistikfeld** | **WOSTD - WochenStunden**
Statistikdateien  | OB
Datenfeld         | -
Beschreibung      | Anzahl der Wochen-Ist-Stunden (pro Kurs) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird. Statistikwert wird berechnet.
**Statistikfeld** | **BERUF - Ausbildungsberuf (BERUF)**
Statistikdateien  | SB, EB
Datenfeld         | MAGELLAN: Schüler > Ausbildung > Beruf (Verzeichnisse > Berufe)
Beschreibung      | Geben Sie hier den Ausbildungsberuf des Schülers ein.
**Statistikfeld** | **UMSCH - Umschulung**
Statistikdateien  | SB
Datenfeld         | MAGELLAN: Schüler > Daten 2 > Umschulung > Umschulung (Verzeichnisse > Umschulungsmerkmale)
Beschreibung      | Bitte erfassen Sie, ob der Schüler ein Umschüler ist.
**Statistikfeld** | **ABSKREIS - Ausbildungsstätte in Kreis**
Statistikdateien  | SB
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Gemeinde
Beschreibung      | Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein. Der Statistikwert wird automatisch daraus errechnet.
**Statistikfeld** | **ABSLAND - Ausbildungsstätte in Bundesland**
Statistikdateien  | SB
Datenfeld         | MAGELLAN: Schüler > Daten 1 > Gemeinde
Beschreibung      | Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein. Der Statistikwert wird automatisch daraus errechnet.

### Lehrerdaten

Einige der Daten können aus der Stundenverwaltung DAVINCI stammen. Aus diesem Grunde unterscheiden wir in der Spalte `Datenfeld` zwischen MAGELLAN: und DAVINCI: Angaben.

**Spalte**        | **Beschreibung**  
----------------- | ----------------
**Statistikfeld** | **DSTNR Dienststellennummer**  
Datenfeld         |Mandanten > Daten 1 > Schulnummer.
Beschreibung      |Geben Sie die vom Land vergebene Schulnummer an.
**Statistikfeld** | **LENR Lehrernummer**  
Datenfeld         | MAGELLAN: Lehrer > Daten 2 > StatistikNr.
Beschreibung      | Geben Sie hier die 7 stellige Statistik Nr. ein.
**Statistikfeld** | **ZUGANG Neuzugang**  
Datenfeld         | MAGELLAN: Lehrer > Daten 2 > Zugang am
Beschreibung      | Geben Sie hier das Datum des Zugangs des Lehrer an Ihre Schule an. Ein Lehrer wird als Neuzugang erkannt, wenn unter Lehrer > Daten 2 > Zugang am ein Datum erfasst wurde, dass nach dem letzten und vor dem aktuellen Statistiktermin liegt.
**Statistikfeld** | **NAME Familienname**  
Datenfeld         | MAGELLAN: Lehrer > Daten 1 > Nachname
Beschreibung      | Geben Sie hier den Nachnamen des Lehrers ein.
**Statistikfeld** | **VNAME Vorname**  
Datenfeld         |  MAGELLAN: Lehrer > Daten 1 > Vorname
Beschreibung      | Geben Sie hier den Vornamen des Lehrers ein.
**Statistikfeld** | **GNAME Geburtsname**  
Datenfeld         |  MAGELLAN: Lehrer > Daten 1 > Geburtsname
Beschreibung      | Geben Sie hier den Geburtsnamen des Lehrers ein.
**Statistikfeld** | **GS Geschlecht**  
Datenfeld         | MAGELLAN: Lehrer > Daten 1 > Geschlecht
Beschreibung      | Wählen Sie hier das Geschlecht des Lehrers aus. Schlüssel 5 = Kein Eintrag ins Geburtsregister
**Statistikfeld** | **GGBDAT Geburtsdatum**  
Datenfeld         | MAGELLAN: Lehrer > Daten 1 > Geboren am
Beschreibung      | Geben Sie hier das Geburtsdatum des Lehrers ein.
**Statistikfeld** | **STAAT Staatsangehörigkeit**  
Datenfeld         | MAGELLAN: Lehrer > Daten 1 > Staatsangeh. 1 (Verzeichnisse > Staatsangehörigkeiten)
Beschreibung      | Geben Sie hier die Nationalität des Lehrers ein.
**Statistikfeld** | **BSCHU Beschäftigungsumfang**  
Datenfeld         | MAGELLAN: Lehrer > Daten 2 > Beschäftigungsverhältnis (Verzeichnisse > Beschäftigungsverhältnis)
Beschreibung      |  Geben Sie hier das Beschäftigungsverhältnis des Lehrers ein.
**Statistikfeld** | **BGRZ Grund Zugang**  
Datenfeld         | MAGELLAN: Lehrer > Daten 2 > Zugangsart(Verzeichnisse > Zugangsarten (Lehrer))
Beschreibung      | Geben Sie hier die Zugangsart des Lehrers ein.
**Statistikfeld** | **BGRA Grund Abgang**  
Datenfeld         | MAGELLAN: Lehrer > Daten 2 > Abgangsart (Verzeichnisse > Abgangsarten (Lehrer))
Beschreibung      | Geben Sie hier die Abgangsart des Lehrers ein.
**Statistikfeld** | **DIST Dienstverhältnis**  
Datenfeld         |  MAGELLAN: Lehrer > Daten 2 > Dienstverhältnis (Verzeichnisse > Dienstverhältnisse)
Beschreibung      |  Geben Sie hier das Dienstverhältnis des Lehrers ein.
**Statistikfeld** | **LAUFB Lehrerlaufbahn**  
Datenfeld         |  MAGELLAN: Lehrer > Daten 3 > Lehramt Typ Lehramt
Beschreibung      | Wählen Sie hier den Lehramtstyp des Lehrers aus.
**Statistikfeld** | **LEBF1-4 Lehrbefähigung 1-4**  
Datenfeld         | MAGELLAN: Lehrer > Daten 3 > Lehramt Typ Lehrbefähigung
Beschreibung      | Wählen Sie hier die Lehrbefähigung des Lehrers aus.
**Statistikfeld** | **SOLL Regelstundenmaß**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | Geben Sie die Sollstunden für jeden Lehrer in seiner Soll-Berechnung an.
**Statistikfeld** | **MEHR genehmigte Mehrarbeit**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | Geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **SABBAT Sabbatjahrt**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **ALTERTZ Altersteilzeit**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **STG1 Grund1-6 - Ausgl. + Erm.Stunden**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **STS1-6 Stunden1-6 - Ausgl. + Erm.Stunden**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **UEBSTD Überstunden**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **UNTSTD Unterstunden**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **IST erteilte Stunden insgesamt**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **MASS1-15 Einrichtung/Maßnahme1-15**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung
**Statistikfeld** | **ISS1-15 erteilte Stunden SA1 - SA15**  
Datenfeld         | DAVINCI: Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel]Stunden
Beschreibung      | geben Sie die Mehr- oder Minderstunden für jeden Lehrer in seiner Soll-Berechnung

### Weggefallene Statistikangaben

-
