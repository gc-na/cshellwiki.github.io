# [Linux] Bash sort Verwendung: Daten sortieren

## Übersicht
Der Befehl `sort` wird verwendet, um Zeilen in einer Datei oder von der Standardeingabe zu sortieren. Er kann alphabetisch, numerisch oder nach anderen Kriterien sortieren, je nach den angegebenen Optionen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
sort [Optionen] [Argumente]
```

## Häufige Optionen
- `-n`: Sortiert numerisch.
- `-r`: Sortiert in umgekehrter Reihenfolge.
- `-k`: Gibt das Sortierfeld an (z.B. `-k 2` für das zweite Feld).
- `-u`: Entfernt doppelte Zeilen.
- `-t`: Legt das Trennzeichen für Felder fest (z.B. `-t,` für Komma).

## Häufige Beispiele
- **Einfaches Sortieren einer Datei:**
  ```bash
  sort datei.txt
  ```

- **Numerisches Sortieren:**
  ```bash
  sort -n zahlen.txt
  ```

- **Umgekehrtes Sortieren:**
  ```bash
  sort -r namen.txt
  ```

- **Sortieren nach einem bestimmten Feld:**
  ```bash
  sort -k 2 daten.csv
  ```

- **Entfernen von Duplikaten:**
  ```bash
  sort -u datei.txt
  ```

## Tipps
- Verwenden Sie `-o`, um die sortierten Ergebnisse direkt in eine Datei zu schreiben:
  ```bash
  sort datei.txt -o sortierte_datei.txt
  ```

- Kombinieren Sie `sort` mit `uniq`, um doppelte Zeilen zu entfernen, nachdem Sie die Daten sortiert haben:
  ```bash
  sort datei.txt | uniq
  ```

- Nutzen Sie `-t` zusammen mit `-k`, um gezielt nach bestimmten Feldern in strukturierten Daten zu sortieren, wie z.B. CSV-Dateien.