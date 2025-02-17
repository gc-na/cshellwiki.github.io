# [Linux] Bash bg Verwendung: Prozesse im Hintergrund fortsetzen

## Übersicht
Der `bg`-Befehl wird in der Bash verwendet, um einen angehaltenen Prozess im Hintergrund fortzusetzen. Dies ist nützlich, wenn Sie einen Prozess gestartet haben, ihn jedoch anhalten mussten, um andere Aufgaben auszuführen.

## Verwendung
Die grundlegende Syntax des `bg`-Befehls lautet:

```bash
bg [optionen] [jobspec]
```

## Häufige Optionen
- `jobspec`: Gibt den Job an, den Sie im Hintergrund fortsetzen möchten. Dies kann die Jobnummer oder der Jobname sein.
- `-l`: Zeigt die Jobnummern in einer langen Form an.

## Häufige Beispiele

1. **Einen angehaltenen Job im Hintergrund fortsetzen**:
   Wenn Sie einen Job mit `Ctrl+Z` angehalten haben, können Sie ihn mit `bg` fortsetzen:
   ```bash
   bg
   ```

2. **Einen spezifischen Job im Hintergrund fortsetzen**:
   Angenommen, Sie haben mehrere Jobs, und Sie möchten Job Nummer 1 fortsetzen:
   ```bash
   bg %1
   ```

3. **Einen Job mit einem bestimmten Namen im Hintergrund fortsetzen**:
   Wenn Sie den Job mit dem Namen "mein_script" haben:
   ```bash
   bg mein_script
   ```

## Tipps
- Verwenden Sie den Befehl `jobs`, um eine Liste aller laufenden und angehaltenen Jobs anzuzeigen, bevor Sie `bg` verwenden.
- Achten Sie darauf, dass Sie den richtigen Job angeben, um Verwirrung zu vermeiden.
- Sie können `bg` in Kombination mit `fg` verwenden, um zwischen Vordergrund- und Hintergrundprozessen zu wechseln.