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


 !!! info "Hinweis"
 
    Dabei steht das <XXX> für die Schulnummer der Schule und <JJJJMMTT> für das Erstellungsdatum z.B. 20140826. Ist beispielsweise die Lehrerdatei am 29.08.2015 von der Schule 12345 erstellt worden, so erhält sie den Dateinamen 12345_LE_20140829.TXT. 

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

!!! warning "Wichtig"
    Statistikkürzel: Voraussetzung für das Ausspielen der Daten in das Statistikformat ist die Angabe des Feldes ```Klassen > Daten 1| > Statistikkürzel```. Das Feld kann beliebig eingetragen werden und sollte eindeutig benannt sein. Üblicherweise wird hier einfach das Klassenkürzel wiederholt. Schüler, für deren Klasse kein Statistikkürzel eingetragen ist, werden statistisch nicht berücksichtigt.

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

**Statistikfeld** | **FAX**
-|-
Datenfeld	|MAGELLAN: Mandanten > Daten 1 > Telefax
Beschreibung|Geben Sie die Faxnummer der Schule ein.
**Statistikfeld**|**EMAIL**
Datenfeld|MAGELLAN: Mandanten > Daten 1 > E-Mail
Beschreibung|Geben Sie die Email-Adresse der Schule ein.
**Statistikfeld**|**SLEIT**
Datenfeld|MAGELLAN: Mandanten > Daten 1 > Schulleiter<br>Lehrer > Daten 1 > VornameLehrer > Daten 1 > Nachname
Beschreibung|Wählen Sie den Schulleiter der Schule aus. Der Schulleiter muss zuvor als Lehrer mit Vor- und Nachnamen eingetragen worden sein.
**Statistikfeld**|**SLGS**
Datenfeld|MAGELLAN: Mandanten > Daten 1 > Schulleiter<br>Lehrer > Daten 1 > Geschlecht
Beschreibung|Wählen Sie den Schulleiter der Schule aus. Der Schulleiter muss zuvor als Lehrer mit seinem Geschlecht eingetragen worden sein.
**Statistikfeld**|**GTB** (GTB)
Datenfeld|MAGELLAN:Mandanten > Daten 1 > Betreuungsform<br>[Betreuungsformen]
Beschreibung|Geben Sie die Betreuungsform der Schule ein.
**Statistikfeld**|**VORWFAX**
Datenfeld|Wird aktuell nicht unterstützt
Beschreibung|Hier sollte die Faxvorwahl stehen.
**Statistikfeld**|**URL**
Datenfeld|MAGELLAN:Mandanten > Daten 1 > Internet
Beschreibung|Geben Sie die Internetpräsens der Schule ein.
**Statistikfeld**|**SVP**
Datenfeld|-
Beschreibung|Wir geben hier fest den Wert „MAGELLAN 6“ aus
**Statistikfeld**|**VERSION**
Datenfeld|-
Beschreibung|Wir geben hier die aktuell installierte MAGELLAN 6 Version (Registry Wert) aus.

### Schülerdaten und Klassendaten

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

**Statistikfeld**| **SNR	SA, EA, SB, EB**
-|-
Datenfeld|MAGELLAN: Schueler > Liste der Schüler > ID
Beschreibung|Die ID des Schülers wird beim Anlegen des Schülers automatisch erstellt und ist eindeutig. Sie wird beim Erstellen der Statistikdateien automatisch gesetzt.
**Statistikfeld**|**SART (SART) 	SA, EA, FB**
Datenfeld|MAGELLAN: Klassen > Daten > Schulart<br>[Schularten]
Beschreibung|Geben Sie hier die Schulart ein.
**Statistikfeld**|**KLNM 	SA, SB**
Datenfeld |MAGELLAN: Klassen > Daten > Statistikkürzel
Beschreibung|Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie das Feld leer lassen.
**Statistikfeld**|**KLK 	SA**
Datenfeld |Zeugnis > Fächer > Unterrichtsart<br>Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung |Dieser Wert setzt sich aus den Feldern:<br>FachUnterrichtsart<br>Fach<br>Status<br>Klassenstufe<br>zusammen und wird automatisch berechnet.<br>Geben Sie im Feld „Unterrichtsart“ folgende Werte an:<br>LK = Leistungskurs<br>GK = Grundkurs<br>Kurs = Kurs bzw. Klassenunterricht<br>Wahlb = Wahlbereich<br>LG = Lerngruppe<br><br>Für übergreifenden Unterricht, GK+LK im Jahrgang 12 und 13 geben Sie im Feld „Unterrichtsart“ = LG ein und im Feld „FachStatus“ = „Übergr“ ein.
**Statistikfeld**|**SNR 	SA, EA, SB, EB**
Datenfeld|MAGELLAN: Schueler > Liste der Schüler > ID
Beschreibung |Die ID des Schülers wird beim Anlegen des Schülers automatisch erstellt und ist eindeutig. Sie wird beim Erstellen der Statistikdateien automatisch gesetzt.
**Statistikfeld**|**SART (SART) 	SA, EA, FB**
Datenfeld |MAGELLAN: Klassen > Daten > Schulart<br>[Schularten]
Beschreibung|Geben Sie hier die Schulart ein.
**Statistikfeld**|**KLNM 	SA, SB**
Datenfeld |MAGELLAN: Klassen > Daten > Statistikkürzel
Beschreibung |Geben Sie hier das Klassenkürzel ein, so wie es in der Statistik erscheinen soll. Sie können bestimmte Klassen von der Statistik ausnehmen, indem Sie das Feld leer lassen.
**Statistikfeld**|**KLK 	SA**
Datenfeld|Zeugnis > Fächer > Unterrichtsart<br>Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung|Dieser Wert setzt sich aus den Feldern:<br>FachUnterrichtsart<br>Fach<br>Status<br>Klassenstufe<br>zusammen und wird automatisch berechnet<br>.Geben Sie im Feld „Unterrichtsart“ folgende Werte an:<br>LK = Leistungskurs<br>GK = Grundkurs<br>Kurs = Kurs bzw. Klassenunterricht<br>Wahlb = Wahlbereich<br>LG = Lerngruppe<br><br>Für übergreifenden Unterricht, GK+LK im Jahrgang 12 und 13 geben Sie im Feld „Unterrichtsart“ = LG ein und im Feld „FachStatus“ = „Übergr“ ein.
**Statistikfeld**| **GS 	SA,EA, SB,EB**
Datenfeld |MAGELLAN: Schüler > Daten 1 > Geschlecht
Beschreibung |Geben Sie hier das Geschlecht des Schülers ein.
**Statistikfeld**| **GBDAT 	SA,EA, SB,EB**
Datenfeld|MAGELLAN: Schüler > Daten 1 > Geboren am
Beschreibung|Geben Sie hier das Geburtsdatum des Schülers ein.
**Statistikfeld** |**STAAT(STAAT) 	SA,EA, SB,EB**
Datenfeld|MAGELLAN: Schüler > Daten 2 > Staatsangeh. 1<br>[Staatsangehörigkeiten]
Beschreibung|Geben Sie hier die Nationalität des Schülers ein.
**Statistikfeld** |**DAZ 	SA, EA**
Datenfeld |MAGELLAN: Schüler > Statistik > Merkmal S6<br>[Schülermerkmale (Bereich S6)]
Beschreibung |Geben Sie die Teilnahme am Unterricht „Deutsch als Zweitsprache“ an.
**Statistikfeld**|**GEBLAND (STAAT) 	SA,EA, SB,EB**
Datenfeld |MAGELLAN: Schüler > Daten 1 > Geburtsland<br>[Staatsangehörigkeiten]
Beschreibung |Geben Sie hier das Geburtsland des Schülers an.
**Statistikfeld**|**ZUZD 	SA,EA, SB,EB**
Datenfeld |MAGELLAN: Schüler > Daten 2 > In Deutschland seit
Beschreibung |Geben Sie hier das das Zuzugsdatum nach Deutschland ein.
**Statistikfeld**| **VERKSPR (VERKSPR) 	SA,EA, SB,EB**
Datenfeld |MAGELLAN: Schüler > Daten 2 > Sprachgruppe<br>[Sprachgruppen]
Beschreibung|Geben Sie hier die Verkehrssprache ein.
**Statistikfeld** | **KONF (KONF) 	SA,EA**
Datenfeld |MAGELLAN: Schüler > Daten 1 > Konfession<br>[Konfessionen]
Beschreibung|Geben Sie hier die Konfession des Schülers ein.
**Statistikfeld** | **GTBU 	SA**
Datenfeld |MAGELLAN: Schüler > Statistik > Merkmal T1
Beschreibung |Geben Sie hier die Teilnahme des Schülers am Ganztagsbetrieb ein.<br>1 oder J = JA<br>leer = NEIN
**Statistikfeld**| **JGSTUF (JGSTUF) 	SA,EA,FA, SB,EB,FB, OA**
Datenfeld|MAGELLAN: Klassen > Zeiträume > Klassenstufe<br>[Klassenstufen]
Beschreibung |Geben Sie hier die Klassenstufe der Klasse in.
**Statistikfeld**|**SCHHERK (1 von 3) (SCHHERK) 	SA**
Datenfeld |MAGELLAN: Schüler > Zugang / Abgang > Bereits besuchte Schulen > Schulform<br>[Schulformen]<br>Schüler > Zugang / Abgang > Bereits besuchte Schulen > Herkunftsschule
Beschreibung |Geben Sie für neu an die Schule gekommene Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.<br>Beachten Sie bitte dass die „Schulform“ eingetragen sein muss.<br>Ein Schüler wird als Neuzugang erkannt, wenn unter ```Schüler > Zugang/Abgang > Zugang am``` ein Datum erfasst wurde, dass nach dem letzten und vor dem aktuellen Statistiktermin liegt.<br>Für Schüler mit der Klassenstufe 1 (Klassen > Zeiträume > Klassenstufe) geben wir automatisch den Wert für den Schlüssel „Neuaufnahme (in die 1. Jahrgangsstufe)“ aus.
**Statistikfeld** |**SCHHERK (2 von 3) (SCHHERK) 	SA**
Datenfeld |MAGELLAN: Schüler > Laufbahn > Häkchen Wiederholer<br>MAGELLAN > Schüler > Laufbahn > Wiederholungsarten<br>[Wiederholungsarten]
Beschreibung|Wiederholer:<br>Setzen Sie bitte für die Schüler im aktuellen Zeitraum das Häkchen für Überspringer.<br>Wählen Sie im Feld Wiederholungsart einen Wert aus.
**Statistikfeld**| **SCHHERK (3 von 3) (SCHHERK) 	SA**
Datenfeld |MAGELLAN: Schüler > Laufbahn > Häkchen Überspringer
Beschreibung |Überspringer:<br>Setzen Sie bitte für die Schüler im aktuellen Zeitraum das Häkchen für Überspringer.
**Statistikfeld** |  **HWS(GKZ) 	SA,EA, SB,EB**
Datenfeld |MAGELLAN: Schüler > Daten 1 > LandSchüler > Daten 1 > Gemeinde
Beschreibung|Geben Sie im Feld „Land“ (das Feld vor „PLZ“) das Kürzel für das Wohnland des Schülers ein. Ein Statistikwert wird eingetragen, wenn der Schüler in Dänemark DK) oder Deutschland(D oder leer) wohnt.Geben Sie im Feld „Gemeinde“ die Wohngemeinde des Schülers ein. Der Statistikwert wird automatisch aus beiden Angaben errechnet.
**Statistikfeld**|**G8 	SA,EA**
Datenfeld |MAGELLAN: Klassen > Daten > Schulart<br>Schüler > Statistik > Merkmal T2
Beschreibung |Geben Sie hier die Teilnahme des Schülers am Schulversuch G8 ein.<br>1 = JA<br>2 = NEIN<br>Wenn dieses Feld bei Gymnasien nicht gefüllt wird, erhalten die Schüler automatisch den Eintrag „2“ für Nein.<br>Nur für Gymnasien, wenn Teilnahme am Schulversuch G8. Dazu prüfen wir die Schulart der Klasse, die eingetragen werden muss.
**Statistikfeld** | **FSWP (FSWP) 	SA,EA**
Datenfeld |MAGELLAN: Schüler > Daten 4 > Förderung > Förderung<br>[Förderungen]
Beschreibung |Geben Sie hier den Förderschwerpunkt des Schülers ein.Nicht bei „Förderzentrum“!
**Statistikfeld** | **IFÖZ (IFÖZ) 	SA,SB**
Datenfeld |MAGELLAN: Schüler > Statistik > Merkmal > S5<br>[Merkmale (Schüler)]
Beschreibung|	Geben Sie hier den die Festlegung des zuständigen Förderzentrums an.
**Statistikfeld**| **JERST 	SA,EA**
Datenfeld |MAGELLAN: Schüler > Daten 2 > Grundschuleintritt
Beschreibung|Geben Sie hier das Datum der Ersteinschulung ein. Wichtig ist lediglich das Jahr.
**Statistikfeld**|**FACH01-20**<br>**KURS (FACH/KURS) 	SA,FB,OA**
Datenfeld|MAGELLAN: Schüler > Zeugnis > Fächer > Fach<br>[Fächer]
Beschreibung |Geben Sie die Fächer des Schülers ein.
**Statistikfeld**|**UART01-20 (UART) 	SA**
Datenfeld |MAGELLAN:<br>Schüler > Zeugnis > Fächer > Fach<br>[Fächer]<br>Schüler > Zeugnis > Fächer > Unterrichtsart<br>Schüler > Zeugnis > Fächer > Fachstatus
Beschreibung|Geben Sie die Fächer des Schülers ein.<br>Für die Statistik werden einige besondere Fächer mit deren Fachstatus und der Schüleranzahl erfasst.<br><br>Unterrichtsfach ABS:<br>Fremdsprache, Fach wg. Nichtteilnahme am Religionsunterricht und Wahlpflichtfächer.<br>Bitte beachten Sie die Übersicht über automatisch erzeugte oder umgesetzte Werte im Abschnitt „Besonderheiten!<br><br>Unterrichtsfach<br>BBS: Nur Darstellung der Fremdsprachen
**Statistikfeld**|**USPR01-20 (FACH) 	SA**
Datenfeld|MAGELLAN:Schüler > Zeugnis > Fächer > Sprache<br>[Kurssprachen]
Beschreibung |Geben Sie die mündl. und schriftl. Unterrichtssprache für ein genehmigtes bilinguales Bildungsangebot für fremdsprachlichen Fachunterricht ein.
**Statistikfeld**|**KSNM01-20 	SA**
Datenfeld |-
Beschreibung|Dieser Wert setzt sich aus den Feldern:<br>FachKuerzel<br>FachKursNr<br>zusammen und wird automatisch berechnet.
**Statistikfeld**|**STD01-20STD 	SA, FB**
Datenfeld|-
Beschreibung |Anzahl der Wochen-Ist-Stunden (pro Fach) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird. Dieser Statistikwert wird aus der Exportdatei [D6, Klassenist] berechnet. Voraussetzung dafür sind identische Einträge in MAGELLAN und DAVINC.<br>Bitte überprüfen Sie in MAGELLAN und DAVINCI:<br>- die Fachkürzel und Fachschlüssel<br>- das Kürzel der verwendeten Unterrichtsart (muss gefüllt sein!)<br>- das Klassenkürzel und die KlassenID
**Statistikfeld**|**MASS (MASS) 	SB, EB**
Datenfeld|MAGELLAN: Klassen > Daten > Bildungsgang [Bildungsgänge]
Beschreibung|Geben Sie hier die Maßnahme/Bildungsgang ein.
**Statistikfeld**|**UFBL (UFBL) 	SB, EB**
Datenfeld |	MAGELLAN: Klassen > Daten > Organisation [Organisationen]
Beschreibung|Geben Sie hier Unterrichtsform/Blockunterricht ein.
**Statistikfeld**|**BEH (BEH) 	SB, EB**
Datenfeld |MAGELLAN: Schueler > Daten 4 > Sonstige Daten > Behinderung [Behinderungsarten]
Beschreibung|Geben Sie hier die Behinderung des Schülers ein.
**Statistikfeld**|**NSCH 	EA, EB**
Datenfeld|MAGELLAN: Schüler > Statistik > Merkmal S1 [Schülermerkmale (Bereich S1)]
Beschreibung|Geben Sie hier ein, ob der Schüler ein Nichtschüler ist.<brb>Kein Eintrag bedeutet „Nein“.
**Statistikfeld**|**JEINSCH 	SB, EB**
Datenfeld|MAGELLAN: Schueler > Statistik > Merkmal T2
Beschreibung|Geben Sie hier das Jahr der Ersteinschulung in das berufsbildende System ein.
**Statistikfeld**|**ENTLJ 	SB**
Datenfeld |MAGELLAN: Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulbesuch bis<br>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung |Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.<br>Beachten Sie bitte, dass die „Schulbesuch bis“ eingetragen sein muss.
**Statistikfeld**|**ABSF (ABSF) 	SB**
Datenfeld |MAGELLAN: Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulform [Schulformen (Herkunft)]<br>Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung |Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus. Beachten Sie bitte, dass die „Schulform“ eingetragen sein muss.
**Statistikfeld**|**LKLST (JGSTUF) 	SB**
Datenfeld 	MAGELLAN:
Schüler > Zugang/Abgang > Bereits besuchte Schulen > Letzte Klassenstufe
[Klassenstufen]
Schüler > Zugang/Abgang > Herkunftsschule
Beschreibung 	Geben Sie für den Schüler die zuletzt besuchte Schule ein und wählen Sie diese im Feld „Herkunftsschule“ aus.
Beachten Sie bitte, dass die „Schulform“ eingetragen sein muss.
Statistikfeld 	AABS 	SB, EB
Datenfeld 	MAGELLAN: Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss
[Abschlüsse (Extern)]
Beschreibung 	Geben Sie hier den höchsten erreichten Abschluss an einer ABS ein.
Statistikfeld 	LABS 	SB, EB
Datenfeld 	MAGELLAN: Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss
[Abschlüsse (Extern)]
Beschreibung 	Geben Sie hier den höchsten erreichten berufsbezogenen Abschluss ein.
Statistikfeld 	WIEDH 	SB
Datenfeld 	MAGELLAN: Schüler > Laufbahn > Allgemein > Wiederholer
Beschreibung 	Haken Sie das Feld „Wiederholer“ an, wenn der Schüler ein Wiederholer ist.Der statistische Wert wird automatisch berechnet.
Statistikfeld 	ZUSKURS (ZUSKURS) 	SB, EB
Datenfeld 	MAGELLAN: Schüler > Statistik > Merkmal S2
[Schülermerkmale (Bereich S2)]
Beschreibung 	Geben Sie an, ob der Schüler Zusatzkurse für weitere Abschlüsse absolviert.
Statistikfeld 	BFKLBS 	SB, EB
Datenfeld 	MAGELLAN: Klasse > Merkmale > Merkmal S3
[Klassenmerkmale (Bereich S3)]
Schueler > Statistik > Merkmal S3
[Schülermerkmale (Bereich S3)]
Beschreibung 	Geben Sie an, ob sich der Schüler oder alle/viele Schüler der Klasse in einer Bezirksfach- oder Landesklasse befinden.Die Angabe beim Schülermerkmal hat vorrang zur Angabe des Klassenmerkmals, wenn beide eingetragen wurden.
Statistikfeld 	ENTL 	EA
Datenfeld 	MAGELLAN: Schüler > Statistik > Merkmal S4
[Schülermerkmale (Bereich S4)]
Beschreibung 	Tragen Sie hier bitte für Abgänger ein, ob der Schüler das allgemeinbildende Schulsystem verlässt oder nicht.Achtung:Wenn der Schüler in einer Klasse < Jahrgang 9 ist, geben wir automatisch den Wert für „Ja, Schüler verbleibt im allgemeinbildenden Schulsystem“ aus.
Statistikfeld 	ABSCHL (ABSCHL) 	EA, EB
Datenfeld 	MAGELLAN: Schüler > Laufbahn > Abschluss > Abschluss 1
[Abschlüsse (Intern)]
Beschreibung 	Der Statistikwert errechnet sich anhand des Eintrags im Feld „Abschluss 1“ aus dem vorangegangenen Schuljahr.Hinweis: Für alle Abgänger (inaktive Schüler mit Abgangsdatum zwischen dem aktuellen und dem vergangenen Statistiktermin unter Zugang/Abgang > AbgangAm), die noch nicht die Schulpflicht erfüllt haben, wird automatisch der Schlüssel für „ohne Abschluss“ in die Statistikdatei übernommen.Schulbesuchsjahre werden am aktuellen Datum und dem Grundschuleintritt errechnet.
Statistikfeld 	ABSCHLBS (ABSCHLBS) 	EB
Datenfeld 	MAGELLAN: Schüler > Laufbahn > Abschluss 2 > Abschlussart
[Abschlussarten]
Beschreibung 	Geben Sie hier den Erfolg des Bildungsgangs ein.
Statistikfeld 	ABINOTE 	EA,EB
Datenfeld 	MAGELLAN: Schüler > Abschluss > Abschluss 1 > Abschlussnote
Beschreibung 	Geben Sie bei bestandenem Abitur hier die Abiturnote mit genau einer Nachkommastelle ein. Nutzer des Abiturmoduls müssen hier keinen Eintrag machen, wenn im Abiturmodul eine Abiturnote vorhanden ist.
Statistikfeld 	INSG 	FB
Datenfeld 	-
Beschreibung 	Anzahl der Schüler bestimmter Fächer, siehe UART.Statistikwert wird berechnet.
Statistikfeld 	WEIBL 	FB
Datenfeld 	-
Beschreibung 	Anzahl der weiblichen Schüler bestimmter Fächer, siehe UART.Statistikwert wird berechnet.
Statistikfeld 	PROFIL 	OB
Datenfeld 	MAGELLAN: Schueler > Daten 3 > ProfilSchueler > Zeugnis > Faecher > Unterrichtsart
Beschreibung 	Tragen Sie das Profil des Schülers ein.Anhand der Eingabe und des gewählten 3. Prüfungsfach berechnet sich beim entsprechenden Fach der Profilschlüssel.
Statistikfeld 	SCHINSG 	OB
Datenfeld 	-
Beschreibung 	Anzahl der Schüler (pro Kurs).Statistikwert wird berechnet.
Statistikfeld 	SCHWEIBL 	OB
Datenfeld 	-
Beschreibung 	Anzahl der weiblichen Schüler (pro Kurs).Statistikwert wird berechnet.
Statistikfeld 	SCHANDS 	FB,OB
Datenfeld 	MAGELLAN: Schüler > Statistik > Merkmal T3
Beschreibung 	Geben Sie im Feld „Merkmal T3“ ein „J“ ein, wenn der Schüler einer anderen Schule den Unterricht besucht.Es wird die Anzahl der Schüler (pro Kurs), die von einer anderen Schule kommen automatisch berechnet.
Statistikfeld 	SCHSTD 	SB
Datenfeld 	-
Beschreibung 	Anzahl der Wochen-Ist-Stunden (pro Schüler) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird.Statistikwert wird berechnet.
Statistikfeld 	WOSTD 	OB
Datenfeld 	-
Beschreibung 	Anzahl der Wochen-Ist-Stunden (pro Kurs) ergibt sich aus der Unterrichtstafel, die von DAVINCI zur Verfügung gestellt wird.
Statistikwert wird berechnet.
Statistikfeld 	BERUF (BERUF) 	SB, EB
Datenfeld 	MAGELLAN: Schüler > Ausbildung > Beruf
[Berufe]
Beschreibung 	Geben Sie hier den Ausbildungsberuf des Schülers ein.
Statistikfeld 	UMSCH 	SB
Datenfeld 	MAGELLAN: Schüler > Daten 2 > Umschulung > Umschulung
[Umschulungsmerkmale]
Beschreibung 	Bitte erfassen Sie, ob der Schüler ein Umschüler ist.
Statistikfeld 	ABSKREIS 	SB
Datenfeld 	MAGELLAN: Schüler > Daten 1 > Gemeinde
Beschreibung 	Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein.Der Statistikwert wird automatisch daraus errechnet.
Statistikfeld 	ABSLAND 	SB
Datenfeld 	MAGELLAN: Schüler > Daten 1 > Gemeinde
Beschreibung 	Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein.Der Statistikwert wird automatisch daraus errechnet.

