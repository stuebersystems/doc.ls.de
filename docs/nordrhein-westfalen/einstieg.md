# Nordrhein-Westfalen

Das Ministerium für Schule und Weiterbildung des Landes Nordrhein-Westfalen fordert mehrmals im Jahr eine statistische Erhebung von den Schulen.
Zur Erstellung der Statistik wird das Programm ASDPC des Schulministerium benötigt. ASDPC verfügt über eine Importschnittstelle zum Einlesen von Daten aus Schulverwaltungsprogrammen.
Mit der `Schnittstelle zu ASDPC`, die über unser Schnittstellen-Modul lizensiert wird, können Sie die benötigten Schnittstellendateien direkt aus MAGELLAN und DAVINCI erzeugen.

## Lizenz

Bitte beachten Sie, wir haben unser Angebot von der jährlich angebotenen Lizenz (bisher veröffentlicht "LANDESSTATISTIK") auf einen Nutzungsvertrag um. Dieser Vertrag beinhaltet die Nutzung, Pflege, Weiterentwicklung und den Support der MAGELLAN Schnittstelle zu verschiedenen Anbietern. Bitte beachten Sie, dass diese Nutzungsverträge nicht den MAGELLAN Support- und Softwarepflegevertrag ersetzen.
**Die jährlich neue Lizenz kann mit der jeweils neuesten Ausgabe von MAGELLAN verwendet werden, wir weisen darauf per Newsletter hin. Wenn Sie einen Nutzungsvertrag abgeschlossen haben, senden wir Ihnen die neue Lizenz und weitere Informationen per Mail zu.**

!!! info "Hinweis"

    Eine DAVINCI-Lizenz wird nur für die EXTERN.DAT und die LEHRER.TXT benötigt, da diese Stundenplandaten enthalten. Jede Datei kann einzeln erzeugt werden, somit benötigen Sie z.B. kein DAVINCI wenn Sie lediglich die SIM.TXT oder die ABI.TXT erzeugen möchten.

## Einführung

Die Schnittstellendateien werden anhand der erfassten Daten in MAGELLAN und DAVINCI erstellt. Hier erhalten Sie eine Übersicht über die Schnittstellendateien:

Dateiname  | Abkürzung | Kapitel                           | Inhalt
---------- | --------- | --------------------------------- | ------
SIM.TXT    | SIM       | [SIM.TXT](schuelerdaten.md)       | Nur MAGELLAN-Daten
LEHRER.TXT | LEHRER    | [LEHRER.TXT](lehrerdaten.md)      | MAGELLAN-Daten und aus DAVINCI der „Allgemeine Statistikexport“
ABI.TXT    | ABI       | [ABI.TXT](abiturdaten.md)         | Nur MAGELLAN-Daten
EXTERN.DAT | EXTERN    | [EXTERN.DAT](stundenplandaten.md) | Nur DAVINCI-Daten aus dem Export für „ASDPC/EXTERN.DAT“

!!! warning "Wichtig"

    Wir erstellen die Dateien entsprechend der Schnittstellenbeschreibungen des statistischen Landesamtes. 
    In einigen Fällen (Beispiel: SIM.TXT) spielen wir zusätzliche Felder aus, die die Zuordnung der Zeilen zu Datensätzen in Ihrem Datenbestand ermöglichen. Damit können wir bei Problemen besser die Ursache im Datenstand finden. Diese zusätzlichen Felder sind in Absprache mit dem statistischen Landesamt integriert und werden von ASDPC beim Import ignoriert.

### Zeitraumbedingte Daten

Viele Schüler- und Klassendaten in MAGELLAN werden zeitraumbezogen pro Schulhalbjahr abgelegt. Je nach Statistkdatei und Datensatz müssen die Daten entsprechend der Vorgaben aus der Schnittstelle aus den unterschiedlichen Halbjahren ausgelesen und ausgewertet werden.

Dateiname  | Ausgelesene Halbjahre
---------- | ---------------------
SIM.TXT    | 1. HJ. aktuelles Schuljahr, 2. HJ. vorangegangenes Schuljahr, 1. HJ. vorangegangenes Schuljahr
LEHRER.TXT | -
ABI.TXT    | 2. HJ. vorangegangenes Schuljahr
EXTERN.DAT | -

Welche Daten wie ausgewertet werden und unter welchen Umständen Daten in den Export aufgenommen werden, entnehmen Sie den einzelnen Kapiteln zu den Schnittstellendateien.

!!! warning "Wichtig"

    Sie müssen immer alle drei Zeiträume im Assistenten angeben, ungeachtet dessen welche Datei Sie zum Export auswählen. Der Exportmechanismus entscheidet von sich aus, welchen Zeitraum zu nehmen.

## Notwendige Schritte

1. Schritt: [Statistikschlüssel aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Dateneingabe
3. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
4. Schritt: [Schnittstellendateien erzeugen](../statistikdaten.erstellen.md)

Verlinkte Schritte werden in den jeweiligen Kapiteln beschrieben. Klicken Sie dazu auf den Link. Alle anderen Schritte werden nachfolgend ausführlich erklärt.

## 2. Dateneingabe

Sie erhalten eine Übersicht der Felder in den Dateien und wie diese in MAGELLAN bzw. DAVINCI einzupflegen sind.
Jede Schnittstellendatei wird in einem einzelnen Kapitel behandelt, die Links zu den Kapiteln finden Sie in der obersten Tabelle in der Spalte "Kapitel".

### Voraussetzungen für alle Daten

Damit die Dateien korrekt erstellt und gefüllt werden können, müssen in MAGELLAN bestimmte Datenfelder immer gefüllt werden. Ist einer der Felder nicht gefüllt erhalten Sie entsprechende Meldungen und der Export wird nicht durchgeführt.

| Datei | Datenfeld in MAGELLAN/DAVINCI | Beschreibung
| ----- | ----------------------------- | ------------
| ALLE  | MAGELLAN: `Mandanten > Daten 2 > Schulformen` | Hauptschulform Ihrer Schule. <br/>Bei Berufskollegs = BK. <br/>**NEU:**<br/>MAGELLAN benötigt jeweils die Hauptschulform, für die Ihre Statistik gelten soll. Diese Schulform sollte als erste erscheinen. MAGELLAN beinhaltet die Möglichkeit die Mandanten-Schulformen anhand des neuen Feldes "Position", diese komfortabel für Sie einzustellen.
| ALLE  | MAGELLAN: `Mandanten > Daten 1 > Schulnummer` | Die Schulnummer Ihrer Schule.
|ALLE| `MAGELLAN > Klassen > Daten > Statistikkürzel`| Bitte übernehmen Sie in dieses Feld bitte den Eintrag aus dem Feld Kürzel. Für die Statistik werden nur Schüler berücksichtigt, die in einer Klasse sind, die diesen Eintrag hat. Bitte kontrollieren Sie, dass auch für die Klassen der vorangegangenen relevanten Zeiträume dieser Wert gefüllt ist.


## 4. Daten erstellen

!!! info "Hinweis"
     Bitte achten Sie darauf, dass Sie für das Erstellen der Daten in MAGELLAN den aktuellsten Zeitraum geöffnet haben.

Die Daten erstellen Sie wie folgt:

1. Klicken Sie im Menü Extras auf `Exporte > Export`.
2. Wenn Sie im MAGELLAN Adminstrator Ihr Bundesland `Nordrhein-Westfalen` hinterlegt haben, steht Ihnen bei der Auswahl der Exportschnittstelle `Landesstatistik Nordrhein-Westfalen` zur Auswahl.
3. Unter Exportdateien wählen Sie die zu erzeugenden Exportdateien aus.
4. Unter Export-Zeiträume stellen Sie den aktuellen Zeitraum ein und die beiden vorangegangenen Halbjahre. Diese sollten bereits nach oben vorsortiert sein.
5. Wenn Sie die LEHRER.TXT für den Export ausgewählt haben, müssen Sie hier Ihre DAVINCI Exportdatei hinterlegen.
6. Klicken Sie auf `Weiter`, um fortzufahren.

### Besonderheiten

#### 2021/2022

Mit MAGELLAN Version 8.0.13 werden keine Datensätze `Bildungsgang abgeschlossen` mehr ausgespielt. Bildungsgangwechsler werden als `Neuzugang an gleicher Schule` erkannt und es werden zusätzliche VO- und LS- Felder gefüllt. ASDPC erkennt den veränderten Bildungsgang und damit den Bildungsgangwechsel.

#### 2020/2021

`Schüler > Daten 1 > Geschlecht` - Ab diesem Jahr möchte das Statistikamt zwei zusätzliche Merkmale zum Geschlecht, sofern diese auftreten. Wie im letzten Jahr bereits berücksichtigt, da MAGELLAN dies schon umgesetzt hatte, den Schlüssel 5 = DIVERS und ab diesem Jahr neu Schlüssel 6 = Nicht eingetragen (im Geburtenregister).
Divers ist als Geschlecht in MAGELLAN auswählbar. Schlüssel 6 wird automatisch erzeugt, wenn kein Geschlecht angegeben wurde.
