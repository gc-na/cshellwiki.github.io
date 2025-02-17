# [Linux] Bash vgcreate Verwendung: Erstellen von Volume-Gruppen

## Übersicht
Der Befehl `vgcreate` wird verwendet, um eine neue Volume-Gruppe in einem Logical Volume Management (LVM) System zu erstellen. Eine Volume-Gruppe ist eine Sammlung von physischen Volumes, die zusammen als ein logisches Volume betrachtet werden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
vgcreate [Optionen] [Name_der_Volume-Gruppe] [Physische_Volumes]
```

## Häufige Optionen
- `-s, --stripes <Anzahl>`: Gibt die Anzahl der Streifen an, die für die Volume-Gruppe verwendet werden sollen.
- `-p, --max-pv <Anzahl>`: Legt die maximale Anzahl an physischen Volumes fest, die in der Volume-Gruppe enthalten sein können.
- `-f, --force`: Erzwingt die Erstellung der Volume-Gruppe, auch wenn einige physische Volumes nicht den Anforderungen entsprechen.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `vgcreate`:

1. **Erstellen einer einfachen Volume-Gruppe:**
   ```bash
   vgcreate meine_volume_gruppe /dev/sdb1 /dev/sdc1
   ```

2. **Erstellen einer Volume-Gruppe mit spezifischen Optionen:**
   ```bash
   vgcreate -s 64k -p 16 meine_volume_gruppe /dev/sdb1 /dev/sdc1
   ```

3. **Erzwingen der Erstellung einer Volume-Gruppe:**
   ```bash
   vgcreate -f meine_volume_gruppe /dev/sdb1 /dev/sdc1
   ```

## Tipps
- Stellen Sie sicher, dass die physischen Volumes, die Sie verwenden möchten, nicht bereits in einer anderen Volume-Gruppe enthalten sind.
- Überprüfen Sie den Status Ihrer Volume-Gruppen regelmäßig mit dem Befehl `vgs`, um sicherzustellen, dass alles ordnungsgemäß funktioniert.
- Nutzen Sie `vgextend`, um später weitere physische Volumes zu einer bestehenden Volume-Gruppe hinzuzufügen, falls erforderlich.