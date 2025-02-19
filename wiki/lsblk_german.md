# [Linux] C Shell (csh) lsblk Verwendung: Zeigt Blockgeräte an

## Übersicht
Der Befehl `lsblk` wird verwendet, um Informationen über Blockgeräte im System anzuzeigen. Er listet alle verfügbaren Blockgeräte auf, einschließlich Festplatten, Partitionen und Wechseldatenträger, und zeigt deren Eigenschaften wie Größe, Typ und Mount-Punkte.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
lsblk [Optionen] [Argumente]
```

## Häufige Optionen
- `-a` oder `--all`: Zeigt alle Geräte an, einschließlich leerer Geräte.
- `-f` oder `--fs`: Zeigt Informationen über das Dateisystem an.
- `-l` oder `--list`: Listet die Geräte in einer einfachen, flachen Liste auf.
- `-o` oder `--output`: Gibt an, welche Spalten angezeigt werden sollen.
- `-p` oder `--paths`: Zeigt die vollständigen Pfade der Geräte an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `lsblk`:

1. **Einfaches Auflisten der Blockgeräte:**

   ```csh
   lsblk
   ```

2. **Auflisten aller Blockgeräte, einschließlich leerer:**

   ```csh
   lsblk -a
   ```

3. **Anzeigen von Blockgeräten mit Dateisysteminformationen:**

   ```csh
   lsblk -f
   ```

4. **Auflisten der Blockgeräte in einer flachen Liste:**

   ```csh
   lsblk -l
   ```

5. **Anpassen der angezeigten Spalten:**

   ```csh
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tipps
- Verwenden Sie die Option `-f`, um schnell Informationen über das Dateisystem zu erhalten, was besonders nützlich ist, wenn Sie mehrere Partitionen verwalten.
- Kombinieren Sie `lsblk` mit anderen Befehlen wie `grep`, um spezifische Geräte zu filtern.
- Nutzen Sie die Option `-p`, wenn Sie die vollständigen Pfade der Geräte benötigen, um Verwirrung bei der Identifizierung von Geräten zu vermeiden.