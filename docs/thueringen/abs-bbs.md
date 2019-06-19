# Thüringen - ABS und BBS

Dieses Kapitel beschreibt für Berufsbildenden Schulen in Thüringen die benötigten Schritte zum Erstellen der elektronischen Landesstatistik für den Abgleich mit dem Kultusministerium in Thüringen im Schuljahr 2007/2008.

>Lesen Sie die Angaben und Vorgehensweise dieses Dokuments sehr genau und beachten Sie bitte alle Ihre Schulart betreffenden Aussagen.
Berufsbildende Schulen benötigen für die Landesstatistik jeweils das Stundenplanmodul von DAVINCI zur Vervollständigung der Statistikdaten.

#Einführung


Die Statistik Thüringen wird seit dem Schuljahr 2007/2008 unterstützt. Grundlage des Statistikmoduls für Thüringen ist das Austauschformat, das in das Erfassungsprogramm des Kultusministeriums eingelesen wird. 
Das Austauschformat ist eine mit Semikolon getrennte ASCII-Textdatei, die jeden Datensatz in einer Zeile hält. Diese Daten lassen sich z.B. nach dem Erstellen mit einem Texteditor betrachten.
Für Sie als Schule bedeutet dies: Sie müssen die folgende Textdatei erstellen und in das Erfassungsprogramm einlesen:

•	SB_xxxxx.svs

Hierbei steht xxxxx für Ihre Schulnummer.
Die Datei erhält die Dateiendung .SVS, kann aber mit einem Texteditor problemlos eingelesen werden. 

Die Datei enthält einige Klassendaten, größtenteils aber Schülerdaten aus dem aktuellen Statistikjahr zum Stichtag.

Wie Sie diese Dateien an das Statistikamt versenden, wird Ihnen direkt durch das Statistikamt mitgeteilt.

##Notwendige Schritte
1. Schritt: [Statistikschlüssel bereinigen und aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Statistisch relevante Daten in DAVINCI bzw. MAGELLAN eingeben
3. Schritt: Kurswahlen von DAVINCI nach MAGELLAN übertragen (nur für Berufsbildende Gymnasien mit Oberstufe)
4. Schritt: Statistikdaten in das MAGELLAN-Datawarehouse übertragen
5. Schritt: Statistikdaten im MAGELLAN DWH-Explorer erstellen


## Eingaben in DAVINCI


Wir empfehlen Ihnen beim Abgleich der IDs der Schüler, Klassen, Lehrer und Fächer sicherheitshalber wie folgt vorzugehen:
1. Öffnen Sie MAGELLAN und wechseln Sie in die entsprechende Ansicht „Schüler“, „Klassen“ oder „Lehrer“. Die Fächerliste finden Sie unter „Verzeichnisse“, „Fächer“. 
2.	Exportieren Sie die Auswahlliste nach Excel und drucken Sie diese zur Vorlage aus.
3.	Öffnen Sie DAVINCI und wechseln Sie in die entsprechende Ansicht der Stammdaten.
4.	Vergleichen Sie die IDs und Kürzel Ihrer Vorlage mit den IDs und Kürzel in der DAVINCI Ansicht und korrigieren Sie ggf. in DAVINCI.


###Veranstaltungsliste

Einige Daten für die Statistik errechnen sich unmittelbar aus den Unterrichtsangaben in der Veranstaltungsliste. Für jede Veranstaltung sollten daher der Lehrer, die Klasse, das Fach und die Unterrichtsstunden eingetragen sein.
###Kurswahldaten und Lehrerdaten von DAVINCI nach MAGELLAN übertragen


Die Kurswahldaten (für Schulen mit Oberstufe) und die Lehrerdaten mit der Soll-Berechnung aus DAVINCI (für die Sollberechnung) müssen für die Statistik nach MAGELLAN übertragen werden. Nachdem Sie die Statistikkontrolle durchgeführt haben und die IDs in beiden Programmen übereinstimmen, sollten sie die Kurswahldaten übernehmen, wie im DAVINCI Handbuch im Kapitel „Spezielles“  unter „Datenaustausch mit MAGELLAN“, „Daten nach MAGELLAN übergeben“ beschrieben.

>Bitte beachten Sie, dass Sie nur mit Kopien der DAVINCI Datei und MAGELLAN Datenbank arbeiten!


# Übertrag ins Datawarehouse

So übertragen Sie Daten in das Datawarehouse:
1.	Wählen Sie in MAGELLAN die Ansicht ```Datawarehouse``` aus.
2.	Klicken Sie dort unterhalb von ```Extras``` auf ```Starten```.
3.	Der Importassistent für das MAGELLAN-Datawarehouse wird gestartet.  Sie müssen sich jetzt erneut an der MAGELLAN Datenbank mit der Administrator- Kennung und Kennwort anmelden.
4.	Klicken Sie auf ```Weiter``` und wählen Sie den passenden Mandanten und  Zeitraum  aus.
5.	Klicken Sie auf ```Weiter``` und dann auf ```Starten```. Die Daten werden jetzt in das MAGELLAN Datawarehouse übertragen.

>Wenn Sie mit Halbjahren arbeiten, müssen Sie diesen Vorgang nur einmal ausführen, um die Daten aus dem aktuellen Zeitraum (1. Halbjahr) zu übertragen.

#Statistikdaten im MAGELLAN-DWH-Explorer erstellen


Jetzt kann die Statistik mittels des MAGELLAN DWH Explorer erstellt werden. Gehen Sie dabei wie folgt vor:
1.	Klicken Sie auf ```Start```, dann auf Programme, dann auf STÜBER SYSTEMS und dann auf MAGELLAN 5/6 DWH Explorer.
2.	Wählen Sie die Ansicht ```Auswertungen``` aus.
3.	Wählen Sie unter Landesstatistik die Option ```Statistikformat für Thüringen``` aus und klicken Sie auf ```Starten```.
4.	Folgen Sie nun den Anweisungen des Assistenten und klicken Sie auf ```Weiter```, um auf die nächste Karte zu kommen. 
5.	Klicken Sie auf ```Weiter``` und folgen Sie den Anweisungen der nächsten Karte.
**Erhebungszeitraum**
Der „Erhebungszeitraum“ ist der Zeitraum in dem der Stichtag liegt. Dieser ist für die Statistik 2007 bei Verwendung von Halbjahren der 01.08.2007 bis zum 31.01.2008.
**Erstellungsdatum**
Tragen Sie das aktuelle Datum ein.
**Stichtag**
Tragen Sie den vom Kultusministerium festgelegten Stichtag für die Statistik ein.
**Exportordner**
Tragen Sie das Verzeichnis ein, in dem die fertigen Statistikdateien abgelegt werden sollen.
6.	Klicken Sie auf ```Weiter``` und Sie erhalten eine letzte Übersicht der zu erstellenden Statistikdateien. Durch einen weiteren Klick auf ```Fertigstellen``` werden die Statistikdateien im Exportordner angelegt.


# Besonderheiten

##Bildungsgänge und Fachrichtungen
Die Schlüssel und Bezeichnungen für die Bildungsgänge und Fachrichtungen wurden miteinander kombiniert. Die Schlüssel werden im Statistikskript automatisch berechnet. Wenn keine Fachrichtung vorhanden war, wurde automatisch die Bezeichnung des Bildungsganges verwendet, ansonsten die Bezeichnung der Fachrichtung.


# Schüler und Klassendaten


Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

<table class="table">
<caption></caption>
<thead>
<tr>
<th colspan=2 >Schüler und Klassendaten</th>
    </tr>
 </thead>
<tbody>
<tr>
    <th>Statistikfeld</th>
        <th align=left>SJ > Schuljahr</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Das aktuelle Schuljahr wird automatisch eingetragen.</td>
    </td>
  </tr>
   <tr>
    <td>Statistikdatei</td>
    <td>  sa	 </td>
    </td>
  </tr>
    <tr>
    <td>Typ</td>
    <td>  P	 </td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>DAT > Eingabedatum</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Das aktuelle Datum wird automatisch eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F1 > SNR (Schulnummer)</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Mandanten > Daten 1 > Schulnummer	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie  im Feld „Schulnummer“ die Schulnummer Ihrer Schule ein.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F2 > Satzart(„Schüler“)	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Daten > Schulart</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Schulart“ die Schulart der Klasse ein.<br/>Wichtig: Von der korrekten Schulart hängt ab, ob z.B. die Kursfelder (bei Beruflichen Gymnasien) der Statistik gefüllt werden.<br/>Grundlage ist das Schlüsselver-zeichnis „Schularten“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F3 > Schulteil</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Der Schulteil wird immer vorbesetzt und ist „1“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F4 > lfd. Nr. der Klasse</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:lassen > Daten > Statistikkürzel</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Statistikkürzel“ eine laufende Nummer für die Klassen ein, die für die Statistik berücksichtigt werden sollen.<br/>Wichtig: Die laufende Nummer muss fortlaufend vergeben werden.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F5 > Y-Zug mit</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Merkmale > Merkmal B1</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Merkmal B1“ die laufende Nummer der Klasse ein, mit der die aktuelle Klasse in mindestens einem Fach zusam-men unterrichtet wird.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F6 > Klassenbezeichnung</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Daten > Kürzel	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Kürzel“ das Klassenkürzel der Klasse ein. Dieser wird bei der Statistik als Klassenbezeichnung verwendet.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F7 > Jahrgangsstufe	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Zeiträume > Zeitraum > Jahrgang	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Jahrgang“ die Jahrgangsstufe der Klasse ein.<br/>Wichtig: Erlaubt sind die Jahrgänge 1-4</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F8 > Unterrichtswochenstunden</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    DAVINCI Stundenplan	     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Die Unterrichtswochenstunden für die Schüler werden automatisch in DAVINCI, anhand der gefüllten Veranstaltungsliste der Klasse berechnet.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F9 > lfd. Nr. des Schülers</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch vergeben und eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F10 > Name	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Nachname</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Nachname“ den „Nachnamen“ des Schülers ein.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F11 > Vorname</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Vorname</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Vorname“ den „Vornamen“ des Schülers ein.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> P 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>           </th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>F12 >  Geburtsdatum	MAGELLAN:Schüler > Daten 1 > Geboren am	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>  Tragen Sie im Feld „Geboren am“ das „Geburtsdatum“ des Schülers ein.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F13 > Geschlecht	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Geschlecht</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>  Tragen Sie im Feld „Geschlecht“ das Geschlecht des Schülers ein.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>  F14 >  Vorbildung</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Abschluss“ die Vorbildung des Schülers ein.Grundlage ist das Schlüsselver-zeichnis „Abschlüsse (Extern)“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  P	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F15 > Klassenart</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Merkmale > Merkmal S2</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Merkmal S2“ die Klassenart ein. Grundlage ist das Schlüsselver-zeichnis „Schülermerkmale (Bereich S2)“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F16 > Schulform</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Daten > Schulform	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Schulform“ die Schulform der Klasse ein.Grundlage ist das Schlüsselver-zeichnis „Schulformen“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F17 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F18 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F19 > Beruf/Bildungsgang <br/>F69 > Fachrichtung	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN: Klassen > Daten > Bildungsgang	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Bildungsgang“ den Bildungs-gang/Fachrichtung der Klasse ein.Grundlage ist das Schlüsselver-zeichnis „Bildungsgaenge“.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F20 > Behinderte/Benachteiligte</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 4 > Behinderung</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Behinderung“ die Art der Behinderung ein.<br/>Grundlage ist das Schlüsselver-zeichnis „Behinderungsarten“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F21 > nicht belegt </th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>-</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F22 > Zugang – Schulart</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>	MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulart<br/>Schüler > Zugang/Abgang > Herkunftsschule	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Schulart“ die Schulart der zuvor besuchten Schule ein.<br/>Wählen Sie die Herkunftsschule im Feld „Herkunftsschule“ aus.<br/>Grundlage ist das Schlüsselverzeichnis „Schularten (Herkunft)“.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F23 > Zugang – Land	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Zugang/Abgang > Bereits besuchte Schulen > UnterlagenSchüler > Zugang/Abgang > Herkunftsschule	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Unterlagen“ das Land der zuvor besuchten Schule ein.<br/>Wählen Sie die Herkunftsschule im Feld „Herkunftsschule“ aus.<br/>Grundlage ist das Schlüsselverzeichnis „Herkunftsunterlagen“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F24 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
    <tr>
    <th>Statistikfeld</th>
        <th align=left>F25 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
    <tr>
    <th>Statistikfeld</th>
        <th align=left>F26 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
    <tr>
    <th>Statistikfeld</th>
        <th align=left>F27 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F28 > Schulabschluss</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Laufbahn > Abschluss > Abschluss 1 > Abschlussart</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Abschluss-art“ den Schulabschluss des Schülers ein.Grundlage ist das Schlüsselverzeichnis „Abschlussarten“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F29 > Entlassungsdatum	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Zugang/Abgang > Abgang > AbgangAm</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Abgang am“ das Entlassungsdatum des Schülers ein.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F30 > Verlängerung</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Laufbahn > Allgemein > Wiederholer	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>	Markieren Sie das Feld „Wiederholer“, wenn der Schüler das Schuljahr wiederholt.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F31 > Ausländer, Aussiedler</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Statistik > Merkmal S1	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Merkmal S1“ den Aussiedler, bzw. Ausländer-status des Schülers ein.Grundlage ist das Schlüsselver-zeichnis „Schülemerkmale Bereich S1“.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F32 > Staatsangehörigkeit	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 2 > Staatsangehörigkeiten > Staatsangeh. 1	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Staatsangeh.1“ die Staatsangehörigkeit des Schülers ein.<br/>Grundlage ist das Schlüsselverzeichnis „Staatsangehoerigkeiten“.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F33 > Wohnort	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Gemeinde	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wählen Sie im Feld „Gemeinde“ den entsprechenden Gemeindeschlüssel aus.<br/>Der Schlüssel für den Wohnort ergibt sich aus dem Gemeindeschlüssel.<br/><br/>Tipp: <br/>Wenn Sie im Feld „PLZ“ eine bekannte Postleitzahl eintragen, wird der Gemeindeschlüssel automatisch für Sie eingetragen.<br/>Grundlage ist das „Postleitzahlenverzeichnis“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F34 > Schülerstatus	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 2 > Umschulung > Umschulung</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Umschulung“ den Schülerstatus ein.<br/>Grundlage ist das Schlüsselver-zeichnis „Umschulungsmerkmale“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F35 > Internat</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 4 > Betreuung > Einrichtung</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Einrichtung“ ein, ob es sich beim dem Schüler um einen Internatsschüler handelt.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F36 > Fahrtdauer</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 4 > Beförderung > Entfernung	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Fahrtdauer“ bei einem Internatsschüler die Fahrtdauer einer einfachen Fahrt zwischen Wohn- und Beschulungsort ein.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F37 > Religionszugehörigkeit</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Konfession</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Konfession“ die Religionszugehörigkeit des Schülers ein.<br/>Grundlage ist das Schlüsselverzeichnis „Konfessionen“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F38 > Religion – Abmeldung<br/>F39 > Religion – Meldung	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Rel.-Wunsch</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Rel.-Wunsch„ die An- oder Abmeldung vom Religionsunterricht ein.<br/>Grundlage ist das Schlüsselverzeichnis „Religionswünsche“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F40 > Religion/Ethik Teilnahme	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Rel.-Teilnahme</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>  Tragen Sie im Feld „Rel.-Teilnahme“ die Teilnahme am Religionsunterricht ein.	</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F41 > Religionsunterrichtsort</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Statistik > Merkmal T2</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Merkmal T2“ die Schulnummer der Schule ein, wenn der Schüler nicht an der Stammschule Religionsunterricht erhält.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F42 > 1.FS-Status<br/>F44 > 2.FS-Status<br/>F46 > 3. FS-Status	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Zeugnis > Fächer > Fachstatus</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Fachstatus“ für jede Fremdsprache den gültigen Fachstatus ein.<br/><br/>Mögliche Werte: „Pflicht“, „Wahlpf“ oder Freiw“<br/><br/>Berufliche Gymnasien: Bei Leistungskursen muss „1PF“ oder „2PF“ gesetzt werden, damit die Kurse für die Statistik korrekt erfasst werden. <br/>Der Fremdsprachenstatus wird dann automatisch auf „Pflicht“ gesetzt.<br/><br/>Grundlage ist das Schlüsselverzeichnis „Fachstati“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F43 > 1.FS-Sprache<br/>F45 > 2.FS-Sprache<br/>F47 > 3. FS-Sprache	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:<br/>Schüler > Daten 3 > Fremdsprachenfolge > 1. -3. Fremdsprache<br/>Schüler > Zeugnis > Fächer > Fach</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wählen Sie in den entsprechen-den Feldern die erteilten Fremdsprachen aus.<br/>Diese Fremdsprachen müssen auch als Fächer mit dem korrekten Fachstatus erfasst sein.<br/>Grundlage ist das Schlüsselverzeichnis „Fächer“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F48 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
   <tr>
    <th>Statistikfeld</th>
        <th align=left>F49 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F50 > 1. Leistungskurs 
<br/>F51 > 2. Leistungskurs	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:<br/>Schüler > Zeugnis > Fächer > FachSchüler > Zeugnis > Fächer > Unterrichtsart<br/>Schüler > Zeugnis > Fächer > Fachstatus	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Nur Berufliche Gymnasien:<br/>Wählen Sie im Feld „Fach“ den Leistungskurs aus. Wählen Sie im Feld „Unterrichtsart“ den Wert „LK “ für Leistungskurs aus.<br/>Wählen Sie im Feld „Fachstatus“ je nach Gegebenheit einen der beiden Werte aus:<br/>„1PF“ für 1. Prüfungsfach„2PF“ für 2. Prüfungsfach</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F52 – F60 > 1. – 9. Grundkurs<br/>F62 >     10. Grundkurs</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:<br/>Schüler > Zeugnis > Fächer > Fach<br/>Schüler > Zeugnis > Fächer > Unterrichtsart<br/>Schüler > Zeugnis > Fächer > Fachstatus	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Nur Berufliche Gymnasien:Wählen Sie im Feld „Fach“ den Grundkurs aus.<br/>Wählen Sie im Feld „Unterrichtsart“ den Wert „GK “ für Grundkurs aus.<br/>Wählen Sie im Feld „Fachstatus“ den Fachstatus aus. <br/>Achten Sie auf die entsprechenden Werte für Fremdsprachen, siehe F43/F45/F47.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F61 > Seminarfach	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:<br/>Schüler > Zeugnis > Fächer > FachSchüler > Zeugnis > Fächer > Unterrichtsart<br/>Schüler > Zeugnis > Fächer > Fachstatus	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Nur Berufliche Gymnasien:<br/>Wählen Sie im Feld „Fach“ das Seminarfach aus. <br/>Wählen Sie im Feld „Unterrichtsart“ den Wert „BL “ für Besondere Lernleistung aus. <br/>Wählen Sie im Feld „Fachstatus“ den Fachstatus aus. <br/>Achten Sie auf die entsprechenden Werte für Fremdsprachen, siehe F43/F45/F47.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F63 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
 <tr>
    <th>Statistikfeld</th>
        <th align=left>F64-F66 > begonnen in der Jahrgangsstufe</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 3 > Fremdsprachenfolge > Von</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Von“ jeweils den Beginn der Fremdsprache ein.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F67 > nicht belegt</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Wird automatisch als Leerfeld eingetragen.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F68 > Berufsfeld</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Klassen > Daten > Berufsfeld</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld “Berufsfeld” das Berufsfeld der Klasse ein.<br/>Grundlage ist das Schlüsselverzeichnis „Berufsfelder“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>B</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F70 > früherer Name	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Statistik > Merkmal T2	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Merkmal T2„ den früheren Namen des Schülers ein, falls der Name sich seit der letzten Statistik geändert hat.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F71 > Geburtsort-/land	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Daten 1 > Geburtsort	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Geburtsort“ die langschriftliche Bezeichnung des Geburtsortes ein, wie er im Schlüsselverzeichnis  „Staatsangehoerigkeiten“ eingetragen ist.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> P 	</td>
    </td>
  </tr>
<tr>
    <th>Statistikfeld</th>
        <th align=left>F72 > Zugang – letzte Tätigkeit	</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Statistik > Merkmal S2	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie im Feld „Merkmal S2“ die letzte Tätigkeit ein.<br/>Grundlage ist das Schlüsselver-zeichnis „Schülermerkmale Bereich S2“.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td>  B	</td>
    </td>
  </tr>
  <tr>
    <th>Statistikfeld</th>
        <th align=left>F73 > Ort des Ausbildungsbetriebes</th>
    </tr>
  <tr>
    <td>Datenfeld</td>
    <td>MAGELLAN:Schüler > Ausbildung > Ausbildungsbetrieb	</td>
    </tr>
  <tr>
    <td>Beschreibung</td>
    <td>Tragen Sie in der Liste der Ausbildungsbetriebe den Ausbildungsbetrieb des Schülers ein.<br/> Für die Statistik wird automatisch die Gemeinde des Ausbildungsbetriebes ausgelesen. <br/>Voraussetzung ist, dass Sie einen Ausbildungsbetrieb bei den Betrieben mit Gemeindeschlüssel erfasst haben.</td>
    </td>
  </tr>
  <tr>
    <td>Statistikdatei</td>
    <td>  sa	</td>
    </td>
  </tr>
 <tr>
    <td>Typ</td>
    <td> B 	</td>
    </td>
  </tr>
</tbody>
</table>

