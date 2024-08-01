# Probleme und Lösungen

## Doppelte GUIDs

### Allgemein

Die Schüler-GUIDSs in Magellan, gehören nicht nur zum Schüler, sondern sollen den Schüler und seine Ausbildung kennzeichnen. Wechselt ein Schüler den Ausbildungsgang, soll eine neue GUID für den Schüler und seine Ausbildung erzeugt werden.
Durch ein zwischenzeitlich behobenes Problem konnten in der Vergangenheit GUIDs mehrfach vergeben worden sein.
Die in der Schülerauswahlliste einblendbaren GUIDs haben hiermit nichts zu tun, die relevanten GUIDs sieht man auf der Ausbildungskarte, wenn Sie in der Verbindung die Region auf Sachsen stellen.

### Dopplungen?

Welche und ob Datensätze es sind, kann man durch folgenden Bericht, der alle GUIDs zeigt, mehrfach auftauchenden GUIDs zusätzlich kennzeichnet. Wenn Sie den Bericht aufrufen, dauert es einen Moment die Daten entsprechend zu gruppieren. In der Vorschau können Sie durch die Seiten blättern, steht nur eine 1 am Ende, ist die Zeile unauffällig. Werden mehr als eine Schülerausbildung zur GUID gefunden, werden die Schüler und ihre Klasse ausgegeben.
Den Bericht `Mandant (Prüfung der Schüler des aktuellen Halbjahres auf doppelte AusbildungsGUID).rpt` finden Sie im Menü `
Mandanten`. Die Anleitung für diesen Bericht lesen Sie bitte [hier]([hier](https://doc.la.stueber.de/berichte/mandanten/Mandant%20%28Pr%C3%BCfung%20der%20Sch%C3%BCler%20des%20aktuellen%20Halbjahres%20auf%20doppelte%20AusbildungsGUID%29/)) nach.

### Exportproblem

Es kann noch eine zweite Situation geben, die es so scheinen lässt, als wenn es Dopplungen gibt.
Der Grund ist aber ein anderer. Für Abgänger sollen die Daten bitte immer in dem Halbjahr erfasst werden, indem die Schüler auch tatsächlich die Schule verlassen. 
Also Abschlussdatum und Abgangsdatum müssen im gleichen Halbjahr liegen.
Tragen Sie versehentlich den Abschluss samt Abschlussdatum im ersten Halbjahr ein, der Schüler verlässt die Schule aber erst im zweiten Halbjahr, auch das Abgangsdatum liegt im zweiten Halbjahr. Was passiert dann: Der Export wird den Schüler im ersten Halbjahr mit dem Abschluss erkennen und eine Zeile für ihn in der XML-Datei erzeugen. Danach erkennt er den Schüler im zweiten Halbjahr als Abgänger und legt eine zweite Zeile in der XML-Datei an. Die Prüfung erkennt die doppelten Zeilen und wird den Schüler  mit "doppelter GUID" monieren.
Lösung: Abschluss, Abschlussdatum und Abgangsdatum werden in dem Halbjahr erfasst, die logisch zu den Daten gehören.

## XML-Meldung

Zusätzlich zu den von uns integrierten Meldungen wird die Datei nach dem Export gegen eine Formatdatei des Statistikamtes geprüft. Verstößt die Datei gegen eine der Vorgaben, erscheint eine Meldung, die im oberen Teil das eigentliche Problem zeigt, weiter unten dann einen Ausschnitt der XML-Datei zeigt, die unter anderem den betroffenen Datensatz enthält. Um die Ursache besser erkennen zu können, kopieren Sie sich den Text aus der Meldung (lässt sich nach Excel exportieren) in eine Textdate. Suchen Sie dann mit der Suchfunktion (STRG+F) nach dem Begriff `</schueler>` und setzen jeweils vor den gefundenen Eintrag einen Return.
Damit wird dann zeilenweise ein Schülerdatensatz dargestellt, die oben gezeigte Meldung lässt sich besser dem Datensatz zuordnen.
