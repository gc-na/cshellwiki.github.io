# [Linux] Bash batch Verwendung: Batch-Jobs planen und ausführen

## Übersicht
Der `batch` Befehl in Bash wird verwendet, um Befehle oder Skripte zu planen, die zu einem späteren Zeitpunkt ausgeführt werden sollen, wenn das System weniger ausgelastet ist. Dies ist besonders nützlich für ressourcenintensive Aufgaben, die nicht sofort ausgeführt werden müssen.

## Verwendung
Die grundlegende Syntax des `batch` Befehls lautet:

```bash
batch [optionen] [argumente]
```

## Häufige Optionen
- `-l`: Gibt die maximale Anzahl der Jobs an, die gleichzeitig ausgeführt werden können.
- `-n`: Legt die maximale Anzahl der Jobs fest, die in einer Warteschlange stehen können.
- `-q`: Gibt die Warteschlange an, in der der Job ausgeführt werden soll.

## Häufige Beispiele

1. **Ein einfaches Skript zur späteren Ausführung hinzufügen:**
   ```bash
   echo "echo 'Hallo Welt'" | batch
   ```

2. **Ein Skript mit einer spezifischen Datei zur Ausführung hinzufügen:**
   ```bash
   batch < mein_skript.sh
   ```

3. **Einen Befehl zur Ausführung hinzufügen und die Ausgabe in eine Datei umleiten:**
   ```bash
   echo "ls -l" | batch > ausgabe.txt
   ```

## Tipps
- Verwenden Sie `atq`, um eine Liste der geplanten Jobs anzuzeigen.
- Nutzen Sie `atrm`, um einen geplanten Job zu löschen, falls er nicht mehr benötigt wird.
- Stellen Sie sicher, dass Ihr Skript ausführbar ist, bevor Sie es mit `batch` einfügen.