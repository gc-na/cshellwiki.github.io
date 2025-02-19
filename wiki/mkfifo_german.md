# [Linux] C Shell (csh) mkfifo Verwendung: Erstellen von benannten Pipes

## Übersicht
Der Befehl `mkfifo` wird verwendet, um benannte Pipes (FIFO-Dateien) zu erstellen. Diese speziellen Dateien ermöglichen die Kommunikation zwischen Prozessen, indem sie Daten in einer First-In-First-Out-Reihenfolge übertragen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
mkfifo [Optionen] [Argumente]
```

## Häufige Optionen
- `-m, --mode`: Setzt die Berechtigungen für die erstellte FIFO-Datei.
- `-Z, --context`: Setzt den Sicherheitskontext für die FIFO-Datei (nur relevant in SELinux-Umgebungen).

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `mkfifo`:

### Beispiel 1: Erstellen einer einfachen FIFO-Datei
```csh
mkfifo meine_fifo
```

### Beispiel 2: Erstellen einer FIFO-Datei mit spezifischen Berechtigungen
```csh
mkfifo -m 644 meine_fifo
```

### Beispiel 3: Erstellen mehrerer FIFO-Dateien auf einmal
```csh
mkfifo fifo1 fifo2 fifo3
```

## Tipps
- Stellen Sie sicher, dass Sie die FIFO-Datei mit einem Prozess lesen, bevor Sie Daten in sie schreiben, um Blockierungen zu vermeiden.
- Verwenden Sie `ls -l`, um die Berechtigungen Ihrer FIFO-Dateien zu überprüfen.
- Nutzen Sie `unlink` oder `rm`, um eine FIFO-Datei zu löschen, wenn sie nicht mehr benötigt wird.