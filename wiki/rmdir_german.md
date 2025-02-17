# [Linux] Bash rmdir Verwendung: Verzeichnis löschen

## Übersicht
Der Befehl `rmdir` wird in Bash verwendet, um leere Verzeichnisse zu löschen. Wenn das Verzeichnis nicht leer ist, wird der Befehl fehlschlagen und eine Fehlermeldung ausgeben.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
rmdir [Optionen] [Argumente]
```

## Häufige Optionen
- `--ignore-fail-on-non-empty`: Ignoriere Fehler, wenn das Verzeichnis nicht leer ist.
- `--verbose`: Zeigt eine detaillierte Ausgabe über die gelöschten Verzeichnisse an.
- `--help`: Zeigt eine Hilfeseite mit weiteren Informationen über den Befehl an.

## Häufige Beispiele
1. **Ein einfaches leeres Verzeichnis löschen:**
   ```bash
   rmdir mein_verzeichnis
   ```

2. **Mehrere leere Verzeichnisse gleichzeitig löschen:**
   ```bash
   rmdir verzeichnis1 verzeichnis2
   ```

3. **Detaillierte Ausgabe beim Löschen anzeigen:**
   ```bash
   rmdir --verbose mein_verzeichnis
   ```

4. **Fehler ignorieren, wenn das Verzeichnis nicht leer ist:**
   ```bash
   rmdir --ignore-fail-on-non-empty mein_verzeichnis
   ```

## Tipps
- Stellen Sie sicher, dass das Verzeichnis wirklich leer ist, bevor Sie `rmdir` verwenden, da der Befehl sonst fehlschlägt.
- Verwenden Sie `--verbose`, um zu bestätigen, dass das Verzeichnis erfolgreich gelöscht wurde.
- Wenn Sie ein Verzeichnis und seinen Inhalt löschen möchten, sollten Sie stattdessen den Befehl `rm -r` verwenden.