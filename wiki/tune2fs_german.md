# [Linux] C Shell (csh) tune2fs Verwendung: Anpassung von ext2/ext3/ext4-Dateisystemen

## Übersicht
Der Befehl `tune2fs` wird verwendet, um verschiedene Parameter eines ext2-, ext3- oder ext4-Dateisystems zu ändern. Mit diesem Befehl können Administratoren Einstellungen wie die maximale Anzahl an Mounts, die Zeit bis zur Überprüfung des Dateisystems und andere wichtige Optionen anpassen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
tune2fs [Optionen] [Argumente]
```

## Häufige Optionen
- `-c <anzahl>`: Setzt die maximale Anzahl an Mounts, nach denen das Dateisystem überprüft werden soll.
- `-i <intervall>`: Legt das Zeitintervall fest, nach dem das Dateisystem überprüft wird.
- `-m <prozent>`: Setzt den Prozentsatz des Speicherplatzes, der für den Root-Benutzer reserviert ist.
- `-L <label>`: Ändert das Label des Dateisystems.
- `-O <features>`: Aktiviert bestimmte Dateisystemfunktionen.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `tune2fs`:

1. **Maximale Anzahl an Mounts setzen:**
   ```bash
   tune2fs -c 30 /dev/sda1
   ```

2. **Überprüfungsintervall auf 6 Monate setzen:**
   ```bash
   tune2fs -i 6m /dev/sda1
   ```

3. **Reservierten Speicherplatz auf 5% setzen:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Label des Dateisystems ändern:**
   ```bash
   tune2fs -L MeinLabel /dev/sda1
   ```

5. **Aktivieren von Dateisystemfunktionen:**
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

## Tipps
- Stellen Sie sicher, dass das Dateisystem nicht gemountet ist, bevor Sie `tune2fs` verwenden, um Datenverlust zu vermeiden.
- Überprüfen Sie die aktuellen Einstellungen des Dateisystems mit dem Befehl `tune2fs -l /dev/sda1`.
- Verwenden Sie `tune2fs` mit Bedacht, da falsche Einstellungen zu Problemen mit dem Dateisystem führen können.