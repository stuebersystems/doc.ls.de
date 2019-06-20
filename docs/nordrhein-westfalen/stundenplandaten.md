# Stundenplandaten \(EXTERN.DAT\)

In DAVINCI können Sie die Stundenplandaten in die Datei EXTERN.DAT für ASDPC exportieren. Als Voraussetzung für einen erfolgreichen Export müssen Sie bestimmte Angaben in DAVINCI machen, die nachfolgend beschrieben sind. Für eine erfolgreiche Übernahme der Daten aus DAVINCI nach ASDPC müssen Sie wie folgt vorgehen.


| Was ist zu tun?  |
|------------------------------------------|
| 1. Geben Sie die notwendigen Daten in DAVINCI an. |
| 2. Erzeugen Sie die Exportdatei EXTERN.DAT. |
| 3. Importieren Sie die Daten in ASDPC.   |


!!! info "Hinweis"

  Für Erstellung der Lehrer.txt aus MAGELLAN heraus ist NICHT die Extern.dat die Grundlage, sondern die txt-Datei die durch dem „Allgemeinen Statistikexport“ erzeugt werden kann.

## UVD.txt ?

Wir zitieren nachstehend aus der Anleitung für [ASDPC](https://schulverwaltungsprogramme.msb.nrw.de/asschule.pdf): 
Die Dateien Extern.dat und UVD.txt werden alternativ verwendet. Eine gleichzeitige Verwendung dieser Dateien ist nicht sinnvoll. 


!!! warning "Wichtig"

 Man benötigt nur eine der beiden Dateien und nicht die UVD.txt und die EXTERN.dat, DAVINCI kann die Extern.dat erzeugen.


## Notwendige Angaben für die ABS-Statistik

Die folgenden Angaben müssen in DAVINCI bei allgemeinbildenden Schulen gemäß der offiziellen Statistikvorgaben gemacht werden. Bitte beachten Sie unbedingt die maximal zulässige Länge für Klassen-, Lehrer- und Fachkürzel.


| Angabe gemäß Statistik | Angabe in DAVINCI   |
|------------------------|------------------------------------------|
| **Klassenkürzel** | Klassenkürzel im Stammdatenfenster auf Registerkarte „Klassen“, maximal 4stellig |
| **Fachkürzel** | Spalte „Schlüssel“ im Stammdatenfenster auf Registerkarte „Fächer“, maximal 4stellig |
| **Wochenstunden** | Spalte „Dauer/W“ in der Unterrichtsliste des Planungsfenster |
| **Lehrerkürzel**  | Lehrerkürzel im Stammdatenfenster auf Registerkarte „Lehrer“ |
| **Schülerzahl insgesamt**  | Spalte „Schüler“ in der Unterrichtsliste des Planungsfensters |
| **Schülerzahl weiblich**   | wird derzeit nicht unterstützt  |
| **Schülerzahl Fremde**  | wird derzeit nicht unterstützt  |



## Notwendige Angaben für die BBS-Statistik

Die folgenden Angaben müssen in DAVINCI bei Berufskollegs gemäß der offiziellen Statistikvorgaben gemacht werden. Bitte beachten Sie unbedingt die maximal zulässige Länge für Klassen-, Lehrer- und Fachkürzel.


| Angabe gemäß Statistik | Angabe in DAVINCI   |
|------------------------|------------------------------------------|
| **Klassenkürzel** | Klassenkürzel im Stammdatenfenster auf Registerkarte „Klassen“, maximal 6stellig |
| **Fachkürzel** | Spalte „Schlüssel“ im Stammdatenfenster auf Registerkarte „Fächer“, maximal 4stellig |
| **Wochenstunden** | Spalte „Dauer/W“ in der Unterrichtsliste des Planungsfenster |
| **Lehrerkürzel**  | Lehrerkürzel im Stammdatenfenster auf Registerkarte „Lehrer“ |
| **Schülerzahl insgesamt**  | Spalte „Schüler“ in der Unterrichtsliste des Planungsfensters |



## EXTERN.DAT erzeugen

So exportieren Sie in DAVINCI 6 die Datei EXTERN.DAT :

1. Klicken Sie auf Plan\|Importieren und Exportieren.
2. Wählen Sie im Dialogfenster Import/Export-Assistent die Option Statistikdaten exportieren und klicken Sie dann auf Weiter.  
3. Wählen Sie die Option Statistik Nordrhein-Westfalen BBS\(ASDPC/EXTERN.DAT\) exportieren oder Statistik Nordrhein-Westfalen ABS \(ASDPC/EXTERN.DAT\)  exportieren und klicken Sie dann auf Weiter.  
4. Geben Sie den Namen der Exportdatei an. Die Datei sollte extern.dat heißen.  
5. Klicken Sie auf OK. Die Datei mit den Stunden-Datensätzen wird erzeugt. Bitte lesen Sie diese Daten direkt in ASDPC ein.

## Formatbeschreibung EXTERN.DAT

### Aufbau für Allgemeinbildende Schulen


| Titel | Stelle | Position  | Inhalt  |
|-------------------|--------------|-----------|------------------------------------------|
| **Klasse**   | 4-stellig | Pos. 1- 4 | Kurzbezeichnung der Klasse   |
| **Gruppe**   | 2-stellig | Pos. 5- 6 | Art der Gruppe   |
| **Wstd**  | 2-stellig | Pos. 7- 8 | Erteilte Wochenstunden |
| **Fach**  | 4-stellig | Pos. 9-12 | Fach |
| **Lehrer**   | 4-stellig | Pos.13-16 | Lehrerkurzbezeichnung  |
| **Schueler** | 2-stellig | Pos.17-18 | Schüler insgesamt   |
| **darunter weiblich** | 2-stellig | Pos.19-20 | Schülerinnen im Unterricht   |
| **Fremde**   | 1-stellig | Pos.21 | Merkmal für Schüler anderer Schulen   |
| **Bildungsgang**   | 3-stellig | Pos. 22-24 |
| **Produktname** | 20-stellig   | Pos.25-44 | Produktname   |
| **Produktversion** | 20-stellig   | Pos.45-64 | Produktversion der verwendeten Schulverwaltungssoftware |

### Aufbau für Berufsbildende Schulen


| Titel | Stelle  | Position   | Inhalt  |
|----------------|------------|------------|------------------------------------------|
| **Klasse**   | 6-stellig  | Pos. 1 - 6 | Kurzbezeichnung der Klasse   |
| **TKM**   | 1-stellig  | Pos. 7  | Teilklassenmerkmal  |
| **Gruppe**   | 2-stellig  | Pos. 8 - 9 | Art der Gruppe   |
| **Wstd**  | 2-stellig  | Pos.10-11  | Erteilte Wochenstunden |
| **Fach**  | 4-stellig  | Pos.12-15  | Fach |
| **Lehrer**   | 4-stellig  | Pos.16-19  | Lehrerkurzbezeichnung  |
| **Schueler** | 2-stellig  | Pos.20-21  | Schüler insgesamt   |
| **Dummy** | 6-stellig  | Pos.22-27  | z.Z. leer  |
| **Produktname** | 20-stellig | Pos.28-47  | Produktname   |
| **Produktversion** | 20-stellig | Pos.48-67  | Produktversion der verwendeten Schulverwaltungssoftware |
