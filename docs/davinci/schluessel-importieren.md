# Schlüssel nach DAVINCI importieren

Die verfügbaren Schlüsselverzeichnisse sehen Sie im Dialogfenster `Schlüsselverzeichnisse`, das Sie über die Schaltfläche Schlüsselverzeichnisse in der Menügruppe `Start > Stammdaten` öffnen können.

> #### info::
> Wenn Sie sich nicht mehr im Programmbereich „Stammdaten“ befinden, können Sie die Schlüsselverzeichnisse alternativ über das Menüregister `Extras > Verwalten`öffnen. Die Schaltfläche `Schlüsselverzeichnisse` steht Ihnen hier in allen Programmbereichen zur Verfügung.

![Das Auswahlfenster „Schlüsselverzeichnisse](/assets/images/DAVINCI.schluessel.png)

Klicken Sie auf das Schlüsselverzeichnis, welches Sie bearbeiten wollen und dann auf „Bearbeiten“, um das betreffende Schlüsselverzeichnis Dialogfenster zu öffnen.

![Das Dialogfenster zum Importieren von Schlüsseln](/assets/images/DAVINCI.schluessel-importdialog.png)

Über `Importieren` können Sie Schlüsselverzeichnisse importieren, die von DAVINCI oder von Ihrem Bundesland in einer entsprechenden Schlüsseldatei zur Verfügung gestellt werden. Beim Importieren werden Schlüssel anhand des Kürzels oder des Schlüssels identifiziert: Bestehende Schlüssel werden überschrieben, neue angefügt.


!!! info "Hinweis"

    DAVINCI erwartet Schlüsseldateien mit der Endung .KEYS und mit der Nummer des Schlüsselverzeichnisses – siehe Dialogfenster `Extras > Schlüsselverzeichnisse` – als Präfix im Dateinamen, also z.B. „23_Unterrichtsarten.keys“. Standardmäßig sollten die so benannten Schlüsseldateien im Schlüsseldateien Ordner liegen, siehe Dialogfenster `Extras > System-Informationen` Ordner `DAVINCIKeysFolder`.

Die Einträge in einer Schlüsseldatei müssen in einer TXT-, CSV- oder KEYS-Datei in einem bestimmten Format gespei-chert sein. Eine Zeile des Schlüsselverzeichnisses entspricht dabei einer Zeile in der Importdatei. Das Format der CSV-Datei können Sie dem folgenden Beispiel entnehmen:

```
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
"AG";"AG";"Arbeitsgemeinschaft";;
"BL";"BL";"Besondere Lernleistung";;
"BU";"BU";"Berufsbezogener Unterricht";;
```
