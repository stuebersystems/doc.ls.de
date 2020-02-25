# Einführung und Statistikkonzept

Die meisten Schulen müssen mindestens einmal im Jahr eine umfangreiche Schulstatistik erstellen und diese Daten an die jeweils zuständige Stelle übermitteln. Dabei muss man von folgenden Voraussetzungen ausgehen:

In jedem Bundesland wird die Statistik in eine Allgemeinbildende und eine Berufsbildende Statistik unterschieden.

* In jedem Bundesland gibt es jeweils eigene statistische Vorgaben. Diese Vorgaben legen den Inhalt der Statistik (Welche Daten werden abgefragt?) und die Form (Papier oder elektronisch?) fest.

* Jedes Bundesland definiert Schlüsselverzeichnisse, die den Inhalt bestimmter Angaben festlegen (z.B. Staatsangehörigkeiten) .

* Alle Statistiken müssen je nach Bundesland und je nach Schulart zu einem festgelegten Erhebungszeitpunkt (meistens im Herbst) erstellt werden.

* Der Aufwand, die geforderte Statistik per Hand zu erstellen, ist in der Regel sehr hoch, egal ob die Daten in Form von Papierbögen ausgefüllt  oder mit Hilfe einer speziellen Erfassungssoftware eingetippt werden müssen.

Eine Schulverwaltungssoftware wie MAGELLAN bietet natürlich eine wesentlich bessere Ausgangsbasis zum Erstellen einer Schulstatistik. Zusammen mit der Stundenplansoftware DAVINCI liegen alle Grunddaten schon in elektronischer Form vor, so dass die Schulstatistik weitestgehend automatisiert berechnet werden kann. Die Zukunft der Schulstatistik liegt ganz klar im elektronischen Austausch von Daten zwischen Schulen und Statistikamt, auch wenn noch nicht alle Bundesländer diesen Weg vollständig unterstützen. Im Folgenden wird das Statistikkonzept von MAGELLAN und DAVINCI näher beschrieben.

## Bevor Sie beginnen

Grundlage für die elektronische Erfassung der Landesstatistikdaten sind Dateien, die von der Schulverwaltungs- bzw. Stundenplansoftware erzeugt werden. Welche Dateien das sind und wie deren Inhalt aussieht, wird durch die Spezifikationen der Schnittstelle Ihres Bundeslandes bestimmt. Diese Spezifikationen erhalten Sie von Ihrem Kultusministerium bzw. Ihrem Statistikamt.

Um Fehler bei der Statistik zu vermeiden, müssen Sie sich unbedingt an diese Spezifikationen halten. So dürfen in der Regel Klassen-, Lehrer- und Fachkürzel oft eine bestimmte Maximallänge an Buchstaben nicht überschreiten.

Zwecks Vermeidung von Eingabefehlern werden in MAGELLAN und DAVINCI bereits bundeslandspezifische Schlüssel mitgeliefert. Diese Schlüssel können Sie in den jeweiligen Programmen importieren. Sie sollten  die vorliegende Dokumentation und die offiziellen Dokumentationen zur Landesstatistik sorgfältig beachten, um unnötigen Aufwand zu vermeiden.

Lesen Sie das für Ihre Schule zutreffende Kapitel in diesem Dokument sehr genau. Beachten Sie außerdem sorgfältig die Spezifikationen Ihres Kultusministeriums bzw. Ihres Statistikamts.

!!! info "Hinweis"

    Überprüfen Sie in MAGELLAN und DAVINCI, ob Ihre Schlüsselverzeichnisse korrekt sind. Korrigieren Sie sie evtl. gemäß der Vorgaben des Statistikamts bzw. des Kultusministeriums, indem Sie die in MAGELLAN mitgelieferten Schlüssel neu importieren oder indem Sie die Schlüsselverzeichnisse entsprechend editieren. STÜBER SYSTEMS liefert die von den Ämtern zur Verfügung gestellten Schlüssel mit. STÜBER SYSTEMS übernimmt allerdings keine Gewähr für die Richtigkeit der Schlüssel.

## Das Statistikkonzept

MAGELLAN verfügt über eine allgemeine Export- und Importschnittstelle aus der Daten der MAGELLAN Datenbank ausgelesen und Daten aus einer von DAVINCI für die Statistik exportierten TXT-Datei (im CSV-Format) eingelesen werden können.
Jeder Import- oder Export von Daten ist eine konkrete Umsetzung der jeweiligen Spezifikationen und kann somit auf spezielle Eigenheiten beim Ausspielen der Daten eingehen.
Die Statistikdateien werden direkt aus MAGELLAN heraus mit Hilfe eines Assistenten erstellt. Werden Stundenplanwerte für die Statistik erwartet, greift der Assistent zusätzlich auf die exportierte aus DAVINCI exportierte TXT-Datei zu. Nicht alle Bundesländer erwarten Stundenplandaten.  
Derzeit werden die Statistikschnittstellen folgende Bundesländer unterstützt:

Bundesland             | MAGELLAN 6 | MAGELLAN 7                | Zur Vollständigen Unterstützung
---------------------- | ---------- | ------------------------- | -------------------------------
Berlin                 | 2018/2019  | 2019/2020 in Vorbereitung | MAGELLAN
Brandenburg            | 2018/2019  | Auf Anfrage               | MAGELLAN
Rheinland-Pfalz        | 2019/2020  | -                         | MAGELLAN / DAVINCI
Mecklenburg-Vorpommern | 2018/2019  | 2019/2020 in Vorbereitung | MAGELLAN / DAVINCI
Nordrhein-Westfalen    | 2018/2019  | veröffentlicht            | MAGELLAN / DAVINCI
Schleswig-Holstein     | 2018/2019  | veröffentlicht            | MAGELLAN / DAVINCI

!!! info "Hinweis"

    Statistikdateien die DAVINCI voraussetzen können nicht ausgespielt werden, wenn Sie DAVINCI nicht als Ihre Stundenplansoftware einsetzen.
    Das Konzept setzt voraus, dass in MAGELLAN und DAVINCI die entsprechenden Daten richtig eingegeben worden sind. Bitte kontrollieren Sie anhand der nachfolgenden Hinweise die Vollständigkeit der Daten.

## Kürzel, Schlüssel, IDs

In den DAVINCI-Stammdaten muss jeder Klasse und jedem Lehrer, der für die Statistik berücksichtigt werden soll, die entsprechende ID aus MAGELLAN zugeordnet werden. Die Fächerkürzel und Schlüssel in DAVINCI müssen mit den Kürzeln und Schlüsseln in MAGELLAN übereinstimmen.

## MAGELLAN

Bei der Arbeit mit MAGELLAN sollten Sie im Hinblick auf die Statistik auf Folgendes achten:

### Schlüsselverzeichnisse

Grundlage vieler Eingabemasken in MAGELLAN sind Schlüsselverzeichnisse, welche die Eingabe auf eine Liste vordefinierter Werte einschränken. Wenn Sie also z.B. bei einem Schüler die Konfession eingeben möchten, so können Sie nur eine Konfession aus dem Schlüsselverzeichnis Konfessionen auswählen. Alle Schlüsselverzeichnisse in MAGELLAN sind frei editierbar und bestehen in der Regel aus den Feldern `Kürzel`, `Schlüssel`, `Bezeichnung`, `GueltigVon` und `GueltigBis`. Während `Kürzel` und `Beschreibung` frei wählbar sind, ist der `Schlüssel` durch das Amt vorgegeben und sollte nicht geändert werden. Damit Sie nun nicht alle Schlüsselverzeichnisse füllen müssen, liefern wir die benötigten Schlüsselverzeichnisse bereits mit. Diese werden durch die Installation von MAGELLAN in einem separaten Ordner abgelegt. Mit Hilfe des MAGELLAN-Administrator können Sie die Schlüsselverzeichnisse Ihres Bundeslandes bzw. Ihrer Schulart jederzeit in die bestehende MAGELLAN-Datenbank einspielen. Wurden mit einem Update neue Schlüssel zur Verfügung gestellt, werden Ihre Schlüsselverzeichnisse nicht automatisch hinzugefügt. Mit Hilfe des MAGELLAN-Administrator müssen Sie die neuen Schlüssel importieren.

### Zeiträume

Schüler- und Klassendaten werden in MAGELLAN zeitraumbezogen gespeichert. Achten Sie daher bei der Definition Ihrer Zeiträume in MAGELLAN darauf, dass diese sich im Anfangs- oder Enddatum nicht überschneiden. Außerdem müssen Sie sich im Klaren darüber sein, dass in der Regel Daten sowohl aus dem aktuellen Zeitraum (also 1. Halbjahr des Schuljahres) als auch aus den beiden vorangegangenen Zeiträumen (also 1. und 2. Halbjahr des davorliegenden Schuljahres) benötigt werden können.

## DAVINCI

Sobald in der Landestatistik stundenplanrelevante Daten benötigt werden, kommt auch DAVINCI mit ins Spiel. Bei der Arbeit mit DAVINCI sollten Sie daher im Hinblick auf die Statistik auf Folgendes achten:

### Schlüsselverzeichnisse

An vielen Stellen in DAVINCI begegnen Ihnen Auswahlfelder, die mit Daten aus einem bestimmten Schlüsselverzeichnis vorbelegt sind. Die Schlüsselverzeichnisse tragen ihren Namen, weil sie in der Re-gel Angaben beinhalten, die für die statistische Auswertung der Stundenplandaten benötigt werden. Alle diese Verzeichnisse enthalten eine Spalte „Schlüssel“, deren Felder mit den Schlüsselwerten versehen werden können, die die Landesstatistikämter für die jährlichen Schulstatistiken herausgeben. Derzeit stehen in DAVINCI verschiedene Schlüsselverzeichnisse zur Verfügung.

Die meisten dieser Schlüsselverzeichnisse sind leer und können von den Schulen je nach dem schulform- und landesspezifischen Bedarf gefüllt werden. Einige Schlüsselverzeichnisse, die häufig benötigt werden und besonders typische Einträge aufweisen, sind bereits mit Standard-oder Beispielwerten versehen. Dies betrifft z.B. das Schlüsselverzeichnis „Unterrichtsarten“, dessen Einträge u. a. der Unterscheidung zwischen Leistungskursen, Grundkursen und anderen Kursen dienen.

Die Schlüsselverzeichnisse gehören nicht eigentlich zu den Stammdaten, vielmehr handelt es sich um Daten zweiter Ordnung, die im Wesentlichen der Beschreibung oder Kategorisierung anderer Daten dienen. Sie kommen nicht nur im Programmbereich „Stammdaten“, sondern auch in den anderen Programmbereichen zum Einsatz. Die vollständige Bearbeitung der Stammdaten setzt aber in der Regel voraus, dass bestimmte Schlüsselverzeichnisse im Vorfeld angepasst werden.

### Datenabgleich mit MAGELLAN

Damit die Daten später sinnvoll zueinander passen, müssen die Stammdaten zwischen MAGELLAN und DAVINCI abgeglichen werden. Das bedeutet, dass vor allem die Stammdaten in DAVINCI (Klassen, Lehrer, Fächer und evtl. Schüler) mit der gleichen ID-Nummer versehen werden wie in MAGELLAN. Diese Aufgabe übernimmt für Sie der Import/Export-Assistent in DAVINCI.

Nähere Informationen hierzu finden Sie auch im MAGELLAN-Handbuch unter [Datenaustausch mit MAGELLAN](https://doc.magellan7.stueber.de/schulverwaltung/howto/abgleich_mit_dav/).

### Lehrer-Soll-Berechnungsschlüssel

Die Mehrarbeits- und Ermäßigungsstunden von Lehrern werden in DAVINCI in der Lehrer-Soll-Berechnung dokumentiert. Grundlage für diese Daten sind die Soll-Berechnungsschlüssel des jeweiligen Bundeslandes. Diese werden bei jeder Installation von DAVINCI automatisch mitinstalliert und können jederzeit in die aktuelle Stundenplandatei importiert werden.
Nähere Informationen hierzu finden Sie auch im DAVINCI-Benutzerhandbuch unter [Lehrer-Zeitkonten](https://doc.davinci6.stueber.de/01.stundenplan/stammdaten/#lehrer-zeitkonten).

### Unterrichtsarten und Fachstatus

Diese Schlüsselverzeichnisse müssen in MAGELLAN und DAVINCI übereinstimmen. Sie werden aus logischen Gründen nicht automatisch beim Datenabgleich abgeglichen.

## Kurswahldaten und Lehrerdaten nach MAGELLAN übertragen

Nachdem Sie die kontrolliert haben, dass die IDs in beiden Programmen übereinstimmen, sollten sie die Kurswahldaten (für Allgemeinbildende Schulen mit Oberstufe) und Lehrerdaten übernehmen, wie im DAVINCI Handbuch im Kapitel „Datenaustausch mit anderen Programmen“  unter „Datenaustausch mit MAGELLAN“, „Daten nach MAGELLAN übergeben“ beschrieben.

!!! info "Hinweis"

    Bitte beachten Sie, dass Sie nur mit Kopien der DAVINCI Datei und MAGELLAN Datenbank arbeiten!

## Daten prüfen

### Oberstufendaten Gymnasien/Gesamtschulen in DAVINCI prüfen

* `Stammdaten > Klassen`: Bitte erfassen Sie in der Spalte ID für alle MSS-Klassen die MAGELLAN-ID.
* `Stammdaten > Fächer`: Für alle Fächer muss in der Spalte „Schlüssel“ der vom Statistikamt vorgeschriebene Schlüssel erfasst werden, z.B. „4“ für das Fach Deutsch.
* `Veranstaltungsübersicht > Klassen`: Für die MSS-Klassen müssen alle Leistungs- und Grundkurse vorhanden sein. 
* Bei schulübergreifendem Unterricht muss im Feld Bemerkungen die Schulnummer der unterrichtenden Schule eingetragen werden. Ist ihre Schule nicht die unterrichtende Schule muss der Kurs mit Dauer =“0“ in die Veranstaltungsübersicht der Klasse aufgenommen werden.

Wir empfehlen Ihnen beim Abgleich der IDs der Schüler, Klassen, Lehrer und Fächer sicherheitshalber wie folgt vorzugehen:

1. Öffnen Sie MAGELLAN und wechseln Sie in die entsprechende Ansicht Schüler, Klassen oder Lehrer. Die Fächerliste finden unter Verzeichnisse, Fächer.
2. Exportieren Sie die Auswahlliste nach Excel und drucken Sie diese zur Vorlage aus.
3. Öffnen Sie DAVINCI und wechseln Sie in die entsprechende Ansicht.
4. Vergleichen Sie die IDs und Kürzel Ihrer Vorlage mit den IDs und Kürzel in der DAVINCI Ansicht und korrigieren Sie ggf. in DAVINCI.

### Daten als Berufsbildende Schule in DAVINCI prüfen

#### Stammdaten

Damit das Klassen-Soll erfasst werden kann, muss jeder Klasse eine Stundentafel zugeordnet werden.

#### Veranstaltungsliste

Einige Daten für die Statistik errechnen sich unmittelbar aus den Unterrichtsangaben in der Veranstaltungsliste. Für jede Veranstaltung sollten daher der Lehrer, die Klasse, das Fach und die Unterrichtsstunden eingetragen sein.

#### Lehrer-Soll-Berechnung

Wert                               | Erläuterung
---------------------------------- | ----
Fachpraxiserhöhung                 | Errechnet sich aufgrund der Aufsummierung der Einträge in der Spalte Differenz der Stundentafel der Klasse.
Soll-Änderung eines Fachs          | Errechnet sich aufgrund des Einträge in der Spalte Differenz der Stundentafel der Klasse für das entsprechende Fach.
Soll-Änderungsgrund für die Klasse | Entspricht dem Eintrag in der Spalte Bemerkung in der Stundentafel der Klasse. Es darf maximal einen Eintrag in der Spalte Bemerkung der Stundentafel der Klasse geben und der Eintrag darf maximal 100 Zeichen lang sein.

## Statistikdaten aus DAVINCI exportieren

Als allgemeinbildendes Gymnasium/Gesamtschule mit Oberstufe bzw. als Berufsbildende Schule müssen Sie aus DAVINCI statistikrelevante Daten exportieren. Diese exportierten Daten werden dann zur eigentlichen Statistikerstellung in MAGELLAN verwendet.

!!! info "Hinweis"

    Ob Sie für Ihr Bundesland DAVINCI-Daten benötigen, lesen Sie bitte in den jeweiligen Abschnitten zur Statistik in Ihrem Bundesland in diesem Dokument.

So exportieren Sie Daten aus DAVINCI:

1. Starten Sie DAVINCI.
2. Klicken Sie dort im Menü `Plan` auf `Importieren und Exportieren`.
3. Wählen Sie unter Export den Punkt `Statistikdaten exportieren` aus und klicken Sie aur `Weiter`.
4. Wählen Sie Ihr Bundesland aus und klicken Sie auf `Weiter`.
5. Geben Sie den Dateipfad und einen passenden Dateinamen zum Export der Statistikdaten an. Klicken Sie auf `OK`. Die Daten werden jetzt in die angegebene Datei exportiert.
