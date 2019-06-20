# Sachsen SaxSVS

Dieses Kapitel beschreibt für Berufsbildenden Schulen in Sachsen die benötigten Schritte zum Erstellen einer Datei, die in SaxSVS eingelesen werden kann.
Die Schnittstelle zum Erstellen der Datei wird erst mit Version 7 zur Verfügung stehen, aber die notwendigen Daten (Schlüsselverzeichnisimporte, Eingaben in MAGELLAN 6) können bereits in der laufenden Version vorbereitend vorgenommen werden. In Version 7 werden weitere statistikrelevante Felder zur Verfügung stehen.

!!! info "Hinweis"

	Zum Erstellen der Statistikdateien benötigen Sie eine Lizenz für das Modul MAGELLAN Landesstatistik 2018 und mindestens die MAGELLAN Version 7! In Version 6 können aber auch ohne die Statistiklizenz Daten als Vorbereitung eingepflegt werden.

## Notwendige Schritte

1. Schritt:  [Schlüsselverzeichnisse importieren](https://doc.ls.stueber.de/schluesselverzeichnisse/schlusselverzeichnisse/) 
2. Schritt: Statistisch relevante Daten in MAGELLAN eingeben
3. Schritt: Statistikdaten erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

Das Statistikamt gibt jährlich aktualisierte Schlüssel für die Landesstatistik heraus. Mit der Ausgabe 6.5.20 von MAGELLAN wurde ein neuer Satz Importdateien für Schlüsselverzeichnisse hinterlegt, die Sie bitte nach MAGELLAN importieren.
Eine Anleitung zum Import finden Sie im Abschnitt [Schlüsselverzeichnisse](https://doc.ls.stueber.de/schluesselverzeichnisse/schlusselverzeichnisse/).



Verzeichnisname|Anmerkung
--|--
BS_Organisationen.keys|relevant für SaxSVS
BS_Schulformen.keys|relevant für SaxSVS
BS_SopaedFoerderungen.keys|relevant für SaxSVS
00_Fachstati.keys|-
00_Faecher.keys|-
00_FoerderSchwerpunkte.keys|relevant für SaxSVS
00_Klassenstufen.keys|-
00_Konfessionen.keys|-
00_Noten.keys|-
00_SchuelerMerkmale.keys|relevant für SaxSVS
00_Sprachreferenzen.keys|-
00_Staatsangehoerigkeiten.keys|relevant für SaxSVS
00_Unterrichtsarten.keys|-
AS_Schulformen.keys|-
BS_Bildungsgaenge.keys|relevant für SaxSVS

## Voraussetzungen

Die Exportdatei kann erst mit der Version 7 von MAGELLAN erzeugt werden. Die Daten Ihrer Schuldatenbank werden beim Umstieg auf die neue Version in eine neue Datenbank übertragen. Insofern können Sie die Eintragungen bereits in der aktuellen Version vornehmen, eine Ausnahme sind die Eintragungen in der Gruppe `Sonderpädagogischer Förderbedarf und Beeinträchtigungen`.

> #### danger::Achtung!
>
> Es können nur Schüler in die Statistik übernommen werden, die eine Ausbildung beim Schüler eingetragen haben. Dies liegt daran, dass SaxSVS eine eindeutige GUID für einen Bildungsgang des Schülers einfordert.
> Damit hängt die Eindeutigkeit eines Datensatzes in SAXSVS an der Verbindung zwischen Schüler und Bildungsgang. In MAGELLAN ist der Bildungsgang nur mit einem Ausbildungsdatensatz zu haben. 

Prüfen Sie bitte, ob alle Ihre Schüler unter `Schüler > Ausbildung` einen Eintrag mit mindestens dem Bildungsgang des Schülers haben! Der Eintrag nur bei der Klasse genügt nicht. Ihnen steht aber eine Sammelzuweisung zur Verfügung, mit deren Hilfe Sie für Gruppen von Schülern einen Bildungsgang hinterlegen können. Sie finden den Aufruf in MAGELLAN 6 unter `Schüler > Bearbeiten > Sammelzuweisung` oder in MAGELLAN 7 unter `Schüler > Schüler > Sammelzuweisung`. Wir empfehlen diese Eintragung in MAGELLAN 6 vorzunehmen, da kein Rückabgleich möglich von 7 zu 6 ist!

### Förderbedarf in MAGELLAN 6 und MAGELLAN 7

In MAGELLAN 6 kann für die Felder `Förderbedarf`, `Schwerpunkt1`,`Schwerpunkt2` und `Behinderung` jeweils nur ein Wert pro Schüler erfasst werden. Diese Einzelwerte werden bei der Übernahme der Daten aus Ihrer MAGELLAN 6-Datenbank in eine MAGELLAN 7-Datenbank als eine Zeile (mit den einzelnen Angaben) einer Liste dargestellt. Sie haben damit die Möglichkeit ab MAGELLAN 7 mehrere Bedarfe (mehrere Zeilen in einer Liste) im Programm zu erfassen.

![Schüler > Daten4](/sachsen/foerderungen.png)


### Exportformat SaxSVS
Die Schnittstelle exportiert eine Datei im XML-Format. Dies bedeutet Sie erhalten eine strukturierte Textdatei nach vorgegebenem Format. 
Allgemeine Informationen zum grundsätzlichen Verständnis von XML-Dateien finden Sie auf z.B. auf [Wikipedia](https://de.wikipedia.org/wiki/Extensible_Markup_Language).

Hier ein kleiner Ausschnitt aus der SaxSVS-Schnittstelle:

```xml
<saxsvs-bbs xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.2.xsd" zeit="TDateTime Today (2001-12-17T09:30:47-05:00)" schuljahr="Zeitraeume.Ausdruck2 (2017/2018)" dienststelle="Mandanten.Schulnummer">
	<schueler extern_id="Schueler.ID">
		<an_vname>Schueler.Vorname</an_vname>
		<an_name>Schueler.Nachname</an_name>
		<an_gebdat>Schueler.Geburtsdatum (YYYY-MM-DD)</an_gebdat>
		<an_gebort>x</an_gebort>
		<an_geschlecht schluessel="K101" extern_id="1">männl.</an_geschlecht>
		<al_kennziffer>SchuelerAusbildung.Bildungsgang</al_kennziffer>
		<al_schulart schluessel="S0502" extern_id="110">BS/BS</al_schulart>
		<al_status schluessel="S1920" extern_id="1">Auszubildender/Schüler</al_status>
		<al_zeitform schluessel="S1832" extern_id="1">v</al_zeitform>
		<al_abschl_dat>Schueler.VoraussichtlichesEnde (2016-01-01)</al_abschl_dat>
		<al_laufb_kl>SchuelerLaufbahn.Klasse (BK19A)</al_laufb_kl>
	</schueler>
</saxsvs-bbs>
```

#### XML-Dateien prüfen
Ein Vorteil von XML-Dateien ist, dass diese über eine weitere Datei, genannt Schemadatei (Dateiformat .XSD) geprüft werden kann. Das Schema gibt vor, wie eine XML-Datei auszusehen hat und z.B. welche Werte grundsätzlich erlaubt sind.
Die Schemadatei für die SAXSVS-Schnittstelle finden Sie [hier](https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.2.xsd).
Um die fertige XML-Datei mit der Schemadatei prüfen zu können, benötigen Sie ein entsprechende Programm, z.B. XML-Spy oder ähnliches. Es gibt auch Online-Prüfungen, 
in denen Sie den Text der XML-Datei kopieren können und den Link zur Prüfdatei im Netz angeben (**Achten Sie auf den Datenschutz bei Prüfungen im Internet**).
Die Prüfungen geben üblicherweise recht gute Fehlerbeschreibungen aus, wenn etwas in der XML-Datei nicht stimmt. 
STÜBER SYSTEMS hat auch eine einfache automatische Prüfung eingebaut, die über den MSXML-Parser angeboten wird. Die Ausgaben der Fehlerbeschreibungen sind allerdings von Hause aus etwas kryptisch und können nur einen Anhaltspunkt geben.


### Einträge in MAGELLAN

Nachstehend finden Sie eine Auflistung der relevanten Felder und der jeweiligen Stelle, an der Sie in MAGELLAN eingepflegt werden.
Ggf. haben wir nach XML-Elementen aufgeteilt.


#### Kopfbereich ( saxsvs-bbs )
```xml
<saxsvs-bbs xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xsi:noNamespaceSchemaLocation="https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.2.xsd" 
  zeit="TDateTime Today (2001-12-17T09:30:47-05:00)" 
  schuljahr="Zeitraeume.Ausdruck2 (2017/2018)" 
  dienststelle="Mandanten.Schulnummer">
```

Titel|Inhalt
---|---
**Statistikfeld**| **... > saxsvs-bbs > zeit **
Beschreibung| Für dieses Feld wird automatisch ein aktueller Datums-/Zeitstempel eingefügt.
**Statistikfeld**| **... > saxsvs-bbs > schuljahr** 
Beschreibung|`MAGELLAN > Verzeichnisse > Zeitraeume > Ausdruck 1`<br/> Tragen Sie das Schuljahr im Format **JJJJ/JJJJ** ein, als Beispiel: 2017/2018
**Statistikfeld**| **... > saxsvs-bbs > dienststelle** 
Beschreibung|`MAGELLAN > Schulnummer` 


#### Schüler ( saxsvs-bbs > schueler )


Titel|Inhalt
---|---
**Statistikfeld**| ** saxsvs-bbs > schueler > extern_id** 
Beschreibung|`Schüler > Ausbildung > GUID`  <br/><br/>  1. Lesen Sie den Abschnitt "Voraussetzungen".<br/>  2. Wenn Sie zuvor MAGELLAN 6 genutzt haben und zum ersten mal in MAGELLAN 7 den Export durchlaufen, dann existieren noch keine GUIDs. Diese werden dann für bestehende aktuelle Ausbildungen angelegt und in der Datenbank gespeichert.<br/>  3. Schüler ohne eine aktuelle Ausbildung im ausgewählten Exportzeitraum werden <b>nicht berücksichtigt</b>. 
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_vname** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Vorname`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_name** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Nachname`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_gebname**
Beschreibung|  `MAGELLAN > Schüler > Daten 1 > Geburtsname`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_gebdat**
Beschreibung|  `MAGELLAN > Schüler > Daten 1 > Geburtsdatum`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_gebort**
Beschreibung|  `MAGELLAN > Schüler > Daten 1 > Geburtsort`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_geschlecht > schluessel** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Geschlecht`<br/> Notwendiger Eintrag wird aus der Eingabe berechnet.
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_geschlecht > extern_id** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Geschlecht`<br/> Notwendiger Eintrag wird aus der Eingabe berechnet.
**Statistikfeld**| **... > saxsvs-bbs > schueler > migration > an_migr_grund** 
Beschreibung| `MAGELLAN > Schüler > Daten 2 > Ndh`<br/> Wenn Migrationshintergrund besteht den Haken bitte aktivieren.
**Statistikfeld**| **... > saxsvs-bbs > schueler > migration > an_migr_dat** 
Beschreibung| `MAGELLAN > Schüler > Statistik > MerkmalU2`
**Statistikfeld**| **... > saxsvs-bbs > schueler > migration > an_migr_daz** 
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Maßnahme/Bedarf` <br/> Mehrere Einträge ab Magellan 7: Liste der Förderungen, eine davon muss den Wert DAZ-3 haben. <br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_kennziffer** 
Beschreibung| `MAGELLAN > Klassen > Daten > Schulform [BS_Schulformen]`<br/>`MAGELLAN > Schüler > Ausbildung > Bildungsgang [BS_Bildungsgaenge]`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_schulart** 
Beschreibung| `MAGELLAN > Klassen > Daten > Bildungsgang [BS_Bildungsgaenge]`<br/>`MAGELLAN > Schüler > Ausbildung > Bildungsgang [BS_Bildungsgaenge]`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_status** 
Beschreibung| `MAGELLAN > Schüler > Statistik > Merkmal S1 [BS_SchuelerMerkmale]`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_zeitform** 
Beschreibung| `MAGELLAN > Klassen > Daten > Organisation [BS_Organisationen]`<br/>`MAGELLAN > Schüler > Ausbildung > Organisation[BS_Organisationen]`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_abschl_dat** 
Beschreibung| `MAGELLAN > Schüler > Zugang / Abgang > Voraus. Ende`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_laufb_kl** 
Beschreibung| `MAGELLAN > Schüler > Auswahl > Klasse`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderungen > af_int > schluessel** 
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Maßnahme/Bedarf [BS_SopaedFoerderungen]`<br/> <br/> Mehrere Einträge ab Magellan 7: Liste der Förderungen <br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderungen > af_int > extern_id** 
Beschreibung| `Wert (S1060) wird von MAGELLAN automatisch eingetragen.`<br/> <br/> Mehrere Einträge ab Magellan 7: Liste der Förderungen <br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_von**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Von`<br/> <br/>  Mehrere Einträge ab Magellan 7: Liste der Förderungen <br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_bis**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Bis`<br/> <br/>  Mehrere Einträge ab Magellan 7:<br/> Liste der Förderungen<br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_rs_std**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Stunden 1`<br/> <br/>  Mehrere Einträge ab Magellan 7: Liste der Förderungen<br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_fs_std**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Stunden 2`<br/> <br/>  Mehrere Einträge ab Magellan 7: Liste der Förderungen <br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_foerdersw > schluessel**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Förderschwerpunkt 1`<br/> <br/> Mehrere Einträge ab Magellan 7: Liste der Förderungen<br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_foerdersw > extern_id**
Beschreibung| `Wert (S1075) wird von MAGELLAN automatisch eingetragen.`<br/> <br/>  Mehrere Einträge ab Magellan 7:Liste der Förderungen <br/>Bitte lesen Sie den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.ls.stueber.de/sachsen/sachsen/#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)


## Statistikdaten erstellen

Für die Erstellung der Exportdatei rufen Sie bitte aus dem Menü `Schüler` den Reiter `Importe/Exporte` auf und wählen den Unterpunkt `Export`. Es startet der Exportassistent, bitte wählen Sie die Schnittstelle `SAX-SVS (BBS)` und fügen über das Plus die gewünschten Exportzeiträume hinzu. Klicken Sie auf `Weiter`!

![Wählen Sie die Schnittstelle und die Zeiträume aus!](/sachsen/export.saxsvs.png)


Auf der Folgekarte wählen Sie bei der `Art der Erstellung` bitte aus, ob Sie nur `Daten prüfen`, `nur Exportdaten erstellen` oder beides wünschen.

![Wählen Sie die Art der Erstellung aus!](/sachsen/pruefen.png)

Wählen Sie einen Speicherort und klicken auf `Weiter`!

![Bitte wählen Sie einen Speicherort!](/sachsen/speicherort.png)

Starten Sie die Erstellung der Exportdatei oder die Prüfung per Klick auf `Fertigstellen`!

![Starten Sie die Erstellung!](/sachsen/fertig.png)





