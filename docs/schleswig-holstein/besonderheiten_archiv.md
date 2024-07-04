# Besonderheiten Archiv

Die Legende zu den nachstehenden Tabellen finden Sie [HIER](https://doc.ls.stueber.de/legende-statistikfelder/).

## Zur Statistik 2016/2017

### Verzeichnis Berufe (BBS)

Folgende Schlüssel wurden ersetzt und müssen, wenn bereits zugeordnet, von Ihnen umgestellt werden.

Schlüssel | Bezeichnung                                                                                 | Änderung
----------|---------------------------------------------------------------------------------------------|-----------------------------
02MS2     | Maschinen- und Anlagenführerin/Maschinen- und Anlagenführer Schwerpunkt Lebensmitteltechnik | Jetzt zu finden unter: 12MFL
02MS3     | Maschinen- und Anlagenführerin/-führer Schwerpunkt Druckweiter- und Papierverarbeitung      | Jetzt zu finden unter: 08MFD

### Verzeichnis Abgangsarten (Lehrer) (ABS/BBS)

Schlüssel | Bezeichnung                                                                                                                     | Änderung
----------|---------------------------------------------------------------------------------------------------------------------------------|-------------
10        | Übergang auf Teilzeitbeschäftigung (Beamte)<br> **Zuvor:** Teilzeitbeschäftigung nach § 88 a, c LBG                             | Textänderung
11        | Übergang auf Teilzeitbeschäftigung (Beschäftigte)<br>**Zuvor:** Übergang auf Teilzeitbeschäftigung (Angestellte nach § 11 TV-L) | Textänderung

### Verzeichnis Bildungsgänge (BBS)

Schlüssel | Bezeichnung                                                                                                                      | Änderung
----------|----------------------------------------------------------------------------------------------------------------------------------|-------------
021       | Prävention im Kindergarten (von Grundschulen erteilt)<br>**Zuvor:** Prävention im Kindergarten                                   | Textänderung
11        | Übergang auf Teilzeitbeschäftigung (Beschäftigte) <br>**Zuvor:** Übergang auf Teilzeitbeschäftigung (Angestellte nach § 11 TV-L) | Textänderung

### Verzeichnis Dienstverhältnisse (ABS/BBS)

Schlüssel | Bezeichnung                                                                                              | Änderung
----------|----------------------------------------------------------------------------------------------------------|-------------
3         | Beamter auf Widerruf / Lehrkraft im Vorbereitungsdienst (Referendar) <br>**Zuvor:** Beamter auf Widerruf | Textänderung

### Verzeichnis Fächer (ABS/BBS) korrigieren

Das Statistikamt hält für die Statistik zwei Kataloge "Fächer" und "Kurse" bereit. In Magellan werden   "Fächer" plus Eigenschaften verwaltet werden, es gibt also kein Verzeichnis der Kurse, da ein Fach mit Eigenschaften wie einer Unterrichtsart, einem Fachstatus, einer Kursnummer usw zum Kurs wird.

!!! info "Hinweis"
    Beide Kataloge werden über das **Verzeichnis Fächer** vereint. Zur Zusammenlegung und Differenzierung der Schlüssel, die als Fächer und Kurse genutzt werden, erhalten die Schlüssel beim Import im Feld "Kürzel" und "Schlüssel" ein "F" oder "K" und in der Bezeichnung den Zusatz "(Fach)" oder "(Kurs)".

Bei Schlüssel die in beiden Katalogen existieren, wird kein Zusatz angehangen.

#### Problem

Der Importmechanismus in Magellan erlaubt keinen Import bereits vorhandener Schlüssel, sowie Aktualisierungen von Bezeichnungen, da diese die Bedeutung eines Schlüssel verändern können und damit Probleme in der Logik bei der Verwendung der Schlüssel in Magellan auftreten können. Weiterhin werden bereits verwendete Einträge nicht gelöscht. Was die Wiederverwendung einen Schlüssels nicht erlaubt,
wenn diese dadurch eine andere Bedeutung bekäme.

#### Lösung

Wir haben im Administrator dazu eine Korrektur integriert. Bitte führen Sie folgende Schritte nacheinander aus.

1. Stellen Sie sicher, dass die aktuelle Version (mindestens die 6.0.179) auf Ihrem Server und auf Ihrem Client installiert sind, nur dann stehen Ihnen die aktuellen Kataloge und die Korrekturfunktion zur Verfügung.
2. Importieren Sie die Schlüsselkataloge über `Magellan Administrator > Datenimporte > Schlüsselverzeichnisse importieren > Schleswig-Holstein und "allgemeinbildende Schule"`.
3. Rufen Sie den Punkt `Magellan Administrator > Datenbankpflege > Datenbank überprüfen` auf und wählen aus der Liste der möglichen Funktionen `SHL: Fächerschlüssel anpassen` aus.

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

Zwar wird lt. dem Amt der Schlüssel 040 nicht mehr als Fach "Orchester/Chor" verwendet, wenn Sie diesen aber bereits in Magellan verwendet haben, kann er nicht vom Importmechanismus gelöscht und durch den neuen ersetzt werden.

### Liste der manuell zu korrigierenden Schlüssel

Alter Schlüssel | Kürzel | Schlüssel | Bezeichnung                                                                           | Gültig von | Kommentar
----------------|--------|-----------|---------------------------------------------------------------------------------------|------------|-------------------------------
009             | 009    | 009       | Gemeinschaftskunde                                                                    | 01.08.2006 | Ersetzt durch: 009_F
011             | 011    | 011       | Dänisch nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen(Kurs/Fach BBS)       | 01.08.2006 | Ersetzt durch: 011_F
016             | 016    | 016       | Englisch nur übergreifender Unterricht - 1.-3. Fremdspr. zusammen (Kurs/Fach BBS)     | 01.08.2014 | Ersetzt durch: 016_F
017             | 017    | 017       | Geographie                                                                            | 01.08.2006 | Ersetzt durch: 017_F
022             | 022    | 022       | Französisch nur übergreifender Unterricht - 1.- 4. Fremdspr. zusammen (Kurs/Fach BBS) | 01.08.2014 | Ersetzt durch: 022_F
-               | 041    | 041       | Rechtskunde                                                                           | 01.08.2006 | Ersetzt durch: 041_F und 041_K
023             | 023    | 023       | Geschichte                                                                            | 01.08.2006 | Ersetzt durch: 023_F
024             | 024    | 024       | Altgriechisch                                                                         | 01.08.2012 | Ersetzt durch: 023_F
028 | 028 | 028 | Neugriechisch | 01.08.2012|  Ersetzt durch: 028_F
031 | 031 | 031 | Italienisch   |01.08.2006 | Ersetzt durch: 031_F
032 | 032 | 032 | Latein nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen (Kurs/Fach BBS)  | 01.08.2006|  Ersetzt durch: 032_F
039 | 039 | 039 | Wirtschaft/Politik  |01.08.2006 | Ersetzt durch: 039_F
041 | 041 | 041 | Rechtskunde| 01.08.2006|  Ersetzt durch: 041_F
045 | 045 | 045 | "Russisch nur übergreifender Unterricht 2.- 4. Fremdspr. zusammen (Kurs/Fach BBS)  | 01.08.2014  |Ersetzt durch: 045_F
047_F | 047_F|  047F|  Heimat-, Welt- und Sachunterricht (Fach)   |01.08.2015  |Textänderung
051 | 051 | 051 | "Spanisch nur übergreifender Unterricht 2. - 4. Fremdspr. zusammen (Kurs/Fach BBS) | 01.08.2014 | Ersetzt durch: 051_F
052 | 052 | 052|  "Türkisch | 01.08.2008 | Ersetzt durch: 052_F
075 | 075 | 075 | "Friesisch  |01.08.2006 | Ersetzt durch: 075_F
-  |111|  111 | Dänisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)  |01.08.2015 | Textänderung
-  |116 | 116 | Englisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen) | 01.08.2015 | Textänderung
-  |117 | 117  |"Wirtschaftslehre/Wirtschaft | 01.08.2006| Ersetzt durch: 117_F und 042_K
-  |122|  122 | Französisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)  |01.08.2015|  Textänderung
-  |132  |132|  Latein - 1. Fremdsprache (Fach)(Kurs, neu begonnen) | 01.08.2015 | Textänderung
143 | 143 | 143 | "Religion, katholisch | 01.08.2006|  Ersetzt durch: 143_F
144 | 144 | 144| Religion, evangelisch | 01.08.2006|  Ersetzt durch: 144_F
-  |211 | 211|  Dänisch - 2. Fremdsprache | 01.08.2006|  Ersetzt durch: 211_F
-  |216|  216 | Englisch - 2. Fremdsprache  |01.08.2006 | Ersetzt durch: 216_F
- | 222 | 222  |Französisch - 2. Fremdsprache | 01.08.2006 | Ersetzt durch: 222_F
- | 232 | 232 | Latein - 2. Fremdsprache  |01.08.2006 | Ersetzt durch: 232_F
- | 245_K | 245K | Russisch - 1. Fremdsprache, fortgeführt Kurs  |01.08.2015 | Textänderung, Achtung: Bedeutung verändert!
- | 251 | 251 | Spanisch- 2. Fremdsprache | 01.08.2006 | Ersetzt durch: 251_F
- | 311 | 311 | Dänisch- 3. Fremdsprache  |01.08.2006 | Ersetzt durch: 311_F
- | 316 | 316 | Englisch - 3. Fremdsprache | 01.08.2006 | Ersetzt durch: 316_F
- | 322 | 322 |Französisch- 3. Fremdsprache | 01.08.2006 | Ersetzt durch: 322_F
-  |332 | 332 | Latein - 3. Fremdsprache |01.08.2006 | Ersetzt durch: 332_F
- | 345 | 345 | Russisch - 3. Fremdsprache  |01.08.2006 | Ersetzt durch: 345_F
- | 351 | 351 | Spanisch - 3. Fremdsprache | 01.08.2006 | Ersetzt durch: 351_F
- | 411 | 411 | Dänisch - 4. Fremdsprache | 01.08.2006 | Ersetzt durch: 411_F
- | 422 | 422 | Französisch - 4. Fremdsprache | 01.08.2006  |Ersetzt durch: 422_F
- | 432 | 432 | Latein - 4. Fremdsprache  |01.08.2006 | Ersetzt durch: 432_F
- | 445 | 445  |Russisch - 4. Fremdsprache | 01.08.2006 | Ersetzt durch: 445_F
- | 451 | 451 | Spanisch - 4. Fremdsprache | 01.08.2006 | Ersetzt durch: 451_F
- | 503 | 503 | Datenverarbeitungstechnik | 01.08.2006  |Ersetzt durch: 503_F und 550_K
- | 509 | 509 | Maschinenbautechnik | 01.08.2006 | Ersetzt durch: 509_F
514 | 514 | 514 | "Sporttheorie  |01.08.2006 | Ersetzt durch: 514_F
970 | 970 | 970|  "WPU - sonstiges Fach | 01.08.2013  Ersetzt durch: 970_F

### Vollständige Übersicht der Fächer und Kurse (Stand 2016/17)

Verwendung    | Kuerzel | Schlüssel | Bezeichnung
--------------|---------|-----------|---------------------------------------------------------------------------------
Fach          | 007_F   | 007F      | Bildhaftes Gestalten/Design (Fach)
Fach          | 009_F   | 009F      | Gemeinschaftskunde (Fach)
Fach          | 011_F   | 011F      | Dänisch nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen (Fach BBS)
Fach          | 016_F   | 016F      | Englisch nur übergreifender Unterricht  - 1.-3. Fremdspr. zusammen (Fach BBS)
Fach          | 017_F   | 017F      | Geographie (Fach)
Fach          | 018_F   | 018F      | Haushaltslehre (Fach)
Fach          | 019_F   | 019F      | Astronomie (Fach)
Fach          | 020_F   | 020F      | Politik (Fach)
Fach          | 022_F   | 022F      | Französisch nur übergreifender Unterricht - 1.- 4. Fremdspr. zusammen (Fach BBS)
Fach          | 023_F   | 023F      | Geschichte (Fach)
Fach          | 024_F   | 024F      | Altgriechisch (Fach)
Fach          | 025_F   | 025F      | Geologie (Fach)
Fach          | 027_F   | 027_F     | Textillehre (Fach)
Fach          | 028_F   | 028F      | Neugriechich (Fach)
Fach          | 031_F   | 031F      | Italienisch (Fach)
Fach          | 032_F   | 032F      | Latein nur übergreifender Unterricht - 1.-4. Fremdspr. zusammen (Fach BBS)
Fach          | 037_F   | 037F      | Kunstgeschichte (Fach)
Fach          | 039_F   | 039F      | Wirtschaft/Politik (Fach)
Fach          | 040_F   | 040F      | Orchester/Chor (Fach)
Fach          | 041_F   | 041F      | Rechtskunde (Fach)
Fach          | 045_F   | 045F      | Russisch nur übergreifender Unterricht  2.- 4. Fremdspr. zusammen (Fach BBS)
Fach          | 047_F   | 047F      | Heimat-, Welt- und Sachunterricht (Fach)
Fach          | 051_F   | 051F      | Spanisch nur übergreifender Unterricht  2. - 4. Fremdspr. zusammen (Fach BBS)
Fach          | 052_F   | 052F      | Türkisch (Fach)
Fach          | 053_F   | 053F      | Technik (Fach)
Fach          | 054_F   | 054F      | Polnisch (Fach)
Fach          | 056_F   | 056F      | Technisches Werken (Fach)
Fach          | 074_F   | 074F      | Deutsch als Zweitsprache (Fach)
Fach          | 075_F   | 075F      | Friesisch (Fach)
Fach          | 076_F   | 076F      | Niederdeutsch (Fach)
Fach          | 083_F   | 083F      | Heilpädagogik (Fach)
Fach          | 089_F   | 089F      | Sonderpädagogik (Fach)
Fach          | 093_F   | 093F      | Eurythmie (Fach)
Fach          | 094_F   | 094F      | Naturwissenschaft (Fach)
Fach          | 115_F   | 115F      | Weltkunde (Fach)
Fach          | 117_F   | 117F      | Wirtschaftslehre/Wirtschaft (Fach)
Fach          | 141_F   | 141F      | Ethik (Fach)
Fach          | 142_F   | 142F      | Islamunterricht (Fach)
Fach          | 143_F   | 143F      | Religion, katholisch (Fach)
Fach          | 144_F   | 144F      | Religion, evangelisch (Fach)
Fach          | 163_F   | 163F      | Türkisch (Fach)
Fach          | 211_F   | 211F      | Dänisch - 2. Fremdsprache (Fach)
Fach          | 216_F   | 216F      | Englisch - 2. Fremdsprache (Fach)
Fach          | 222_F   | 222F      | Französisch - 2. Fremdsprache (Fach)
Fach          | 232_F   | 232F      | Latein - 2. Fremdsprache (Fach)
Fach          | 251_F   | 251F      | Spanisch - 2. Fremdsprache (Fach)
Fach          | 311_F   | 311F      | Dänisch - 3. Fremdsprache (Fach)
Fach          | 316_F   | 316F      | Englisch - 3. Fremdsprache (Fach)
Fach          | 322_F   | 322F      | Französisch - 3. Fremdsprache (Fach)
Fach          | 332_F   | 332F      | Latein - 3. Fremdsprache (Fach)
Fach          | 345_F   | 345F      | Russisch - 3. Fremdsprache (Fach)
Fach          | 351_F   | 351F      | Spanisch - 3. Fremdsprache (Fach)
Fach          | 411_F   | 411F      | Dänisch - 4. Fremdsprache (Fach)
Fach          | 422_F   | 422F      | Französisch - 4. Fremdsprache (Fach)
Fach          | 432_F   | 432F      | Latein - 4. Fremdsprache (Fach)
Fach          | 445_F   | 445F      | Russisch - 4. Fremdsprache (Fach)
Fach          | 451_F   | 451F      | Spanisch - 4. Fremdsprache (Fach)
Fach          | 452_F   | 452F      | sonstige moderne Fremdsprachen (Fach)
Fach          | 453_F   | 453F      | sonstige alte Fremdsprachen (Fach)
Fach          | 503F    | 503_F     | Datenverarbeitungstechnik (Fach)
Fach          | 505_F   | 505F      | Ernährungslehre mit Chemie (Fach)
Fach          | 509_F   | 509F      | Maschinenbautechnik (Fach)
Fach          | 510_F   | 510F      | Pädagogik/Psychologie (Fach)
Fach          | 512_F   | 512F      | Rechnungswesen (Fach)
Fach          | 514_F   | 514F      | Sporttheorie (Fach)
Fach          | 516_F   | 516F      | Wirtschaftstheorie und -politik (Fach)
Fach          | 517_F   | 517F      | Wirtschaftsenglisch (Fach)
Fach          | 600_F   | 600F      | Dänisch (USPR)
Fach          | 601_F   | 601F      | Englisch (USPR)
Fach          | 602_F   | 602F      | Französisch (USPR)
Fach          | 605_F   | 605F      | Spanisch (USPR)
Fach          | 910_F   | 910F      | Seminarfach (Fach)
Fach          | 916_F   | 916F      | Arbeitsgemeinschaft (AG) (Fach)
Fach          | 919_F   | 919F      | WPU - Gestalten (Fach)
Fach          | 920_F   | 920F      | WPU - 2. Fremdsprache (Fach)
Fach          | 921_F   | 921F      | WPU - Naturwissenschaften (Fach)
Fach          | 922_F   | 922F      | WPU - Gesellschaftswissenschaften (Fach)
Fach          | 923_F   | 923F      | WPU - Arbeit/Wirtschaft und Verbraucherbildung (Fach)
Fach          | 924_F   | 924F      | WPU - Ästhetische Bildung (Fach)
Fach          | 925_F   | 925F      | WPU - Sport (Fach)
Fach          | 928_F   | 928F      | WPU - Wirtschaftslehre (Fach)
Fach          | 929_F   | 929F      | WPU - Technik (Fach)
Fach          | 930_F   | 930F      | WPU - Angewandte Informatik (Fach)
Fach          | 931_F   | 931F      | WPU - Darstellendes Spiel (Fach)
Fach          | 970_F   | 970F      | WPU - sonstiges Fach (Fach)
Kurs          | 040_K   | 040K      | Religion (Kurs)
Kurs          | 041_K   | 041K      | Religion / Ethik (Kurs)
Kurs          | 042_K   | 042K      | Wirtschaftslehre (Kurs)
Kurs          | 145_K   | 145K      | Russisch - 1. Fremdsprache (Kurs, neu begonnen)
Kurs          | 151_K   | 151K      | Spanisch - 1. Fremdsprache (Kurs, neu begonnen)
Kurs          | 152_K   | 152K      | Türkisch - 1. Fremdsprache (Kurs, neu begonnen)
Kurs          | 211_K   | 211K      | Dänisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 216_K   | 216K      | Englisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 222_K   | 222K      | Französisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 232_K   | 232K      | Latein - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 245_K   | 245K      | Russisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 251_K   | 251K      | Spanisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 252_K   | 252K      | Türkisch - 1. Fremdsprache, fortgeführt (Kurs)
Kurs          | 311_K   | 311K      | Dänisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 316_K   | 316K      | Englisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 322_K   | 322K      | Französisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 332_K   | 332K      | Latein - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 345_K   | 345K      | Russisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 351_K   | 351K      | Spanisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 352_K   | 352K      | Türkisch - 2. Fremdsprache, neu begonnen (Kurs)
Kurs          | 411_K   | 411K      | Dänisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs          | 416_K   | 416K      | Englisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs          | 422_K   | 422K      | Französisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs          | 432_K   | 432K      | Latein - 2. Fremdsprache, fortgeführt (Kurs)
Kurs          | 445_K   | 445K      | Russisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs          | 451_K   | 451K      | Spanisch - 2. Fremdsprache, fortgeführt (Kurs)
Kurs          | 452_K   | 452K      | Türkisch, 2. Fremdsprache (Kurs)
Kurs          | 506_K   | 506K      | Gemeinschaftskunde (Kurs)
Kurs          | 517_K   | 517K      | Agrarbiologie (Kurs)
Kurs          | 518_K   | 518K      | Biotechnologie (Kurs)
Kurs          | 519_K   | 519K      | Technik (Kurs)
Kurs          | 520_K   | 520K      | Berufliche Informatik (Kurs)
Kurs          | 521_K   | 521K      | Ernährung (Kurs)
Kurs          | 522_K   | 522K      | Erziehungswissenschaften (Kurs)
Kurs          | 523_K   | 523K      | Rechnungswesen (auslaufend) (Kurs)
Kurs          | 525_K   | 525K      | Betriebswirtschaftslehre (Kurs)
Kurs          | 526_K   | 526K      | Volkswirtschaftslehre (Kurs)
Kurs          | 545_K   | 545K      | Erneuerbare Energien (Kurs)
Kurs          | 550_K   | 550K      | Datenverarbeitungstechnik (Kurs)
Kurs          | 551_K   | 551K      | Ernährungslehre / Diätetik, Körperpflegekunde (Kurs)
Kurs          | 552_K   | 552K      | Hauswirtschaft (Kurs)
Kurs          | 553_K   | 553K      | Ökotrophologie (Kurs)
Kurs          | 554_K   | 554K      | Chemisch-pharmazeutische Übungen (Kurs)
Kurs          | 555_K   | 555K      | Galenische Übungen (Kurs)
Kurs          | 556_K   | 556K      | Medizinproduktekunde (Kurs)
Kurs          | 557_K   | 557K      | Pharmazietechnik (Kurs)
Kurs          | 558_K   | 558K      | Ökologie und Gesundheit (Kurs)
Kurs und Fach | 3       | 3         | Physik
Kurs und Fach | 6       | 6         | Kunst
Kurs und Fach | 8       | 8         | Biologie
Kurs und Fach | 10      | 10        | Chemie
Kurs und Fach | 12      | 12        | Mathematik
Kurs und Fach | 13      | 13        | Datenverarbeitung/Informatik
Kurs und Fach | 14      | 14        | Deutsch
Kurs und Fach | 26      | 26        | Sport
Kurs und Fach | 36      | 36        | Musik
Kurs und Fach | 38      | 38        | Philosophie
Kurs und Fach | 111     | 111       | Dänisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach | 116     | 116       | Englisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach | 122     | 122       | Französisch - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach | 132     | 132       | Latein - 1. Fremdsprache (Fach)(Kurs, neu begonnen)
Kurs und Fach | 500     | 500       | Agrartechnik mit Biologie
Kurs und Fach | 501     | 501       | Bautechnik
Kurs und Fach | 502     | 502       | Darstellendes Spiel
Kurs und Fach | 504     | 504       | Elektrotechnik
Kurs und Fach | 507     | 507       | Gesundheit
Kurs und Fach | 508     | 508       | Literatur
Kurs und Fach | 513     | 513       | Rechtslehre
Kurs und Fach | 515     | 515       | Wirtschaftsgeographie
Kurs und Fach | 999     | 999       | sonstiges Fach, sonstiger Kurs

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

### UART – Unterrichtsarten in Magellan

Die für die Statistik abgefragten Schlüsselwerte können zu Teil nicht genutzt werden, weil Magellan-interne Eingaben für den Zeugnisdruck oder die Zeugniserstellung erwartet werden.

Die nachfolgende Tabelle zeigt Ihnen welche Magellan-Eintragungen erkannt und in entsprechende Werte für die Statistikwerte gewandelt werden.

!!! info "Hinweis"
  Ist die Unterrichtsart leer, nicht der Fachstatus WahlPF oder Freiw gewählt, oder entspricht keinem der nachfolgenden Werte, wird generell der Wert P für Pflichtfach ausgegeben. Es ist kein gesonderter Eintrag für die Unterrichtsart Pflicht notwendig.
  Es wird in den Verzeichnissen Unterrichtsarten und Fachstatus immer der Wert der Spalte Schlüssel berücksichtigt.

Bedeutung                            | Feld           | Schlüssel     | Ausgabe für die Statistikdatei
-------------------------------------|----------------|---------------|-------------------------------
Pflicht                              | Unterrichtsart | P oder leer   | P
Förderunterricht                     | Unterrichtsart | FOE           | U
Freiwilliger Unterricht (AGs)        | Unterrichtsart | AG            | F
Profilgebend                         | Unterrichtsart | P-KURS        | G
Kernfach                             | Unterrichtsart | KF oder E     | K
Zusatzunterricht Mittlerer Abschluss | Unterrichtsart | Z oder ZUSATZ | Z
Wahlpflichtangebot                   | Unterrichtsart | WPU1…WPU4     | W
Wahlpflichtangebot                   | Fachstatus     | WahlPF        | W
Freiwilliger Unterricht (AGs)        | Fachstatus     | Freiw         | F

### Zur Statistik 2014/2015

In einigen Schlüsselverzeichnissen hat es Änderung gegeben, die ggf. die Bedeutung der Schlüssel ändern und Sie damit gezwungen sind, bei den betroffenen Datensätzen die Auswahl zu erneuern.

#### Bildungsgänge

Kuerzel | Schluessel | Alte Bezeichnung                          | Neue Bezeichnung
--------|------------|-------------------------------------------|---------------------------------------------------------------
901     | 901        | BS – Zusatzunterricht Hauptschulabschluss | BS - Zusatzunterricht Erster allgemeinbildender Schulabschluss

#### Klassenstufen

Kuerzel | Schluessel | Alte Bezeichnung                           | Neue Bezeichnung
--------|------------|--------------------------------------------|-------------------------------------------
Q3      | Q3         | Qualifikationsphase 3 (14. Jahrgangsstufe) | Qualifikationsphase 3 (ehemals 13. Jgst.)
Q5      | Q5         | -                                          | Qualifikationsphase 5 (14. Jahrgangsstufe)

#### Schularten, Schulformen

Kuerzel | Schluessel | Alte Bezeichnung    | Neue Bezeichnung
--------|------------|---------------------|-----------------------------------
120     | 120        | Gemeinschaftsschule | Gemeinschaftsschule mit Oberstufe
115     | 115        | -                   | Gemeinschaftsschule ohne Oberstufe

#### Herkunft (Schulformen)

Kuerzel | Schluessel | Alte Bezeichnung                     | Neue Bezeichnung
--------|------------|--------------------------------------|----------------------------------------------------
17      | 17         | Zugang aus einer Gemeinschaftsschule | Zugang aus einer Gemeinschaftsschule mit Oberstufe
15      | 15         | -                                    | Zugang aus einer Gemeinschaftsschule ohne Oberstufe

#### Weggefallene Felder, die nicht mehr erfragt werden

Nur für die aktuellen Schüler der allgemeinbildenden Schule wird die Schulübergangsempfehlung der Grundschule (SAE) nicht mehr erfragt.

### Zur Statistik 2013/2014

Gastschüler werden aus der Statistik ausgeschlossen, wenn Sie in Magellan den entsprechenden Schüler unter `Schüler > Daten 3 > Verschiedenes > Gastschüler` als Gastschüler markieren.

### Zur Statistik 2012/2013

Das Feld SAE wurde bisher unter `Schüler > Laufbahn > Empfehlung` gespeichert. Ab der Statistik 2012/2013 wird dieser Wert nun unter `Schüler > Zugang/Abgang > Zugang – Empfehlung` gespeichert.

Die bereits unter `Schüler > Laufbahn > Empfehlung` eingetragen Werte können über die eine spezielle Funktion in das Feld `Schüler > Zugang/Abgang > Zugang – Empfehlung` kopiert werden.

Dazu gehen Sie wie folgt vor:

1. Starten die den Magellan-Administrator.
2. Wählen Sie „Datenbankpflege“.
3. Klicken Sie bei „Datenbank prüfen“ auf die Schaltfläche „Start“.
4. Wählen Sie „Empfehlungen umkopieren“ und klicken Sie dann auf OK.

### Zur Statistik 2011/2012

#### Erstmalig Statistik für Berufsbildende Schulen

In diesem Jahr spielen wir erstmalig auch die Statistik für Berufsbildende Schulen aus.
Aus Gründen der Übersichtlichkeit werden die neu hinzugekommenen BBS Felder werden nicht gesondert farblich im Anhang dargestellt. Sie bekommen lediglich ein „*“ in der Spalte Statistikdatei.

#### Statistikdatei „BM“ - Besondere Massnahmen

Die Statistikdatei „Besondere Massnahmen“ wird vom Statistikamt ab diesem Jahr nicht mehr erfragt. Damit fallen auch alle Eingaben dazu in Magellan und DaVinci raus.

Die Bezeichnungen der Schlüssel werden aus Gründen der Eindeutigkeit von Schlüsseln nicht geändert. Von Zeit zu Zeit erhalten bestehende Schlüssel neue Bedeutungen und es wird lediglich die Bezeichnung verändert. Solche Schlüssel müssen von Ihnen manuell verändert werden.

Weggefallene Felder, die nicht mehr erfragt werden:

* MIGST – Migrantenstatus (SA)
* HEIM – Heimunterbringung (SA)
