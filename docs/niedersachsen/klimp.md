# Export der Klassendaten aus Magellan

## Wichtige Informationen

1. [Beachten Sie bitte die Mindesteingaben für den Export](https://doc.ls.stueber.de/niedersachsen/einstieg/#voraussetzungen-fur-den-export))
2. Lesen Sie dieses Kapitel gut durch, die meisten Probleme berufen sich auf fehlende oder falsche Eingaben.
3. Lesen Sie im Kapitel [Schnittstellendatei aus Magellan erzeugen](exportdatei_erzeugen.md), wie Sie den Export durchführen.
4. Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

Nachstehend finden Sie eine Auflistung der relevanten Felder und der jeweiligen Stelle, an der Sie in Magellan eingepflegt werden.

### Klassendaten

Titel            | Inhalt
---------------- | ------
**Feld**         | **1-2 - Schulgliederung** - MI
**Beschreibung** | `Klassen > Daten > Schulform`<br>Geben Sie hier die Schulform ein. Grundlage ist das Schlüsselverzeichnis „Schulformen“
**Feld**         | **3-12 - Kurzbezeichnung der Klasse** - MI
**Beschreibung** | `Klassen > Daten > Statistikkürzel`<br>Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie unter Statistikkürzel nichts eintragen.
**Feld**         | **13 - Nummer des Standortes**
**Beschreibung** | Es wird immer **0** = Hauptstandort ausgespielt. Es werden keine weiteren Standorte unterstützt.
**Feld**         | **14 - Klasse ist pädagogische Einheit der Schuljahrgangs 3 und 4**
**Beschreibung** | `Klassen > Zeiträume > Klassenstufe`<br>**Nur Grundschulen** Über den Import der Schlüssel wurden zwei spezielle Klassenstufen 3/4";"UEG34" und "4/3";"UEG43" angelegt. Die erste ist für einen 3. Jahrgang, einer hahrgangsübergreifendenden Klassenstufe gedacht, die zweite für einen 4. Jahrgang.
**Feld**         | **15 - Klasse ist Eingangsstufe**
**Beschreibung** | `Klassen > Merkmale > Merkmal S3`<br>**Nur Grundschulen** Wählen Sie hier den Wert aus, wenn es sich um eine Eingangsstufe handelt.
**Feld**         | *16 - nicht mehr relevant (bisher: Klasse ist Integrationsklasse: J oder N)*
**Beschreibung** | -
**Feld**         | **17 - Klasse ist Sprachlernklasse**
**Beschreibung** | `Klassen > Merkmale > Merkmal S2`<br>Geben Sie hier an, ob die Klasse eine Sprachlernklasse ist. Grundlage ist das Schlüsselverzeichnis "Merkmale (Klassen)"(Bereich S2). Keine Angabe entspricht dem Wert „Nein“.
**Feld**         | *18 - nicht mehr relevant (bisher: Klasse ist Förderklasse für Aussiedler*
**Beschreibung** | -

### JG - Schuljahrgangsdaten

Titel            | Inhalt
---------------- | ------
**Feld**         | **19-20 - Beginn Schuljahrgangsdaten: JG = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "JG"
**Feld**         | **21-22 - Schuljahrgang: 00 – 13 und gemäß Tabelle „Zulässige Schuljahrgänge“**
**Beschreibung** | `Klassen > Zeiträume > Zeitraum > Jahrgang`<br>Geben Sie hier den Jahrgang der Klasse ein.
**Feld**         | **23-26 - Anz. Schüler/innen zusammen**
**Beschreibung** | Es werden alle Schüler der Klasse zusammengezählt und ausgegeben.
**Feld**         | **27-30 - nicht mehr relevant (bisher: Schüler/innen nichtdt. Herk.spr. siehe WJG)**
**Beschreibung** | -
**Feld**         | *31-34 - nicht mehr relevant (bisher: darunter weiblich siehe WJG)*
**Beschreibung** | -
**Feld**         | **35-38 - Schüler/innen mit ev. Religionszugehörigkeit**
**Beschreibung** | `Schüler > Daten 1 > Konfession`<br> Es werden alle Schüler der Klasse mit der entsprechenden Konfession zusammengezählt und ausgegeben.
**Feld**         | **39-42 - Schüler/innen mit kath. Religionszugehörigkeit**
**Beschreibung** | `Schüler > Daten 1 > Konfession`<br> Es werden alle Schüler der Klasse mit der entsprechenden Konfession zusammengezählt und ausgegeben.
**Feld**         | **43-46 - Schüler/innen mit islamischer Religionszugehörigkeit**
**Beschreibung** | `Schüler > Daten 1 > Konfession`<br> Es werden alle Schüler der Klasse mit der entsprechenden Konfession zusammengezählt und ausgegeben.
**Feld**         | **47-50 - Schüler/innen mit sonstiger Religionszugehörigkeit**
**Beschreibung** | `Schüler > Daten 1 > Konfession`<br> Es werden alle Schüler der Klasse mit der entsprechenden Konfession zusammengezählt und ausgegeben.
**Feld**         | **51-54 - Schüler/innen ohne Religionszugehörigkeit**
**Beschreibung** | `Schüler > Daten 1 > Konfession`<br> Es werden alle Schüler der Klasse mit der entsprechenden Konfession zusammengezählt und ausgegeben.
**Feld**         | **55-58 - Schüler/innen mit Teilnahme am ev. Religionsunterricht**
**Beschreibung** | `Schüler > Daten 1 > Rel.-Teilnahme`<br> Es werden alle Schüler der Klasse mit der entsprechenden Teilnahme am Religoinsunterricht zusammengezählt und ausgegeben.
**Feld**         | **59-62 - Schüler/innen mit Teilnahme am kath. Religionsunterricht**
**Beschreibung** | `Schüler > Daten 1 > Rel.-Teilnahme`<br> Es werden alle Schüler der Klasse mit der entsprechenden Teilnahme am Religoinsunterricht zusammengezählt und ausgegeben.
**Feld**         | **63-66 - Schüler/innen mit Teilnahme am Unterricht Werte und Normen**<br>Bei Grundschulen nur an den Schulen möglich, die am Schulversuch „WuN an GS“ teilnehmen.
**Beschreibung** | `Schüler > Daten 1 > Rel.-Teilnahme`<br> Es werden alle Schüler der Klasse mit der entsprechenden Teilnahme am Religoinsunterricht zusammengezählt und ausgegeben.
**Feld**         | **67-70 - Schüler/innen ohne Teilnahme am Religionsunterricht**
**Beschreibung** | -
**Feld**         | *71-72 - nicht mehr relevant (bisher: anteilig erteilte Std. ev. Reli.unterricht (99 = 9,9 Std.))*
**Beschreibung** | -
**Feld**         | *73-74 - nicht mehr relevant (bisher: anteilig erteilte Std. kath. Reli.unterricht (99 = 9,9 Std.))*
**Beschreibung** | -
**Feld**         | *75-76 - nicht mehr relevant (bisher: anteilig erteilte Std. Unterricht Werte und Normen (99 = 9,9 Std.))*
**Beschreibung** | -
**Feld**         | *77-80 - nicht mehr relevant (bisher: Ausl. Schüler/innen mit Förderkurs Deutsch als Zweitsprache)*
**Beschreibung** | -
**Feld**         | *81-84 - nicht mehr relevant (bisher: Ausl. Schüler/innen mit Förderunterricht)*
**Beschreibung** | -
**Feld**         | *85-88 - nicht mehr relevant (bisher: Ausl. Schüler/innen mit mutterspr. Unterricht)*
**Beschreibung** | -

### WJG - Weitere Schuljahrgangsdaten (0 – 1-mal zulässig)

Titel            | Inhalt
---------------- | ------
**Feld**         | **1-3 - WJG = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "WJG"
**Feld**         | **4-7 - Schüler/innen mit Migrationshintergrund**
**Beschreibung** | `Schueler > Daten 1 > Geschlecht`, `Schueler > Daten 1 > Staatsangehörigkeit > NdH`<br>Geben Sie das Geschlecht an, und markieren Sie, wenn der Schüler nicht deutscher Herkunft ist. Es werden alle Schüler entsprechend zusammengezählt und ausgegeben.
**Feld**         | **8-11 - darunter weiblich**
**Beschreibung** | `Schueler > Daten 1 > Geschlecht`, `Schueler > Daten 1 > Staatsangehörigkeit > NdH`<br>Geben Sie das Geschlecht an, und markieren Sie, wenn der Schüler nicht deutscher Herkunft ist. Es werden alle weiblichen Schüler entsprechend zusammengezählt und ausgegeben.
**Feld**         | *12-15 - nicht mehr relevant (bisher: Schüler/innen nichtdeutscher Herkunftsspr. mit Förderbedarf in Deutsch insgesamt)*
**Beschreibung** | -
**Feld**         | *16-19 - darunter weiblich*
**Beschreibung** | -
**Feld**         | **20-23 - Schüler/innen mit Teilnahme am Unterricht Philosophie (zurzeit nur SEK II)**
**Beschreibung** | 
**Feld**         | **24-27 - Schüler/innen mit Teilnahme am islamischen Religionsunterricht**
**Beschreibung** | 
**Feld**         | **28-31 - Schüler/innen mit Teilnahme am konfessionell-kooperativen Religionsunterricht**
**Beschreibung** | 
**Feld**         | *32-35 - nicht mehr relevant (bisher: Schüler/innen mit Laufbahnempfehlung Gymnasium (nur Schuljahrgang 05))*
**Beschreibung** | -
**Feld**         | *36-39 - nicht mehr relevant (bisher: Schüler/innen mit Laufbahnempfehlung Realschule (nur Schuljahrgang 05))*
**Beschreibung** | -
**Feld**         | *40-43 - nicht mehr relevant (bisher: Schüler/innen mit Laufbahnempfehlung Hauptschule (nur Schuljahrgang 05))*
**Beschreibung** | -
**Feld**         | *44-47 - nicht mehr relevant (bisher: Wiederholer/innen dieser Schule (nur Schuljahrgang 05))*
**Beschreibung** | -
**Feld**         | *48-51 - nicht mehr relevant (bisher: sonstige Zugänge an diese Schule (nur Schuljahrgang 05))*
**Beschreibung** | -
- | **Wechsel auf andere Schulformen seit dem letzten Stichtag:**
**Feld**         | 52-55 - Abgänge auf HS
**Beschreibung** | `Schüler > Daten 2 > Abgang > Abgangsart`, `Schüler > Daten 2 > Abgang > Abgang am`<br>Geben Sie die Abgangsart und das Datum des Abgangs von der Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 56-59 - Abgänge auf RS
**Beschreibung** | `Schüler > Daten 2 > Abgang > Abgangsart`, `Schüler > Daten 2 > Abgang > Abgang am`<br>Geben Sie die Abgangsart und das Datum des Abgangs von der Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 60-63 - Abgänge auf GY
**Beschreibung** | `Schüler > Daten 2 > Abgang > Abgangsart`, `Schüler > Daten 2 > Abgang > Abgang am`<br>Geben Sie die Abgangsart und das Datum des Abgangs von der Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 64-67 - Abgänge auf IGS
**Beschreibung** | `Schüler > Daten 2 > Abgang > Abgangsart`, `Schüler > Daten 2 > Abgang > Abgang am`<br>Geben Sie die Abgangsart und das Datum des Abgangs von der Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 68-71 - Abgänge auf FöS
**Beschreibung** | `Schüler > Daten 2 > Abgang > Abgangsart`, `Schüler > Daten 2 > Abgang > Abgang am`<br>Geben Sie die Abgangsart und das Datum des Abgangs von der Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 72-75 - Zugänge von HS
**Beschreibung** | `Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Schulart`, `Schüler > Daten 2 > Zugang > Zugang am`<br>Geben Sie die Schulart der Herkunftsschule und das Datum des Zugangs an Ihre Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 76-79 - Zugänge von RS
**Beschreibung** | `Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Schulart`, `Schüler > Daten 2 > Zugang > Zugang am`<br>Geben Sie die Schulart der Herkunftsschule und das Datum des Zugangs an Ihre Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 80-83 - Zugänge von GY
**Beschreibung** | `Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Schulart`, `Schüler > Daten 2 > Zugang > Zugang am`<br>Geben Sie die Schulart der Herkunftsschule und das Datum des Zugangs an Ihre Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 84-87 - Zugänge von IGS
**Beschreibung** | `Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Schulart`, `Schüler > Daten 2 > Zugang > Zugang am`<br>Geben Sie die Schulart der Herkunftsschule und das Datum des Zugangs an Ihre Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | 88-91 - Zugänge von FöS
**Beschreibung** | `Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Schulart`, `Schüler > Daten 2 > Zugang > Zugang am`<br>Geben Sie die Schulart der Herkunftsschule und das Datum des Zugangs an Ihre Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.

### Zusätzliche Schuljahrgangsdaten (0 – 1-mal zulässig)

Titel            | Inhalt
---------------- | ------
**Feld**         | **1-3 - ZJG = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "ZJG"
- |**Ergänzung zu Wechsel auf andere Schulformen seit dem letzten Stichtag:**
**Feld**         | **4-7 - Abgänge auf OBS**
**Beschreibung** | `Schüler > Daten 2 > Abgang > Abgangsart`, `Schüler > Daten 2 > Abgang > Abgang am`<br>Geben Sie die Abgangsart und das Datum des Abgangs von der Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **8-11 - Zugänge von OBS**
**Beschreibung** | `Schüler > Daten 2 > Bereits besuchte Schulen > Herkunftsschule > Schulart`, `Schüler > Daten 2 > Zugang > Zugang am`<br>Geben Sie die Schulart der Herkunftsschule und das Datum des Zugangs an Ihre Schule an. Es werden enstprechend die Schüler zusammengezählt und ausgegeben.
- | **Anzahl inklusiv beschulter Schülerinnen und Schüler nach Förderschwerpunkten:**<br>Im Schuljahr 2020/2021 im SEK II-Bereich nur für die SJG 11 und 12 (EP und Q1) zulässig
**Feld**         | **12-15 - Lernen (im SEK II-Bereich zurzeit nicht zulässig)**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **16-19 - Sprache**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **20-23 - Emotionale und soziale Entwicklung**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **24-27 - Hören**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **28-31 - Sehen**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **32-35 - Körperliche und motorische Entwicklung**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **36-39 - Geistige Entwicklung (im SEK II-Bereich zurzeit nicht zulässig)**
**Beschreibung** | `Schueler > Daten 4 > Beeinträchtigungen und Fördermaßnahmen > Förderschwerpunkt 1`<br>Geben Sie den Förderschwerpunkt 1 an. Es werden entsprechend die Schüler zusammengezählt und ausgegeben.

### Daten zur Herkunft der Schüler/innen (1 - 12-mal zulässig)

**Format:** ZBSxx88889999

Titel            | Inhalt
---------------- | ------
**Feld**         | **ZBS = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "ZBS"
**Feld**         | **xx = Art der Herkunft (gemäß SCHLUESS.TXT, Kennung ZBS)**
**Beschreibung** | `Schueler > Merkmale > Merkmal S1`<br>Wählen Sie die Herkunft.
**Feld**         | **8888 = Anz. Schüler/innen zusammen je Art der Herkunft (4-stellig)**
**Beschreibung** | Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **9999 = darunter weiblich (4-stellig)**
**Beschreibung** | Es werden entsprechend die weiblichen Schüler zusammengezählt und ausgegeben.

### Staatsangehörigkeit der Schüler/innen mit nichtdeutscher Staatsangehörigkeit (0 - 12-mal zulässig)

**Format:** STAxxx88889999

Titel            | Inhalt
---------------- | ------
**Feld**         | **STA = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "STA"
**Feld**         | **xxx = Schlüssel Staatsangehörigkeit (gemäß SCHLUESS.TXT, Kennung STK)**
**Beschreibung** | `Schueler > Daten 1 > Staatsangehörigkeiten > Staatsangeh. 1`<br>Wählen Sie die Staatsangehörigkeit des Schüler aus.
**Feld**         | **8888 = Anz. Schüler/innen zusammen je Staatsangehörigkeit (4-stellig)**
**Beschreibung** | Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **9999 = darunter weiblich (4-stellig)**
**Beschreibung** | Es werden entsprechend die weiblichen Schüler zusammengezählt und ausgegeben.

### Unterricht in Fremdsprachen (0 - 10-mal zulässig)

**Format:** FSPxx8888

Titel            | Inhalt
---------------- | ------
**Feld**         | **FSP = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "FSP"
**Feld**         | **xx = Schlüssel Fremdsprache (gemäß SCHLUESS.TXT, Kennung FSP)**
**Beschreibung** | `Schueler > Zeugnis > Fächer`<br>Geben Sie für die Schüler die entsprechenden Fremdsprachenfächer an. Wenn die Fremdsprache unterrichtet wurde, dann wir diese gezählt.
**Feld**         | **8888 = Anz. Schüler/innen zusammen je Fremdsprache (4-stellig)**
**Beschreibung** | Es werden entsprechend die Schüler zusammengezählt und ausgegeben.

### Schüler/innen nach Geburtsjahrgängen (n-mal zulässig, n > 0)

**Format:** GEBxxxx88889999

Titel            | Inhalt
---------------- | ------
**Feld**         | **GEB = Konstante**
**Beschreibung** | Ausgabe des festen Wertes "GEB"
**Feld**         | **xxxx = Geburtsjahrgang**
**Beschreibung** | `Schueler > Daten 1 > Geburtdatum`<br>Geben Sie beim Schüler jeweils das Geburtsdatum an.
**Feld**         | **8888 = Anz. Schüler/innen zusammen je Geburtsjahrgang (4-stellig)**
**Beschreibung** | Es werden entsprechend die Schüler zusammengezählt und ausgegeben.
**Feld**         | **9999 = darunter weiblich (4-stellig)**
**Beschreibung** | Es werden entsprechend die weiblichen Schüler zusammengezählt und ausgegeben.
