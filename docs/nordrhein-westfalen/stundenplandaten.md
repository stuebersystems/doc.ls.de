# Stundenplandaten \(EXTERN.DAT\)

In DAVINCI können Sie die Stundenplandaten in die Datei EXTERN.DAT für ASDPC exportieren. Als Voraussetzung für einen erfolgreichen Export müssen Sie bestimmte Angaben in DAVINCI machen, die nachfolgend beschrieben sind. Für eine erfolgreiche Übernahme der Daten aus DAVINCI nach ASDPC müssen Sie wie folgt vorgehen.

## Folgende Schritt sind auszuführen

1. Geben Sie die notwendigen Daten in DAVINCI an.
2. Erzeugen Sie die Exportdatei EXTERN.DAT.
3. Importieren Sie die Daten in ASDPC.

!!! info "Hinweis"

   Für Erstellung der LEHRER.TXT aus MAGELLAN heraus ist NICHT die EXTERN.DAT die Grundlage, sondern die txt-Datei die durch dem „Allgemeinen Schnittstellenexport“ erzeugt werden kann.

## UVD.TXT

Wir zitieren nachstehend aus der Anleitung für [ASDPC](https://schulverwaltungsprogramme.msb.nrw.de/asschule.pdf):
Die Dateien EXTERN.DAT und UVD.TXT werden alternativ verwendet. Eine gleichzeitige Verwendung dieser Dateien ist nicht sinnvoll.

!!! warning "Wichtig"

     Es wird nur eine der beiden Dateien (UVD.TXT, EXTERN.DAT) benötigt. DAVINCI kann die EXTERN.DAT erzeugen.

## Dateneingabe

### ABS

Die folgenden Angaben müssen in DAVINCI bei allgemeinbildenden Schulen gemäß der offiziellen Vorgaben gemacht werden. Bitte beachten Sie unbedingt die maximal zulässige Länge für Klassen-, Lehrer- und Fachkürzel.

Art               | Inhalt
----------------- | ------
**Exportfeld**    | **Klassenkürzel**
Beschreibung      | Klassenkürzel im Stammdatenfenster auf Registerkarte „Klassen“, maximal 4stellig
**Exportfeld**    | **Fachkürzel**
Beschreibung      | Spalte „Schlüssel“ im Stammdatenfenster auf Registerkarte „Fächer“, maximal 4stellig
**Exportfeld**    | **Wochenstunden**
Beschreibung      | Spalte „Dauer/W“ in der Unterrichtsliste des Planungsfenster
**Exportfeld**    | **Lehrerkürzel**
Beschreibung      | Lehrerkürzel im Stammdatenfenster auf Registerkarte „Lehrer“
**Exportfeld**    | **Schülerzahl insgesamt**
Beschreibung      | Spalte „Schüler“ in der Unterrichtsliste des Planungsfensters
**Exportfeld**    | **Schülerzahl weiblich**
Beschreibung      | wird derzeit nicht unterstützt
**Exportfeld**    | **Schülerzahl Fremde**
Beschreibung      | wird derzeit nicht unterstützt

### BBS

Die folgenden Angaben müssen in DAVINCI bei Berufskollegs gemäß der offiziellen Vorgaben gemacht werden. Bitte beachten Sie unbedingt die maximal zulässige Länge für Klassen-, Lehrer- und Fachkürzel.

Art               | Inhalt
----------------- | ------
**Exportfeld**    | **Klassenkürzel**
Beschreibung      | Klassenkürzel im Stammdatenfenster auf Registerkarte „Klassen“, maximal 6stellig
**Exportfeld**    | **Fachkürzel**
Beschreibung      | Spalte „Schlüssel“ im Stammdatenfenster auf Registerkarte „Fächer“, maximal 4stellig
**Exportfeld**    | **Wochenstunden**
Beschreibung      | Spalte „Dauer/W“ in der Unterrichtsliste des Planungsfenster
**Exportfeld**    | **Lehrerkürzel**
Beschreibung      | Lehrerkürzel im Stammdatenfenster auf Registerkarte „Lehrer“
**Exportfeld**    | **Schülerzahl insgesamt**
Beschreibung      | Spalte „Schüler“ in der Unterrichtsliste des Planungsfensters

## EXTERN.DAT erzeugen

So exportieren Sie in DAVINCI 6 die Datei EXTERN.DAT:

1. Klicken Sie auf Plan > Importieren und Exportieren.
2. Wählen Sie im Dialogfenster Import/Export-Assistent die Option Statistikdaten exportieren und klicken Sie dann auf `Weiter`.
3. Wählen Sie die Option Statistik Nordrhein-Westfalen BBS\(ASDPC/EXTERN.DAT\) exportieren oder Statistik Nordrhein-Westfalen ABS \(ASDPC/EXTERN.DAT\) exportieren und klicken Sie dann auf `Weiter`.
4. Geben Sie den Namen der Exportdatei an. Die Datei sollte EXTERN.DAT heißen.  
5. Klicken Sie auf `OK`. Die Datei mit den Stunden-Datensätzen wird erzeugt. Bitte lesen Sie diese Daten direkt in ASDPC ein.

## Formatbeschreibung EXTERN.DAT

### Aufbau für Allgemeinbildende Schulen

Titel                 | Stellen    | Position | Inhalt
--------------------- | ---------- | -------- | ------
**Klasse**            | 4-stellig  | 01-04    | Kurzbezeichnung der Klasse
**Gruppe**            | 2-stellig  | 05-06    | Art der Gruppe
**Wstd**              | 2-stellig  | 07-08    | Erteilte Wochenstunden
**Fach**              | 4-stellig  | 09-12    | Fach
**Lehrer**            | 4-stellig  | 13-16    | Lehrerkurzbezeichnung
**Schueler**          | 2-stellig  | 17-18    | Schüler insgesamt
**darunter weiblich** | 2-stellig  | 19-20    | Schülerinnen im Unterricht
**Fremde**            | 1-stellig  |    21    | Merkmal für Schüler anderer Schulen
**Bildungsgang**      | 3-stellig  | 22-24    | -
**Produktname**       | 20-stellig | 25-44    | Produktname
**Produktversion**    | 20-stellig | 45-64    | Produktversion der verwendeten Schulverwaltungssoftware

### Aufbau für Berufsbildende Schulen

Titel                 | Stellen    | Position | Inhalt
--------------------- | ---------- | -------- | ------
**Klasse**            | 6-stellig  | 01-06    | Kurzbezeichnung der Klasse
**TKM**               | 1-stellig  |    07    | Teilklassenmerkmal
**Gruppe**            | 2-stellig  | 08-09    | Art der Gruppe
**Wstd**              | 2-stellig  | 10-11    | Erteilte Wochenstunden
**Fach**              | 4-stellig  | 12-15    | Fach
**Lehrer**            | 4-stellig  | 16-19    | Lehrerkurzbezeichnung
**Schueler**          | 2-stellig  | 20-21    | Schüler insgesamt
**Dummy**             | 6-stellig  | 22-27    | -
**Produktname**       | 20-stellig | 28-47    | Produktname
**Produktversion**    | 20-stellig | 48-67    | Produktversion der verwendeten Schulverwaltungssoftware
