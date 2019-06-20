# Schlüssel nach MAGELLAN importieren

Um die Schlüssel in MAGELLAN zu verwenden, müssen sie vorab importiert werden. Bitte gehen Sie dazu folgendermaßen vor:

1. Starten Sie den Magellan-Administrator.
2. Wechseln Sie in die Ansicht ```Datenimporte```.
3. Klicken Sie auf Starten im Punkt ```Schlüsselverzeichnisse importieren```.
4. Im Dialogfenster geben Sie Ihr Bundesland, Ihrer Schulart und Mandanten (Ihre Schule) und bestätigen mit ```OK ```an.

## Was passiert beim Schlüsselimport?

Um sicherzustellen, dass in Ihrer Datenbank den aktuellen Vorgaben des Bundeslandes entsprechen, führt der Assistent die folgenden Schritte aus für die zu füllenden Verzeichnisse aus:

1. Schritt: Alle bisher in Ihrer Datenbank nicht verwendeten Schlüssel werden entfernt. Betroffen sind davon nicht alle Verzeichnisse, sondern nur die, für die eine keys-Datei existiert.
2. Schritt: Alle übrigen Schlüssel werden durch ein älteres Gültigkeitsdatum inaktiv (graue Raute) gesetzt.
3. Schritt: Neue Schlüssel werden eingefügt und mit einem aktuellen Gültigkeitsdatum versehen (aktiv=blaue Raute).
4. Schritt: Bereits vorhandene Schlüssel (überprüft wird der Wert in der Spalte Schlüssel) werden auch mit einem aktuellen Gültigkeitsdatum versehen und werden dadurch als aktive Schlüssel (blaue Raute) angezeigt.

## Gültigkeit der Schlüssel

Alle Schlüssel können als gültig (blaue Raute) oder ungültig (graue Raute) mit Hilfe des Gültigkeitszeitraumes markiert werden. Damit kann zwischen Schlüsseln unterschieden werden, die zu einer bereits abgeschlossenen Statistik gültig waren oder es aktuell erst sind. Die blaue oder graue Markierung richtet sich nach dem in der Datenbank eingestellten Zeitraum. Für den ausgewählten Zeitraum ungültige Schlüssel werden automatisch im Auswahlfeld nach unten sortiert.

## Nachkontrolle der Verzeichnisse


!!! info "Hinweis"

    Bitte beachten Sie: Entscheidend für die Statistik ist der Wert in der Spalte Schlüssel in Ihren Verzeichnissen. Ist diese Spalte bei einem Schlüsseldatensatz nicht gefüllt, kann kein statistischer Wert ausgelesen werden. Bitte kontrollieren Sie die Verzeichnisse und ergänzen gegeben falls den Wert in der Spalte Schlüssel.
