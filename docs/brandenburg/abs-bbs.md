# Brandenburg - ABS und BBS

Dieses Kapitel beschreibt für Allgemeinbildende und Berufsbildende Schulen in Brandenburg die benötigten Schritte zum Erstellen der elektronischen Landesstatistik für den Abgleich mit dem Landesbetrieb für Datenverarbeitung und Statistik im Schuljahr 2015/2016. Die Schulstatistik 2015/2016 wird derzeit nur für Berufsbildende Schulen unterstützt.

> Die Legende zu den nachstehenden Tabellen finden Sie [HIER](../legende-statistikfelder.md).

## Einführung

Zur Erfassung von Lehrer-, Unterrichts- und Schülerindividualdaten für die jährliche Statistik setzt das Land Brandenburg das Programm LUSD-BB ein.

Dieses Programm erwartet eine Reihe von Dateien in einem bestimmten zeichengetrennten Textformat, die importiert werden müssen.

Für Sie als Schule bedeutet dies: Sie müssen die folgenden Textdateien aus MAGELLAN erzeugen:

Daten|Inhalt
--|--
KLnnnnnn.TXT |Klassendaten; ABS und BBS; MAGELLAN
SPnnnnnn.TXT |Schülerindividualdaten; ABS und BBS; MAGELLAN
SKnnnnnn.TXT |Kursdaten pro Schüler; ABS und BBS; MAGELLAN
LAnnnnnn.TXT |Daten Ermäßigungen und Anrechnungen (Abminderungen) der Lehrkräfte; ABS und BBS; MAGELLAN und DAVINCI

Darüber hinaus können noch folgende Dateien nach LUSD-BB eingespielt werden, die derzeit von MAGELLAN nicht unterstützt werden.

Daten|Inhalt
--|--
LUnnnnnn.TXT |Daten Lehrerunterrichtsverteilung; ABS und BBS
FLnnnnnn.TXT |Lehrerstammdaten für Schulen freier Träger; ABS und BBS

>Hierbei steht nnnnnn für Ihre 6-stellige Schulnummer.

In LUSD-BB müssen Sie zuvor die Lehrerstammdaten eingelesen haben. Wie Sie die Daten in LUSD-BB importieren, erfahren Sie beim Landesbetrieb für Datenverarbeitung und Statistik. Das Statistikamt fordert diese Daten aus dem aktuellen (1. Halbjahr 2015/2016) und aus dem gesamten vorangegangenen Schuljahr (1. und 2. Halbjahr 2014/2015).

##Notwendige Schritte


1.	Schritt: [Statistikschlüssel aktualisieren](../magellan/schluessel-importieren.md) 
2.	Schritt: Dateneingabe
3.	Schritt: [Datenprüfung](../datenpruefung.md)
4.	Schritt: Statistikdateien erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

##Statistikschlüssel aktualisieren


Statistikämter setzen für einige Felder Wertelisten voraus, die STÜBER SYSTEMS in Form von Schlüsselverzeichnissen zur Verfügung stellt. Bitte lesen Sie dazu den Abschnitt [Schlüsselverzeichnisse importieren](../magellan/schluessel-importieren.md).

##Statistisch relevante Daten eingeben


Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang, in einer tabellarischen Übersicht.
Statistikkürzel
Voraussetzung für das Ausspielen der Daten in das Statistikformat ist die Angabe des Feldes ```Klassen > Daten 1 > Statistikkürzel```. Das Feld kann beliebig eingetragen werden und sollte eindeutig benannt sein. Üblicherweise wird hier einfach das Klassenkürzel wiederholt.
Schüler, für deren Klasse kein Statistikkürzel eingetragen ist, werden statistisch nicht berücksichtigt.

##Zusätzliche Eingaben im Kurs- und Stundenplanmodul
Kurs- und Stundenplanmodul von DAVINCI vornehmen. Genauere Informationen zu den Eingaben für DAVINCI finden Sie in der nachfolgenden tabellarischen Übersicht.
Überprüfen Sie in DAVINCI als Berufsbildende Schule

###Stammdaten
Damit das Klassen-Soll erfasst werden kann, muss jeder Klasse eine Stundentafel zugeordnet werden.
###Veranstaltungsliste
Einige Daten für die Statistik errechnen sich unmittelbar aus den Unterrichtsangaben in der Veranstaltungsliste. Für jede Veranstaltung sollten daher der Lehrer, die Klasse, das Fach und die Unterrichtsstunden eingetragen sein.
###Lehrer-Soll-Berechnung

Was|Wie
--|--
Fachpraxiserhöhung|Errechnet sich aufgrund der Aufsummierung der Einträge in der Spalte Differenz der Stundentafel der Klasse.
Soll-Änderung eines Fachs| Errechnet sich aufgrund des Einträge in der Spalte Differenz der Stundentafel der Klasse für das entsprechende Fach.
Soll-Änderungsgrund für die Klasse|Entspricht dem Eintrag in der Spalte Bemerkung in der Stundentafel der Klasse. Es darf maximal einen Eintrag in der Spalte Bemerkung der Stundentafel der Klasse geben und der Eintrag darf maximal 100 Zeichen lang sein.
##Statistikdaten aus DAVINCI exportieren


Wenn Sie die Lehrer Abminderungen und Unterrichtsverteilung aus MAGELLAN heraus exportieren möchten, dann müssen Sie aus DAVINCI statistikrelevante Daten exportieren. Diese exportierten Daten werden dann zur eigentlichen Statistikerstellung in MAGELLAN verwendet. Wenn Sie diese Dateien nicht aus MAGELLAN importieren möchten und die Daten direkt in LUSD-BB erfassen, dann wird der DAVINCI Export nicht benötigt.

So exportieren Sie Daten aus DAVINCI:

1.	Starten Sie DAVINCI.
2.	Klicken Sie dort im Menü ```Plan``` auf ```Importieren und Exportieren```.
3.	Wählen Sie im Import/Export Assistenten unter Export ```Statistikdaten exportieren```.
4.	Wählen Sie ```Allgemeines Statistikformat exportieren```.
5.	Geben Sie Speicherort und Dateinamen.txt an.
6.	Klicken Sie auf ```Weiter```. Die Daten werden jetzt in die angegebene Datei exportiert.


##Datenprüfung


Vor dem Erstellen der eigentlichen Statistikdateien sollten Sie eine Prüfung der Daten in MAGELLAN bzw. DAVINCI vornehmen. Da uns vom Statistikamt keine Prüfungen zur Verfügung stehen, sollten Sie die Prüfungen von LUSD-BB nutzen, die beim Import angezeigt werden und die Korrekturen dann in MAGELLAN bzw. DAVINCI vornehmen.
##Statistikdaten erstellen


Zum Erstellen der Statistikdateien gehen Sie wie folgt vor:
1.	Starten Sie MAGELLAN.
2.	Klicken Sie im Menü ```Extras``` auf ```Statistik```.
3.	Wählen Sie als Bundesland Brandenburg und als Schulart Berufsbildende Schule (BBS). Klicken Sie dann auf ```Weiter```.
4.	Wählen Sie als Art der Erstellung ```Nur Statistikdateien erstellen```. Markieren Sie die Dateien, welche Sie erstellen möchten. Unter Statistikzeiträume auswählen müssen Sie den Erhebungszeitpunkt (02.11.2015), den aktuellen Zeitraum (1. Halbjahr 2015/2016) und die Zeiträume des Vorjahres (2. Halbjahr 2014/2015 und 1. Halbjahr 2014/2015) einstellen. 
5.	Geben Sie Ggf. eine DAVINCI-Exportdatei an. Klicken Sie dann auf ```Weiter```. 
6.	Geben Sie das Erstellungsdatum an und wählen Sie den Ordner für den späteren Export der Statistikdateien aus. Klicken Sie auf ```Weiter```. Klicken Sie auf ```Start```, um die Erstellung der Statistikdateien zu starten.



# Statistikfelder mit Beschreibung


>Die Legende zu den nachstehenden Tabellen finden Sie [HIER](../legende-statistikfelder.md).

##Allgemeine Daten


Statistikfeld in der Statistikdatei	|Datenfeld in MAGELLAN/DAVINCI	|Beschreibung|Statistikdatei
--|--|--|--
SNR	MAGELLAN|Mandanten > Daten 1 > Schulnummer|Geben Sie hier Ihre Schulnummer ein.|	Alle
ABT|Mandanten > Daten 1 > Außenstelle|Geben Sie hier Ihre Abteilungsnummer ein. (MAGELLAN unterstützt derzeit nur den Gesamtimport. Das Abteilungsweise einlesen wird derzeit nicht unterstützt. Geben Sie 00 an. Für OSZ gilt immer 00.)	|

##Schüler und Klassen- bzw. Kursdaten


Statistikfeld in der Statistikdatei	|Datenfeld in MAGELLAN/DAVINCI	|Beschreibung|Statistikdatei
--|--|--|--
KLASSE	|MAGELLAN:Klassen > Daten 1 > Statistikkürzel|	Geben Sie hier das Statistikkürzel für die Klasse ein. Für die Statistik werden nur Klassen berücksichtigt, die ein Statistikkürzel eingetragen haben.	|KL, SP
KLASSART (Schlüssel 04)|	MAGELLAN:Klassen > Merkmale > Merkmal S1|	Art der Klasse.	         |KL
SKZ|	/	|Eine laufende Nummer pro Schüler, die zusammen mit dem Klassennamen den Schüler für den Import eindeutig machen.Dieser Wert wird beim Erstellen der Statistikdatei berechnet.	          |SP,SK
SNAME	|MAGELLAN:Schüler > Daten 1 > Nachname	|Geben Sie hier den Nachnamen des Schülers ein.  |SP
SVORNAME|MAGELLAN:Schüler > Daten 1 > Vorname	|Geben Sie hier den Vornamen des Schülers ein.	 |SP
GESCHL	|MAGELLAN:Schüler > Daten 1 > Geschlecht|Geben Sie hier das Geschlecht des Schülers ein. |SP
GEBDAT	|MAGELLAN:Schüler > Daten 1 > Geboren am|Geben Sie hier das Geburtsdatum des Schülers ein.|SP
ERSTDAT	|MAGELLAN:Schüler > Daten 2 > Grundschuleintritt > Grundschuleintritt|Geben Sie hier das Datum der Ersteinschulung ein. Für die Statistik ist nur das richtige Jahr relevant. Wurde der Schüler bereits einmal eingeschult und vor Vollendung des 1. Schuljahres zurückgestellt, dann ist das aktuelle Jahr anzugeben, in dem er wieder eingeschult wird.                                                     |SP
REGHERK (Schlüssel 08)|MAGELLAN:Schüler > Daten 1 > Land > Schüler > Daten 1 > Gemeinde|Geben Sie bei Schülern, die in Polen leben, in das  Feld „Land“ den Wert „PL“ ein. Wohnt der Schüler in Deutschland müssen Sie einen gültigen Gemeindeschlüssel eingeben.                                             |SP
STATUS|	MAGELLAN:Schüler >  Statistik > Merkmal S1	|Geben Sie hier die Statusauswahl ein. Grundlage ist das Schlüsselverzeichnis „Schülermerkmale“ (Bereich S1).	                                       |SP
STAATSAN(Schlüssel 09)|	MAGELLAN:Schüler > Daten 2 >  Staatsangehörigkeit > Staatsangeh. 1|	Geben Sie hier die Staatsangehörigkeit des Schülers, oder das Herkunftsland bei Aussiedlern ein. Grundlage ist das Schlüsselverzeichnis „Staatsangehörigkeiten“.	                                                  |SP
EINZUGL	|MAGELLAN:Schüler > Statistik > Merkmal T1	|Geben Sie hier den Wert „Ja“ ein, wenn der Schüler einzugliedernder im Sinne der Eingliederungsverordnung ist. Wenn Sie hier nichts eingeben, oder das Feld anderweitig verwenden, dann ist der Standardwert für die Statistik gleich „Nein“.	               |SP
AUFNDAT	|MAGELLAN:Schüler > Zugang/Abgang > Zugang > Zugang am	|Geben Sie hier das Zugangsdatum an der Schule ein.	                                                                                      |SP
JG, JGVJ (Schlüssel 11)|MAGELLAN:Klassen > Zeiträume > Zeitraum > Klassenstufe|Geben Sie hier den Jahrgang des Schuljahres für die gesamte Klasse ein. Es wird automatisch der Jahrgang des aktuellen sowie des vorangegangenen Schuljahres ausgelesen, vorausgesetzt, Sie haben im vorangegangenen Schuljahr den Jahrgang eingetragen. War der Schüler im letzten Schuljahr nicht auf der Schule muss die Jahrgangsstufe des vorangegangenen Schuljahres im Feld „Letzte Klassenstufe“ der bereits besuchten Schule eingetragen werden. Grundlage ist das Schlüsselverzeichnis „Klassenstufen“.              |SP                        
|Schüler > Zugang / Abgang >  Bereits besuchte Schulen> Schule > Letzte Klassenstufe            ||
BIG (Schlüssel 12)	|MAGELLAN:Klassen > Bildungsgang|Geben Sie hier den aktuellen Bildungsgang der Klasse ein. Wählen Sie den aktuellen Ausbildungsbetrieb aus der Liste aus. Grundlage ist das Schlüsselverzeichnis „Bildungsgänge“.	                                                        |SP,LU 
BIGVJ (Schlüssel 12)|MAGELLAN:Klassen > Bildungsgang|Geben Sie im vorangegangenen Schuljahr den Bildungsgang ein, vorausgesetzt, Sie der Schüler war im letzten Schuljahr an Ihrer Schule. War der Schüler im letzten Schuljahr nicht auf der Schule muss der Bildungsgang des vorangegangenen Schuljahres im Feld „Unterlagen“ der bereits besuchten Schule eingetragen werden.Grundlage ist das Schlüsselverzeichnis „Bildungsgaenge“.                                                          |SP
|Schüler > Zugang / Abgang >  Bereits besuchte Schulen > Schule > Unterlagen                   ||		
SNRVJ|	/	|Nicht für BBS und ZBW – leer für BBS und Schulen des zweiten Bildungsweges!|	SP
HERKSFVJ (ABS),HERKSF (BBS, ZBW) (Schlüssel 15)	|MAGELLAN:Klassen > Schulform|Geben Sie im vorangegangenen Schuljahr die Schulform der Klasse ein, vorausgesetzt der Schüler war im letzten Schuljahr an Ihrer Schule. War der Schüler im letzten Schuljahr nicht auf der Schule muss die Schulform des vorangegangenen Schuljahres im Feld „Schulform“ der bereits besuchten Schule eingetragen werden.  Wählen Sie bei „Herkunftsschule“ die zuletzt besuchte Schule aus. Je nachdem, ob ABS, BBS oder ZBW wird HERKSF oder HERSFVJ vom Statistikamt verlangt.                                                 |SP
|Schüler > Zugang/Abgang >  bereits besuchte Schulen > Schulform                               ||
|Schüler > Zugang/Abgang >  Herkunftsschule                                                    ||		
LANDVJ	|MAGELLAN:Schüler > Zugang/Abgang >  Bereits besuchte Schulen > Schule|Ist der Schüler aus einem anderen Bundesland neu an die Schule gekommen, so wird das Bundesland benötigt.Geben Sie bei „Bereits besuchte Schulen“ die vorangegangene Schule ein. Wählen Sie bei „Herkunftsschule“ die zuletzt besuchte Schule aus. Sie müssen die korrekte Gemeindekennziffer eingeben, damit das Bundesland berechnet werden kann.                                                                                         |SP
|Schüler > Zugang/Abgang > Herkunftsschule                                                    ||
|Schulen > Daten > Gemeinde		                                                              ||
STAATVJ(Schlüssel 09)|MAGELLAN:Schüler > Zugang/Abgang > Bereits besuchte Schulen > Unterlagen|Ist der Schüler aus einem anderen Land neu an die Schule gekommen, so wird der Staat benötigt. Geben Sie bei „Bereits besuchte Schulen“ die Herkunftsschule ein. Die Schule müssen Sie vorher unter Schulen angelegt haben. Dort müssen Sie das „Land“ der Schule eintragen. Wählen Sie bei „Herkunftsschule“ die zuletzt besuchte Schule aus.                                                                          |SP
|Schüler > Zugang/Abgang  >  Herkunftsschule	                                              ||	
GRUNDEMP (Schlüssel 13)|MAGELLAN:Schüler > Laufbahn > Allgemein > Empfehlung|	Geben Sie hier die Grundschulempfehlung für den Schüler ein. Grundlage ist das Schlüsselverzeichnis „Empfehlungen“. Nur Jahrgangsstufe 7, sonst leer!                                                                  |SP
HABSCHL (Schlüssel 14)|MAGELLAN: Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss|	Geben Sie hier den bisher höchsten erreichten schulischen Abschluss ein. Nur BBS und Einrichtungen des zweiten Bildungsweges, sonst leer!	                                                                  |SP
ZF  (Schlüssel B)|MAGELLAN:Klasse > Daten > Organisation|Geben Sie hier die Zeitform der Klasse an. Nur BBS und ZBW, sonst leer!	                                                               |SP,LU
UMSCHUEL|MAGELLAN:Schüler > Daten 2 > Umschulung > Umschulung|	Geben Sie hier an, ob der Schüler Umschüler ist oder an einer Einstiegsqualifizierung teilnimmt. Standardwert bei leerem Feld ist „Nein“.                                                                                                |SP
WIEDERH|MAGELLAN:Schüler > Laufbahn > Allgemein > Wiederholer|Geben Sie hier ein, ob der Schüler Wiederholer ist. Geben Sie bei freiwilliger Wiederholung dies im Feld „Wiederholungsart“ ein.Andernfalls wird davon ausgegangen, dass der Schüler wg. Nichtversetzung wiederholt.                      |SP
|Schüler > Laufbahn > Allgemein > Wiederholungsart		                                      ||
FKL (Schlüssel B)|	MAGELLAN:Klasse > Daten > Beruf	|Geben Sie hier den Beruf der Klasse ein. Nur BBS!                                                                                                 |SP
AUSBER|Ausbildungsbereich|Immer leer!                                                         |SP
AUSVER|Art des Ausbildungsvertrages|Immer leer!	                                              |SP
AUSKREIS|MAGELLAN:Schüler > Ausbildung > Liste der Ausbildungsbetriebe > Betrieb|Geben Sie hier den aktuellen Ausbildungsbetrieb des Schülers ein. Wählen Sie den aktuellen Ausbildungsbetrieb aus der Liste der erfassten Ausbildungsbetriebe aus. Geben Sie beim aktuellen Ausbildungsbetrieb die korrekte Gemeindekennziffer ein. Nur duale Ausbildung!	                                               |SP
|Schüler > Daten 1 > Ausbildung		                                                          ||
|Betriebe > Daten 1 > Gemeinde  		                                                      ||	
SPFART (Schlüssel 16)|	MAGELLAN: Schüler > Daten 4 > Förderung > Förderung|	Geben Sie hier die Art des sonderpädagogischen Förderbedarfs ein. Grundlage ist das Schlüsselverzeichnis „Förderungen“. Nur Primarstufe, Sek. I und II	                                                                   |SP
MBEHIND/AUTIST|	MAGELLAN:Schüler > Daten 4 > Behinderung|	Bisher wurde die Mehrfachbehinderung im Merkmal T2 abgebildet. Dies ändert sich ab diesem Jahr. Dafür kommt das statistische Feld AUTIST hinzu, beide werden wie folgt abgefragt. Geben Sie in diesem Feld bitte an, ob der Schüler Mehrfachbehindert, Autistisch oder Beides ist. Wenn Sie hier nichts angeben, dann ist der Standardwert für die Statistik  gleich „Nein“.	                                                                             |SP
HKUNT	|MAGELLAN:Schüler > Merkmale > Merkmal T3	|Geben Sie hier den Wert „Ja“ ein, wenn der Schüler Haus-/ Krankenhausunterricht hat. Wenn Sie hier nichts eingeben, oder das Feld anderweitig verwenden, dann ist der Standardwert für die Statistik  gleich „Nein“.	                                 |SP
BEFRLER	|MAGELLAN:Schüler > Merkmale > Merkmal S2|	Geben Sie hier eine LER-Unterrichtsbefreiung ein. Grundlage ist das Schlüsselverzeichnis „Schülermerkmale“ Bereich S2.	                        |SP
FSPSTATA (Schlüssel 17)	|MAGELLAN:Schüler > Daten 3 > Fremdsprachenfolge >  1. Fremdsprache > Status|Geben Sie bei der ersten Fremdsprache im Feld  „Status“ den Status der Fremdsprache ein. Für die Statistik stehen die Werte „abgewählt“ und „Wahlunterricht“ zur Verfügung. Im Feld Zusatz können Sie folgende Merkmale eingeben: Wahlunterricht / Arbeitsgemeinschaft, Begegnungssprache- > bei Förderunterricht , BSOBG - > bei Pflichtfach                                                   |SP
|Schüler > Daten 3 > Fremdsprachenfolge >  1. Fremdsprache  > Zusatz                           ||
FSPJGA	|MAGELLAN:Schüler > Daten 3 > Fremdsprachenfolge > 1.Fremdsprache > Von	|Geben Sie hier den Jahrgang ein an dem der Schüler begonnen hat die Fremdsprache zu erlernen. Der Schlüssel für die Statistik wird berechnet. Grundlage der Berechnung ist das Schlüsselverzeichnis „Klassenstufen“.|SP
FSPFACHA (Schlüssel 18/06)|	MAGELLAN: Schüler > Daten 3 > Fremdsprachenfolge >  1. Fremdsprache|	Geben Sie hier die erste Fremdsprache ein. Grundlage ist das Schlüsselverzeichnis „Fächer“.	   |SP
FSPSTATB (Schlüssel 17)|MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge >  2. Fremdsprache > Status|Lesen Sie dazu die Beschreibung des Feldes „FSPSTATA“.	                                 |SP
|Schüler > Daten 3 >  Fremdsprachenfolge >  2. Fremdsprache  > Zusatz	                       ||
SFPJGB|	MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge > 2.Fremdsprache > Von|	Geben Sie hier den Jahrgang ein, an dem der Schüler begonnen hat die Fremdsprache zu erlernen. Der Schlüssel für die Statistik wird berechnet. Grundlage der Berechnung ist das Schlüsselverzeichnis „Klassenstufen“.|SP
FSPFACHB [Schlüssel 18/06)|MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge >  2. Fremdsprache|Geben Sie hier die zweite Fremdsprache ein. Grundlage ist das Schlüsselverzeichnis „Fächer“.	              |SP
FSPSTATC (Schlüssel 17)|	MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge >  3. Fremdsprache > Status|Lesen Sie dazu die Beschreibung des Feldes „FSPSTATA“.	                                 |SP
|Schüler > Daten 3 >  Fremdsprachenfolge >  3. Fremdsprache  > Zusatz	                       ||
FSPJGC|	MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge > 3.Fremdsprache > Von|	Geben Sie hier den Jahrgang ein an dem der Schüler begonnen hat die Fremdsprache zu erlernen. Der Schlüssel für die Statistik wird berechnet. Grundlage der Berechnung ist das Schlüsselverzeichnis „Klassenstufen“.|SP
FSPFACHC (Schlüssel 18/06)|	MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge >  3. Fremdsprache|	Geben Sie hier die dritte Fremdsprache ein.Grundlage ist das Schlüsselverzeichnis „Fächer“.	   |SP
FSPSTATD (Schlüssel 17)|	Schüler > Daten 3 >  Fremdsprachenfolge >  4. Fremdsprache > Status|Lesen Sie dazu die Beschreibung des Feldes „FSPSTATA“.                                               |SP
|Schüler > Daten 3 >  Fremdsprachenfolge >  4. Fremdsprache  > Zusatz	                       ||	
FSPJGD	|MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge > 4.Fremdsprache > Von|	Geben Sie hier den Jahrgang ein an dem der Schüler begonnen hat die Fremdsprache zu erlernen. Der Schlüssel für die Statistik wird berechnet.Grundlage der Berechnung ist das Schlüsselverzeichnis „Klassenstufen“.	|SP
FSPFACHD (Schlüssel 18/06)	MAGELLAN:Schüler > Daten 3 >  Fremdsprachenfolge >  4. Fremdsprache	|Geben Sie hier die vierte Fremdsprache ein. Grundlage ist das Schlüsselverzeichnis „Fächer“.	       |SP
FSPSTATE|/|	                                                                                    |SP
FSPJGE	|/|		                                                                                |SP
FSPFACHE|/|  	                                                                                |SP
RELEVANG/RELKATHO|	MAGELLAN:Schüler > Daten 1 > Rel.-Teilnahme	|Geben Sie hier die Teilnahme am Religionsunterricht ein. Grundlage ist das Schlüsselverzeichnis „Religion (Teilnahmen)“.	     |SP
GANZTAG	|MAGELLAN:Schüler > Merkmale > Merkmal T4	|Geben Sie hier den Wert „Ja“ ein, wenn der Schüler am Ganztagsunterricht teilnimmt. Wenn Sie hier nichts eingeben, oder das Feld anderweitig verwenden, dann ist der Standardwert für die Statistik  gleich „Nein“.	                                 |SP
GEBLAND (Schlüssel 09)	|MAGELLAN:Schüler > Daten 1 > Geburtsland	|Geben Sie hier das Geburtsland des Schülers ein. Grundlage ist das Schlüsselverzeichnis „Staatsangehörigkeiten“.	                |SP
JAHRZUZUG	|MAGELLAN:Schüler > Daten 2 > In Deutschland seit	|Geben Sie hier das Datum des Zuzugs nach Deutschland ein. Statistisch relevant ist nur das Zuzugsjahr.	                             |SP
VSPRA (Schlüssel 22)|	MAGELLAN:Schüler > Daten 2 > Sprachgruppe	|Geben Sie hier die Verkehrssprache ein, wenn sie nicht deutsch ist.	                                                            |SP
BABSCHL (Schlüssel 23)	|MAGELLAN:Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss	|Geben Sie hie den bisher höchsten erreichten beruflichen Abschluss ein. Grundlage ist das Schlüsselverzeichnis „Abschlüsse (Intern)“. Für BBS und zweiter Bildungsweg!	                                         |SP
LJAHR|	MAGELLAN:Schüler >  Zugang/Abgang >  Bereits besuchte Schulen > Bis	|Geben Sie das Jahr des letzten Schulbesuches ein.Hierzu müssen Sie die Herkunftsschule eingetragen und das Feld „Bis“ der bereits besuchten Schule ausgefüllt haben, wenn sich der Schüler im letzten Jahr nicht an Ihrer Schule befand. Andernfalls wird das Jahr berechnet. Statistisch relevant ist nur das Jahr. Für BBS!	   |SP
RELHUMAN|MAGELLAN:Schüler > Merkmale > Merkmal S3	|Geben Sie hier die Teilnahme am humanistischen Lebenskundeunterricht ein. Grundlage ist das Schlüsselverzeichnis „Schülermerkmale“ (Bereich S3).|SP

