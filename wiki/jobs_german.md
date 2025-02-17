# [Linux] Bash jobs Verwendung: Zeigt aktive Jobs an

## Übersicht
Der Befehl `jobs` in Bash wird verwendet, um eine Liste der aktuell laufenden Jobs in der aktuellen Shell-Sitzung anzuzeigen. Ein Job ist ein Prozess, der von der Shell gestartet wurde und entweder im Vordergrund oder im Hintergrund läuft. Mit `jobs` können Benutzer den Status dieser Prozesse überwachen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
jobs [Optionen] [Argumente]
```

## Häufige Optionen
- `-l`: Zeigt die Prozess-ID (PID) der Jobs an.
- `-n`: Zeigt nur Jobs an, die seit der letzten Ausführung von `jobs` geändert wurden.
- `-p`: Gibt nur die Prozess-IDs der Jobs aus.

## Häufige Beispiele
1. **Einfaches Anzeigen von Jobs:**
   ```bash
   jobs
   ```

2. **Jobs mit Prozess-IDs anzeigen:**
   ```bash
   jobs -l
   ```

3. **Nur neue oder geänderte Jobs anzeigen:**
   ```bash
   jobs -n
   ```

4. **Nur die Prozess-IDs der Jobs anzeigen:**
   ```bash
   jobs -p
   ```

## Tipps
- Verwenden Sie `bg` und `fg`, um Jobs im Hintergrund oder Vordergrund fortzusetzen, nachdem Sie sie mit `Ctrl + Z` gestoppt haben.
- Überprüfen Sie regelmäßig Ihre Jobs mit `jobs`, um sicherzustellen, dass keine wichtigen Prozesse im Hintergrund laufen, die Sie möglicherweise vergessen haben.
- Nutzen Sie die Optionen `-l` oder `-p`, wenn Sie spezifische Informationen über Ihre Jobs benötigen, insbesondere wenn Sie mit mehreren Prozessen arbeiten.