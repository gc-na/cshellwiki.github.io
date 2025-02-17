# [Linux] Bash fdisk Verwendung: Partitionierung von Festplatten

## Übersicht
Der `fdisk`-Befehl ist ein leistungsstarkes Tool zur Partitionierung von Festplatten unter Linux. Mit `fdisk` können Benutzer Partitionen erstellen, löschen und verwalten, um den Speicherplatz auf ihren Festplatten effizient zu nutzen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
fdisk [Optionen] [Gerät]
```

Hierbei ist `[Gerät]` das Laufwerk, das Sie partitionieren möchten, z. B. `/dev/sda`.

## Häufige Optionen
- `-l`: Listet alle Partitionen auf den angeschlossenen Festplatten auf.
- `-n`: Erstellt eine neue Partition.
- `-d`: Löscht eine bestehende Partition.
- `-u`: Zeigt die Partitionen in Sektoren an.
- `-p`: Gibt die Partitionstabelle des angegebenen Geräts aus.

## Häufige Beispiele

### Auflisten der Partitionen
Um alle Partitionen auf den angeschlossenen Festplatten anzuzeigen, verwenden Sie:

```bash
fdisk -l
```

### Neue Partition erstellen
Um eine neue Partition auf `/dev/sda` zu erstellen, starten Sie `fdisk` mit dem Gerät:

```bash
fdisk /dev/sda
```
Dann folgen Sie den Anweisungen im interaktiven Menü, um eine neue Partition zu erstellen.

### Partition löschen
Um eine Partition zu löschen, starten Sie ebenfalls `fdisk`:

```bash
fdisk /dev/sda
```
Wählen Sie im interaktiven Menü die Option zum Löschen einer Partition und geben Sie die entsprechende Partitionsnummer an.

### Partitionstabelle anzeigen
Um die Partitionstabelle eines bestimmten Geräts anzuzeigen, verwenden Sie:

```bash
fdisk -p /dev/sda
```

## Tipps
- **Sichern Sie Ihre Daten**: Bevor Sie Partitionen ändern, sollten Sie immer ein Backup Ihrer wichtigen Daten erstellen.
- **Verwenden Sie `parted` für größere Festplatten**: Für Festplatten über 2 TB oder wenn Sie GPT-Partitionen benötigen, ist `parted` oft die bessere Wahl.
- **Seien Sie vorsichtig mit `d`**: Das Löschen von Partitionen ist endgültig und kann zu Datenverlust führen. Stellen Sie sicher, dass Sie die richtige Partition auswählen.