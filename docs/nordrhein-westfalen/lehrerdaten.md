# Lehrerdaten der LEHRER.TXT

## Voraussetzungen zum Export

[Beachten Sie bitte die Mindesteingaben für die Schnittstelle!](https://doc.ls.stueber.de/nordrhein-westfalen/abs-bbs/#voraussetzungen-für-alle-statistikdaten)

Magellan benötigt zur Erzeugung der LEHRER.TXT Stundendaten aus DaVinci 6.

## Export der DaVinci Daten

So exportieren Sie in DaVinci 6 die Statistikdaten zur Erzeugung der LEHRER.TXT in Magellan.

1. Klicken Sie auf `Plan > Importieren und Exportieren`.
2. Wählen Sie im Dialogfenster Import/Export-Assistent die Option `Statistikdaten exportieren` und klicken Sie dann auf `Weiter`.
3. Wählen Sie die Option `Allgemeines Statistikformat` exportieren und klicken Sie dann auf `Weiter`.
4. Geben Sie den Namen der Exportdatei an, z.B. DAVINCI_export.txt
5. Klicken Sie auf `OK`. Die Datei mit den Stunden-Datensätzen wird erzeugt.
6. In der Maske bei der Auswahl geben Sie im unteren Eingabefeld den Pfad zur exportierten DaVinci Exportdatei an, diese wird von Magellan dann eingelesen und für die LEHRER.TXT ausgewertet.

!!! info "Hinweis"

    Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

## Dateneingabe

Art               | Inhalt
----------------- | ------
**Exportfeld**    | **Schulnummer**
Datenfeld         | Magellan: Mandanten > Daten 1 > Schulnummer
Beschreibung      | Tragen Sie Ihre 6-Stellige Schulnummer ein.
**Exportfeld**    | **Lehrerabkürzung**
Datenfeld         | Magellan: Lehrer > Daten 1 > Kürzel
Beschreibung      | Tragen Sie für jeden Lehrer der Schule das 4-Stellige Lehrerkürzel (identisch zur LID 123) ein.
**Exportfeld**    | **Pflichtstundensoll**
Datenfeld         | DaVinci:Stammdaten > Lehrer > Zeitkonto > Schlüssel[Lehrer-Soll-Schluessel] > Stunden
Beschreibung      | Geben Sie die Pflichtstunden für jeden Lehrer in seiner Soll-Berechnung in den Stammdaten an. Kürzel/Schlüssel ist gleich PFLICHT.
**Exportfeld**    | **Produktname**
Datenfeld         | -
Beschreibung      | Wir geben hier fest den Wert „Magellan 7“ aus
**Exportfeld**    | **Produktversion**
Datenfeld         | -
Beschreibung      | Wir geben hier die aktuell installierte Magellan 7 Version (Registry Wert) aus.
**Exportfeld**    | **Satzart65 – Grund / Satzart65 – Stunden**
Datenfeld         | DaVinci: Stammdaten > Lehrer > Zeitkonto > Schlüssel [Lehrer-Soll-Schluessel] > Stunden
Beschreibung      | Geben Sie die Anrechnungsstunden für jeden Lehrer in seiner Soll-Berechnung an.   Kürzel/Schlüssel ist gleich ANR.
**Exportfeld**    | **Satzart66 – Grund / Satzart66 – Stunden**
Datenfeld         | DaVinci: Stammdaten > Lehrer > Zeitkonto > Schlüssel [Lehrer-Soll-Schluessel] > Stunden
Beschreibung      | Geben Sie die Mehrarbeitsstunden für jeden Lehrer in seiner Soll-Berechnung an. Kürzel/Schlüssel ist gleich MEHR.
**Exportfeld**    | **Satzart67 – Grund / Satzart67 – Stunden**
Datenfeld         | DaVinci: Stammdaten > Lehrer > Zeitkonto > Schlüssel [Lehrer-Soll-Schluessel] > Stunden
Beschreibung      | Geben Sie die Ermäßigungsstunden für jeden Lehrer in seiner Soll-Berechnung an. Kürzel/Schlüssel ist gleich ERM.
