# [Linux] C Shell (csh) vgcreate Verwendung: Erstellen von Volume-Gruppen

## Übersicht
Der Befehl `vgcreate` wird verwendet, um eine neue Volume-Gruppe in einem Logical Volume Management (LVM) System zu erstellen. Eine Volume-Gruppe ist eine Sammlung von logischen Volumes, die Speicherplatz effizient verwalten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
vgcreate [Optionen] [Argumente]
```

## Häufige Optionen
- `-s, --stripes <Anzahl>`: Gibt die Anzahl der Streifen an, die für die Volume-Gruppe verwendet werden sollen.
- `-p, --pe-size <Größe>`: Legt die Größe der physischen Extents fest.
- `--metadatasize <Größe>`: Bestimmt die Größe der Metadaten für die Volume-Gruppe.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `vgcreate`:

1. **Erstellen einer einfachen Volume-Gruppe:**
   ```csh
   vgcreate meine_volume_gruppe /dev/sda1 /dev/sda2
   ```

2. **Erstellen einer Volume-Gruppe mit einer bestimmten Extent-Größe:**
   ```csh
   vgcreate -p 16M meine_volume_gruppe /dev/sda1 /dev/sda2
   ```

3. **Erstellen einer Volume-Gruppe mit Streifen:**
   ```csh
   vgcreate -s 64K meine_volume_gruppe /dev/sda1 /dev/sda2
   ```

## Tipps
- Stellen Sie sicher, dass die verwendeten physikalischen Volumes (PVs) unbenutzt sind, bevor Sie eine Volume-Gruppe erstellen.
- Überprüfen Sie die aktuelle Konfiguration Ihrer LVM-Umgebung mit dem Befehl `vgdisplay`, um sicherzustellen, dass alles korrekt eingerichtet ist.
- Verwenden Sie `man vgcreate`, um die vollständige Dokumentation und alle verfügbaren Optionen zu lesen.