# Mecklenburg-Vorpommern - SIP

Das Schulberichtssystem (SBS) wurde durch das Schulinformations- und Planungssystem M-V (SIP) am 03.01.2013 abgelöst. Somit erfolgt für allgemein bildende und berufliche Schulen die Datenerhebung in einem System. STÜBER SYSTEMS bietet Ihnen die Möglichkeit, Daten für die SIP-Schnittstelle mit Magellan zu exportieren. 

## Einführung

Das Kultusministerium fordert die elektronische Erfassung im XML-Dateiformat. Die Schuldaten können in diesem Format aus Magellan heraus erzeugt werden. Das XML-Dateiformat ist eine Auszeichnungssprache zur Darstellung hierarchisch strukturierter Daten in Form von Textdateien.

Durch die Hierarchie können explizit Daten für Allgemeinbildende und Berufsbildende Schulen getrennt werden und es ist somit nicht erforderlich unterschiedliche Dateien für die jeweiligen Schulformen zu erzeugen. 

Für Sie als Schule bedeutet dies: Sie müssen die folgende XML-Datei über das Webportal https://portal.schule-mv.de übertragen:

xxxxx_[DATUM].xml 
Hierbei steht xxxxx für Ihre Schulnummer und [DATUM] für das aktuelle Datum.


!!! info "Hinweis"

  Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

### Notwendige Schritte


1. Schritt:[Schlüsselverzeichnisse importieren](../schluesselverzeichnisse.md) 
2. Schritt: Statistisch relevante Daten in daVinci bzw. Magellan eingeben
3. Schritt: Kurswahlen von daVinci nach Magellan übertragen \(nur für Gymnasien\/Gesamtschulen mit Oberstufe\)
4. Schritt: Statistikdaten aus daVinci exportieren
5. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
6. Schritt: Statistikdaten erstellen.    

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

Das Statistikamt gibt jährlich aktualisierte Schlüssel für die Landesstatistik heraus. Die aktuellen Schlüssel des Statistikamtes finden Sie auf der gemeinsamen Veröffentlichungsplattform von Schulaufsicht und amtlicher Statistik \(www.egsch.bildung-rp.de\).
Eine Anleitung zum Import finden Sie im Abschnitt [Schlüsselverzeichnisse](../schluesselverzeichnisse.md).

## Statistisch relevante Daten eingeben

Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang, in einer tabellarischen Übersicht. 

## Statistikdaten erstellen

Die Erstellung der Statistikdateien werden zuerst alle erforderlichen Daten aus Magellan ausgelesen, dann wird eine Datenprüfung vorgenommen und danach die Daten in die XML-Datei gespeichert. 

>Das Einlesen der Daten aus Magellan erfolgt bei jeder Art der Erstellung ohne Berücksichtigung der zu erstellenden Statistikdatei.

Diese Prüfung ist eine Plausibilitätsprüfung, die beim Erstellen des Exports die zu exportierenden Werte mit den erwarteten Werten der SIP-Statistikschlüssel vergleicht und Ihnen Rückmeldung in Form von Hinweisen gibt, wenn ein Exportwert nicht mit einem Wert im Bereich der erwarteten Schlüssel passt.

## Datenprüfung und Export starten


1.	Starten Sie MAGELLAN.
1.	Klicken Sie im Menü ```Extras``` auf ```Export > SIP…```
2.	Es wird das in MAGELLAN aktuell eingestellte Schulhalbjahr als Erhebungszeitraum voreingetragen. Wenn vorhanden, wählen Sie das davorliegende Schulhalbjahr aus, damit ggf. aufgetretene Änderungen korrekt erfasst werden können.
3.	Wählen Sie die Schulform Ihrer Schule, Allgemeinbildende Schule (ABS) oder Berufsbildende Schulen (BBS) aus. Dies ist wichtig für die korrekte Ausgabe und Prüfung Ihrer Daten.
4.	Das ```Gültig ab``` und ```Gültig bis``` Datum werden durch den ausgewählten Erhebungszeitraum vorberechnet und können entsprechend verändert werden, um die Gültigkeit Ihrer Daten anzupassen.
5.	Geben Sie im Feld Exportordner den Dateipfad in dem die Exportdatei abgelegt werden soll. Klicken Sie dann auf ```Weiter```.
6.	Auf der nächsten Seite erhalten Sie noch einmal eine Übersicht zum Datenexport. Klicken Sie auf ```Weiter```.
7.	Klicken Sie auf ```Start```, um die Datenprüfung und Export der Daten zu starten.
 

!!! info "Hinweis"

  Sie können nur bedingt Daten aus der Vergangenheit für SIP exportieren, aus diesem Grunde werden Ihnen nur das aktuelle Schuljahr und das vorangegangene Schuljahr zur Auswahl gestellt.

## Ergebnis der Datenprüfung auswerten 

Die Ergebnisse der Datenprüfung werden unter Hinweise aufgelistet. Sind dort keine Hinweise enthalten, sind die Daten für die Abgabe an das Statistikamt korrekt eingegeben. Die Hinweise werden unterschieden nach Art der Datei, dem betroffenen Datensatz, Kontroll-Nr der Plausibilität und dem eigentlichen Meldungstext. Sie können die Hinweise gruppieren und/oder Filtern und über die Schaltfläche ```Export nach Excel``` nach Excel exportieren.
Sie müssen nun die Meldungen in MAGELLAN bearbeiten und dann erneut eine Datenprüfung durchführen.


!!! info "Hinweis"

  Viele in der Prüfung abgefragte Werte werden nicht in den Statistikdateien ausgegeben, dienen aber als Voraussetzung für die Plausibilitätsprüfungen. Beispiel: Zur Prüfung von  korrekten Fremdsprachen bei allgemeinbildenden Schulen muss die Schulart angegeben sein. Wurde diese nicht oder fehlerhaft angegeben, gibt die Prüfung eine Fehlermeldung aufgrund dieser Bedingung aus.

## Fremdsprachen


!!! info "Hinweis"

  Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).


In der Übergabe der Daten für die SIP-Schnittstelle wird das Feld FremdSpracheArtID aus kombinierten Einträgen aus den Feldern Schüler|Daten3|Fremdsprachen|Status und Zusatz berechnet. Nachfolgend finden Sie die Übersicht der möglichen Eintragungen:

<table class="table">
<caption></caption>
<thead>
<tr>
<th style="background-color:#CEE3F6;">Status in Magellan </th>
<th style="background-color:#CEE3F6;">Zusatz in Magellan</th>
<th style="background-color:#CEE3F6;">Berechneter Wert für die SIP-Übergabe</th>
    </tr>
 </thead>
<tbody>
<tr>
    <td align=left style="background-color:#FFFFFF;">Ergänzend</td>
    <td align=left style="background-color:#FFFFFF;">Muttersprachl. Unterricht</td>
    <td align=left style="background-color:#FFFFFF;">muttersprachl. Unterricht als Ergänzungsunterricht</td>
    </tr>
    <tr>
    <td align=left style="background-color:#F0F8FF;">Leer</td>
    <td align=left style="background-color:#F0F8FF;">Muttersprachl. Unterricht</td>
    <td align=left style="background-color:#F0F8FF;">muttersprachl. Unterricht als Fremdsprache</td>
    </tr>
    <tr>
    <td align=left style="background-color:#FFFFFF;">Leer</td>
    <td align=left style="background-color:#FFFFFF;">Neigungsunterricht</td>
    <td align=left style="background-color:#FFFFFF;">Neigungsunterricht</td>
    </tr>
<tr>
    <td align=left style="background-color:#F0F8FF;">Leer</td>
    <td align=left style="background-color:#F0F8FF;">Pflichtfach</td>
    <td align=left style="background-color:#F0F8FF;">Pflichtfach</td>
    </tr>
    <tr>
    <td align=left style="background-color:#FFFFFF;">Leer</td>
    <td align=left style="background-color:#FFFFFF;">Wahlpflichtfach</td>
    <td align=left style="background-color:#FFFFFF;">Wahlpflichtfach</td>
    </tr>
    <td align=left style="background-color:#F0F8FF;">Leer</td>
    <td align=left style="background-color:#F0F8FF;">Basiskurs</td>
    <td align=left style="background-color:#F0F8FF;">Basiskurs</td>
    </tr>
    <tr>
    <td align=left style="background-color:#FFFFFF;">Leer</td>
    <td align=left style="background-color:#FFFFFF;">Erweiterungskurs</td>
    <td align=left style="background-color:#FFFFFF;">Erweiterungskurs</td>
    </tr>
<tr>
    <td align=left style="background-color:#F0F8FF;">Leer</td>
    <td align=left style="background-color:#F0F8FF;">Gymnasialkurs</td>
    <td align=left style="background-color:#F0F8FF;">Gymnasialkurs Sek I (IGS)</td>
    </tr>
    <tr>
    <td align=left style="background-color:#FFFFFF;">Fach</td>
    <td align=left style="background-color:#FFFFFF;">Wahlpflichtfach</td>
    <td align=left style="background-color:#FFFFFF;">Fach als Wahlpflichtfach</td>
    </tr>
<tr>
    <td align=left style="background-color:#F0F8FF;">Hauptfach</td>
    <td align=left style="background-color:#F0F8FF;">Pflichtfach</td>
    <td align=left style="background-color:#F0F8FF;">Hauptfach als Pflichtfach</td>
    </tr>
    <tr>
    <td align=left style="background-color:#FFFFFF;">Hauptfach</td>
    <td align=left style="background-color:#FFFFFF;">Wahlpflichtfach</td>
    <td align=left style="background-color:#FFFFFF;">Hauptfach als Wahlpflichtfach</td>
    </tr>
<tr>
    <td align=left style="background-color:#F0F8FF;">Fach</td>
    <td align=left style="background-color:#F0F8FF;">Wahlfach (fakultative FS)</td>
    <td align=left style="background-color:#F0F8FF;">Fach als Wahlfach</td>
    </tr>
 <tr>
    <td align=left style="background-color:#FFFFFF;">Hauptfach</td>
    <td align=left style="background-color:#FFFFFF;">Wahlfach (fakultative FS)</td>
    <td align=left style="background-color:#FFFFFF;">Hauptfach als Wahlfach</td>
    </tr>
    <tr>
    <td align=left style="background-color:#F0F8FF;">Leer</td>
    <td align=left style="background-color:#F0F8FF;">Förderunterricht</td>
    <td align=left style="background-color:#F0F8FF;">abgewählt</td>
    </tr>
  </tbody>
</table>

## Besonderheiten Statistik


!!! info "Hinweis"

  Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

### Besonderheiten Statistik 2014/2015

## Kopfdaten der Statistikdatei



<table class="table">
<caption></caption>
<thead>
<tr>
<th colspan=2 style="background-color:#FFFFFF;">Kopfdaten der Statistikdatei</th>
    </tr>
 </thead>
<tbody>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>KopfId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wert wird fest eingetragen.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Version</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Das Erhebungsjahr wird automatisch beim Erstellen der Statistikdateien mit eingetragen und muss nicht in Magellan eingegeben werden.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>ExportSystem</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>      SIP   </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wert wird fest eingetragen.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Umfang</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wert wird fest eingetragen. Aktuell wird nur eine Gesamtdatenlieferung unterstützt</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>ErstelltAm</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>-</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Das Datum, an dem die Statistikdatei erzeugt wurde. Wert wird automatisch beim Erstellen der Statistikdatei eingetragen.</td>
    </td>
  </tr>
</tbody>
</table>


## Schuldaten



!!! info "Hinweis"

  Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).


<table class="table">
<caption></caption>
<thead>
<tr>
<th colspan=2 style="background-color:#FFFFFF;">Schuldaten</th>
    </tr>
 </thead>
<tbody>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>SchuleId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Mandanten > Daten 1 >   Schulnummer</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier die Schulnummer Ihrer Schule ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Kontakt > EMail</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:   Mandanten > Daten 1 >   Email</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier die E-Mail-Adresse Ihrer Schule ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Kontakt > Internet</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:   Mandanten > Daten 1 >   Internet</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier die Internetadresse Ihrer Schule ein.</td>
    </td>
  </tr>
 <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Kontakt > Telefon</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Mandanten > Daten 1 >  Telefon</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier die Telefonnummer Ihrer Schule ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > SchulArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:   Klassen > Daten 1 >  Schulart   [Schularten]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier die Schulart der Klasse aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > Klasse > KlassenId  </th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Klassen > ID</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Es wird automatisch die ID der Klasse mit dem Prefix ‚F‘ eingetragen. Dies führt dazu, dass die Klasse im SIP-System neu eingelesen wird. Es werden alle Klassen berücksichtigt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > Klasse > Bezeichnung</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Klassen > Kuerzel</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Es wird automatisch das Kürzel der Klasse eingetragen.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > Klasse > GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > Klasse > GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > SchulTeil > Klasse > JahrgangsStufe > JahrgangsStufeId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Magellan:  Klassen > Klassenstufe   [Klassenstufen]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Klassenstufe der Klasse aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > FachId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > FachErweiterungId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
   <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > BilingualId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > WochenStd</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > DauerStd</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
      <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeSchulArt >  SchulartId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeSchulArt >  GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeSchulArt >  GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeJahrgangsStufe >  JahrgangsStufe</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeJahrgangsStufe >  GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeJahrgangsStufe >  GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeArt > UeArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeArt > GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
      <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Ue > UeArt > GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>|Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
</tbody>
</table>


## Schülerdaten


>Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).


<table class="table">
<caption></caption>
<thead>
<tr>
<th colspan=2 style="background-color:#FFFFFF;">Schülerdaten</th>
    </tr>
 </thead>
<tbody>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schüler > ID</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Es wird automatisch die ID des Schülers mit dem Präfix ‚F‘ eingetragen. Dies führt dazu, dass der Schüler im SIP-System neu eingelesen wird. Es werden alle eingeschulten Schüler berücksichtigt, sowie ausgeschulten, dessen Abgang im statistisch relevanten Zeitraum liegt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > GeschlechtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:Schüler > Daten 1 >   Geschlecht</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier das Geschlecht des Schülers aus.   Der statistische Wert wird intern berechnet.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler >    StaatsangehoerigkeitId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Schüler > Daten 2 > Staatsangehörigkeit >   Staatsangeh. 1   [Staatsangehoerigkeiten]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier die 1. Staatsangehörigkeit des Schülers aus. </td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Staatsangehoerigkeit2Id|</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:Schüler > Daten 2 > Staatsangehörigkeit > Staatsangeh. 2[Staatsangehoerigkeiten]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier die 2. Staatsangehörigkeit des Schülers aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > VerkehrsSpracheId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:Schüler > Daten 2 > Staatsangehörigkeit >Verkehrssprache [Muttersprachen]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier Verkehrssprache des Schülers aus. </td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Vorname</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schüler > Daten 1 > Vorname</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier den Vornamen des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Nachname</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schüler > Daten 1 > Nachname</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier den Nachnamen des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > GebDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schüler > Daten 1 > Geburtsdatum</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier das Geburtsdatum des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > GebLandId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schüler > Daten 1 > Geburtsland [Staatsangehoerigkeiten]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier das Geburtsland des Schülers aus.</td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > GebOrtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>      -   </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > GebOrtsteil</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>      -   </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > EinschulArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>      -   </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > EinschulArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Schüler > Zugang/Abgang > Zugang > Einschulung</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier die Art der Einschulung des Schülers aus. <br/>Berufsschulen müssen hier keine Eingabe machen, es wird immer der Wert -1 ausgespielt. <br/>Für Allgemeinbildende Schulen berechnet sich der statistische Wert intern, sobald eine Angabe gemacht wird. Anderenfalls wird der Wert -1 ausgespielt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>           </th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>         </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>  	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > EinschulDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Schüler > Daten 2 > Grundschuleintritt >   Grundschuleintritt</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier das Grundschul- Eintrittsdatum ein.     Wenn kein Wert angegeben wird, wird der Wert 01.01.1900 ausgespielt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > ZuzugsDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:          Schüler > Statistik >      Merkmal U1</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Falls der Schüler nach Mecklenburg-Vorpommern zugezogen ist, tragen Sie für den Schüler das Zuzugsdatum ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > WohnOrtPlz</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Schüler > Daten 1 >  Postleitzahl</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier die Postleitzahl zum Wohnort des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > WonOrtsteil</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:     Schüler > Daten 1 > Ort</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier den Wohnort des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > StrasseNr</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:      Schüler > Daten 1 > Strasse</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie hier die Strasse und Hausnummer zum Wohnort des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > AnAbmeldung</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
    <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Angabe</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
      <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Besonderheit</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
 <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Vorjahr >  BetaetigungVorjahrId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: <br/> Schüler > Zugang/Abgang >  Bereits besuchte Schule > Unterlagen <br/>Schüler > Zugang/Abgang >  Herkunftsschule  [Herkunftsunterlagen] </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie beim Schüler die Herkunftsschule aus.  <br/> Wählen Sie im Feld Unterlagen der Herkunftsschule vorangegangene Betätigung des Schülers aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Vorjahr >    JahrgangsStufeVorjahrId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: <br/>    Schüler > Zugang/Abgang >  Bereits besuchte Schule >  Letzte Klassenstufe <br/>Schüler > Zugang/Abgang >   Herkunftsschule  [Klassenstufen]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie beim Schüler die Herkunftsschule aus.  <br/> Wählen Sie aus dem Feld Letzte Klassenstufe aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>           </th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>         </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>  	</td>
    </td>
  </tr>
 <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Fremdsprache >      FremdspracheId  </th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:   Schüler > Daten 3 >   Fremdsprachenfolge >    1. Fremdsprache /2. Fremdsprache/3. Fremdsprache/4. Fremdsprache [Faecher]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie für den Schüler die 1. – 4. Fremdsprache aus. <br/>Für SIP werden soviele Daten ausgespielt, wie hier Fremdsprachen für den Schüler ausgewählt werden. Dies betrifft dann allem voran die folgenden Felder zur Fremdsprache.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Fremdsprache > FremdSpracheArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:Schüler > Daten 3 > Fremdsprachenfolge > Status/Zusatz</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie Status und Zusatz zur jeweiligen Fremdsprache des Schülers aus.  Der SIP-Schlüssel berechnet sich intern aus der Kombination beider Werte.   <br/>Die gültigen Kombinationsmöglichkeiten finden Sie im Abschnitt [Fremdsprachen](#Fremdsprachen).</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Fremdsprache > VonJahrgangsStufeId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schüler > Daten 3 > Fremdsprachenfolge > Von</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Jahrgangsstufe zur jeweiligen Fremdsprache des Schülers aus, seit dem die Fremdsprache gegeben wurde. Da das Amt SchlüsselIds als Werte verlangt, geben Sie bitte folgende Zahlen als Werte an:<br/><br/>2	=	Jahrgangsstufe 1     <br/>3	=	Jahrgangsstufe 2    <br/>4	=	Jahrgangsstufe 3    <br/>5	=	Jahrgangsstufe 4      <br/>6	=	Jahrgangsstufe 5      <br/>7 =	Jahrgangsstufe 6     <br/>8 =	Jahrgangsstufe 7     <br/>9	=	Jahrgangsstufe 8     <br/>10	=	Jahrgangsstufe 9   <br/>11	=	Jahrgangsstufe 10   <br/>12	=	Jahrgangsstufe 11    <br/>13	=	Jahrgangsstufe 12    <br/>14	=  Jahrgangsstufe 13   <br/>15	=	Unterstufe         <br/>16	=	Mittelstufe        <br/>17	=	Oberstufe           <br/>18	=	Abschlussstufe       <br/>19	=	Frühförderung       <br/>20	=	1.Jahr Berufliche Schule       <br/>21	=	2.Jahr Berufliche Schule       <br/>22	=	3.Jahr Berufliche Schule      <br/>23	=	4.Jahr Berufliche Schule       <br/>24	=	5.Jahr Berufliche Schule	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Fremdsprache >   BisJahrgangsStufeId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:Schüler > Daten 3 > Fremdsprachenfolge > Bis	</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Jahrgangsstufe zur jeweiligen Fremdsprache des Schülers aus, bis dem die Fremdsprache gegeben wird/wurde. Geben Sie bitte die Werte wie zuvor in VonJahrgangsStufeId angebeben an.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Fremdsprache > Reihenfolge</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Die Reihenfolge der Fremdsprache ergibt sich durch die Eingabe in Magellan und wird berechnet ausgespielt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > Foerderung	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.</td>
    </td>
  </tr>
 <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerKlasse > KlasseId	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Klassen > ID	</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Es wird automatisch die ID der Klasse mit dem Prefix ‚F‘ eingetragen. Dies führt dazu, dass die Klasse im SIP-System neu eingelesen wird. Hierbei handelt es sich um die Klasse des Schülers im aktuellen und, wenn vorhanden im vorherigen Zeitraum. Dies gilt auch für die weiteren Merkmale im Knoten SchuelerKlasse.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerKlasse > BildungsGangId	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: <br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildungsgang [Bildungsgaenge] </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie den Bildungsgang des Schülers aus. Grundsätzlich reicht hier der Bildungsgang der Klasse, wenn Schüler mit abweichenden Bildungsgängen eine Klasse besuchen, wählen Sie den abweichenden Bildungsgang  in der Ausbildung des jeweiligen Schülers aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerKlasse > FachRichtungId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: <br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildungsgang [Bildungsgaenge]<br/>Verzeichnisse > Bildungsgänge > Fachrichtung [Bildungsgaenge] [Fachrichtungen]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie den Bildungsgang des Schülers aus. Grundsätzlich reicht hier der Bildungsgang der Klasse, wenn Schüler mit abweichenden Bildungsgängen eine Klasse besuchen, wählen Sie den abweichenden Bildungsgang  in der Ausbildung des jeweiligen Schülers aus.<br/>Nur für BBS! <br/>Wählen Sie wie bereits beschrieben den Bildungsgang des Schülers aus. Wenn dieser Bildungsgang eine Fachrichtung eingetragen hat, wird diese ausgespielt. </td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerKlasse > JahrgangsStufeId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Klassen > Klassenstufe [Klassenstufen]	</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Klassenstufe der Klasse aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerKlasse > StatusId	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schueler > Status </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td> - 	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schueler > Laufbahn > Allgemein > Versetzt > Versetzungsart  [Versetzungsarten]	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Der Status des Schülers ergibt sich durch seinen Status (aktiv/inaktiv) und/oder seiner Versetzung und Versetzungsart. Entsprechend wird der auszuspielende Schlüssel berechnet. Dabei werden nicht alle möglichen Statusschlüssel unterstützt. Folgende Schlüssel werden unterstützt:<br/><br/>9	 Schüler (Status 3)  <br/>10 versetzt (Status 3/4; Versetzt)  <br/>11 aufgestiegen (Status 3;       Versetzt; Versetzungsart: 11)  <br/> 12 überspringt freiw. JgSt (  Status 3; Versetzt;  Versetzungsart: 12) <br/>13 nicht versetzt (Status 3;  Nicht Versetzt) <br/>14 tritt freiwillig zurück (Status 3;  Nicht Versetzt; Versetzungsart: 14) <br/>15 wechselt Klasse (Status 3; Versetzungsart: 15) <br/>16 Wegzug aus MV (Status 4;      Abgangsart: 16)            <br/>17 Absolvent verbleibt ABS  (Status 4; Abgangsart: 17)                     <br/>18 Absolvent verbleibt BLS (  Status 4; Abgangsart: 18)                      <br/>19 Absolvent verläßt ABS (Status 4; Abgangsart: 19)    <br/>20 Absolvent verläßt BLS       (Status 4; Abgangsart: 20)   <br/>21 Abgänger (Status 4;  Abgangsart: 21)  <br/>22 Abbrecher (Status 4;      Abgangsart: 22) <br/>23 verstorben (Status 4;   Abgangsart: 23)   <br/>24 wechselt Schule (Status 4;   Abgangsart: 24) <br/>26 abgeordnet (Status 4;      Abgangsart: 26)   <br/><br/>Folgende Schlüssel werden nicht unterstützt:   <br/>4 angemeldet (Bewerber)  <br/>5 zurückgezogen (Bewerber) <br/>6 angenommen (Bewerber)               <br/>7 abgelehnt (Bewerber)<br/>8 zurückgestellt (Bewerber)</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchuelerKlasse > GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>  -       </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler >  SchuelerKlasse > GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>    -     </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>  Schule > Schueler > SchuelerUe >   UeId	<br/>
Schule > Schueler > SchuelerUe >  UeArtId	<br/>
Schule > Schueler > SchuelerUe >   GueltigAb<br/>	
Schule > Schueler > SchuelerUe >   GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Merkmal wird nicht unterstützt.	</td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchulischeVorbildungAllgemeinbildend > AbschlussId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Schueler > Daten 2 > Höchster Abschluss ABS > Abschluss [AbschluesseExtern]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen den höchsten allgemeinbildenden Abschluss des Schüler aus.</td>
    </td>
  </tr>	
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler >  SchulischeVorbildungAllgemeinbildend > AbschlussDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schueler > Daten 2 > Höchster Abschluss ABS >   Erreicht am	</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie das Abschlussdatum zum höchsten allgemeinbildenden Abschluss des Schülers ein</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler >      SchulischeVorbildungBBSSchulisch > AbschlussId	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:   Schueler > Daten 2 > Höchster Abschluss BBS > Abschluss   [AbschluesseExtern]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen den höchsten schulischen berufsbildenden Abschluss des Schüler aus.	 </td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchulischeVorbildungBBSSchulisch > AbschlussDatum	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Schueler > Daten 2 > Höchster Abschluss BBS >   Erreicht am	</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie das Abschlussdatum zum höchsten schulischen berufsbildenden Abschluss des Schülers ein.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchulischeVorbildungBerufsbezogenBeruflich > AbschlussId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  Schueler > Daten 2 > Höchster Abschluss BBS > Beruf     [AbschluesseExtern]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen den höchsten beruflichen Abschluss des Schüler aus.	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler > SchulischeVorbildungBerufsbezogenBeruflich > AbschlussDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:   Schueler > Daten 2 > Höchster Abschluss BBS >  Erreicht am</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>  Tragen Sie das Abschlussdatum zum höchsten beruflichen Abschluss des Schülers ein.   Derzeit wird das Datumsfeld in Magellan nicht angezeigt.	 </td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler >  AbschlussAllgemeinbildend > AbschlussId  <br/>Schule > Schueler > AbschlussBerufsbezogenSchulisch > AbschlussId	</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: <br/>Schueler > Laufbahn > Abschluss > Abschluss 1 [AbschluesseIntern]<br/>Schueler > Laufbahn >    Abschluss >  Abschluss 1 [AbschluesseIntern]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die, an Ihrer Schule gemachten Abschlüsse des Schülers aus.<br/>Je nach Schulart wird es im entsprechenden Knoten ausgespielt.	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Schueler >  AbschlussAllgemeinbildend >   AbschlussDatum   <br/><br/>Schule > Schueler >    AbschlussBerufsbezogenSchulisch > AbschlussDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan:  <br/>Schueler > Laufbahn >  Abschluss >    Abschluss 1 >    Abschlussdatum </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie zu den Abschlüssen jeweils das Abschlussdatum ein. Je nach Schulart wird es im entsprechenden Knoten ausgespielt.</td>
    </td>
  </tr>
 </tbody>
</table>


## Lehrerdaten


>Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

<table class="table">
<caption></caption>
<thead>
<tr>
<th colspan=2 style="background-color:#FFFFFF;">Titel</th>
    </tr>
 </thead>
<tbody>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > LehrerId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > ID</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Es wird automatisch die ID des Lehrers mit dem Präfix ‚F‘ eingetragen. Dies führt dazu, dass der Lehrer im SIP-System neu eingelesen wird.   <br/> Es werden alle Lehrer berücksichtigt. </td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > GeschlechtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > Daten 1 >       Geschlecht</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie hier das Geschlecht des Lehrers aus. Der statistische Wert wird intern berechnet.</td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > LehrAmtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Lehrer > Daten 3 >   Lehrämter <br/>Lehrer > Daten 3 > Lehrämter > Lehramtstyp [Lehraemter]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Nur für Freie Schulen!  <br/>  Es wird der erste Eintrag, der als Lehramt eingetragen ist, ausgespielt.  <br/>Aktuell gibt es noch keine Unterscheidung zu freien Schulen und es wird für alle Schulen ausgespielt. <br/> Standardwert: Leer</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > StaatsangehoerigkeitId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > Daten 1 >  Staatsangeh. [Staatsangehoerigkeiten]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Staastangehörigkeit des Lehrers aus.    Standardwert: 0</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > TaetigkeitArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > Daten 2 >   Dienstbez.   [Dienstbez]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Nur für Freie Schulen!  Wählen Sie hier die Dienstbezeichnung des Lehrers aus.   Aktuell gibt es noch keine Unterscheidung zu freien Schulen und es wird für alle Schulen ausgespielt.   Standardwert: - 1 </td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > PersonenGruppeId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Lehrer > Daten 2 >     Besch-verh.</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td> Nur für Freie Schulen!   Wählen Sie das Beschäftigungsverhältnis des Lehrers aus.   Aktuell gibt es noch keine Unterscheidung zu freien Schulen und es wird für alle Schulen ausgespielt.    Standardwert: -1 	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Titel</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > Daten 1 > Anrede</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Anrede des Lehrers aus.    Standardwert: Leer</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Vorname</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > Daten 1 > Vorname</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie den Vornamen des Lehrers ein.  Standardwert: Leer</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Nachname</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>      Lehrer > Daten 1 >    Nachname   </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie den Nachnamen des Lehrers ein.     Standardwert: Leer</td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > GebDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td> Lehrer > Daten 1 >   Geburtsdatum<br/></td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie das Geburtsdatum des Lehrers ein.  Standardwert: 01.01.1900</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > FachLehrBefaehigung > FachID</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>  Lehrer > Daten 3 >    Lehrämter<br/>    Lehrer > Daten 3 >   Lehrämter > Lehramtstyp      [Lehraemter]    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>  |
 Es werden alle als Lehrbefähigung eingetragenen Lehrämter ausgespielt.  Standardwert: Knoten wird nicht angelegt.	</td>
    </td>
  </tr>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Ausbildung >  AbschlussArtId<br/>
Schule > Lehrer > Ausbildung >   QualifikationId<br/><br/>
Schule > Lehrer > Beschaeftigung >   ZugangsArtId<br/>
Schule > Lehrer > Beschaeftigung >   BeschaeftigungsUmfangId<br/>
Schule > Lehrer > Beschaeftigung >   RegelStundenId<br/>
Schule > Lehrer > Beschaeftigung >   VertragsStunden<br/>
Schule > Lehrer > Beschaeftigung >   ZugangsDatum<br/><br/>
Schule > Lehrer > LehrerUe > UeId<br/>
Schule > Lehrer > LehrerUe >  GueltigAb<br/>
Schule > Lehrer > LehrerUe >   GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td> Merkmale werden nicht unterstützt. 	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Altersteilzeit > GrundId<br/>
Schule > Lehrer > Altersteilzeit >   Stunden<br/>
Schule > Lehrer > Altersteilzeit >   GueltigAb<br/>
Schule > Lehrer > Altersteilzeit >  GueltigBis<br/><br/>
Schule > Lehrer > Arbeitszeitkonto >     GrundId<br/>           
Schule > Lehrer > Arbeitszeitkonto >  Stunden<br/>
Schule > Lehrer > Arbeitszeitkonto >    GueltigAb<br/>
Schule > Lehrer > Arbeitszeitkonto >      GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>         </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Nur für Freie Schulen! <br/> Merkmale werden nicht unterstützt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Rolle > RolleId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Mandanten > Daten 1 > Schulleiter/Stellvertreter <br/>Klassen > Zeitraeume >  Klassenleiter1</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie beim Mandanten ein, welche Lehrer die Rolle des Schulleiters und des Stellvertreters haben.    <br/>Achtung: Aktuell wird die Rolle des Klassenleiters nicht unterstützt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Rolle > KlasseId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wird entsprechend der Rolle berechnet.   -1 bei Schulleiter und Stellvertreter.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Rolle > GueltigAb</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Entsprechend der Eingabe im Dialogfenster.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Rolle > GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>      -   </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td> Entsprechend der Eingabe im Dialogfenster. 	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Anrechnung >  AnrechnungsArtId<br/>
Schule > Lehrer > Anrechnung >     Stunden<br/>
Schule > Lehrer > Anrechnung >       GueltigAb<br/>
Schule > Lehrer > Anrechnung >      GueltigBis<br/><br/>
Schule > Lehrer > PmsAEinsatz >      EinsatzArtId<br/>
Schule > Lehrer > PmsAEinsatz >     Stunden<br/>
Schule > Lehrer > PmsAEinsatz >     GueltigAb<br/>
Schule > Lehrer > PmsAEinsatz >    GueltigBis<br/><br/>
Schule > Lehrer > StundenAbgabe >    SchuleId<br/>
Schule > Lehrer > StundenAbgabe >  Stunden<br/>
Schule > Lehrer > StundenAbgabe >       GueltigAb<br/>
Schule > Lehrer > StundenAbgabe >  GueltigBis</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>   -      </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td> Merkmale werden nicht unterstützt. 	</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Abgang >  AbgangsArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Lehrer > Daten 2 >  Abgangsart  LehrerAbgaenge]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Abgangsart des Lehrers aus.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > Lehrer > Abgang > AbgangsDatum</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Lehrer > Daten 2 >   Abgang am</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Tragen Sie das Abgangsdatum des Lehrers ein.</td>
    </td>
  </tr>
</tbody>
</table>

## Nicht-Schülerdaten


!!! info "Hinweis"

  Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).


<table class="table">
<caption></caption>
<thead>
<tr>
<th colspan=2 style="background-color:#FFFFFF;">Nicht-Schülerdaten</th>
    </tr>
 </thead>
<tbody>
<tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > NichtSchueler > PruefungsArtId</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>Magellan: Schueler > Statistik >    Merkmal S1 [SchuelerMerkmale]. [Bereich 6]</td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>Wählen Sie die Prüfungsart des NichtSchülers aus. Zur weiteren Berechnung werden nur Schüler berücksichtigt, die hier einen Eintrag haben. Wichtig: Zur Unterscheidung von Deutsch und NichtDeutsch wird die Staatsangehörigkeit berücksichtig. Eine leere Staastangehörigkeit wird als Deutsch gezählt.</td>
    </td>
  </tr>
  <tr style="background-color:#CEE3F6;">
    <th>Statistikfeld</th>
        <th align=left>Schule > NichtSchueler > MaennlichDeutsch<br/>
Schule > NichtSchueler > WeiblichDeutsch<br/>
Schule > NichtSchueler > MaennlichNichtDeutsch<br/>
Schule > NichtSchueler > WeiblichNichtDeutsch</th>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Datenfeld</td>
    <td>     -    </td>
    </tr>
  <tr style="background-color:#FFFFFF;">
    <td>Beschreibung</td>
    <td>  Diese Werte werden intern berechnet.	</td>
    </td>
  </tr>
</tbody>
</table>
