# [Linux] Bash tune2fs Verwendung: Anpassen von ext2/ext3/ext4 Dateisystemen

## Übersicht
Der Befehl `tune2fs` wird verwendet, um verschiedene Parameter eines ext2-, ext3- oder ext4-Dateisystems zu ändern. Dies ermöglicht es Benutzern, die Leistung und das Verhalten des Dateisystems anzupassen, ohne die Daten zu verlieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
tune2fs [Optionen] [Argumente]
```

## Häufige Optionen
- `-c <anzahl>`: Setzt die maximale Anzahl der Mounts, nach denen das Dateisystem überprüft werden soll.
- `-i <Intervall>`: Legt das Zeitintervall fest, nach dem das Dateisystem überprüft werden soll.
- `-m <Prozentsatz>`: Setzt den Prozentsatz des Speicherplatzes, der für den Root-Benutzer reserviert ist.
- `-L <Label>`: Ändert das Label des Dateisystems.
- `-O <Feature>`: Aktiviert bestimmte Dateisystemmerkmale.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `tune2fs`:

1. **Maximale Anzahl der Mounts setzen:**
   ```bash
   tune2fs -c 30 /dev/sda1
   ```
   Dieser Befehl setzt die maximale Anzahl der Mounts auf 30 für das Dateisystem auf `/dev/sda1`.

2. **Zeitintervall für die Überprüfung festlegen:**
   ```bash
   tune2fs -i 2w /dev/sda1
   ```
   Dieser Befehl legt fest, dass das Dateisystem alle zwei Wochen überprüft werden soll.

3. **Reservierten Speicherplatz ändern:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```
   Hiermit wird der reservierte Speicherplatz für den Root-Benutzer auf 5% gesetzt.

4. **Label des Dateisystems ändern:**
   ```bash
   tune2fs -L MeinLabel /dev/sda1
   ```
   Dieser Befehl ändert das Label des Dateisystems auf `/dev/sda1` in "MeinLabel".

5. **Aktivieren eines Dateisystemmerkmals:**
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```
   Hiermit wird das `dir_index`-Merkmal für das Dateisystem aktiviert, was die Verzeichnissuche beschleunigen kann.

## Tipps
- Führen Sie `tune2fs` immer mit Root-Rechten aus, um sicherzustellen, dass Sie die erforderlichen Berechtigungen haben.
- Überprüfen Sie die aktuellen Einstellungen des Dateisystems mit dem Befehl `tune2fs -l /dev/sda1`, um zu sehen, welche Parameter bereits konfiguriert sind.
- Seien Sie vorsichtig beim Ändern von Parametern, da falsche Einstellungen die Stabilität des Dateisystems beeinträchtigen können.