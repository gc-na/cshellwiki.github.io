# [Linux] Bash parted Verwendung: Partitionen verwalten

## Übersicht
Der `parted` Befehl ist ein leistungsstarkes Werkzeug zur Verwaltung von Festplattenpartitionen in Linux. Mit `parted` können Benutzer Partitionen erstellen, löschen, ändern und Informationen über die Partitionen auf einem Speichermedium anzeigen.

## Verwendung
Die grundlegende Syntax des `parted` Befehls lautet:

```bash
parted [Optionen] [Argumente]
```

## Häufige Optionen
- `-l` oder `--list`: Zeigt eine Liste aller erkannten Festplatten und deren Partitionen an.
- `mklabel`: Erstellt ein neues Partitionierungsschema (z. B. msdos oder gpt).
- `mkpart`: Erstellt eine neue Partition.
- `rm`: Löscht eine bestehende Partition.
- `resizepart`: Ändert die Größe einer bestehenden Partition.
- `print`: Zeigt die Partitionstabelle der aktuellen Festplatte an.

## Häufige Beispiele

### 1. Partitionstabelle anzeigen
Um die Partitionstabelle einer Festplatte anzuzeigen, verwenden Sie:

```bash
parted /dev/sda print
```

### 2. Neue Partition erstellen
Um eine neue Partition zu erstellen, verwenden Sie den folgenden Befehl:

```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### 3. Partition löschen
Um eine Partition zu löschen, verwenden Sie:

```bash
parted /dev/sda rm 1
```

### 4. Partition vergrößern
Um die Größe einer Partition zu ändern, verwenden Sie:

```bash
parted /dev/sda resizepart 1 200MiB
```

### 5. Partitionstabelle erstellen
Um eine neue Partitionstabelle zu erstellen, verwenden Sie:

```bash
parted /dev/sda mklabel gpt
```

## Tipps
- Stellen Sie sicher, dass Sie ein Backup Ihrer Daten haben, bevor Sie Partitionen ändern oder löschen.
- Verwenden Sie `parted` im interaktiven Modus, indem Sie einfach `parted /dev/sda` eingeben, um mehrere Befehle nacheinander auszuführen.
- Überprüfen Sie nach Änderungen die Partitionstabelle erneut mit `print`, um sicherzustellen, dass alles korrekt ist.