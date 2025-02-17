# [Linux] Bash lvcreate Verwendung: Logische Volumes erstellen

## Übersicht
Der Befehl `lvcreate` wird verwendet, um logische Volumes innerhalb eines Volume Groups (VG) in einem Logical Volume Manager (LVM) zu erstellen. Dies ermöglicht eine flexible Verwaltung von Speicherplatz auf Linux-Systemen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
lvcreate [Optionen] [Argumente]
```

## Häufige Optionen
- `-n, --name <Name>`: Gibt den Namen des zu erstellenden logischen Volumes an.
- `-L, --size <Größe>`: Legt die Größe des logischen Volumes fest.
- `-l, --extents <Anzahl>`: Gibt die Anzahl der Extents an, die für das logische Volume verwendet werden sollen.
- `-C, --mirrors <Anzahl>`: Gibt die Anzahl der Spiegelungen für das logische Volume an.
- `-Z, --zero n`: Gibt an, ob das logische Volume beim Erstellen mit Nullen gefüllt werden soll (n=1 für Ja, n=0 für Nein).

## Häufige Beispiele

1. **Erstellen eines logischen Volumes mit einer bestimmten Größe:**

```bash
lvcreate -L 10G -n mein_volume vg_name
```

2. **Erstellen eines logischen Volumes mit Extents:**

```bash
lvcreate -l 100 -n mein_extent_volume vg_name
```

3. **Erstellen eines gespiegelten logischen Volumes:**

```bash
lvcreate -m 1 -L 20G -n mein_spiegel_volume vg_name
```

4. **Erstellen eines logischen Volumes und mit Nullen füllen:**

```bash
lvcreate -L 5G -n mein_gefuelltes_volume -Z y vg_name
```

## Tipps
- Überprüfen Sie vor dem Erstellen eines logischen Volumes den verfügbaren Speicherplatz in Ihrer Volume Group mit `vgdisplay`.
- Verwenden Sie `lvdisplay`, um Informationen über die erstellten logischen Volumes zu erhalten.
- Planen Sie die Größe und Anzahl der logischen Volumes im Voraus, um eine effiziente Nutzung des Speicherplatzes zu gewährleisten.