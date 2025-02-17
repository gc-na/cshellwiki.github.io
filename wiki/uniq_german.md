# [Linux] Bash uniq Verwendung: Duplikate in einer Datei entfernen

## Übersicht
Der `uniq` Befehl in Bash wird verwendet, um aufeinanderfolgende doppelte Zeilen in einer Datei zu entfernen oder zu zählen. Er ist besonders nützlich, um Daten zu bereinigen und die Lesbarkeit von Textdateien zu verbessern.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
uniq [Optionen] [Argumente]
```

## Häufige Optionen
- `-c`: Zählt die Anzahl der Vorkommen jeder Zeile.
- `-d`: Gibt nur die doppelten Zeilen aus.
- `-u`: Gibt nur die einzigartigen (einmaligen) Zeilen aus.
- `-i`: Ignoriert Groß- und Kleinschreibung bei der Vergleichung.
- `-w N`: Vergleicht nur die ersten N Zeichen jeder Zeile.

## Häufige Beispiele

1. **Einfaches Entfernen von Duplikaten**:
   ```bash
   uniq datei.txt
   ```

2. **Zählen der Vorkommen jeder Zeile**:
   ```bash
   uniq -c datei.txt
   ```

3. **Nur doppelte Zeilen anzeigen**:
   ```bash
   uniq -d datei.txt
   ```

4. **Nur einzigartige Zeilen anzeigen**:
   ```bash
   uniq -u datei.txt
   ```

5. **Groß- und Kleinschreibung ignorieren**:
   ```bash
   uniq -i datei.txt
   ```

6. **Vergleich der ersten N Zeichen**:
   ```bash
   uniq -w 5 datei.txt
   ```

## Tipps
- Stellen Sie sicher, dass die Eingabedatei sortiert ist, bevor Sie `uniq` verwenden, da der Befehl nur aufeinanderfolgende Duplikate entfernt.
- Kombinieren Sie `uniq` häufig mit dem `sort` Befehl, um eine vollständige Bereinigung der Daten zu erreichen:
  ```bash
  sort datei.txt | uniq
  ```
- Nutzen Sie die Option `-c`, um schnell zu sehen, wie oft jede Zeile in der Datei vorkommt, was bei der Analyse von Daten hilfreich sein kann.