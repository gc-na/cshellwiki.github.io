# [Linux] Bash mount Verwendung: Einbinden von Dateisystemen

## Übersicht
Der Befehl `mount` wird in Linux verwendet, um Dateisysteme in das Verzeichnisbaum-System des Betriebssystems einzubinden. Dies ermöglicht den Zugriff auf die Daten auf verschiedenen Speichermedien, wie Festplatten, USB-Sticks oder Netzwerkfreigaben.

## Verwendung
Die grundlegende Syntax des `mount`-Befehls lautet:

```bash
mount [Optionen] [Gerät] [Zielverzeichnis]
```

## Häufige Optionen
- `-t`: Gibt den Typ des Dateisystems an (z. B. ext4, ntfs).
- `-o`: Ermöglicht das Angeben von Optionen wie `ro` (read-only) oder `rw` (read-write).
- `-a`: Mountet alle Dateisysteme, die in der Datei `/etc/fstab` aufgeführt sind.
- `-r`: Mountet das Dateisystem im Nur-Lese-Modus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `mount`-Befehls:

1. **Einbinden eines USB-Sticks:**
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. **Einbinden eines ext4-Dateisystems mit spezifischen Optionen:**
   ```bash
   mount -t ext4 -o rw /dev/sda1 /mnt/data
   ```

3. **Einbinden aller in fstab definierten Dateisysteme:**
   ```bash
   mount -a
   ```

4. **Einbinden eines Netzwerkfreigabe (NFS):**
   ```bash
   mount -t nfs 192.168.1.100:/freigabe /mnt/nfs
   ```

## Tipps
- Stellen Sie sicher, dass das Zielverzeichnis existiert, bevor Sie den Befehl ausführen.
- Verwenden Sie `umount`, um ein eingebundenes Dateisystem sicher zu trennen.
- Überprüfen Sie die Berechtigungen des Zielverzeichnisses, um sicherzustellen, dass Sie die erforderlichen Zugriffsrechte haben.
- Nutzen Sie `df -h`, um eine Übersicht über alle aktuell eingebundenen Dateisysteme zu erhalten.