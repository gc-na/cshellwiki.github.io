# [Linux] Bash lsblk Verwendung: Zeigt Blockgeräte und deren Informationen an

## Übersicht
Der Befehl `lsblk` wird verwendet, um Informationen über Blockgeräte im Linux-System anzuzeigen. Dazu gehören Festplatten, Partitionen und andere Speichermedien. Mit `lsblk` können Sie die Struktur und den Status Ihrer Speichergeräte leicht erkennen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
lsblk [Optionen] [Argumente]
```

## Häufige Optionen
- `-a` oder `--all`: Zeigt alle Geräte an, einschließlich leerer Geräte.
- `-f` oder `--fs`: Zeigt Dateisysteminformationen an.
- `-l` oder `--list`: Listet die Geräte in einer einfachen, zeilenweisen Form auf.
- `-o` oder `--output`: Bestimmt, welche Spalten angezeigt werden sollen.
- `-p` oder `--paths`: Zeigt die vollständigen Pfade der Geräte an.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `lsblk`:

1. **Einfaches Auflisten von Blockgeräten:**
   ```bash
   lsblk
   ```

2. **Auflisten aller Blockgeräte, einschließlich leerer Geräte:**
   ```bash
   lsblk -a
   ```

3. **Anzeigen von Blockgeräten mit Dateisysteminformationen:**
   ```bash
   lsblk -f
   ```

4. **Auflisten der Blockgeräte in einer einfachen, zeilenweisen Form:**
   ```bash
   lsblk -l
   ```

5. **Anpassen der angezeigten Spalten:**
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tipps
- Verwenden Sie die Option `-f`, um schnell zu überprüfen, welches Dateisystem auf einem bestimmten Gerät vorhanden ist.
- Kombinieren Sie `lsblk` mit anderen Befehlen wie `grep`, um gezielt nach bestimmten Geräten zu suchen.
- Nutzen Sie die Option `-p`, wenn Sie die vollständigen Pfade der Geräte benötigen, was bei Skripten hilfreich sein kann.