# [Linux] Bash uname Verwendung: Systeminformationen anzeigen

## Übersicht
Der Befehl `uname` wird verwendet, um Informationen über das Betriebssystem und die Hardware des Systems anzuzeigen. Er liefert grundlegende Details wie den Namen des Kernels, die Version und die Architektur des Systems.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
uname [Optionen]
```

## Häufige Optionen
- `-a`: Zeigt alle verfügbaren Informationen an.
- `-s`: Gibt den Namen des Kernels aus.
- `-n`: Gibt den Netzwerk-Hostnamen des Systems aus.
- `-r`: Zeigt die Kernel-Version an.
- `-v`: Gibt die Versionsnummer des Kernels aus.
- `-m`: Zeigt die Maschinenarchitektur an.
- `-p`: Gibt den Prozessor-Typ aus (wenn verfügbar).
- `-i`: Zeigt die Hardware-Plattform an.
- `-o`: Gibt den Namen des Betriebssystems aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `uname`-Befehls:

1. **Alle Informationen anzeigen:**
   ```bash
   uname -a
   ```

2. **Nur den Kernel-Namen anzeigen:**
   ```bash
   uname -s
   ```

3. **Kernel-Version anzeigen:**
   ```bash
   uname -r
   ```

4. **Maschinenarchitektur anzeigen:**
   ```bash
   uname -m
   ```

5. **Netzwerk-Hostnamen anzeigen:**
   ```bash
   uname -n
   ```

## Tipps
- Verwenden Sie `uname -a`, um einen umfassenden Überblick über Ihr System zu erhalten.
- Kombinieren Sie `uname` mit anderen Befehlen, um Skripte zu erstellen, die auf spezifische Systeminformationen reagieren.
- Beachten Sie, dass einige Optionen je nach System und Kernel-Version unterschiedliche Informationen zurückgeben können.