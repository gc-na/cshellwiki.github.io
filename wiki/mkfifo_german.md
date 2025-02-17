# [Linux] Bash mkfifo Verwendung: Erstellen von benannten Pipes

## Übersicht
Der Befehl `mkfifo` wird verwendet, um benannte Pipes (FIFO) in Unix-ähnlichen Betriebssystemen zu erstellen. Eine benannte Pipe ermöglicht es Prozessen, Daten in einer First-In-First-Out-Reihenfolge zu kommunizieren, was die Interprozesskommunikation erleichtert.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
mkfifo [Optionen] [Argumente]
```

## Häufige Optionen
- `-m, --mode=MODE`: Setzt die Berechtigungen für die erstellte Pipe. `MODE` kann in Oktal- oder symbolischer Form angegeben werden.
- `--help`: Zeigt eine Hilfeseite mit Informationen zur Verwendung des Befehls an.
- `--version`: Gibt die Versionsnummer des Befehls aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `mkfifo`:

1. **Erstellen einer einfachen benannten Pipe:**
   ```bash
   mkfifo meine_pipe
   ```

2. **Erstellen einer benannten Pipe mit spezifischen Berechtigungen:**
   ```bash
   mkfifo -m 644 meine_pipe
   ```

3. **Verwenden der benannten Pipe in einem einfachen Beispiel:**
   - In einem Terminal:
   ```bash
   cat > meine_pipe
   ```
   - In einem anderen Terminal:
   ```bash
   cat meine_pipe
   ```

4. **Erstellen mehrerer benannter Pipes auf einmal:**
   ```bash
   mkfifo pipe1 pipe2 pipe3
   ```

## Tipps
- Stellen Sie sicher, dass Sie die Pipe schließen, nachdem Sie die Kommunikation abgeschlossen haben, um Ressourcen freizugeben.
- Überprüfen Sie die Berechtigungen der Pipe, um sicherzustellen, dass die gewünschten Prozesse darauf zugreifen können.
- Nutzen Sie `mkfifo` in Skripten, um die Interprozesskommunikation zwischen verschiedenen Teilen Ihres Programms zu ermöglichen.