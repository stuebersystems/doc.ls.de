# Nordrhein-Westfalen - ABS und BBS

Das Ministerium für Schule und Weiterbildung des Landes Nordrhein-Westfalen fordert mehrmals im Jahr eine statistische Erhebung von den Schulen.
Mit dem Landesstatistik-Modul können Sie die benötigten Statistikdaten direkt aus MAGELLAN und DAVINCI in die Dateien für den Datenaustausch mit dem Programm ASDPC des Schulministeriums exportieren.

## Einführung

Der Export kann jederzeit für das aktuelle Halbjahr auf Basis der Daten in MAGELLAN in elektronischer Form vorgenommen werden. Die Statistikdaten werden wie gefordert im Dateiformat aus MAGELLAN erzeugt.
Für Sie als Schule bedeutet dies: Sie müssen die folgenden Textdateien je nach Schulart in das entsprechende Statistikprogramm importieren: 

Dateiname|Inhalt|Kapitel
--|--|--
xxxxx_SIM_YYYYMMDD.TXT |nur MAGELLAN-Daten|[SIM.TXT](schuelerdaten.md)
xxxxx_LEHRER_YYYYMMDD.TXT |MAGELLAN-Daten und aus DAVINCI der „Allgemeine Statistikexport“|[LEHRER.TXT](lehrerdaten.md)
xxxxx_ABI_YYYYMMDD.TXT |nur MAGELLAN-Daten|[ABI.TXT](abiturdaten.md)
EXTERN.DAT|nur DAVINCI-Daten aus dem Export für „ASDPC/EXTERN.DAT“|[EXTERN.DAT](stundenplandaten.md)

Hierbei steht xxxxx für Ihre Schulnummer und YYYYMMDD für das Erstellungsdatum der Datei.

!!! info "Hinweis"

     Sie müssen die xxxxx_SIM_YYYYMMDD.TXT für den Import in ASDPC vorher in SIM.TXT umbenennen, da sonst ASDPC die Datei nicht annimmt.

Die Datei SIM.TXT wertet Daten aus dem aktuellen Halbjahr (1. Halbjahr 2018/2019), sowie dem gesamten vorangehenden Schuljahr (1. und 2. Halbjahr 2017/2018) aus. Die Schnittstelle kann sowohl für die Haupterhebung im Herbst wie auch für die Halbjahreserhebung genutzt werden. Im Unterschied zur Haupterhebung ist für die Halbjahreserhebung nur die Datei SIM.TXT zu erzeugen.

## DAVINCI-LIZENZ?

Eine DAVINCI Lizenz wird nur für die EXTERN.DAT und die LEHRER.TXT benötigt, da diese Stundenplandaten enthalten. Jede Datei kann einzeln erzeugt werden, somit benötigen Sie z.B. kein DAVINCI wenn Sie lediglich die SIM.TXT oder die ABI.TXT erzeugen möchten.

## Notwendige Schritte


1. Schritt: [Statistikschlüssel aktualisieren](../schluesselverzeichnisse.md) 
2. Schritt: Dateneingabe
3. Schritt: [Datenprüfung](https://doc.ls.stueber.de/datenpruefung/)
4. Schritt: Statistikdateien erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

Statistikämter setzen für einige Felder Wertelisten voraus, die STÜBER SYSTEMS in Form von Schlüsselverzeichnissen zur Verfügung stellt. Bitte lesen Sie dazu den Abschnitt [Schlüsselverzeichnisse importieren](../schluesselverzeichnisse.md).

## Voraussetzungen für alle Statistikdaten

Damit die Statistikdateien korrekt erstellt und gefüllt werden können, müssen in MAGELLAN bestimmte Datenfelder immer gefüllt werden.


| Statistikfeld in der Statistikdatei | Datenfeld in MAGELLAN/DAVINCI            | Beschreibung                             |
|-------------------------------------|------------------------------------------|------------------------------------------|
| ALLE Statistikdateien               | MAGELLAN:<br/>`Mandanten > Daten 2 > Schulformen` | Hauptschulform Ihrer Schule. <br/>Bei Berufskollegs = BK. <br/>Wichtig: <br/>MAGELLAN sortiert die Schulformen. Die Schulform sollte als erste erscheinen. Um sicher zu gehen, sollten Sie zuerst alle Schulformen entfernen und dann die Hauptschulform als Erstes eintragen. |
| Pruefstatus (ABI.TXT)               | MAGELLAN:<br/>`Schüler > Abschluss > Abschluss 1 > Abschlussart` | Für Berufskollegs: <br/>Es werden nur Schüler in der ABI.TXT berücksichtigt, die das Abitur bestanden haben und dementsprechend, das Statistikfeld Pruefstatus auf Wert 1 gesetzt haben. Das Feld berechnet sich gemäß der Eingaben in `MAGELLAN > Abitur > Prüfung > Status` |


## Besonderheiten

### Verzeichnis Abgangsarten (BBS) / Abschlüsse Extern (BBS) / Abschlüsse Intern (BBS)



| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| **0F**        | Mittlerer Abschluss (FOS-Reife ohne Qualifikationsvermerk/Berechtigung zum Besuch der gymn. OS)<br/>Zuvor: Mittlerer Abschluss (Fachoberschulreife ohne Qualifikationsvermerk) | Textänderung |
| **0G**        | Mittlerer Schulabschluss (FOS-Reife mit Qualifikationsvermerk/Berechtigung zum Besuch der gymn. OS)<br/>Zuvor: Mittlerer Schulabschluss (nach Klasse 11 für G8 Schüler / FOS-Reife mit Qualifikationsvermerk) | Textänderung |
| **1B**        | Abschlusszeugnis (berufl. Kenntn., Fähigkeiten und Fertigkeiten) und HS-Abschluss gleichw. Abschluss<br/>Zuvor: Abschlusszeugnis und Hauptschulabschluss | Textänderung |
| **3A**        | Berufsschulabschluss (Während der Berufsausbildung keinen höherwertigen ABS-Abschluss erworben)<br/>Zuvor: Berufsschulabschluss (für Schüler mit HS-Abschluss nach Klasse 10 oder höheren Abschluss) | Textänderung |
| **3D**        | Berufsschulabschluss und HS-Abschluss oder gleichwertig nach Klasse 10<br/>Zuvor: Berufsschul- und Hauptschulabschluss nach Klasse 10 | Textänderung |
| **3F**        | Berufsschul- und Mittlerer Schulabschluss (FOS-Reife ohne Berechtigung zum Besuch der gymn. OS)<br/>Zuvor: Berufsschul- und Mittlerer Abschluss (Fachoberschulreife ohne Qualifikationsvermerk) | Textänderung |
| **5F**        | Berufs- und Mittl. Abschluss (FOS-Reife ohne Qualifikationsv./Berechtigung zum Besuch der gymn. OS)<br/>Zuvor: Berufsabschluss und Mittlerer Schulabschluss, FOS-Reife o. Qualifikationsvermerk(nur Hiberniakolleg) | Textänderung |
| **5G**        | Berufs- und Mittl. Abschluss (FOS-Reife mit Qualifikationsv./Berechtigung zum Besuch der gymn. OS)<br/>Zuvor: Berufs- und Mittlerer Abschluss (Fachoberschulreife mit Qualifikationsvermerk) | Textänderung |

### Verzeichnis Schulformen (Herkunft) (ABS)

| Schlüssel | Bezeichnung                              | Änderung     |
|-----------|------------------------------------------|--------------|
| **A01**       | Berufsschule, Fachklassen (Teilzeit)<br/>Zuvor: BS;TZ | Textänderung |
| **A02**       | Berufsschule, Fachklassen/Fachhochschulreife (Teilzeit)<br/>Zuvor: BS/FHR; TZ | Textänderung |
| **A03**       | Berufsschule, Fachklassen/erweiterte Zusatzqualifikation (Teilzeit)<br/>Zuvor: BS/ZQ; TZ | Textänderung |
| **A04**       | Berufsschule, Fachklassen mit erweitertem Stützunterricht (Teilzeit)<br/>Zuvor: BS/Stütz; TZ | Textänderung |
| **B01**       | Berufsfachschule, Berufsabschluss/Fachoberschulreife (2-jährig, Vollzeit)<br/>Zuvor: BAB/FOR 2j.; VZ | Textänderung |
| **B02**       | Berufsfachschule, Berufsgrundbildung/Fachoberschulreife (2-jährig, Vollzeit)<br/>Zuvor: BG/FOR 2j.; VZ | Textänderung |
| **B04**       | Berufsfachschule, Berufsabschluss/Fachoberschulreife (nach BKAZVO, BBiG/HwO, in Vollzeit)<br/>Zuvor: BAB/FOR; VZ | Textänderung |
| **B05**       | Berufsfachschule, Berufsabschluss/Fachhochschulreife (nach BKAZVO, BBiG/HwO in Vollzeit)<br/>Zuvor: BAB/FHR; VZ | Textänderung |
| **C01**       | Berufsfachschule, Berufsabschluss/Fachhochschulreife (ohne Berufspraktikum, 3-jährig, Vollzeit)<br/>Zuvor: BAB/FHR 3j.; VZ (ohne Berufspraktikum) | Textänderung |
| **C02**       | Berufsfachschule, Berufsabschluss (2-jährig, Vollzeit)<br/>Zuvor: BAB 2j.; VZ | Textänderung |
| **C03**       | Berufsfachschule, Berufliche Kenntnisse/FHR (HBFS) (2-jährig, Vollzeit)<br/>Zuvor: BK/FHR 2j.; VZ | Textänderung |
| **C05**       | Fachoberschule, Fachoberschule Kl. 11 (1-jährig, Teilzeit)<br/>Zuvor: BK/FHR 1j.; TZ (FOS KL. 11) | Textänderung |
| **C06**       | Fachoberschule, Fachoberschule Kl. 12S (1-jährig, Vollzeit)<br/>Zuvor: BK/FHR 1j.; VZ (FOS KL. 12S) | Textänderung |
| **C07**       | Fachoberschule, Fachoberschule Kl. 12B (2-jährig, Teilzeit)<br/>Zuvor: BK/FHR 2j.; TZ (FOS KL. 12B) | Textänderung |
| **C08**       | Fachoberschule, Fachoberschule Kl. 12B (1-jährig, Vollzeit)<br/>Zuvor: BK/FHR 1j.; VZ (FOS KL. 12B) | Textänderung |
| **D01**       | Berufl. Gymnasium, Berufsabschluss/Allg. Hochschulreife (mit Berufspraktikum; 4-jährig, Vollzeit)<br/>Zuvor: BAB/AHR 4j.; VZ | Textänderung | **D02**       | Berufliches Gymnasium, Berufliche Kenntnisse/Allg. Hochschulreife<br/>zuvor: BK/AHR 3j.; VZ | Textänderung |
| **D05**       | Fachoberschule, Fachoberschule Kl. 13 (1-jährig, Vollzeit)<br/>Zuvor: AHR 1j.; VZ (FOS Kl. 13) | Textänderung |
| **D06**       | Fachoberschule, Fachoberschule Kl. 13 (2-jährig, Teilzeit)<br/>Zuvor: AHR 2j.; TZ (FOS Kl. 13) | Textänderung |
| **E01**       | Fachschule (2-jährig, Vollzeit)<br/>Zuvor: BW 2j.; VZ (FS) | Textänderung |
| **E02**       | Fachschule (4-jährig, Teilzeit)<br/>Zuvor: BW 4j.; TZ (FS) | Textänderung |
| **E03**       | Fachschule (verkürzt/1-jährig, Vollzeit)<br/>Zuvor: BW 1j.; VZ (FS verkürzt) | Textänderung |
| **E04**       | Fachschule (verkürzt/2-jährig, Teilzeit)<br/>Zuvor: BW 2j.; TZ (FS verkürzt) | Textänderung |
| **E05**       | Fachschule für Sozialwesen (mit Berufspraktikum/3-jährig, Vollzeit)<br/>Zuvor: BAB/FT 3j.; VZ (FS f. Sozialwesen) | Textänderung |
| **E07**       | Fachschule für Sozialwesen (mit Berufspraktikum/6-jährig, Teilzeit)<br/>Zuvor: BAB/FT 6j.; TZ (FS f. Sozialwesen) | Textänderung |
| **E13**       | Fachschule (3-jährig, Teilzeit)<br/>Zuvor: BW 3j.; TZ (FS) | Textänderung |


## 2015/2016

### 00_Staatsangehoerigkeiten

Bitte ändern Sie folgende Schlüssel manuell um, da das Statistikamt die Bedeutung der Schlüssel für dieses Jahr verändert hat.


| Kürzel | Schlüssel | Bezeichnung  |
|--------|-----------|--------------|
| 465    | 465       | taiwanesisch |

### Förderschwerpunkt2

Der 2. Förderschwerpunkt wurde in der Vergangenheit mangels passender Felder im Feld „Behinderung“ abgefragt. Dies ändert sich dieses Jahr. Sie müssen den 2. Förderschwerpunkt im neuen Feld „Schwerpunkt 2“ eintragen. 

Wenn Sie bereits eingetragenen Werte im Feld „Behinderung“ haben, führen Sie bitte im MAGELLAN-Administrator den Punkt  `Datenbankpflege > Datenbank überprüfen >  NRW: Förderschwerpunkte umkopieren` aus. Dieser kopiert den Wert aus „Behinderung“ nach „Schwerpunkt 2“ und entfernt den Wert dann aus „Behinderung“.

Achten Sie bitte darauf, dass dieser Vorgang erst nach dem Import der Schlüsselverzeichnisse durchgeführt werden darf.

## 2014/2015


Die Abiturstatistik enthielt noch einige Ungereimtheiten die korrigiert wurden. Es müssen für dieses Jahr entweder das zusätzliche Schlüsselverzeichnis „Abschlussarten“ importiert werden, oder die drei Werte werden manuell in MAGELLAN nachgetragen. Die fehlenden Schlüssel lauten wie folgt:

### 00_Abschlussarten


| Kürzel     | Schlüssel | Bezeichnung                 |
|------------|-----------|-----------------------------|
| ABI        | 1         | Abitur bestanden            |
| Kein ABI   | 2         | Abitur nicht bestanden      |
| Keine Zul. | 3         | Nicht zum Abitur zugelassen |
