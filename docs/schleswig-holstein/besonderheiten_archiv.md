## Besonderheiten Archiv

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](../legende-statistikfelder.md).

## Zur Statistik 2016/2017

### Verzeichnis Berufe (BBS)

Folgende Schlüssel wurden ersetzt und müssen, wenn bereits zugeordnet, von Ihnen umgestellt werden.

<table class="table">
<thead>
  <tr> 
    <th>Schlüssel</th>
    <th>Bezeichnung</th>
    <th>Änderung</th>
  </tr> 
</thead>
<tbody>
   <tr> 
    <td>02MS2</td>
    <td>Maschinen- und Anlagenführerin/Maschinen- und Anlagenführer Schwerpunkt Lebensmitteltechnik</td>
    <td>Jetzt zu finden unter: <strong>12MFL</strong></td>
  </tr>
  <tr> 
    <td>02MS3</td>
    <td>Maschinen- und Anlagenführerin/-führer Schwerpunkt Druckweiter- und Papierverarbeitung</td>
    <td>Jetzt zu finden unter: <strong>08MFD</strong></td>
  </tr> 
</tbody>
</table>

### Verzeichnis Abgangsarten (Lehrer) (ABS/BBS)

<table class="table" >
<thead> 
  <tr> 
    <th>Schlüssel</th> 
    <th>Bezeichnung</th> 
    <th>Änderung</th> 
  </tr>
</thead>
<tbody>
  <tr> 
    <td rowspan="2">10</td> 
    <td>Übergang auf Teilzeitbeschäftigung (Beamte)</td> 
    <td rowspan="2">Textänderung</td> </tr> 
  <tr> 
    <td><strong>Zuvor:</strong> Teilzeitbeschäftigung nach § 88 a, c LBG</td> 
  </tr>  
  <tr> 
    <td rowspan="2">11</td> 
    <td>Übergang auf Teilzeitbeschäftigung (Beschäftigte)</td> 
    <td rowspan="2">Textänderung</td> </tr> 
  <tr> 
    <td><strong>Zuvor:</strong> Übergang auf Teilzeitbeschäftigung (Angestellte nach § 11 TV-L)</td> 
  </tr>  
</tbody>
</table>

### Verzeichnis Bildungsgänge (BBS)

<table class="table" >
<thead> 
  <tr> 
    <th>Schlüssel</th> 
    <th>Bezeichnung</th> 
    <th>Änderung</th> 
  </tr>
</thead>
<tbody>
  <tr> 
    <td rowspan="2">021</td> 
    <td>Prävention im Kindergarten (von Grundschulen erteilt)</td> 
    <td rowspan="2">Textänderung</td> </tr> 
  <tr> 
    <td><strong>Zuvor:</strong> Prävention im Kindergarten</td> 
  </tr>  
  <tr> 
    <td rowspan="2">11</td> 
    <td>Übergang auf Teilzeitbeschäftigung (Beschäftigte)</td> 
    <td rowspan="2">Textänderung</td> </tr> 
  <tr> 
    <td><strong>Zuvor:</strong> Übergang auf Teilzeitbeschäftigung (Angestellte nach § 11 TV-L)</td> 
  </tr>  
</tbody>
</table>

### Verzeichnis Dienstverhältnisse (ABS/BBS)

<table class="table" >
<thead> 
  <tr> 
    <th>Schlüssel</th> 
    <th>Bezeichnung</th> 
    <th>Änderung</th> 
  </tr>
</thead>
<tbody>
  <tr> 
    <td rowspan="2">3</td> 
    <td>Beamter auf Widerruf / Lehrkraft im Vorbereitungsdienst (Referendar)</td> 
    <td rowspan="2">Textänderung</td> </tr> 
  <tr> 
    <td><strong>Zuvor:</strong> Beamter auf Widerruf</td> 
  </tr>  
</tbody>
</table>


### Verzeichnis Fächer (ABS/BBS) korrigieren 

Das Statistikamt hält für die Statistik zwei Kataloge "Fächer" und "Kurse" bereit. In MAGELLAN werden   "Fächer" plus Eigenschaften verwaltet werden, es gibt also kein Verzeichnis der Kurse, da ein Fach mit Eigenschaften wie einer Unterrichtsart, einem Fachstatus, einer Kursnummer usw zum Kurs wird.

> Beide Kataloge werden über das **Verzeichnis Fächer** vereint. Zur Zusammenlegung und Differenzierung der Schlüssel, die als Fächer und Kurse genutzt werden, erhalten die Schlüssel beim Import im Feld "Kürzel" und "Schlüssel" ein "F" oder "K" und in der Bezeichnung den Zusatz "(Fach)" oder "(Kurs)".

Bei Schlüssel die in beiden Katalogen existieren, wird kein Zusatz angehangen.

**Problem**

Der Importmechanismus in MAGELLAN erlaubt keinen Import bereits vorhandener Schlüssel, sowie Aktualisierungen von Bezeichnungen, da diese die Bedeutung eines Schlüssel verändern können und damit Probleme in der Logik bei der Verwendung der Schlüssel in MAGELLAN auftreten können. Weiterhin werden bereits verwendete Einträge nicht gelöscht. Was die Wiederverwendung einen Schlüssels nicht erlaubt,
wenn diese dadurch eine andere Bedeutung bekäme.

**Lösung**

Wir haben im Administrator dazu eine Korrektur integriert. Bitte führen Sie folgende Schritte nacheinander aus. 

1. Stellen Sie sicher, dass die aktuelle Version (mindestens die 6.0.179) auf Ihrem Server und auf Ihrem Client installiert sind, nur dann stehen Ihnen die aktuellen Kataloge und die Korrekturfunktion zur Verfügung.
2. Importieren Sie die Schlüsselkataloge über ```MAGELLAN ADMINISTRATOR > Datenimporte > Schlüsselverzeichnisse importieren > Schleswig-Holstein und "allgemeinbildende Schule"```.
3. Rufen Sie den Punkt MAGELLAN ADMINISTRATOR > Datenbankpflege > Datenbank überprüfen auf und wählen aus der Liste der möglichen Funktionen "SHL: Fächerschlüssel anpassen" aus.

![Assistent zum Anpassen der Fächerschlüssel für SHL](../images/shl.umschluesseln.png)

Gerade in diesem Fall, müssen deshalb Schlüssel bei logischen Änderungen manuell angepasst werden. Dies ist der Fall, wenn 

1. Wenn im Katalog "Fächer" und "Kurse" der gleiche Schlüssel mit unterschiedlichen Bedeutungen vorhanden ist, dann muss der Schlüssel manuell hinzugefügt werden.
2. Wenn ein Schlüssel nur noch in einem der beiden Kataloge verwendet wird, dann muss der Zusatz angepasst werden, damit Sie nicht versehentlich einen falschen Eintrag wählen.

Beispiel:

In diesem Jahr ist es so, dass sowohl für Fächer als auch für Kurse der gleiche Schlüssel mit unterschiedlichen Bedeutungen verwendet wurde,

Beispiel:
  Schlüssel: "040", 
  Bezeichnung im Fach: "Orchester/Chor"
  Bezeichnung im Kurs: "Religion"

Zwar wird lt. dem Amt der Schlüssel 040 nicht mehr als Fach "Orchester/Chor" verwendet, wenn Sie diesen aber bereits in MAGELLAN verwendet haben, kann er nicht vom Importmechanismus gelöscht und durch den neuen ersetzt werden. 

### Liste der manuell zu korrigierenden Schlüssel

<table class="table" >
<thead> 
  <tr> 
    <th>Alter Schlüssel</th>     
    <th>Kürzel</th>     
    <th>Schlüssel</th> 
    <th>Bezeichnung</th> 
    <th>Gültig von</th> 
    <th>Kommentar</th>
  </tr>
</thead>
<body>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">009</td>    
    <td>009</td> 
    <td>009</td> 
    <td>Gemeinschaftskunde</td>
    <td>01.08.2006</td> 
    <td style="color: black">Ersetzt durch: <b>009_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">011</td>    
    <td>011</td> 
    <td>011</td> 
    <td>Dänisch nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen(Kurs/Fach BBS)</td>
    <td>01.08.2006</td> 
    <td style="color: black">Ersetzt durch: <b>011_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">016</td>    
    <td>016</td> 
    <td>016</td> 
     <td>Englisch nur übergreifender Unterricht  - 1.-3. Fremdspr. zusammen (Kurs/Fach BBS)</td>
    <td>01.08.2014</td> 
    <td style="color: black">Ersetzt durch: <b>016_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">017</td>    
    <td>017</td> 
    <td>017</td> 
     <td>Geographie</td>
    <td>01.08.2006</td> 
    <td style="color: black">Ersetzt durch: <b>017_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">022</td>
    <td>022</td>
    <td>022</td>
    <td>Französisch nur übergreifender Unterricht - 1.- 4. Fremdspr. zusammen (Kurs/Fach BBS)</td>    
    <td>01.08.2014</td>   
    <td style="color: black">Ersetzt durch: <b>022_F</b></td>
  </tr> 
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>041</td> 
    <td>041</td>
    <td>Rechtskunde</td>
    <td>01.08.2006</td> 
    <td style="color: black">Ersetzt durch: <b>041_F</b> und <b>041_K</b></td> 
  </tr>  
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">023</td>
    <td>023</td>
    <td>023</td>
    <td>Geschichte</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>023_F</b></td>
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">024</td>    
    <td>024</td> 
    <td>024</td> 
    <td>Altgriechisch</td>
    <td>01.08.2012</td> 
    <td style="color: black">Ersetzt durch: <b>023_F</b></td>
  </tr>  
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">027</td>    
    <td>027</td> 
    <td>027</td> 
    <td>Textillehre</td>
    <td>01.08.2006</td> 
    <td style="color: black">Ersetzt durch: <b>027_F</b></td>
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">028</td>    
    <td>028</td> 
    <td>028</td> 
    <td>Neugriechich</td>
    <td>01.08.2012</td>
    <td style="color: black">Ersetzt durch: <b>028_F</b></td>
  </tr> 
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">031</td>    
    <td>031</td> 
    <td>031</td> 
    <td>Italienisch</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>031_F</b></td>
  </tr> 
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">032</td>    
    <td>032</td> 
    <td>032</td> 
    <td>Latein nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen (Kurs/Fach BBS)</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>032_F</b></td>
  </tr>  
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">039</td>    
    <td>039</td> 
    <td>039</td> 
    <td>Wirtschaft/Politik</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>039_F</b></td>
  </tr>    
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">041</td>    
    <td>041</td> 
    <td>041</td> 
    <td>Rechtskunde</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>041_F</b></td>
  </tr>    
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">045</td>    
    <td>045</td> 
    <td>045</td> 
    <td>"Russisch nur übergreifender Unterricht  2.- 4. Fremdspr. zusammen (Kurs/Fach BBS)</td>
    <td>01.08.2014</td>
    <td style="color: black">Ersetzt durch: <b>045_F</b></td>
  </tr>  
  <tr> 
    <td style="font-weight: bold; text-align:center">047_F</td>
    <td>047_F</td> 
    <td>047F</td> 
    <td style="color: blue">Heimat-, Welt- und Sachunterricht (Fach)</td> 
    <td style="color: blue">01.08.2015</td>
    <td>Textänderung</td>    
  </tr>   
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">051</td>    
    <td>051</td>
    <td>051</td> 
    <td>"Spanisch nur übergreifender Unterricht  2. - 4. Fremdspr. zusammen (Kurs/Fach BBS)</td>
    <td>01.08.2014</td>
    <td style="color: black">Ersetzt durch: <b>051_F</b></td> 
  </tr>    
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">052</td>    
    <td>052</td> 
    <td>052</td> 
    <td>"Türkisch</td>
    <td>01.08.2008</td>
    <td style="color: black">Ersetzt durch: <b>052_F</b></td>  
  </tr>   
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">075</td>    
    <td>075</td> 
    <td>075</td> 
    <td>"Friesisch</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>075_F</b></td>  
  </tr> 
  <tr>
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>111</td> 
    <td>111</td> 
    <td>Dänisch - 1. Fremdsprache 
      <font style="color: blue">(Fach)(Kurs, neu begonnen)</font>
    </td>
    <td>01.08.2015</td>
    <td>Textänderung</td>
  </tr> 
  <tr>
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>116</td> 
    <td>116</td> 
    <td>Englisch - 1. Fremdsprache 
      <font style="color: blue">(Fach)(Kurs, neu begonnen)</font>
    </td>
    <td>01.08.2015</td>
    <td>Textänderung</td>
  </tr> 
  <tr style="color: red"> 
    <td style="font-weight: bold; text-align:center">-</td> 
    <td>117</td>     
    <td>117</td>     
    <td>"Wirtschaftslehre/Wirtschaft</td>    
    <td>01.08.2006</td>   
    <td style="color: black">Ersetzt durch: <b>117_F</b> und <b>042_K</b></td>
  </tr>
  <tr>
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>122</td> 
    <td>122</td> 
    <td>Französisch - 1. Fremdsprache 
      <font style="color: blue">(Fach)(Kurs, neu begonnen)</font>
    </td>
    <td>01.08.2015</td>
    <td>Textänderung</td>
  </tr> 
  <tr>
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>132</td> 
    <td>132</td> 
    <td>Latein - 1. Fremdsprache 
      <font style="color: blue">(Fach)(Kurs, neu begonnen)</font>
    </td>
    <td>01.08.2015</td>
    <td>Textänderung</td>
  </tr> 
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">143</td>    
    <td>143</td> 
    <td>143</td> 
    <td>"Religion, katholisch</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>143_F</b></td>
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">144</td>    
    <td>144</td> 
    <td>144</td> 
    <td>Religion, evangelisch</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>144_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>211</td> 
    <td>211</td> 
    <td>Dänisch - 2. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>211_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>216</td> 
    <td>216</td> 
    <td>Englisch - 2. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>216_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>222</td> 
    <td>222</td> 
    <td>Französisch - 2. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>222_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>232</td> 
    <td>232</td> 
    <td>Latein - 2. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>232_F</b></td> 
  </tr>
  <tr>
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>245_K</td> 
    <td>245K</td> 
    <td>Russisch - <font style="color: blue">1. Fremdsprache, fortgeführt</font> Kurs</td>
    <td style="color: blue">01.08.2015</td>
    <td>Textänderung, Achtung: <b>Bedeutung verändert!</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>251</td> 
    <td>251</td> 
    <td>Spanisch- 2. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>251_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>311</td> 
    <td>311</td> 
    <td>Dänisch- 3. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>311_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>316</td> 
    <td>316</td> 
    <td>Englisch - 3. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>316_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>322</td> 
    <td>322</td> 
    <td>Französisch- 3. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>322_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>332</td> 
    <td>332</td> 
    <td>Latein - 3. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>332_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>345</td> 
    <td>345</td> 
    <td>Russisch - 3. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>345_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>351</td> 
    <td>351</td> 
    <td>Spanisch - 3. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>351_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>411</td> 
    <td>411</td> 
    <td>Dänisch - 4. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>411_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>422</td> 
    <td>422</td> 
    <td>Französisch - 4. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>422_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>432</td> 
    <td>432</td> 
    <td>Latein - 4. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>432_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>445</td> 
    <td>445</td> 
    <td>Russisch - 4. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>445_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>451</td> 
    <td>451</td> 
    <td>Spanisch - 4. Fremdsprache</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>451_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>503</td> 
    <td>503</td> 
    <td>Datenverarbeitungstechnik</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>503_F</b> und <b>550_K</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">-</td>    
    <td>509</td> 
    <td>509</td> 
    <td>Maschinenbautechnik</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>509_F</b></td> 
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">514</td>    
    <td>514</td> 
    <td>514</td> 
    <td>"Sporttheorie</td>
    <td>01.08.2006</td>
    <td style="color: black">Ersetzt durch: <b>514_F</b></td>  
  </tr>
  <tr style="color: red">
    <td style="font-weight: bold; text-align:center">970</td>    
    <td>970</td> 
    <td>970</td> 
    <td>"WPU - sonstiges Fach</td>
    <td>01.08.2013</td>
    <td style="color: black">Ersetzt durch: <b>970_F</b></td>  
  </tr>
</tbody>
</table>

### Vollständige Übersicht der Fächer und Kurse (Stand 2016/17)

Verwendung|Kuerzel|Schlüssel|Bezeichnung
--|--|--|--
Fach|007_F|007F|Bildhaftes Gestalten/Design (Fach)
Fach|009_F|009F|Gemeinschaftskunde (Fach)
Fach|011_F|011F|Dänisch nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen (Fach BBS)
Fach|016_F|016F|Englisch nur übergreifender Unterricht  - 1.-3. Fremdspr. zusammen (Fach BBS)
Fach|017_F|017F|Geographie (Fach)
Fach|018_F|018F|Haushaltslehre (Fach)
Fach|019_F|019F|Astronomie (Fach)
Fach|020_F|020F|Politik (Fach)
Fach|022_F|022F|Französisch nur übergreifender Unterricht - 1.- 4. Fremdspr. zusammen (Fach BBS)
Fach|023_F|023F|Geschichte (Fach)
Fach|024_F|024F|Altgriechisch (Fach)
Fach|025_F|025F|Geologie (Fach)
Fach|027_F|027_F|Textillehre (Fach)
Fach|028_F|028F|Neugriechich (Fach)
Fach|031_F|031F|Italienisch (Fach)
Fach|032_F|032F|Latein nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen (Fach BBS)
Fach|037_F|037F|Kunstgeschichte (Fach)
Fach|039_F|039F|Wirtschaft/Politik (Fach)
Fach|040_F|040F|Orchester/Chor (Fach)
Fach|041_F|041F|Rechtskunde (Fach)
Fach|045_F|045F|Russisch nur übergreifender Unterricht  2.- 4. Fremdspr. zusammen (Fach BBS)
Fach|047_F|047F|Heimat-, Welt- und Sachunterricht (Fach)
Fach|051_F|051F|Spanisch nur übergreifender Unterricht  2. - 4. Fremdspr. zusammen (Fach BBS)
Fach|052_F|052F|Türkisch (Fach)
Fach|053_F|053F|Technik (Fach)
Fach|054_F|054F|Polnisch (Fach)
Fach|056_F|056F|Technisches Werken (Fach)
Fach|074_F|074F|Deutsch als Zweitsprache (Fach)
Fach|075_F|075F|Friesisch (Fach)
Fach|076_F|076F|Niederdeutsch (Fach)
Fach|083_F|083F|Heilpädagogik (Fach)
Fach|089_F|089F|Sonderpädagogik (Fach)
Fach|093_F|093F|Eurythmie (Fach)
Fach|094_F|094F|Naturwissenschaft (Fach)
Fach|115_F|115F|Weltkunde (Fach)
Fach|117_F|117F|Wirtschaftslehre/Wirtschaft (Fach)
Fach|141_F|141F|Ethik (Fach)
Fach|142_F|142F|Islamunterricht (Fach)
Fach|143_F|143F|Religion, katholisch (Fach)
Fach|144_F|144F|Religion, evangelisch (Fach)
Fach|163_F|163F|Türkisch (Fach)
Fach|211_F|211F|Dänisch - 2. Fremdsprache (Fach)
Fach|216_F|216F|Englisch - 2. Fremdsprache (Fach)
Fach|222_F|222F|Französisch - 2. Fremdsprache (Fach)
Fach|232_F|232F|Latein - 2. Fremdsprache (Fach)
Fach|251_F|251F|Spanisch - 2. Fremdsprache (Fach)
Fach|311_F|311F|Dänisch - 3. Fremdsprache (Fach)
Fach|316_F|316F|Englisch - 3. Fremdsprache (Fach)
Fach|322_F|322F|Französisch - 3. Fremdsprache (Fach)
Fach|332_F|332F|Latein - 3. Fremdsprache (Fach)
Fach|345_F|345F|Russisch - 3. Fremdsprache (Fach)
Fach|351_F|351F|Spanisch - 3. Fremdsprache (Fach)
Fach|411_F|411F|Dänisch - 4. Fremdsprache (Fach)
Fach|422_F|422F|Französisch - 4. Fremdsprache (Fach)
Fach|432_F|432F|Latein - 4. Fremdsprache (Fach)
Fach|445_F|445F|Russisch - 4. Fremdsprache (Fach)
Fach|451_F|451F|Spanisch - 4. Fremdsprache (Fach)
Fach|452_F|452F|sonstige moderne Fremdsprachen (Fach)
Fach|453_F|453F|sonstige alte Fremdsprachen (Fach)
Fach|503F|503_F|Datenverarbeitungstechnik (Fach)
Fach|505_F|505F|Ernährungslehre mit Chemie (Fach)
Fach|509_F|509F|Maschinenbautechnik (Fach)
Fach|510_F|510F|Pädagogik/Psychologie (Fach)
Fach|512_F|512F|Rechnungswesen (Fach)
Fach|514_F|514F|Sporttheorie (Fach)
Fach|516_F|516F|Wirtschaftstheorie und -politik (Fach)
Fach|517_F|517F|Wirtschaftsenglisch (Fach)
Fach|600_F|600F|Dänisch (USPR)
Fach|601_F|601F|Englisch (USPR)
Fach|602_F|602F|Französisch (USPR)
Fach|605_F|605F|Spanisch (USPR)
Fach|910_F|910F|Seminarfach (Fach)
Fach|916_F|916F|Arbeitsgemeinschaft (AG) (Fach)
Fach|919_F|919F|WPU - Gestalten (Fach)
Fach|920_F|920F|WPU - 2. Fremdsprache (Fach)
Fach|921_F|921F|WPU - Naturwissenschaften (Fach)
Fach|922_F|922F|WPU - Gesellschaftswissenschaften (Fach)
Fach|923_F|923F|WPU - Arbeit/Wirtschaft und Verbraucherbildung (Fach)
Fach|924_F|924F|WPU - Ästhetische Bildung (Fach)
Fach|925_F|925F|WPU - Sport (Fach)
Fach|928_F|928F|WPU - Wirtschaftslehre (Fach)
Fach|929_F|929F|WPU - Technik (Fach)
Fach|930_F|930F|WPU - Angewandte Informatik (Fach)
Fach|931_F|931F|WPU - Darstellendes Spiel (Fach)
Fach|970_F|970F|WPU - sonstiges Fach (Fach)
Kurs|040_K|040K|Religion (Kurs)
Kurs|041_K|041K|Religion / Ethik (Kurs)
Kurs|042_K|042K|Wirtschaftslehre (Kurs)
Kurs|145_K|145K|Russisch - 1. Fremdsprache (Kurs, neu begonnen)
Kurs|151_K|151K|Spanisch - 1. Fremdsprache (Kurs, neu begonnen)
Kurs|152_K|152K|Türkisch - 1. Fremdsprache (Kurs, neu begonnen)
Kurs|211_K|211K|Dänisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|216_K|216K|Englisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|222_K|222K|Französisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|232_K|232K|Latein - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|245_K|245K|Russisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|251_K|251K|Spanisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|252_K|252K|Türkisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs|311_K|311K|Dänisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|316_K|316K|Englisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|322_K|322K|Französisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|332_K|332K|Latein - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|345_K|345K|Russisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|351_K|351K|Spanisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|352_K|352K|Türkisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs|411_K|411K|Dänisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs|416_K|416K|Englisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs|422_K|422K|Französisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs|432_K|432K|Latein - 2. Fremdsprache, fortgeführt (Kurs)
Kurs|445_K|445K|Russisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs|451_K|451K|Spanisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs|452_K|452K|Türkisch, 2. Fremdsprache (Kurs)
Kurs|506_K|506K|Gemeinschaftskunde (Kurs)
Kurs|517_K|517K|Agrarbiologie (Kurs)
Kurs|518_K|518K|Biotechnologie (Kurs)
Kurs|519_K|519K|Technik (Kurs)
Kurs|520_K|520K|Berufliche Informatik (Kurs)
Kurs|521_K|521K|Ernährung (Kurs)
Kurs|522_K|522K|Erziehungswissenschaften (Kurs)
Kurs|523_K|523K|Rechnungswesen (auslaufend) (Kurs)
Kurs|525_K|525K|Betriebswirtschaftslehre (Kurs)
Kurs|526_K|526K|Volkswirtschaftslehre (Kurs)
Kurs|545_K|545K|Erneuerbare Energien (Kurs)
Kurs|550_K|550K|Datenverarbeitungstechnik (Kurs)
Kurs|551_K|551K|Ernährungslehre / Diätetik, Körperpflegekunde (Kurs)
Kurs|552_K|552K|Hauswirtschaft (Kurs)
Kurs|553_K|553K|Ökotrophologie (Kurs)
Kurs|554_K|554K|Chemisch-pharmazeutische Übungen (Kurs)
Kurs|555_K|555K|Galenische Übungen (Kurs)
Kurs|556_K|556K|Medizinproduktekunde (Kurs)
Kurs|557_K|557K|Pharmazietechnik (Kurs)
Kurs|558_K|558K|Ökologie und Gesundheit (Kurs)
Kurs und Fach|3|3|Physik
Kurs und Fach|6|6|Kunst
Kurs und Fach|8|8|Biologie
Kurs und Fach|10|10|Chemie
Kurs und Fach|12|12|Mathematik
Kurs und Fach|13|13|Datenverarbeitung/Informatik
Kurs und Fach|14|14|Deutsch
Kurs und Fach|26|26|Sport
Kurs und Fach|36|36|Musik
Kurs und Fach|38|38|Philosophie
Kurs und Fach|111|111|Dänisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach|116|116|Englisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach|122|122|Französisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach|132|132|Latein - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach|500|500|Agrartechnik mit Biologie
Kurs und Fach|501|501|Bautechnik
Kurs und Fach|502|502|Darstellendes Spiel
Kurs und Fach|504|504|Elektrotechnik
Kurs und Fach|507|507|Gesundheit
Kurs und Fach|508|508|Literatur
Kurs und Fach|513|513|Rechtslehre
Kurs und Fach|515|515|Wirtschaftsgeographie
Kurs und Fach|999|999|sonstiges Fach, sonstiger Kurs

### Verzeichnis Lehrämter (ABS/BBS)

<table class="table" >
<thead>
  <tr>
    <th>Schlüssel</th>
    <th>Bezeichnung</th>
    <th>Änderung</th>
 </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">04</td>
    <td>Sonderschullehrer/ -innen / Förderzentrumslehrer/-innen</td>
    <td rowspan="2">Textänderung</td> 
  </tr>
  <tr>
    <td><strong>Zuvor:</strong> Sonderschullehrer/ -innen</td>
  </tr>
  <tr>
    <td rowspan="2">HSN</td>
    <td>Heimat- und Sachunterricht/td>
    <td rowspan="2">Textänderung</td> 
  </tr>
  <tr>
    <td><strong>Zuvor:</strong> Sachunterricht,naturwissenschaftlich</td>
  </tr>
  <tr>
    <td rowspan="2">SBL</td>
    <td>Sonderpädagogische Lehrbefähigungen für Blinde / Blindenpädagogik</td>
    <td rowspan="2">Textänderung</td> 
  </tr>
  <tr>
    <td><strong>Zuvor:</strong> Sonderpädagogische Lehrbefähigungen für Blinde/td>
  </tr>
</tbody>
</table>

### Zur Statistik 2015/2016

Es könnte sein, dass Sie die Plausibilität **SA1110** verstärkt erhalten. 

Dies liegt evtl. dran, dass Sie die Fremdsprachenschlüssel 011, 016, 022, 032, 045, 051, 600, 601, 602, 605 eingetragen haben. 
Diese dienen aber nur für spezielle Zwecke, z.B. der Schlüssel 016 = Englisch (Nur bei übergreifendem Unterricht). 

Durch die Zusammenfassung der Fächer und Schülerdatei muss nun die genaue Fremdsprache der Fremdsprachenfolge ausgegeben werden. Für Englisch 1. Fremdsprache wäre dies nun der Schlüssel 116 = Englisch 1. Fremdsprache. 

### UART – Unterrichtsarten in MAGELLAN

Die für die Statistik abgefragten Schlüsselwerte können zu Teil nicht genutzt werden, weil MAGELLAN-interne Eingaben für den Zeugnisdruck oder die Zeugniserstellung erwartet werden. 

Die nachfolgende Tabelle zeigt Ihnen welche MAGELLAN-Eintragungen erkannt und in entsprechende Werte für die Statistikwerte gewandelt werden.

>Ist die Unterrichtsart leer, nicht der Fachstatus WahlPF oder Freiw gewählt, oder entspricht keinem der nachfolgenden Werte, wird generell der Wert P für Pflichtfach ausgegeben. Es ist kein gesonderter Eintrag für die Unterrichtsart Pflicht notwendig. 

>Es wird in den Verzeichnissen Unterrichtsarten und Fachstatus immer der Wert der Spalte Schlüssel berücksichtigt.

Bedeutung	                        |Feld	       |Schlüssel	 |Ausgabe für die Statistikdatei
------------------------------------|--------------|-------------|------------------------------
Pflicht	                         	|Unterrichtsart|P oder leer  |P
Förderunterricht                    |Unterrichtsart|FOE          |U
Freiwilliger Unterricht (AGs)       |Unterrichtsart|AG           |F
Profilgebend                        |Unterrichtsart|P-KURS       |G
Kernfach	                        |Unterrichtsart|KF oder E    |K
Zusatzunterricht Mittlerer Abschluss|Unterrichtsart|Z oder ZUSATZ|Z
Wahlpflichtangebot	                |Unterrichtsart|WPU1…WPU4    |W
Wahlpflichtangebot	                |Fachstatus	   |WahlPF       |W
Freiwilliger Unterricht (AGs)       |Fachstatus	   |Freiw	     |F


### Zur Statistik 2014/2015

In einigen Schlüsselverzeichnissen hat es Änderung gegeben, die ggf. die Bedeutung der Schlüssel ändern und Sie damit gezwungen sind, bei den betroffenen Datensätzen die Auswahl zu erneuern.

#### Bildungsgänge

Kuerzel	|Schluessel	|Alte Bezeichnung	|Neue Bezeichnung
--|--|--|--
901	|901	|BS – Zusatzunterricht Hauptschulabschluss	|BS - Zusatzunterricht Erster allgemeinbildender Schulabschluss

#### Klassenstufen

Kuerzel|	Schluessel	|Alte Bezeichnung	|Neue Bezeichnung
--|--|--|--
Q3	|Q3	|Qualifikationsphase 3 (14. Jahrgangsstufe)	|Qualifikationsphase 3 (ehemals 13. Jgst.)
Q5	|Q5	|-	|Qualifikationsphase 5 (14. Jahrgangsstufe)

#### Schularten, Schulformen

Kuerzel	|Schluessel	|Alte Bezeichnung	|Neue Bezeichnung
--|--|--|--
120	|120	|Gemeinschaftsschule	|Gemeinschaftsschule mit Oberstufe
115|	115	|-	|Gemeinschaftsschule ohne Oberstufe

#### Herkunft (Schulformen)

Kuerzel	|Schluessel	|Alte Bezeichnung	|Neue Bezeichnung
--|--|--|--
17	|17	|Zugang aus einer Gemeinschaftsschule	|Zugang aus einer Gemeinschaftsschule mit Oberstufe
15	|15	|-	|Zugang aus einer Gemeinschaftsschule ohne Oberstufe

#### Weggefallene Felder, die nicht mehr erfragt werden.

Nur für die aktuellen Schüler der allgemeinbildenden Schule wird die Schulübergangsempfehlung der Grundschule (SAE) nicht mehr erfragt.

### Zur Statistik 2013/2014

Gastschüler werden aus der Statistik ausgeschlossen, wenn Sie in MAGELLAN den entsprechenden Schüler unter ```Schüler > Daten 3 > Verschiedenes > Gastschüler``` als Gastschüler markieren.

### Zur Statistik 2012/2013

Das Feld SAE wurde bisher unter ```Schüler > Laufbahn > Empfehlung ```gespeichert. Ab der Statistik 2012/2013 wird dieser Wert nun unter ```Schüler > Zugang/Abgang > Zugang – Empfehlung``` gespeichert.

Die bereits unter ```Schüler > Laufbahn > Empfehlung ```eingetragen Werte können über die eine spezielle Funktion in das Feld ```Schüler > Zugang/Abgang > Zugang – Empfehlung``` kopiert werden. 

Dazu gehen Sie wie folgt vor:

1.	Starten die den MAGELLAN-Administrator.
2.	Wählen Sie „Datenbankpflege“.
3.	Klicken Sie bei „Datenbank prüfen“ auf die Schaltfläche „Start“.
4.	Wählen Sie „Empfehlungen umkopieren“ und klicken Sie dann auf OK.

### Zur Statistik 2011/2012

#### Erstmalig Statistik für Berufsbildende Schulen

In diesem Jahr spielen wir erstmalig auch die Statistik für Berufsbildende Schulen aus. 
Aus Gründen der Übersichtlichkeit werden die neu hinzugekommenen BBS Felder werden nicht gesondert farblich im Anhang dargestellt. Sie bekommen lediglich ein „*“ in der Spalte Statistikdatei.

#### Statistikdatei „BM“ - Besondere Massnahmen.

Die Statistikdatei „Besondere Massnahmen“ wird vom Statistikamt ab diesem Jahr nicht mehr erfragt. Damit fallen auch alle Eingaben dazu in MAGELLAN und DAVINCI raus.

Die Bezeichnungen der Schlüssel werden aus Gründen der Eindeutigkeit von Schlüsseln nicht geändert. Von Zeit zu Zeit erhalten bestehende Schlüssel neue Bedeutungen und es wird lediglich die Bezeichnung verändert. Solche Schlüssel müssen von Ihnen manuell verändert werden.

Weggefallene Felder, die nicht mehr erfragt werden:

* MIGST – Migrantenstatus (SA)
* HEIM – Heimunterbringung (SA)