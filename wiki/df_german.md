# [Linux] Bash df Verwendung: Zeigt den Speicherplatz auf Dateisystemen an

## Übersicht
Der Befehl `df` (disk free) wird verwendet, um Informationen über den verfügbaren und verwendeten Speicherplatz auf Dateisystemen anzuzeigen. Er gibt eine Übersicht über die Speicherkapazität und die Nutzung der verschiedenen Dateisysteme auf einem Linux- oder Unix-basierten System.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
df [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Gibt die Größen in menschenlesbarem Format aus (z. B. KB, MB, GB).
- `-T`: Zeigt den Typ des Dateisystems an.
- `-a`: Zeigt auch die Dateisysteme mit 0 Speicherplatz an.
- `-i`: Zeigt Informationen über die Inodes an, anstelle von Speicherplatz.
- `--total`: Zeigt die Gesamtsummen für alle Dateisysteme an.

## Häufige Beispiele
- Um den verfügbaren Speicherplatz in einem menschenlesbaren Format anzuzeigen:

```bash
df -h
```

- Um Informationen über alle Dateisysteme, einschließlich der mit 0 Speicherplatz, anzuzeigen:

```bash
df -a
```

- Um den Typ des Dateisystems zusammen mit den Speicherinformationen anzuzeigen:

```bash
df -T
```

- Um Informationen über die Inodes anzuzeigen:

```bash
df -i
```

- Um die Gesamtsummen für alle Dateisysteme anzuzeigen:

```bash
df --total
```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, besonders wenn Sie mit großen Speichermengen arbeiten.
- Kombinieren Sie `df` mit anderen Befehlen wie `grep`, um spezifische Dateisysteme herauszufiltern.
- Überprüfen Sie regelmäßig den Speicherplatz, um sicherzustellen, dass Ihr System nicht überlastet wird.