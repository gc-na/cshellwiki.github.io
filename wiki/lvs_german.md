# [Linux] Bash lvs Verwendung: Zeigt logische Volumes an

## Übersicht
Der Befehl `lvs` wird verwendet, um Informationen über logische Volumes im Logical Volume Manager (LVM) anzuzeigen. Er gibt eine Übersicht über die logischen Volumes, die auf einem System vorhanden sind, einschließlich ihrer Größe, Status und anderer relevanter Informationen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
lvs [Optionen] [Argumente]
```

## Häufige Optionen
- `-o, --units`: Gibt die Einheiten für die Ausgabe an (z.B. k, M, G).
- `-a, --all`: Zeigt auch inaktive logische Volumes an.
- `-n, --noheadings`: Unterdrückt die Kopfzeile in der Ausgabe.
- `-f, --full`: Zeigt vollständige Informationen über die logischen Volumes an.

## Häufige Beispiele
Um alle logischen Volumes anzuzeigen:

```bash
lvs
```

Um die logischen Volumes mit spezifischen Einheiten anzuzeigen:

```bash
lvs -o +devices
```

Um auch inaktive logische Volumes anzuzeigen:

```bash
lvs -a
```

Um die Ausgabe ohne Kopfzeile anzuzeigen:

```bash
lvs -n
```

## Tipps
- Verwenden Sie die Option `-o`, um nur die benötigten Informationen anzuzeigen und die Ausgabe übersichtlicher zu gestalten.
- Nutzen Sie die Option `-a`, wenn Sie auch inaktive Volumes überprüfen möchten, um einen vollständigen Überblick über Ihre LVM-Konfiguration zu erhalten.
- Kombinieren Sie `lvs` mit anderen LVM-Befehlen wie `lvcreate` oder `lvremove`, um effizienter mit logischen Volumes zu arbeiten.