# Schleswig-Holstein - ABS und BBS

Dieses Kapitel beschreibt für Allgemeinbildende und Berufsbildende Schulen in Schleswig-Holstein die benötigten Schritte zum Erstellen der elektronischen Landesstatistik im Statistik-Online-Verfahren für das Schuljahr 2018/2019. 

## Einführung

Auf Basis der erfassten Daten in MAGELLAN und DAVINCI können Sie die Herbststatistik für das Statistikamt bzw. das Ministerium vollständig elektronisch erstellen. Mit Hilfe des Statistik-Assistenten für Schleswig-Holstein können Sie die folgenden Dateien erzeugen:

Datei |Inhalt
--|--
XXX_DATSA_JJJJMMTT.TXT| Beinhaltet alle Daten der Schüler und gegebenen Fächer<br> an allgemeinbildenden Schulen im aktuellen Schuljahr.
XXX_DATEA_JJJJMMTT.TXT| Beinhaltet alle Daten der Entlassenen Schüler<br> an allgemeinbildenden Schulen im aktuellen Schuljahr.
XXX_DATSB_JJJJMMTT.TXT| Beinhaltet alle Daten der Schüler<br> an berufsbildenden Schulen im aktuellen Schuljahr.
XXX_DATEB_JJJJMMTT.TXT| Beinhaltet alle Daten der Entlassenen Schüler an<br> berufsbildenden Schulen im aktuellen Schuljahr.
XXX_DATFB_JJJJMMTT.TXT| Beinhaltet Angaben zu speziellen Fächern <br> an allgemeinbildenden Schulen.
XXX_DATLD_JJJJMMTT.TXT| Beinhaltet alle Daten der Schule im aktuellen Schuljahr<br> an allgemeinbildenden und berufsbildenden Schulen.
XXX_DATOS_JJJJMMTT.TXT| Beinhaltet alle Angaben zu den Kursen in der Oberstufe<br> an allgemeinbildenden und berufsbildenden Schulen.
XXX_DATLE_JJJJMMTT.TXT| Beinhaltet alle Daten der Lehrer im aktuellen Schuljahr<br> an allgemeinbildenden und berufsbildenden Schulen.


> Dabei steht das <XXX> für die Schulnummer der Schule und <JJJJMMTT> für das Erstellungsdatum z.B. 20140826. Ist beispielsweise die Lehrerdatei am 29.08.2015 von der Schule 12345 erstellt worden, so erhält sie den Dateinamen 12345_LE_20140829.TXT. 

Wie Sie diese Dateien an das Statistikamt versenden, wird Ihnen direkt durch das Statistikamt mitgeteilt.

Notwendige Schritte:

1. Schritt: [Statistikschlüssel bereinigen und aktualisieren](../schluesselverzeichnisse.md)
2. Schritt: Statistisch relevante Daten in DAVINCI bzw. MAGELLAN eingeben
3. Schritt: Kurswahlen (nur für Gymnasien/Gesamtschulen mit Oberstufe) 
4. Schritt: Lehrer (Soll-Ist-Berechnung) von DAVINCI nach MAGELLAN übertragen 
5. Schritt: Statistikdaten aus DAVINCI exportieren
6. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
7. Schritt: Statistikdaten erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistisch relevante Daten eingeben

Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang, in einer tabellarischen Übersicht.

>Statistikkürzel: Voraussetzung für das Ausspielen der Daten in das Statistikformat ist die Angabe des Feldes ```Klassen > Daten 1| > Statistikkürzel```. Das Feld kann beliebig eingetragen werden und sollte eindeutig benannt sein. Üblicherweise wird hier einfach das Klassenkürzel wiederholt. Schüler, für deren Klasse kein Statistikkürzel eingetragen ist, werden statistisch nicht berücksichtigt.

Statistikfeld|Datenfeld in MAGELLAN/DAVINCI|Beschreibung
--|--|--
- |MAGELLAN:<br>Klassen > Daten > Statistikkürzel |Über das Statistikkürzel steuern Sie, ob diese Klasse und dessen Schüler statistisch relevant sind und in den Statistikdateien berücksichtigt werden sollen.
- |MAGELLAN:<br>Schüler > Daten 3 > Verschiedenes > Gastschüler |Wenn Sie den Haken beim Gastschüler setzen, wird der Schüler nicht mit in der Statistik berücksichtigt.

## Eingaben in DAVINCI

!!! info "Hinweis"

  Sie müssen zusätzliche Eingaben im Kurs- und Stundenplanmodul von DAVINCI vornehmen. Genauere Informationen zu den Eingaben für DAVINCI finden Sie in der nachfolgenden tabellarischen Übersicht.

Überprüfen Sie in DAVINCI (bei Gymnasien/Gesamtschulen) bitte folgende Punkte:

Wo|Was
--|--
Stammdaten > Klassen|Bitte erfassen Sie in der Spalte ID für alle Oberstufen Klassen die MAGELLAN-ID.
Stammdaten > Fächer|Für alle Fächer muss in der Spalte „Schlüssel“ der vom Statistikamt vorgeschriebene Schlüssel erfasst werden, z.B. „014“ für das Fach Deutsch.
Veranstaltungsübersicht > Klassen|Achten Sie darauf alle Leistungs- und Grundkurse eingetragen zu haben. 

Wir empfehlen Ihnen beim Abgleich der IDs der Schüler, Klassen, Lehrer und Fächer sicherheitshalber wie folgt vorzugehen:

1. Öffnen Sie MAGELLAN und wechseln Sie in die entsprechende Ansicht „Schüler“, „Klassen“ oder „Lehrer“. Die Fächerliste finden unter „Verzeichnisse“, „Fächer“. 
2. Exportieren Sie die Auswahlliste nach Excel und drucken Sie diese zur Vorlage aus.
3. Öffnen Sie DAVINCI und wechseln Sie in die entsprechende Ansicht. 
4. Vergleichen Sie die IDs und Kürzel Ihrer Vorlage mit den IDs und Kürzel in der DAVINCI Ansicht und korrigieren Sie ggf. in DAVINCI.

## Kurswahldaten und Lehrerdaten von DAVINCI nach MAGELLAN übertragen

### Kurswahl

Schulen mit Oberstufe müssen ihre Kurswahldaten für die Statistik in DAVINCI mit MAGELLAN abgleichen. Nachdem die IDs in beiden Programmen übereinstimmen, sollten sie die Kurswahldaten (Schülerkurswahl) übernehmen, wie im DAVINCI Handbuch im Kapitel „Spezielles“ unter „Datenaustausch mit MAGELLAN“, „Daten nach MAGELLAN übergeben“ beschrieben.

### Lehrerdaten

Nachdem in DAVINCI unter ``Stammdaten > Lehrer`` die Solländerungsgründe erfasst wurden, müssen diese Informationen von DAVINCI nach MAGELLAN abgeglichen werden. Der Übertrag erfolgt beim Abgleich des Punktes „Lehrer“.

!!! info "Hinweis"

  Bitte beachten Sie, dass Sie nur mit Kopien der DAVINCI Datei und MAGELLAN Datenbank arbeiten!

## Statistikdaten aus DAVINCI exportieren

Als Schule mit Oberstufe müssen Sie aus DAVINCI statistikrelevante Daten exportieren. Diese exportierten Daten werden dann zur eigentlichen Statistikerstellung in MAGELLAN verwendet.
So exportieren Sie Daten aus DAVINCI:

1. Wählen Sie unter ``Plan > Importieren und Exportieren > Statistikdaten exportieren`` aus und dann mit ``Statistik Schleswig-Holstein exportieren``
2. Geben Sie eine Exportdatei an. Klicken Sie auf ``OK``. 
3. Die Daten werden jetzt in die angegebene Datei exportiert.

## Besonderheiten

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

### Zur Statistik 2016/2017

Zur aktuellen Statistik existieren derzeit keine Besonderheiten.

## Statistikdateien

### Schuldaten

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

<table class="table">
  <thead>
<tr>
<th colspan="2" style="background-color:#FFFFFF;">Schuldaten (Leitdatei)</th>
</tr>
  </thead>
  

  <tbody>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>FAX</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>MAGELLAN: Mandanten > Daten 1 > Telefax</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Geben Sie die Faxnummer der Schule ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>EMAIL</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>MAGELLAN: Mandanten > Daten 1 > E-Mail</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Geben Sie die Email-Adresse der Schule ein.</td>
</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SLEIT</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>MAGELLAN: Mandanten > Daten 1 > Schulleiter<br/>
Lehrer > Daten 1 > VornameLehrer > Daten 1 > Nachname
</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Wählen Sie den Schulleiter der Schule aus. <br/>Der Schulleiter muss zuvor als Lehrer mit Vor- und Nachnamen eingetragen worden sein.</td>
</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SLGS</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>MAGELLAN: Mandanten > Daten 1 > Schulleiter<br/>Lehrer > Daten 1 > Geschlecht</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Wählen Sie den Schulleiter der Schule aus. <br/>Der Schulleiter muss zuvor als Lehrer mit seinem Geschlecht eingetragen worden sein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>GTB (GTB)</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>MAGELLAN:Mandanten > Daten 1 > Betreuungsform<br/>[Betreuungsformen] </td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Geben Sie die Betreuungsform der Schule ein.</td> 
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>VORWFAX</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>Wird aktuell nicht unterstützt</td>
</tr>
<tr>
<td>Beschreibung</td>
<td> Hier sollte die Faxvorwahl stehen.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>URL</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>MAGELLAN:Mandanten > Daten 1 > Internet</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Geben Sie die Internetpräsens der Schule ein.</td> 
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SVP</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Wir geben hier fest den Wert „MAGELLAN 6“ aus</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>VERSION</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Wir geben hier die aktuell installierte MAGELLAN 6 Version (Registry Wert) aus.</td>
</tr>
  </tbody>
</table>

### Schülerdaten und Klassendaten

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

<table class="table">
  <thead>
<tr>
<th colspan="3" style="background-color:#FFFFFF;">Schüler- und Klassendaten</th>
</tr>
   </thead>
  <tbody>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SNR</th>
<th align="right">SA, EA, SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schueler > Liste der Schüler > ID</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Die ID des Schülers wird beim Anlegen des Schülers automatisch erstellt und ist eindeutig. Sie wird beim Erstellen der Statistikdateien automatisch gesetzt.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SART (SART)</th>
<th align="right">SA, EA, FB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Klassen > Daten > Schulart<br/>[Schularten]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Schulart ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>KLNM</th>
<th align="right">SA, SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Klassen > Daten > Statistikkürzel</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie das Feld leer lassen.</td>
</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>KLK</th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2MAGELLAN: Schüler > Zeugnis > Fächer > Unterrichtsart<br/>Schüler > Zeugnis > Fächer > Fachstatus</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2> Dieser Wert setzt sich aus den Feldern:<br/>FachUnterrichtsart<br/>Fach<br/>Status<br/>Klassenstufe <br/>zusammen und wird automatisch berechnet.<br/>Geben Sie im Feld „Unterrichtsart“ folgende Werte an:<br/>LK = Leistungskurs<br/>GK = Grundkurs<br/>Kurs = Kurs bzw. Klassenunterricht<br/>Wahlb = Wahlbereich<br/>LG = Lerngruppe<br/><br/> Für übergreifenden Unterricht, GK+LK im Jahrgang 12 und 13 geben Sie im Feld „Unterrichtsart“ = LG ein und im Feld „FachStatus“ = „Übergr“ ein. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>GS</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 > Geschlecht</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das Geschlecht des Schülers ein. </td>
</tr>   
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>GBDAT</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 > Geboren am </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das Geburtsdatum des Schülers ein. </td>
</tr>  
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>STAAT(STAAT)</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 > Staatsangeh. 1<br/>[Staatsangehörigkeiten]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Nationalität des Schülers ein.</td>
</tr>  
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>DAZ</th>
<th align="right">SA, <font color=green>EA</font></th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal S6<br/>[Schülermerkmale  (Bereich S6)] </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2><font color=green>Geben Sie die Teilnahme am Unterricht „Deutsch als Zweitsprache“ an.</font></td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left> GEBLAND (STAAT)</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 >  Geburtsland<br/>[Staatsangehörigkeiten] </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das Geburtsland des Schülers an.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ZUZD</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 >  In Deutschland seit</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das das Zuzugsdatum nach Deutschland ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>VERKSPR (VERKSPR)</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 > Sprachgruppe<br/>[Sprachgruppen]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Verkehrssprache ein. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>KONF (KONF)</th>
<th align="right">SA,EA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 > Konfession<br/>[Konfessionen]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Konfession des Schülers ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>GTBU</th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal T1</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>
  Geben Sie hier die Teilnahme des Schülers am Ganztagsbetrieb ein.<br/>
  <ul>
<li>1 oder J = JA</li> 
<li>leer = NEIN</li>
  </ul>
</td>
</tr>   
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>JGSTUF (JGSTUF)</th>
<th align="right">SA,EA,FA, SB,EB,FB, OA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Klassen > Zeiträume > Klassenstufe<br/>[Klassenstufen]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Klassenstufe der Klasse in. </td>
</tr>   
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHHERK (1 von 3) (SCHHERK)</th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Zugang / Abgang > Bereits besuchte Schulen > Schulform<br/>[Schulformen]<br/>Schüler > Zugang / Abgang > Bereits besuchte Schulen > Herkunftsschule</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie für neu an die Schule gekommene  Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.<br/>Beachten Sie bitte dass die „Schulform“ eingetragen sein muss. <br/>Ein Schüler wird als Neuzugang erkannt, wenn unter ```Schüler > Zugang/Abgang > Zugang am``` ein Datum erfasst wurde, dass nach dem letzten und vor dem aktuellen Statistiktermin liegt.<br/>Für Schüler mit der Klassenstufe 1 (Klassen > Zeiträume > Klassenstufe) geben wir automatisch den Wert für den Schlüssel „Neuaufnahme (in die 1. Jahrgangsstufe)“ aus.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHHERK (2 von 3) (SCHHERK)</th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Laufbahn > Häkchen Wiederholer<br/>MAGELLAN > Schüler > Laufbahn > Wiederholungsarten<br/>[Wiederholungsarten] </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Wiederholer:<br/>Setzen Sie bitte für die Schüler im aktuellen Zeitraum das Häkchen für Überspringer.<br/>Wählen Sie im Feld Wiederholungsart einen Wert aus.</td> 
</tr>   
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHHERK (3 von 3) (SCHHERK) </th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Laufbahn > Häkchen Überspringer </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Überspringer:<br/>Setzen Sie bitte für die Schüler im aktuellen Zeitraum das Häkchen für Überspringer.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>HWS(GKZ)</th>
<th align="right">SA,EA, SB,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 > LandSchüler > Daten 1 > Gemeinde</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie im Feld „Land“ (das Feld vor „PLZ“) das Kürzel für das Wohnland des Schülers ein.  Ein Statistikwert wird eingetragen, wenn der Schüler in Dänemark DK) oder Deutschland(D oder leer) wohnt.Geben Sie im Feld „Gemeinde“ die Wohngemeinde des Schülers ein.Der Statistikwert wird automatisch aus beiden Angaben errechnet. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>G8</th>
<th align="right">SA,EA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN:<br/>Klassen > Daten > Schulart<br/>Schüler > Statistik > Merkmal T2 </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Teilnahme des Schülers am Schulversuch G8 ein. <br/>1 = JA<br/>2 = NEIN<br/>Wenn dieses Feld bei Gymnasien nicht gefüllt wird, erhalten die Schüler automatisch den Eintrag „2“ für Nein.<br/>Nur für Gymnasien, wenn Teilnahme am Schulversuch G8. <br/>Dazu prüfen wir die Schulart der Klasse, die eingetragen werden muss. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>FSWP (FSWP) </th>
<th align="right">SA,EA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 4 > Förderung > Förderung<br/>[Förderungen]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier den Förderschwerpunkt des Schülers ein.Nicht bei „Förderzentrum“!</td>
</tr>
<tr style="background-color:#CEE3F6; color: green;">
<th>Statistikfeld</th>
<th align=left>IFÖZ (IFÖZ) </th>
<th align="right">SA,SB</th>
</tr>
<tr style="background-color:#FFFFFF; color: green;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal > S5<br/>[Merkmale (Schüler)]</td>
</tr>
<tr style="color: green;">
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier den die Festlegung des zuständigen Förderzentrums an.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>JERST</th>
<th align="right">SA,EA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 > Grundschuleintritt </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das Datum der Ersteinschulung ein. Wichtig ist lediglich das Jahr.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>FACH01-20<br/>KURS (FACH/KURS)</th>
<th align="right">SA,FB,OA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Zeugnis > Fächer > Fach<br/>[Fächer]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie die Fächer des Schülers ein. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>UART01-20 (UART)</font></th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN:<br/>
  Schüler > Zeugnis > Fächer > Fach<br/>[Fächer]<br/>
  Schüler > Zeugnis > Fächer > Unterrichtsart<br/>
  Schüler > Zeugnis > Fächer > Fachstatus 
</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>
  Geben Sie die Fächer des Schülers ein.<br/>
  Für die Statistik werden einige besondere Fächer mit deren Fachstatus und der Schüleranzahl erfasst.<br/><br/>
  Unterrichtsfach ABS:<br/> 
  Fremdsprache, Fach wg. Nichtteilnahme am Religionsunterricht und Wahlpflichtfächer.<br/> 
  Bitte beachten Sie die Übersicht über automatisch erzeugte oder umgesetzte Werte im Abschnitt „Besonderheiten“!<br/><br/>
  Unterrichtsfach<br/> 
  BBS: Nur Darstellung der Fremdsprachen
</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>USPR01-20 (FACH)</th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN:Schüler > Zeugnis > Fächer > Sprache<br/>[Kurssprachen]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie die mündl. und schriftl. Unterrichtssprache für ein genehmigtes bilinguales Bildungsangebot für fremdsprachlichen Fachunterricht ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>KSNM01-20</th>
<th align="right">SA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Dieser Wert setzt sich aus den Feldern:<br/>FachKuerzel<br/>FachKursNr <br/>zusammen und wird automatisch berechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>STD01-20STD</th>
<th align="right">SA, FB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>
  Anzahl der Wochen-Ist-Stunden (pro Fach) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird. Dieser Statistikwert wird aus der Exportdatei [D6, Klassenist] berechnet.
  Voraussetzung dafür sind identische Einträge in MAGELLAN und DAVINC. <br/>
  Bitte überprüfen Sie in MAGELLAN und DAVINCI:<br/>- die Fachkürzel und Fachschlüssel<br/>- das Kürzel der verwendeten  Unterrichtsart (muss gefüllt sein!)<br/>
  - das Klassenkürzel und die KlassenID
</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>MASS (MASS)</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Klassen > Daten >  Bildungsgang<br/>[Bildungsgänge]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Maßnahme/Bildungsgang ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>UFBL (UFBL)</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Klassen > Daten >  Organisation<br/>[Organisationen]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier Unterrichtsform/Blockunterricht ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>BEH (BEH)</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schueler > Daten 4 >  Sonstige Daten >  Behinderung<br/>[Behinderungsarten] </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier die Behinderung des Schülers ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>NSCH</th>
<th align="right">EA, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal S1<br/>[Schülermerkmale  (Bereich S1)]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier ein, ob der Schüler ein Nichtschüler ist. <br/>Kein Eintrag bedeutet „Nein“. </td> 
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>JEINSCH</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schueler > Statistik > Merkmal T2</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier das Jahr der Ersteinschulung in das berufsbildende System ein.</td> 
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ENTLJ</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN:<br/>Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulbesuch bis<br/>Schüler > Zugang/Abgang > Herkunftsschule</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. <br/>Beachten Sie bitte, dass die „Schulbesuch bis“ eingetragen sein muss. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ABSF (ABSF)</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN:<br/>Schüler > Zugang/Abgang >  Bereits besuchte Schulen >  Schulform<br/>[Schulformen (Herkunft)]<br/>Schüler > Zugang/Abgang >  Herkunftsschule</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. Beachten Sie bitte, dass die „Schulform“ eingetragen sein muss.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>LKLST (JGSTUF)</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN:<br/>Schüler > Zugang/Abgang >  Bereits besuchte Schulen > Letzte Klassenstufe<br/>[Klassenstufen]<br/>Schüler > Zugang/Abgang >  Herkunftsschule</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. <br/>Beachten Sie bitte, dass die „Schulform“ eingetragen sein muss.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>AABS</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 > Höchster Abschluss ABS >  Abschluss<br/>[Abschlüsse (Extern)]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier den höchsten erreichten Abschluss an einer ABS ein.</td>
</td>
</tr>
   <tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>LABS</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss<br/>[Abschlüsse (Extern)]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier den höchsten erreichten berufsbezogenen Abschluss ein.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>WIEDH</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Laufbahn > Allgemein > Wiederholer</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Haken Sie das Feld „Wiederholer“ an, wenn der Schüler ein Wiederholer ist.Der statistische Wert wird automatisch berechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ZUSKURS (ZUSKURS)</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal S2<br/>[Schülermerkmale (Bereich S2)]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie an, ob der Schüler Zusatzkurse für weitere Abschlüsse absolviert.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>BFKLBS</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Klasse > Merkmale >  Merkmal S3<br/>[Klassenmerkmale (Bereich S3)]<br/>Schueler > Statistik  >  Merkmal S3<br/>[Schülermerkmale (Bereich S3)] </td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie an, ob sich der Schüler oder alle/viele Schüler der Klasse in einer Bezirksfach- oder Landesklasse befinden.Die Angabe beim Schülermerkmal hat vorrang zur Angabe des Klassenmerkmals, wenn beide eingetragen wurden.</td>
</tr>  
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ENTL</th>
<th align="right">EA</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal S4<br/>[Schülermerkmale (Bereich S4)]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Tragen Sie hier bitte für Abgänger ein, ob der Schüler das allgemeinbildende Schulsystem verlässt oder nicht.Achtung:Wenn der Schüler in einer Klasse < Jahrgang 9 ist, geben wir automatisch den Wert für „Ja, Schüler verbleibt im allgemeinbildenden Schulsystem“ aus.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ABSCHL (ABSCHL)</th>
<th align="right">EA, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Laufbahn > Abschluss > Abschluss 1<br/>[Abschlüsse (Intern)]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Der Statistikwert errechnet sich anhand des  Eintrags im Feld „Abschluss 1“ aus dem vorangegangenen Schuljahr.Hinweis: Für alle Abgänger (inaktive Schüler mit Abgangsdatum zwischen dem aktuellen und dem vergangenen Statistiktermin unter Zugang/Abgang > AbgangAm), die noch nicht die Schulpflicht erfüllt haben, wird automatisch der Schlüssel für „ohne Abschluss“ in die Statistikdatei übernommen.Schulbesuchsjahre werden am aktuellen Datum und dem Grundschuleintritt errechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ABSCHLBS (ABSCHLBS)</th>
<th align="right">EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Laufbahn > Abschluss 2 > Abschlussart<br/>[Abschlussarten]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier den Erfolg des Bildungsgangs ein.</td> 
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ABINOTE</th>
<th align="right">EA,EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Abschluss > Abschluss 1 > Abschlussnote</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>INSG</th>
<th align="right">FB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Anzahl der Schüler bestimmter Fächer, siehe UART.Statistikwert wird berechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>WEIBL</th>
<th align="right">FB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Anzahl der weiblichen Schüler bestimmter Fächer, siehe UART.Statistikwert wird berechnet.</td> 
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>PROFIL</th>
<th align="right">OB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schueler > Daten 3 > ProfilSchueler > Zeugnis > Faecher > Unterrichtsart</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Tragen Sie das Profil des Schülers ein.Anhand der Eingabe und des gewählten 3. Prüfungsfach berechnet sich beim entsprechenden Fach der Profilschlüssel.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHINSG</th>
<th align="right">OB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Anzahl der Schüler (pro Kurs).Statistikwert wird berechnet. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHWEIBL</th>
<th align="right">OB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Anzahl der weiblichen Schüler (pro Kurs).Statistikwert wird berechnet.</td><tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHANDS</th>
<th align="right">FB,OB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Statistik > Merkmal T3</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie im Feld „Merkmal T3“ ein „J“ ein, wenn der Schüler einer anderen Schule den Unterricht besucht.Es wird die Anzahl der Schüler (pro Kurs), die von einer anderen Schule kommen automatisch berechnet. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>SCHSTD</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Anzahl der Wochen-Ist-Stunden (pro Schüler) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird.Statistikwert wird berechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>WOSTD</th>
<th align="right">OB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>-</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Anzahl der Wochen-Ist-Stunden (pro Kurs) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird.<br/>Statistikwert wird berechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>BERUF (BERUF)</th>
<th align="right">SB, EB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Ausbildung > Beruf<br/>[Berufe]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie hier den Ausbildungsberuf des Schülers ein. </td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>UMSCH</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 2 > Umschulung > Umschulung<br/>[Umschulungsmerkmale]</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Bitte erfassen Sie, ob der Schüler ein Umschüler ist.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ABSKREIS</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 > Gemeinde</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein.Der Statistikwert wird automatisch daraus errechnet.</td>
</tr>
<tr style="background-color:#CEE3F6;">
<th>Statistikfeld</th>
<th align=left>ABSLAND</th>
<th align="right">SB</th>
</tr>
<tr style="background-color:#FFFFFF;">
<td>Datenfeld</td>
<td colspan=2>MAGELLAN: Schüler > Daten 1 > Gemeinde</td>
</tr>
<tr>
<td>Beschreibung</td>
<td colspan=2>Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein.Der Statistikwert wird automatisch daraus errechnet.</td>
</tr>
  </tbody>
</table>