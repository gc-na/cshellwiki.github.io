# [Linux] C Shell (csh) batch Verwendung: Batch-Jobs planen und ausführen

## Übersicht
Der Befehl `batch` wird verwendet, um Befehle oder Skripte zu planen, die zu einem späteren Zeitpunkt ausgeführt werden sollen, wenn das System weniger ausgelastet ist. Dies ist besonders nützlich für ressourcenintensive Aufgaben, die nicht sofort ausgeführt werden müssen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
batch [Optionen] [Argumente]
```

## Häufige Optionen
- `-l`: Führt den Befehl in einer Login-Shell aus.
- `-m`: Sendet eine E-Mail-Benachrichtigung, wenn der Job abgeschlossen ist.
- `-q`: Wartet, bis die Systemlast unter einen bestimmten Wert fällt, bevor der Job ausgeführt wird.

## Häufige Beispiele

1. **Einen einfachen Befehl planen:**
   Um einen Befehl zu planen, geben Sie einfach den Befehl in die Eingabeaufforderung ein:
   ```csh
   echo "ls -l" | batch
   ```

2. **Ein Skript zur späteren Ausführung planen:**
   Um ein Skript zu planen, verwenden Sie den folgenden Befehl:
   ```csh
   batch < mein_skript.sh
   ```

3. **Einen Befehl mit Optionen planen:**
   Um einen Befehl mit der `-m` Option zu planen, der eine E-Mail sendet, wenn der Job abgeschlossen ist:
   ```csh
   echo "backup.sh" | batch -m
   ```

## Tipps
- Stellen Sie sicher, dass Sie die richtigen Berechtigungen haben, um Skripte oder Befehle auszuführen, die Sie planen möchten.
- Überprüfen Sie regelmäßig die Warteschlange Ihrer geplanten Jobs, um sicherzustellen, dass alles wie gewünscht funktioniert.
- Nutzen Sie die E-Mail-Benachrichtigung, um über den Abschluss Ihrer Jobs informiert zu werden, insbesondere bei längeren Aufgaben.