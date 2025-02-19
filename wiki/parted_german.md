# [Linux] C Shell (csh) parted Verwendung: Partitionen verwalten

## Übersicht
Der Befehl `parted` wird verwendet, um Partitionen auf Festplatten zu erstellen, zu löschen, zu ändern und zu verwalten. Er bietet eine benutzerfreundliche Schnittstelle zur Verwaltung von Partitionen und unterstützt verschiedene Dateisysteme.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
parted [Optionen] [Argumente]
```

## Häufige Optionen
- `-l`: Listet alle erkannten Partitionen auf.
- `mkpart`: Erstellt eine neue Partition.
- `rm`: Löscht eine bestehende Partition.
- `resizepart`: Ändert die Größe einer Partition.
- `print`: Zeigt die Partitionstabelle an.

## Häufige Beispiele

### 1. Partitionstabelle anzeigen
Um die Partitionstabelle der Festplatte anzuzeigen, verwenden Sie:

```bash
parted /dev/sda print
```

### 2. Neue Partition erstellen
Um eine neue Partition zu erstellen, können Sie den folgenden Befehl verwenden:

```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### 3. Partition löschen
Um eine Partition zu löschen, verwenden Sie:

```bash
parted /dev/sda rm 1
```

### 4. Partition vergrößern
Um eine bestehende Partition zu vergrößern, verwenden Sie:

```bash
parted /dev/sda resizepart 1 200MiB
```

## Tipps
- Stellen Sie sicher, dass Sie eine Sicherung Ihrer Daten haben, bevor Sie Partitionen ändern.
- Verwenden Sie `parted` mit Bedacht, da falsche Befehle zu Datenverlust führen können.
- Überprüfen Sie die Partitionen regelmäßig mit `parted -l`, um sicherzustellen, dass alles korrekt ist.