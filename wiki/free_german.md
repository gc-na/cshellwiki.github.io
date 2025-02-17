# [Linux] Bash free Befehl: Zeigt den Speicherstatus an

## Übersicht
Der `free` Befehl in Bash wird verwendet, um Informationen über den verfügbaren und verwendeten Speicher im System anzuzeigen. Er liefert eine Übersicht über den RAM und den Swap-Speicher, was nützlich ist, um den aktuellen Zustand des Systems zu überwachen.

## Verwendung
Die grundlegende Syntax des `free` Befehls lautet:

```bash
free [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Zeigt die Speicherwerte in einem menschenlesbaren Format an (z.B. in MB oder GB).
- `-m`: Gibt die Werte in Megabyte aus.
- `-g`: Gibt die Werte in Gigabyte aus.
- `-s <Sekunden>`: Aktualisiert die Ausgabe alle angegebenen Sekunden.
- `-t`: Zeigt die Gesamtsumme von verwendetem und verfügbarem Speicher an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `free` Befehls:

1. **Einfacher Speicherstatus**
   ```bash
   free
   ```

2. **Speicherstatus in menschenlesbarem Format**
   ```bash
   free -h
   ```

3. **Speicherstatus in Megabyte**
   ```bash
   free -m
   ```

4. **Speicherstatus in Gigabyte**
   ```bash
   free -g
   ```

5. **Aktualisierung der Speicheranzeige alle 5 Sekunden**
   ```bash
   free -s 5
   ```

6. **Speicherstatus mit Gesamtsumme**
   ```bash
   free -t
   ```

## Tipps
- Verwenden Sie die `-h` Option, um die Ausgabe leichter verständlich zu machen, insbesondere wenn Sie mit großen Speichermengen arbeiten.
- Kombinieren Sie `free` mit anderen Befehlen wie `watch`, um die Speicherwerte in Echtzeit zu überwachen:
  ```bash
  watch free -h
  ```
- Nutzen Sie die `-s` Option, um regelmäßig den Speicherstatus zu überprüfen, was hilfreich sein kann, um Speicherlecks zu identifizieren.