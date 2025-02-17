# [Linux] Bash vgextend Verwendung: Volumes zu einer Volume-Gruppe hinzufügen

## Übersicht
Der Befehl `vgextend` wird verwendet, um logische Volumes zu einer bestehenden Volume-Gruppe in einem Linux-System hinzuzufügen. Dies ist besonders nützlich, wenn mehr Speicherplatz benötigt wird, ohne die bestehende Volume-Gruppe neu zu erstellen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
vgextend [Optionen] [Volume-Gruppe] [Physische Volumes]
```

## Häufige Optionen
- `-l, --extents`: Gibt die Anzahl der Extents an, die hinzugefügt werden sollen.
- `-n, --no-resize`: Verhindert, dass die Volume-Gruppe automatisch vergrößert wird.
- `--test`: Führt einen Testlauf durch, ohne Änderungen vorzunehmen.

## Häufige Beispiele

1. **Hinzufügen eines physischen Volumes zu einer Volume-Gruppe**
   ```bash
   vgextend meine_volume_gruppe /dev/sdb1
   ```

2. **Hinzufügen mehrerer physischer Volumes**
   ```bash
   vgextend meine_volume_gruppe /dev/sdb1 /dev/sdc1
   ```

3. **Testlauf für das Hinzufügen eines physischen Volumes**
   ```bash
   vgextend --test meine_volume_gruppe /dev/sdb1
   ```

4. **Hinzufügen von Extents zu einer Volume-Gruppe**
   ```bash
   vgextend -l +100 meine_volume_gruppe /dev/sdb1
   ```

## Tipps
- Stellen Sie sicher, dass die physischen Volumes, die Sie hinzufügen möchten, nicht bereits in einer anderen Volume-Gruppe verwendet werden.
- Überprüfen Sie den Status Ihrer Volume-Gruppe nach dem Hinzufügen von physischen Volumes mit dem Befehl `vgdisplay`.
- Nutzen Sie den `--test`-Schalter, um sicherzustellen, dass Ihre Befehle wie gewünscht funktionieren, bevor Sie Änderungen vornehmen.