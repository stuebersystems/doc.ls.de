# Magellan-Data Warehouse

!!! warning "Wichtig"

     *Magellan 6*: Nur für die Statistik im Bundesland Niedersachsen wird das Data Warehouse benötigt, alle anderen Statistiken werden direkt aus Magellan erzeugt.
     
     *Magellan 7*: Für alle Regionen, für die Statistikschnittstellen angeboten werden, wird die Statistik ohne den Umweg über das Data Warehouse direkt aus Magellan erzeugt.

## Magellan-DWH Explorer

Das Magellan-Data Warehouse ist eine Datenbank, die von der aktuellen Magellan -Datenbank getrennt ist. Sie dient als Basis für die Erstellung einiger Statistiken. Das Magellan-Datawarehouse wird dafür sowohl von Magellan als auch von DaVinci mit den notwendigen Daten versorgt. Eine manuelle Eingabe in das Magellan-Datawarehouse ist nicht möglich. Über den Magellan-Data Warehouse-Explorer (Kurzform: Magellan-DWH Explorer) können Sie den Inhalt des Magellan-Data Warehouses betrachten und die entsprechenden Landesstatistiken erstellen.

Um den Magellan-DWH Explorer zu starten, gehen Sie wie folgt vor:

* Klicken Sie auf `Start`, dann auf `Programme`, dann auf `STÜBERSYSTEMS` und dann auf `Magellan-Data Warehouse-Explorer`.

* Alternativ können Sie den `Magellan-Data Warehouse-Explorer` auch direkt aus Magellan starten. Gehen Sie dazu in Magellan auf `Ansicht > Data Warehouse` und wählen Sie dann die Option `Magellan-DWH Explorer starten`.

![In Magellan können Sie hier den MagellanDWHExplorer starten](/assets/images/DWH1.png)

### Datenbestand betrachten

Nach dem Start des Magellan-DWH Explorers, können Sie den Datenbestand des Magellan-Data Warehouses betrachten. Gehen Sie dazu auf `Ansicht > Archivierte Daten`. Alle Daten im Magellan-Data Warehouse sind mit einem Zeitstempel versehen, der aus einem Anfangs- und Enddatum besteht. Dadurch können die im Magellan-Data Warehouse archivierten Daten eindeutig den Zeiträumen in Magellan zugeordnet werden. Um den Datenbestand zu betrachten, müssen Sie auf der Registerkarte `Auswahl` immer einen Mandanten und einen aktuellen Zeitpunkt auswählen, zu dem Sie die archivierten Daten betrachten möchten.

![ Wählen Sie hier einen Mandanten und einen Zeitpunkt aus.](/assets/images/DWH2.png)

### Datenbestand auswerten

Auf Basis der archivierten Daten können Sie diverse Landesstatistiken erstellen und Berichte drucken. Wechseln Sie dazu in den Bereich „Auswertungen“. Die Berichte dienen dabei hauptsächlich der Kontrolle der erstellten Dateien für die Landesstatistiken.
