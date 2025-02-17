# [Linux] Bash iostat Verwendung: Überwachung der Systemleistung

## Übersicht
Der Befehl `iostat` wird verwendet, um die Eingabe-/Ausgabe-Statistiken von Systemgeräten und Partitionen zu überwachen. Er hilft dabei, die Leistung von Festplatten und anderen Speichermedien zu analysieren und Engpässe zu identifizieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
iostat [Optionen] [Argumente]
```

## Häufige Optionen
- `-x`: Zeigt erweiterte Statistiken für Geräte an.
- `-m`: Gibt die Ausgabe in Megabyte pro Sekunde an.
- `-p`: Zeigt Statistiken für Partitionen an.
- `-t`: Fügt Zeitstempel zur Ausgabe hinzu.
- `-h`: Gibt die Ausgabe in einem menschenlesbaren Format aus.

## Häufige Beispiele

### Beispiel 1: Grundlegende Nutzung
Um die grundlegenden I/O-Statistiken anzuzeigen, verwenden Sie einfach:

```bash
iostat
```

### Beispiel 2: Erweiterte Statistiken
Um erweiterte Statistiken für alle Geräte anzuzeigen, verwenden Sie:

```bash
iostat -x
```

### Beispiel 3: Ausgabe in Megabyte
Um die Statistiken in Megabyte pro Sekunde anzuzeigen, verwenden Sie:

```bash
iostat -m
```

### Beispiel 4: Statistiken für Partitionen
Um die Statistiken für alle Partitionen anzuzeigen, können Sie den folgenden Befehl verwenden:

```bash
iostat -p ALL
```

### Beispiel 5: Mit Zeitstempel
Um die Statistiken mit Zeitstempel anzuzeigen, verwenden Sie:

```bash
iostat -t
```

## Tipps
- Führen Sie `iostat` regelmäßig aus, um Trends in der Systemleistung zu erkennen.
- Kombinieren Sie `iostat` mit anderen Monitoring-Tools, um eine umfassendere Analyse zu erhalten.
- Nutzen Sie die `-h` Option, um die Ausgabe leichter lesbar zu machen, insbesondere bei großen Zahlen.