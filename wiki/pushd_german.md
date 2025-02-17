# [Linux] Bash pushd Verwendung: Verzeichniswechsel und -verwaltung

## Übersicht
Der Befehl `pushd` wird in der Bash verwendet, um das aktuelle Verzeichnis auf einen Stack zu legen und gleichzeitig in ein anderes Verzeichnis zu wechseln. Dies ermöglicht eine einfache Navigation zwischen Verzeichnissen, ohne den Überblick über die vorherigen Verzeichnisse zu verlieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
pushd [Optionen] [Argumente]
```

## Häufige Optionen
- `+N`: Wechselt zu dem N-ten Verzeichnis im Stack.
- `-N`: Wechselt zu dem N-ten Verzeichnis im Stack, aber in umgekehrter Reihenfolge.
- `-`: Wechselt zurück zum vorherigen Verzeichnis.

## Häufige Beispiele

1. **Wechsel zu einem Verzeichnis und speichern des aktuellen Verzeichnisses:**
   ```bash
   pushd /pfad/zum/verzeichnis
   ```

2. **Wechsel zu einem Verzeichnis im Stack:**
   ```bash
   pushd +1
   ```

3. **Zurück zum vorherigen Verzeichnis:**
   ```bash
   pushd -
   ```

4. **Wechsel zu einem Verzeichnis und gleichzeitig den Stack anzeigen:**
   ```bash
   pushd /pfad/zum/verzeichnis && dirs
   ```

## Tipps
- Verwenden Sie `dirs`, um den aktuellen Stack der Verzeichnisse anzuzeigen.
- Nutzen Sie `popd`, um das oberste Verzeichnis vom Stack zu entfernen und zurückzukehren.
- Kombinieren Sie `pushd` mit Skripten, um die Verzeichnisnavigation zu automatisieren und zu vereinfachen.