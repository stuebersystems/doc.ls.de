# GPC (Gesundheitsstatistik per PC)

## Allgemein
Mit dem IT-Programm GPC (Gesundheitsstatistik per PC) kann die Zahl der statistikrelevanten Krankentage aller Lehrkräfte mit einem Dienst- oder Arbeitsverhältnis zum Land NRW elektronisch erfasst werden und in den jährlichen Bericht der Landesregierung über den Krankenstand in der Landesverwaltung NRW für den Landtag NRW einfließen.

## Statistikexport NRW GPC – Krankheitsstatistik mit DAVINCI

In DAVINCI können Sie den Statistikexport GPC durchführen. Als Voraussetzung für einen erfolgreichen Export müssen Sie bestimmte Angaben in DAVINCI machen, die nachfolgend beschrieben sind. 

## Notwendige Angaben in DAVINCI

Geben Sie die notwendigen Daten in DAVINCI an.

1. ``Stammdatenfenster > Lehrer``: Tragen Sie in Spalte "Geb.Datum" das Geburtsdatum Ihrer Lehrer ein.

![](/assets/images/Stammdaten.Lehrer.Gebdatum.png)

2. In DAVINCI gibt es das neue Schlüsselverzeichnis „Lehrerfehlgrunddetails“.

![Schlüsselverzeichnis "Lehrerfehlgrunddetails"] (/assets/images/Lehrerfehlgrunddetails.png)

Wir liefern dafür ein entsprechendes Verzeichnis, welches Sie unter ``Schlüsselverzeichnisse|Lehrerfehlgrunddetails`` importieren können.

 ...\Stueber Systems\daVinci 6\Schlüssel\10_Lehrerfehlgrunddetails.keys

![Import Schlüsselverzeichnis] (/assets/images/Lehrerfehlgrunddetails01.png)

Folgende Lehrerfehlgrunddetails stehen Ihnen nach dem Import zur Verfügung:

![](/assets/images/Lehrerfehlgrunddetails02.png)

Auf diese können Sie im "Fehlzeit"-Dialog im VERTRETUNGSPLAN zurückgreifen. Für Lehrer können Sie nun noch feiner bestimmen, was KRANK bedeutet, also z.B. KRANK mit Attest usw.. 

![](/assets/images/Fehlzeit-Dialog.png)

## Notwendige Daten aus DAVINCI erzeugen

So exportieren Sie in DAVINCI 6 die Daten

1. Klicken Sie auf ``Plan|Importieren und Exportieren``.
2. Wählen Sie im Dialogfenster ``Import/Export-Assistent`` die Option ``Statistikdaten exportieren`` und klicken Sie dann auf Weiter.
3. Wählen Sie die Option ``Statistik Nordrhein-Westfalen GPC exportieren`` und klicken Sie dann auf Weiter.

![](/assets/images/GPC.png)

4. Wählen Sie entsprechend der gewählten Auswahl den Namen der Exportdatei an. 

![](/assets/images/GPC.Dateiname.png)

5. Klicken Sie auf OK. Die Datei wird erzeugt.
6. Die Summendaten exportieren Sie bitte aus der Übersicht "Lehrer-Arbeitstage". (Bereich "Übersichten|Lehrer Arbeitstage"). Der "Lehrer-Fehlgrund-Schlüssel" für Krankheiten muss den Wert "krank" haben.

## Export der Summendaten aus der Übersicht "Lehrer-Arbeitstage"

So exportieren Sie die Summendaten aus der Übersicht "Lehrer-Arbeitstage":

1. Wechseln Sie in den Bereich "Übersichten" und wählen hier "Lehrer Arbeitstage" aus.

![](/assets/images/uebersicht.Lehrer.Arbeitstage.png)