# Export des Daten zum Religionsunterricht aus MAGELLAN

## Wichtige Informationen

1. [Beachten Sie bitte die Mindesteingaben für den Export](https://doc.ls.stueber.de/niedersachsen/einstieg/#voraussetzungen-fur-den-export)
2. Lesen Sie dieses Kapitel gut durch, die meisten Probleme berufen sich auf fehlende oder falsche Eingaben.
3. Lesen Sie im Kapitel [Schnittstellendatei aus MAGELLAN erzeugen](exportdatei_erzeugen.md), wie Sie den Export durchführen.
4. Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).
5.Lesen Sie im Kapitel [Statistikdaten aus DAVINCI exportieren](davinciexportdatei_erzeugen.md), wie Sie den Export durchführen. 

Nachstehend finden Sie eine Auflistung der relevanten Felder und der jeweiligen Stelle, an der Sie in MAGELLAN eingepflegt werden.

### Religionsunterricht

Voraussetzung: MAGELLAN und DAVINCI Daten sind synchron. Bitte lesen Sie dazu das Kapitel "XXX" im "MAGELLAN/DAVINCI" Handbuch.

Titel            | Inhalt
---------------- | ------
**Feld**         | **1-2 - Schulgliederung** - MI
**Beschreibung** | `MAGELLAN: Klassen > Daten > Schulform`<br>Geben Sie hier die Schulform ein. Grundlage ist das Schlüsselverzeichnis „Schulformen“.
**Feld**         | **3-4 - Schuljahrgang: 00 – 13 und gemäß Tabelle „Zulässige Schuljahrgänge“** - MI
**Beschreibung** | `MAGELLAN: Klassen > Zeiträume > Zeitraum > Jahrgang`<br>Geben Sie hier den Jahrgang der Klasse ein.
**Feld**         | **5-6 - Anzahl Lerngruppen ev. Religionsunterricht**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > Fachkürzel`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht, zusammengezählt und ausgegeben.
**Feld**         | **7-10 - Anzahl Stunden ev. Religionsunterricht (9999 = 999,9 Std.)**
**Beschreibung** |  `DAVINCI: D4/Unterrichtstafel > KlassenIst`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht und das KlassenIst summiert zusammengezählt und ausgegeben.
**Feld**         | **11-12 - Anzahl Lerngruppen kath. Religionsunterricht**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > Fachkürzel`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht, zusammengezählt und ausgegeben.
**Feld**         | **13-16 - Anzahl Stunden kath. Religionsunterricht (9999 = 999,9 Std.)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > KlassenIst`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht und das KlassenIst summiert zusammengezählt und ausgegeben.
**Feld**         | **17-18 - Anzahl Lerngruppen Unterricht Werte und Normen**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > Fachkürzel`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht, zusammengezählt und ausgegeben.
**Feld**         | **19-22 - Anzahl Stunden Unterricht Werte und Normen (9999 = 999,9 Std.)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > KlassenIst`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht und das KlassenIst summiert zusammengezählt und ausgegeben.
**Feld**         | **23-24 - Anzahl Lerngruppen Unterricht Philosophie (zurzeit nur SEK II)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > Fachkürzel`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht, zusammengezählt und ausgegeben.
**Feld**         | **25-28 - Anzahl Stunden Unterricht Philosophie (9999 = 999,9 Std.)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > KlassenIst`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht und das KlassenIst summiert zusammengezählt und ausgegeben.
**Feld**         | **29-30 - Anzahl Lerngruppen islamischer Religionsunterricht**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > Fachkürzel`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht, zusammengezählt und ausgegeben.
**Feld**         | **31-34 - Anzahl Stunden islamischer Religionsunterricht (9999 = 999,9 Std.)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > KlassenIst`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht und das KlassenIst summiert zusammengezählt und ausgegeben.
**Feld**         | **35-36 - Anzahl Lerngruppen konfessionell-kooperativer Religionsunterricht)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > Fachkürzel`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht, zusammengezählt und ausgegeben.
**Feld**         | **37-40 - Stunden konfessionell-kooperativer Religionsunterricht (9999 = 999,9 Std.)**
**Beschreibung** | `DAVINCI: D4/Unterrichtstafel > KlassenIst`<br>Entsprechend der Klasse wird im DAVINCI Export der Unterricht gesucht und das KlassenIst summiert zusammengezählt und ausgegeben.
