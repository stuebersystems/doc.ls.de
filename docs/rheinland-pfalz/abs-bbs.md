# Rheinland-Pfalz - ABS und BBS

Dieses Kapitel beschreibt für Allgemeinbildende und Berufsbildenden Schulen in Rheinland-Pfalz die benötigten Schritte zum Erstellen der elektronischen Landesstatistik für den Abgleich mit dem Statistikamt in Bad Ems im Schuljahr 2018/2019.

> #### danger::Achtung!
>
> Zum Erstellen der Statistikdateien benötigen Sie eine Lizenz für das Modul MAGELLAN Landesstatistik 2018 und mindestens die MAGELLAN Version 6.5.23!


Lesen Sie die Angaben und Vorgehensweise dieses Dokuments sehr genau und beachten Sie bitte alle Ihre Schulart betreffenden Aussagen.

Aktuelle Änderungen zur Statistik 2018/2019 sehen Sie [**hier!**](https://doc.ls.stueber.de/rheinland-pfalz/changelog/)

## Einführung

Das statistische Landesamt fordert die elektronische Landesstatistik im XML Dateiformat. Die statistischen Daten können in diesem Format aus Magellan heraus erzeugt werden.
Für Sie als Schule bedeutet dies: Sie müssen die folgenden XML-Dateien je nach Schulart an das Statistikamt in Bad Ems verschicken:


| Schulart                      | Dateiname                           |
|:------------------------------|:------------------------------------|
| Für Allgemeinbildende Schulen | SchuelerAbsNeuanlage_2018_xxxxx.xml |
| Für Allgemeinbildende Schulen | SchuelerAbsBewegung_2018_xxxxx.xml  |
| Für Berufsbildende Schulen    | xxxxx-SchuelerBbsNeuanlage.xml      |
| Für Berufsbildende Schulen    | xxxxx-SchuelerBbsBewegung.xml       |
| Für Berufsbildende Schulen    | xxxxx-LehrerNeuanlage.xml           |



Hierbei steht xxxxx für Ihre Schulnummer.

Die Neuanlage- und Bewegungsdaten sind für alle Schulformen erforderlich und größtenteils identisch. Das Statistikamt fordert diese Daten aus dem aktuellen und den zwei vorangegangenen Halbjahren.

Die Daten der SchuelerNeuanlage kommen aus dem aktuellen Halbjahr (1. Halbjahr 2018/2019). Für die Daten der SchuelerBewegung wird das gesamte vorangehende Schuljahr (1. und 2. Halbjahr 2017/2018) ausgewertet. 
Die Daten der LehrerNeuanlage dagegen werden zeitraumunabhängig herangezogen und werden nur für Berufsbildende Schulen aus MAGELLAN heraus erstellt. Wie Sie diese Dateien an das Statistikamt versenden, wird Ihnen direkt durch das Statistikamt mitgeteilt.

> ABS-STATISTIK OHNE LEHRERANGABEN
> Für Allgemeinbildende Schulen sind im Schuljahr 2018/2019 keine Lehrerangaben notwendig, da die Lehrerdatei nur über die Excel-Datei der ADD erstellt wird.

## DAVINCI-LIZENZ?

Gymnasien/Gesamtschulen \(Oberstufe\) benötigen für die Landesstatistik jeweils das Stunden- und das Kursplanmodul von daVinci zur Vervollständigung der Statistikdaten.
Berufsbildende Schulen benötigen für die Landesstatistik jeweils das Stundenplanmodul von daVinci zur Vervollständigung der Statistikdaten.
Lesen Sie folgende Punkte aufmerksam durch. Punkte, die nur für Gymnasien\/Gesamtschulen mit Oberstufe oder Berufsbildende Schulen interessant sind, werden gesondert ausgezeichnet.

## Notwendige Schritte


1. Schritt:[Schlüsselverzeichnisse importieren, PLZs aktualisieren](https://doc.ls.stueber.de/schluesselverzeichnisse/). Bitte beachten Sie den Abschnitt "Besonderheiten 2018/2019" am Ende der Beschreibung!
2. Schritt: Statistisch relevante Daten in daVinci bzw. Magellan eingeben
3. Schritt: Kurswahlen von daVinci nach Magellan übertragen \(nur für Gymnasien\/Gesamtschulen mit Oberstufe\)
4. Schritt: Statistikdaten aus daVinci exportieren
5. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
6. Schritt: Statistikdaten erstellen.    

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

Das Statistikamt gibt jährlich aktualisierte Schlüssel für die Landesstatistik heraus. Die aktuellen Schlüssel des Statistikamtes finden Sie auf der gemeinsamen Veröffentlichungsplattform von Schulaufsicht und amtlicher Statistik \(www.egsch.bildung-rp.de\).
Eine Anleitung zum Import finden Sie im Abschnitt [Schlüsselverzeichnisse](https://doc.ls.stueber.de/schluesselverzeichnisse/).

> #### warning::Wichtig!
>
> In diesem Jahr müssen bitte zusätzlich  die Postleitzahlen neu eingelesen werden. Im Anschluss müssen die Gemeinden synchronisiert werden, eine Anleitung finden Sie im Abschnitt [Schlüsselverzeichnisse](https://doc.ls.stueber.de/schluesselverzeichnisse/)!


## Stundenplandaten

Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang, in einer tabellarischen Übersicht.

Sie müssen zusätzliche Eingaben im Kurs- und Stundenplanmodul von daVinci vornehmen. Genauere Informationen zu den Eingaben für daVinci finden Sie in der nachfolgenden tabellarischen Übersicht.

### Für die Oberstufe bei Gymnasien/Gesamtschulen


| Wo                                | Was                                      |
|-----------------------------------|------------------------------------------|
| Stammdaten > Klassen              | Bitte erfassen Sie in der Spalte ID für alle MSS-Klassen die Magellan-ID. |
| Stammdaten > Fächer               | Für alle Fächer muss in der Spalte „Schlüssel“ der vom Statistikamt vorgeschriebene Schlüssel erfasst werden, z.B. „4“ für das Fach Deutsch. |
| Veranstaltungsübersicht > Klassen | Für die MSS-Klassen müssen alle Leistungs- und Grundkurse vorhanden sein. Bei schulübergreifendem Unterricht muss im Feld Bemerkungen (siehe Statistikfeld KursArt im Anhang) die Schulnummer der unterrichtenden Schule eingetragen werden. Ist ihre Schule nicht die unterrichtende Schule muss der Kurs mit Dauer =“0“ in die Veranstaltungsübersicht der Klasse aufgenommen werden. |



### Abgleich der IDs zwischen MAGELLAN und DAVINCI


Wir empfehlen Ihnen beim Abgleich der IDs der Schüler, Klassen, Lehrer und Fächer sicherheitshalber wie folgt vorzugehen:
1.	Öffnen Sie Magellan und wechseln Sie in die entsprechende Ansicht Schüler, Klassen oder Lehrer. Die Fächerliste finden unter Verzeichnisse, Fächer. 
1.	Exportieren Sie die Auswahlliste nach Excel und drucken Sie diese zur Vorlage aus.
2.	Öffnen Sie daVinci und wechseln Sie in die entsprechende Ansicht. 
3.	Vergleichen Sie die IDs und Kürzel Ihrer Vorlage mit den IDs und Kürzel in der daVinci Ansicht und korrigieren Sie ggf. in daVinci.

## Für Berufsbildende Schulen


### Stammdaten

Damit das Klassen-Soll erfasst werden kann, muss jeder Klasse eine Stundentafel zugeordnet werden.

### Veranstaltungsliste

Einige Daten für die Statistik errechnen sich unmittelbar aus den Unterrichtsangaben in der Veranstaltungsliste. Für jede Veranstaltung sollten daher der Lehrer, die Klasse, das Fach und die Unterrichtsstunden eingetragen sein.

### Lehrer-Soll-Berechnung


| Wo                                 | Was                                      |
|------------------------------------|------------------------------------------|
| Fachpraxiserhöhung                 | Errechnet sich aufgrund der Aufsummierung der Einträge in der Spalte Differenz der Stundentafel der Klasse. |
| Soll-Änderung eines Fachs          | Errechnet sich aufgrund des Einträge in der Spalte Differenz der Stundentafel der Klasse für das entsprechende Fach. |
| Soll-Änderungsgrund für die Klasse | Die Änderungsgründe sind ab der Statistik 2014/15 veranstaltungs- und nicht mehr klassenbasiert einzutragen. Wählen Sie dazu in der Veranstaltungskategorie (Veranstaltungsliste > Rechtsklick auf die Veranstaltung > Veranstaltung bearbeiten > Kategorie) den entsprechenden Schlüssel aus. Die Schlüssel (aus der Datei „25_RLP_Veranstaltungskategorien.keys“) können Sie unter Extras > Schlüsselverzeichnisse > Veranstaltungskategorien > Import in Ihre Plandatei importieren. |



### Kurswahldaten und Lehrerdaten von daVinci nach Magellan übertragen

Nachdem Sie die Statistikkontrolle durchgeführt haben und die IDs in beiden Programmen übereinstimmen, sollten sie die Kurswahldaten (für Allgemeinbildende Schulen mit Oberstufe) und Lehrerdaten übernehmen, wie im daVinci Handbuch im Kapitel „Spezielles“  unter „Datenaustausch mit Magellan“, „Daten nach Magellan übergeben“ beschrieben.

>
Bitte beachten Sie, dass Sie nur mit Kopien der daVinci Datei und Magellan Datenbank arbeiten!
Statistikdaten aus daVinci exportieren

>Als allgemeinbildendes Gymnasium/Gesamtschule mit Oberstufe bzw. als Berufsbildende Schule müssen Sie aus daVinci statistikrelevante Daten exportieren. Diese exportierten Daten werden dann zur eigentlichen Statistikerstellung in Magellan verwendet.

>Ist Ihre Schule kein Gymnasium/keine Gesamtschule mit Oberstufe bzw. Berufsbildende Schule, so benötigen Sie keine daVinci-Daten für die Statistik.

Exportieren der statistisch relevanten Daten aus DAVINCI
So exportieren Sie Daten aus daVinci:
1.	Starten Sie daVinci.
1.	Klicken Sie dort im Menü Extras auf Exportieren.
2.	Wählen Sie unter Typ Rheinland-Pfalz und geben Sie die Exportdatei an.
3.	Klicken Sie auf OK. Die Daten werden jetzt in die angegebene Datei exportiert.

### Aufgestockte Grundkurse

Wie Sie aufgestockte Grundkurse in DAVINCI eintragen können, beschreiben wir [**hier**](https://doc.davinci6.stueber.de/course-plan/#aufgestockte-grundkurse).

## Statistikdaten aus DAVINCI exportieren

So exportieren Sie Daten aus DAVINCI:

1.	Starten Sie DAVINCI.
2.	Klicken Sie dort im Menü ```Plan``` auf ```Importieren und Exportieren```.
3.	Wählen Sie unter Export den Punkt ```Statistikdaten exportieren``` aus und klicken Sie auf  ```Weiter```.
4.	Wählen Sie Ihr Bundesland (`Statistik Rheinland-Pfalz (auch edoo.sys) exportieren`) aus  und klicken Sie auf ```Weiter```.
5.	Geben Sie den Dateipfad und einen passenden Dateinamen ()Beispiel: mien.export.txtei zum Export der Statistikdaten an.

Klicken Sie auf `OK`. Die Daten werden jetzt in die angegebene Datei exportiert. Auf diese Datei verweisen Sie später aus dem Statistikassistenten von MAGELLAN.

 > #### warning::Wichtig!
 >
 > Diese Datei wird nur von Berufsbildenden Schulen und Gymnasien benötigt. 

## ABS: Wann wird die 2.Fremdsprache ausgegeben?
Ob nur die erste Fremdsprache in die ABSNeuanlage-Datei übergeben wird oder auch weitere berechnet MAGELLAN anhand von Einträgen in verschiedene Felder. Geprüft werden folgende Felder:

```Klasse > Zeiträume > Zeitraum > Klassenstufe```

```Klassen > Daten > Schulart```

```Schüler > Daten3 > Fremdsprache > Status```

```Schüler > Daten 4 > Förderung > Förderung```

**Beispiel:**

Die 2.Fremdsprache wird ausgelesen wenn, die Klassenstufe größer/gleich 5 ist, als Schulart der Klasse der Schlüssel 30 (Gymnasium) und der Fremdsprachenstatus 5 (Pflicht) gewählt wurde.

oder

Die 2.Fremdsprache wird ausgelesen wenn, die Klassenstufe größer/gleich 6 ist, die Schulart  20 (Realschule), 21 (Realschule Plus) oder  40 (IGS) und der Fremdsprachenstatus 6 (Wahlpflicht) oder 2 (Wahlfach (fakultativ)) ist.

oder 

Die 2.Fremdsprache wird ausgelesen wenn, die Klassenstufe größer 5 ist (also ab 6.Klasse), die Förderung nicht 20 (ganzheitliche Entwicklung) ist, die Schulart  20 (Realschule), 21 (Realschule Plus) oder  23 (Realschule Plus und Fachoberschule)  ist.

In allen anderen Situationen wird die 2.Fremdsprache (und Folgesprachen!) nicht für die Statistikdatei ausgegeben.



## Voraussetzungen


Wie Sie wissen, müssen je nach Statistikdatei unterschiedliche Datenmengen ausgespielt werden. In den Neuzugangsdateien beispielsweise nur Neuzugänge, in den Bewegungsdaten Abgänger und in der BBS aber auch Schüler, die den Bildungsgang beenden aber in der Schule verbleiben.

Dieser Abschnitt vermittelt Ihnen welche Werte in Magellan abgefragt werden, damit die Daten in den entsprechenden Statistikdateien berücksichtigt werden.


| Operator | Bedeutung   |
|----------|-------------|
| UND      | und         |
| ODER     | oder        |
| <        | kleiner als |
| >        | größer als  |
| =        | gleich      |



Beispiel:

Schüler.Status = 4 UND Abschluss1 = 18, bedeutet, der Ausdruck gilt, wenn der Schüler inaktiv ist und Schüler Abitur erlangt hat. Wenn zuzätzlich z.B. noch ODER Abschluss1 = 43 mit dabei wäre, dann gilt der Ausdruck auch, wenn ein Schüler statt dem Abschluss Abitur, den Abschluss FH-Reife hätte.

### Für Schülerneuzugangsdaten

> #### info::Wichtig
>
> Bitte beachten Sie, das hier lediglich die Punkte gezeigt werden, die dazu führen, dass der Schüler in die Datei gespielt wird. Alle zu füllenden Felder beschreiben wir im Abschnitt "Welche Eintragungen werden erwartet?".


Klassen und Schüler werden in der Statistikdatei berücksichtigt, wenn folgende Kriterien zutreffen:

**ABS**



| Datenfeld in MAGELLAN                    | Beschreibung MAGELLAN                    |
|------------------------------------------|-----------------------------------------:|
| Klassen > Daten > **Statistikkürzel**    | Es werden alle Schüler berücksichtigt, deren Klasse ein Statistikkürzel eingetragen wurde. Das Statistikkürzel sollte gleich dem Klassenkürzel sein. |
| Schüler > Statistik > **MerkmalS7**      | Um einzelne Schüler von der Statistik auszuschließen wählen Sie bitte den Wert „Ausschluss“ (Schlüsselwert „J“) aus. |
| Schüler > Zugang/Abgang > Abgang > **ZugangAm** | Erhebungsdatum	(ZugangAm <= Erhebungsdatum UND AbgangAm >= Erhebungsdatum) ODER AbgangAm = Leer |
| Schüler > Zugang/Abgang > Abgang > **AbgangAm** | Erhebungsdatum	(ZugangAm <= Erhebungsdatum UND AbgangAm >= Erhebungsdatum) ODER AbgangAm = Leer |



**BBS**



| Datenfeld in MAGELLAN                    | Beschreibung MAGELLAN                    |
|------------------------------------------|------------------------------------------|
| Klassen > Daten > **Statistikkürzel**    | Es werden alle Schüler berücksichtigt, deren Klasse ein Statistikkürzel eingetragen wurde. Das Statistikkürzel sollte gleich dem Klassenkürzel sein. |
| Schüler > Statistik > **MerkmalS7**      | Um einzelne Schüler von der Statistik auszuschließen wählen Sie bitte den Wert „Ausschluss“ (Schlüsselwert „J“) aus. |
| Schüler > Zugang/Abgang > Abgang > **ZugangAm** | ZugangAm <> Leer UND ZugangAm > Erhebungsdatum |
| **Erhebungsdatum**                       | ZugangAm <> Leer UND ZugangAm > Erhebungsdatum |



### Für Schülerbewegungsdaten

> #### info::Wichtig
>
> Bitte beachten Sie, das hier lediglich die Punkte gezeigt werden, die dazu führen, dass der Schüler in die Datei gespielt wird. Alle zu füllenden Felder beschreiben wir im Abschnitt "Welche Eintragungen werden erwartet?".


Die Bewegungsdatei enthält Schüler- und Klassendaten aus den vergangenen 2 Halbjahren. Für die aktuelle Herbststatistik bedeutet das, dass das 1.Halbjahr  und das 2. Halbjahr des vergangenen Schuljahres ausgewertet werden.

> #### danger::Achtung!
>
> Die Bewegungsdatei enthält Daten von Abgängern und Absolventen die bestimmte Anforderungen erfüllen.
> **ABS:**
> - Abgänger mit erfüllter Schulpflicht (auch ohne Hauptschulabschluss, also Abgänger-/innen)
> - Absolventen mit Hauptschulabschluss, qualifiziertem Sekundarabschluss I, erfüllten schulischen Voraussetzungen für die Fachhochschulreife oder Abiturienten
> - Absolventen die den höchst möglichen Abschluss an der Schule erreicht haben und an einer andere Schule wechseln um eine höhere Qualifikation zu erreichen 
>
>Beispiel: *Realschüler wechselt nach der 10. mit Realschulabschluss auf ein Gymnasium.
>
>**NICHT **in die Bewegungsdaten gehören:
> - Schüler die nur umziehen und daher die Schule wechseln
> - Schüler die von einer Schulart auf die gleiche wechseln (von einer Realschule zu einer anderen Realschule)
> - Schüler die von einer Gesamtschule (mit Oberstufe) aus Klasse 12 auf ein Gymnasium in die 13 wechseln (der Abschluss bleibe der selbe)
> - Schüler die von einer Realschule an eine Hauptschule wechseln oder vom Gymnasium auf die Realschule o.ä. 
> ---
>** BBS:**
> - jeder Schüler der einen Bildungsgang durchlaufen hat, egal ob mit Erfolg oder ohne Abgänger/Abbrecher, wenn sie ein Abgangszeugnis erhalten haben, dafür muss bei den Schülern das Feld `Schüler > Laufbahn > Abschluss > Abschluss1` gefüllt sein.




Klassen und Schüler werden in der Statistikdatei berücksichtigt, wenn eins der nachfolgenden Kriterien zutrifft:

**ABS und BBS**


| Datenfeld in MAGELLAN                    | Beschreibung MAGELLAN                    |
|------------------------------------------|------------------------------------------|
| Klassen > Daten > **Statistikkürzel**    | Es werden alle Schüler berücksichtigt, deren Klasse ein Statistikkürzel eingetragen wurde. Das Statistikkürzel sollte gleich dem Klassenkürzel sein. |
| Schüler > Statistik > **MerkmalS7**      | Um einzelne Schüler von der Statistik auszuschließen wählen Sie bitte den Wert „Ausschluss“ (Schlüsselwert „J“) aus.<br /> |
| Klasse > Zeiträume > Zeitraum > **Klassenstufe**<br /><br />Klassen > Daten 1 > **Schulart**<br /><br />Schüler > **Status**<br /><br />Schüler > Zugang/Abgang > Abgang > **Übergang**<br /><br />Schüler > Laufbahn > Allgemein > **Versetzungsart**<br /><br />Schüler > Laufbahn > Allgemein > **Entscheidung**<br /><br />Schüler > Laufbahn > Abschluss > **Abschluss1**<br /><br />Schüler > Laufbahn > Allgemein > **Wiederholungsart** | Status = 4 (Inaktiv) UND<br />Abschluss 1 = 1 (Abgang ohne HS-Abschluss) II<br />Abschluss 1 = 7 (HS-Abschluss) II<br />Abschluss 1 = 15 (Qualifizierte SK-I) II<br />Abschluss 1 = 18 (Abitur) II<br />Abschluss 1 = 43 (FH-Reife) ODER<br />Versetzungsart = 5 (Nicht versetzt) ODER<br />{ Übergänger berücksichtigen }<br />(Klassenstufe = 4 UND<br /> Schulart = 11 (Grundschüler) UND<br /> Uebergang <> Leer) ODER<br />{ UEOS-Verbleib berücksichtigen }<br />(Klassenstufe = 6) UND<br /> Entscheidung <> Leer) ODER<br />{ Freiwilliger Wiederholer / Überspringer <br /> berücksichtigen }<br />(<br /> (Klassenstufe = 5 ODER Klassenstufe = 6) UND<br /> (Wiederholungsart = 3 ODER Wiederholungsart = 5) <br />) <br /> |
| Klasse > Zeiträume > Zeitraum > **Klassenstufe** <br /><br />Schüler > **Status**<br /><br />Schüler > Laufbahn > Allgemein > **Versetzungsart**<br /><br />Schüler > Laufbahn > Abschluss > **Abschluss1Art** | Status = 3 (Aktiv) UND<br />{ Klassenstufe 12 oder 13 und Abitur nicht bestanden }<br />(Klassenstufe = 13 UND <br /> Abschluss1Art = 2 (Abitur nicht bestanden)) ODER<br />Versetzungsart = 5 (Nicht versetzt) ODER<br />{ Freiwilliger Wiederholer / Überspringer berücksichtigen }<br />(<br />(Klassenstufe = 5 ODER Klassenstufe = 6) UND<br />(Wiederholungsart = 3 ODER Wiederholungsart = 5)<br />) |




**Nur BBS**



| Datenfeld in MAGELLAN                    | Beschreibung MAGELLAN                    |
|------------------------------------------|------------------------------------------|
| Klassen > Daten > **Statistikkürzel**    | Es werden alle Schüler berücksichtigt, deren Klasse ein Statistikkürzel eingetragen wurde. Das Statistikkürzel sollte gleich dem Klassenkürzel sein. |
| Schüler > Statistik > **MerkmalS7**      | Um einzelne Schüler von der Statistik auszuschließen wählen Sie bitte den Wert „Ausschluss“ (Schlüsselwert „J“) aus. |
| Schüler > **Status** <br/><br/> Schüler > Laufbahn > Abschluss > **Abschluss1Datum** | Status = 3 (Aktiv) UND Abschlussdatum muss innerhalb des entsprechenden Schulhalbjahres liegen, um Schüler auszuschließen, die einen Abschluss zuvor oder danach gemacht haben. |
| Schüler > **Status** <br/><br/> Schüler > Zugang/Abgang > Abgang > **AbgangAm** | Status = 4 (Inaktiv) UND Abgangsdatum muss innerhalb des entsprechenden Schulhalbjahres liegen, um Schüler auszuschließen, die zuvor oder danach abgegangen sind. |


### Für Lehrerdaten


Lehrer werden in der Statistikdatei berücksichtigt, wenn folgende Kriterien zutreffen:


| Datenfeld in MAGELLAN                    | Beschreibung MAGELLAN                    |
|------------------------------------------|------------------------------------------|
| Lehrer > **Status**<br/><br/> Lehrer > Daten 2 > **Abgangsart**<br /><br /> Lehrer > Daten 2 > **Zugang am**<br/><br/> Lehrer > Daten 2 > **Abgang am**<br/><br/> **Erhebungsdatum**<br/><br/> **Erhebungsdatum letzter Statistik** | Status = 1 aktiv, blaue Raute ODER Status = 0 inaktiv, graue Raute <br/> UND <br/> Abgang am <> leer <br/> UND <br/> Abgang am <= Erhebungsdatum <br/> UND <br/> Abgang am > Erhebungsdatum letzter Statistik <br/> UND <br/> Abgangsgrund <> leer |




> #### warning::Wichtig!
>
> Lehrer, die nach dem letzten Statistiktermin an Ihre Schule wechselten und vor dem aktuellen Statistiktermin Ihre Schule verlassen haben, werden statistisch nicht an Ihrer Schule ausgewertet, sollen also nicht in Ihrer LehrerNeuanlage.xml erscheinen. Sie werden statistisch an der Herkunftschule als Abgang und an der neuen Schule als Zugang geführt.

### Für allgemeine Daten


| Statistikfeld in der Statistikdatei | Datenfeld in MAGELLAN/DAVINCI            | Beschreibung                             | Statistikdatei |
|-------------------------------------|------------------------------------------|------------------------------------------|----------------|
| DateiKopf > **SchulNr**             | MAGELLAN: Mandanten > Daten 1 > Schulnummer | Geben Sie hier Ihre Schulnummer ein.     | Alle           |
| DateiKopf > **ErhebungsJahr**       |                                          | Das Erhebungsjahr wird automatisch beim Erstellen der Statistikdateien mit eingetragen und muss nicht in MAGELLAN eingegeben werden. | Alle           |





## Besonderheiten der Statistik nach Schuljahren

### Besonderheiten Statistik 2018/2019
 
#### Gebietsreform

Einige Werte im Verzeichnis Postleitzahlen haben sich verändert, daher muss bitte das Postleitzahlverzeichnis (ab Version 6.5.23) neu importiert werden und anschließend die Synchronisierung der Postleitzahlen und Ort der Schüler mit den Inhalten des Postleitzahlverzeichnisses durchgeführt werden.


##### Postleitzahlverzeichnis importieren

Prüfen Sie bitte, ob in Ihrem Schulnetzwerk mindestens die 6.5.23 eingesetzt wird.
Öffnen Sie anschließend bitte im MAGELLAN Administrator den Punkt `Datenimporte > Postleitzahlverzeichnis importieren`. 
Wählen Sie im Assistenten für `für folgendes Land` den Wert `Rheinland-Pfalz` aus und für `importiere folgenden Katalog` bitte `alle Kataloge`. Starten Sie den Assistenten über die Schaltfläche `Fertigstellen`.

![Importieren des Postleitzahlverzeichnisses](../images/RLP_PLZ_importieren.png)

##### Gemeinden synchronisieren

Wenn das Einlesen der Postleitzahlen abgeschlossen ist, müssen die neuen Einträge im Verzeichnis mit den bestehenden Werten der Schüler, Lehrer, Schulen und Betriebe abgeglichen werden. Dabei wird die Postleitzahl und der Ort des jeweiligen Datensatzes (je Schüler, Lehrer usw.) mit den Inhalten des Postleitzahlverzeichnisses verglichen und falls eine Übereinstimmung vorliegt mit der Gemeindekennziffer ergänzt.

![Synchronisieren der Gemeinden](../images/RLP_Gemeinden_sync.png)

##### Vollständigkeit der Gemeindekennziffern für Schüler überprüfen

Sollte anhand der Postleitzahl und des Ortes zwischen den Schülern und dem Postleitzahlverzeichnis keine Übereinstimmung festgestellt werden, bekommt der Schüler keine Gemeindekennziffer zugewiesen. In der Regel genügt die Korrektur des Schülerortes oder der Schüler-PLZ und ein erneuter Durchlauf des `Gemeinden synchronisierens`. Damit Sie einen Überblick haben, für welchen Schüler die Zuweisung nicht gelungen ist, finden Sie in `MAGELLAN > Mandanden > Mandant markieren > Drucken ` den Prüfbericht "Mandant (Ausgabe Schueler ohne Gemeindekennziffer).rpt". Rufen Sie pro Halbjahr diesen Bericht auf, es werden nur Schüler gezeigt, denen keine Gemeindekennziffer zugeordnet werden konnte.

#### Verzeichnis Herkunftsarten (ABS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 1         | 1: Schüler/-in, für 2018/19 schulpflichtig und jetzt eingeschult (gem. § 57 SchulG)" | Textänderung |
| 2         | 2: Schüler/-in, für 2017/18 schulpflichtig, aber erst jetzt eingeschult (gem. § 58 Abs.2 SchulG) | Textänderung |
| 3         | Schüler/-in, nach der Einschulung im August 2017 im Laufe des Schuljahres 2017/18 zurückgetreten und jetzt wieder aufgenommen (gem. § 6 Grundschulordnung) | Textänderung |



#### Verzeichnis Lehrer-Abgänge (ABS/BBS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 9         | 9: Dauerhafte Dienstunfähigkeit bzw. Berufs- oder Erwerbsunfähigkeit | Textänderung |
| 26        | 26: Versetzung an Behörden außerhalb des Schuldienstes (z. B. Schulbehörde, BM, Studienseminar) | Textänderung |



#### Verzeichnis Lehrer-Zugänge (ABS/BBS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 25        | Rückkehr nach Tätigkeit bei einer Behörde außerhalb des Schuldienstes (z. B. Schulbehörde, BM, Studienseminar) | Textänderung |


#### Verzeichnis Schulformen-Herkunft (BBS)


| Schlüssel | Bezeichnung                        | Änderung     |
|-----------|------------------------------------|--------------|
| 824       | 824: Höhere Berufsfachschule (HBF) | Textänderung |



#### Verzeichnis Berufe (BBS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 26312170  | 26312170: Informations- und Telekommunikationssystem-Elektroniker/in | Textänderung |
| 62322320  | 62322320: Fachpraktiker/in für Fachverkauf im Lebensmittelhandwerk (§42m HwO) SP Fleischerei | Textänderung |


#### Verzeichnis Bildungsgaenge (BBS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 8610082   | 8610082: FS Sozialwesen Fr Sozialpädagogik (berufsbegleitend- 48 Std.) | Textänderung |



#### Besonderheiten Statistik 2016/2017

#### Bildungsgang 8610080 FS Sozialwesen (BBS)

**Schüler mit Berufspraktikum**

Schüler/innen, die im vergangenen Jahr den Bildungsgang 8610080 FS Sozialwesen
Fr Sozialpädagogik besucht haben und in diesem Jahr ihr Berufspraktikum absolvie-
ren, werden nicht ausgeschult. 
Bitte ändern Sie den Bildungsgang unter ```MAGELLAN > Schüler > Ausbildung > Bildungsgang```
von 8610080 auf 8610081 geändert und Klassenstufen unter ```Klasse > Zeiträume > Zeitraum > Klassenstufe``` um 1 Jahr. Für die so markierten Schüler werden keine Neuzugangs- oder Vorbildungsdaten erzeugt.

**Schüler, die den Bildungsgang abbrechen**

Schulen Sie diese Schüer aus und vergeben unter ``` Schüler > Laufbahn > Abschluss > Abschluss1``` den Schlüssel 50 (Abgangszeugnis (aufgrund Abgang vor Bildungsgangende)).


#### Verzeichnis Herkunftsarten (BBS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 7         | Berufsreife (ehemals Hauptschulabschluss) | Textänderung |



#### Verzeichnis Herkunftsarten (ABS)


| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| 1         | Schüler/-in, für 2016/17 schulpflichtig und jetzt eingeschult (gem. § 57 SchulG) | Textänderung |
| 2         | Schüler/-in, für 2015/16 schulpflichtig, aber erst jetzt eingeschult (gem. § 58 Abs.2 SchulG) | Textänderung |
| 3         | Schüler/-in, nach der Einschulung im August 2015 im Laufe des Schuljahres 2015/16 zurückgetreten und jetzt wieder aufgenommen (gem. § 6 Grundschulordnung) | Textänderung |


 
#### Besonderheiten Statistik 2014/2015

**Berufskennziffern austauschen**

>Nur, wenn Sie noch nicht die neue Systematik der Berufskennziffern nutzen, sollten Sie diesen Abschnitt berücksichtigen!

Für das Schuljahr 2014/2015 mussten aufgrund einer systematischen Änderung der Berufskennziffern, die aktuell enthaltenen Berufskennziffern in Magellan ausgetauscht werden, bevor die neuen Statistikschlüssel auf dem üblichen Wege aktualisiert werden können.

1.	Öffnen Sie Magellan-Administrator und wechseln Sie in die Ansicht ```Datenbankpflege```. 
2.	Klicken Sie auf ```Starten``` im ```Datenbank überprüfen```.
3.	Im Dialogfenster wählen Sie als Datenbank Magellan-Datenbank und als Aktion ```RLP-Berufskennziffern austauschen``` aus.
4.	Klicken Sie auf ```OK```. Es erscheint ein Dialogfenster mit Fortschrittsanzeige, warten Sie bis die Aktion beendet wurde, um die Dialogfenster zu schließen.

Danach können die Schlüsselverzeichnisse auf dem üblichen Wege aktualisiert werden. 
[Bitte schauen Sie hier.](https://doc.ls.stueber.de/schluesselverzeichnisse/schlusselverzeichnisse/)


**Einzelne Schüler von der Statistik ausschließen** 
Durch den Import der Schlüsselverzeichnisse AS_SchuelerMerkmale.keys oder BS_SchuelerMerkmale.keys wird ein neuer Schlüssel für das Feld Schüler > Statistik > MerkmalS7 erzeugt. Sie können durch Auswahl des Werts „Ausschluss“ den Schüler nicht in die Statistikdaten mit ausgeben. 
Sie können den Schlüssel auch manuell anlegen, wechseln Sie dazu zm Punkt Verzeichnisse > Merkmale und tragen die folgenden Werte ein:


| Kürzel     | Schlüssel | Bezeichnung                            | Bereich   |
|------------|-----------|----------------------------------------|-----------|
| Ausschluss | J         | Schüler von der Statistik ausschließen | MerkmalS7 |



**Neue Berufskennzahlen**
Durch die Umstellung der Berufskennzahlen in ein neues System, müssen alle bestehenden Berufsschlüssel in MAGELLAN ausgetauscht werden. Dies sollten Sie vor dem Import der neuen Schlüsselverzeichnisse gemacht haben. Bitte lesen Sie dazu den Abschnitt [Berufskennziffern austauschen](https://doc.ls.stueber.de/rlp/rheinland-pfalz_-_abs_und_bbs/#berufskennziffern-austauschen).

**Kreisgebietsreform**
Ab diesem Jahr gibt es einen gesonderten Postleitzahlen-Import für Rheinland-Pfalz im MAGELLAN-Administrator unter Datenimport > Postleitzahlen importieren. Importieren Sie die aktuellen Postleitzahlen und anschließend das Gemeindeverzeichnis über die Auswahl Ihres Bundeslandes. Damit erhalten Sie die aktuellen Umschlüsselungen der Verbands-gemeinden durch die Kreisgebietsreform.

>Bedenken Sie bitte, dass Sie danach über Datenbankpflege > Daten überprüfen die Gemeinden synchronisieren müssen.


| Feld                 | Was hat sich geändert                    | Datei                |
|----------------------|------------------------------------------|----------------------|
| Schueler > Neuzugang | Alle Schüler, die ein Zugangsdatum nach dem letzten Statistiktermin haben, werden als Neuzugang gekennzeichnet. | SchuelerBBSNeuanlage |
| Klasse > Beruf       | wird für diese Datei nicht mehr abgefragt und somit wird klassenseitig für die Statistik kein Berufsschlüssel mehr benötigt. Aus diesem Grunde ändert sich die Logik für die Eingabe des Berufes in MAGELLAN wie folgt: Wenn die gesamte Klasse für einen Ausbildungsberuf bestimmt ist, dann tragen Sie den Beruf bei der Klasse ein. In Klassen mit gemischten Ausbildungsberufen, tragen Sie den überwiegenden Berufsschlüssel bei der Klassen und die Abweichungen erfassen Sie in den Ausbildungsdaten der Schüler. **Es wird Schüler vor Klasse geprüft.** Diese Logik ändert nichts daran, dass Berufe für die Statistik nur in bestimmten Schulformen tatsächlich ausgespielt werden. | SchuelerBBSNeuanlage |


#### Besonderheiten Statistik 2013/2014


In den Schulabschlüssen (BP_AbschlussArt, BP_ZweitAbschluss, BP_Schulabschluss) gibt es Neuerungen:


| Entfällt                                 | wird ersetzt durch                       |
|------------------------------------------|------------------------------------------|
| **48** - Fachhochschulreife (mindestens schulischer Teil) | **43** - Fachhochschulreife  (schulischer Teil)" und **44** - Fachhochschulreife (schulischer und praktischer Teil) |



#### Besonderheiten Statistik 2011/2012


**Manuelle Änderungen der Kataloge:**
Zum Schuljahr 2010/11 wurde der Schlüssel der Verbandsgemeinde für die Stadt Cochem geändert. Durch Einschluss der ehemaligen verbandsfreien Gemeinde Cochem in die Verbandsgemeinde Cochem-Land, wurde diese Änderung erforderlich. 

Bitte ändern Sie in MAGELLAN unter Verzeichnisse > Postleitzahlen > Gemeinden (bitte oben rechts Rheinland-Pfalz wählen) in der Spalte "VG" den Wert für "Cochem, Stadt" von "00" auf "01".

| Schluessel | Bezeichnung  | VG |
|------------|--------------|----|
| 07135020   | Cochem,Stadt | 01 |



#### Besonderheiten Statistik 2010/2011


Die Bezeichnungen der Schlüssel werden aus Gründen der Eindeutigkeit von Schlüsseln nicht geändert. Von Zeit zu Zeit erhalten bestehende Schlüssel neue Bedeutungen und es wird lediglich die Bezeichnung verändert. Solche Schlüssel müssen von Ihnen manuell verändert werden.

In MAGELLAN ist unter  "Klassen > Daten > Beruf" bei einer Klasse der Berufsschule immer ein Beruf einzutragen (bei BVJ optional), um eine korrekte Fehlererkennung zu gewährleisten. 

>Wird einer der folgenden  „Sonderberufe“ eingetragen, dann wird die Ausgabe dieses Klassen-Berufs in der Statistikdatei SchuelerBbsNeuanlage.xml unterdrückt, da das StaLa dies erfordert.


| Schlüssel | Bedeutung                                |
|-----------|------------------------------------------|
| 96000100  | Mithelfende im elterlichen Betrieb oder Haushalt |
| 97000100  | Beschäftigungsverhältnis ohne Ausbildungsvertrag |
| 98000100  | Nichtbeschäftigte (Arbeitslose)          |
| 99000100  | Berufsvorbereitungsjahr                  |
| 99000150  | Schüler/-in in Sondermaßnahmen  Schüler/-in in Sondermaßnahmen |



#### Besonderheiten Statistik 2009/2010

**ABS**


| Feld                                     | Was hat sich geändert                    | Datei                |
|------------------------------------------|------------------------------------------|----------------------|
| Klasse > G8GTS                           | bitte markieren Sie die G8-Klassen mit „Ja“ oder Nein unter Klassen > Merkmale > Merkmal B3. | SchuelerAbsNeuanlage |
| Schueler > ABS2BBS                       | LMZ-Projekt wird automatisch  anhand des Grundschuleintrittes [1997-2001] in die Datei übernommen. | SchuelerAbsNeuanlage |
| Klasse > Schueler > FremdSprachen > FremdSprache > StatusFach | Für die Erfassung dieses Wertes wurden ab der Version 5.2.22 in MAGELLAN neue Felder angelgelegt, die auch per Sammelzuweisung befüllt werden können. Sie finden die neuen Felder unter Schüler > Daten3 > Fremdsprachenfolge > Zusatz.  Sie können aus einer vorgegebenen Werteliste auswählen, diese Werte werden von automatisch als entsprechender Schlüsselwert in die Statistikdatei übertragen.  Unter Bearbeiten > Sammelzuweisung haben Sie die Möglichkeit die Werte auch für mehrere Schüler gleichzeitig zu vergeben. | SchuelerAbsNeuanlage |
| Klasse > Schueler > LaufbahnEmpfehlung   | Es wurde die Bedeutung eines bereits bestehenden Schlüssels verändert. Bitte ändern Sie nach dem Einlesen der Schlüssel unter MAGELLAN > Verzeichnisse > weitere Schlüsselverzeichnisse > Empfehlungen folgendes ab: Der Schlüssel sollte nicht entfernt werden, da die Verwendung in der Vergangenheit korrekt war. Bitte ergänzen Sie stattdessen das GueltigBis-Datum (01.08.2008) und ändern den Wert in der Spalte Schluessel auf „alt“. | SchuelerAbsBewegung  |
| Klasse > Schueler > NichtVersetzt        | Bitte kontrollieren Sie zusätzlich das Verzeichnis „Versetzungsarten“. Hier wurde im letzten Jahr die Bedeutung des Schlüssels mit dem Schlüsselwert 5 verändert. Bitte achten Sie darauf, dass folgende Eintragungen vorgenommen worden sind: Kürzel und Schlüssel erhalten den Wert 5, die Bezeichnung ist "Schüler/-in wurde nicht versetzt". | SchuelerAbsBewegung  |



**BBS**


| Feld                                   | Was hat sich geändert                    | Datei                |
|----------------------------------------|------------------------------------------|----------------------|
| Klasse > Schueler > Name  und  Vorname | werden neu mit in die Datei mit ausgegeben. | SchuelerBBSNeuanlage |
| Keine Änderungen                       | Keine Änderungen                         | SchuelerBBSBewegung  |




#### Besonderheiten Statistik 2008/2009


Anpassung der Schlüsseltabellen an das Statistische Landesamt:

Das StaLa verwendet zum Teil andere Bezeichnungen für Schlüsseltabellen (auch mit anderen Bedeutungen),  als es in Magellan der Fall war. 

Wenn das StaLa von Schularten sprach, war in Magellan von Schulformen die Rede. In Magellan befanden sich im Verzeichnis Schularten statistische Daten für die LehrerNeuanlage. Wir haben dies jetzt an das StaLa angepasst, damit es in Zukunft nicht mehr zu Verwirrungen kommt. 

Dies bedeutet für Sie:


| Feld                        | Was hat sich geändert                    | Datei |
|-----------------------------|------------------------------------------|-------|
| Schularten                  | Die Schularten, wie sie in den Plausibilitätsmeldungen erwähnt werden, müssen in Klasse > Schularten eingetragen werden. | -     |
| Schulformen                 | Die Schulformen befinden sich in Klasse > Schulformen. | -     |
| Verfuegbar > SchulFormStufe | Das Statistikfeld Verfuegbar > SchulFormStufe für die LehrerNeuanlage befindet sich in Klasse > Merkmale > Merkmal S3. | -     |



**Für BBS**


| Feld                                     | Was hat sich |
|------------------------------------------|--------------|
| geändert                                 | Datei        |
| Schüler > Laufbahn > Abschluss > Abschluss1 > Abschlussdatum | Pflichtfeld  |


