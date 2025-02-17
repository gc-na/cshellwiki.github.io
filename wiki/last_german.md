# [Linux] Bash last Befehl: Zeigt die letzten Anmeldungen an

## Übersicht
Der Befehl `last` zeigt eine Liste der letzten Benutzeranmeldungen auf einem System an. Er liest die Datei `/var/log/wtmp`, um Informationen über Anmeldungen, Abmeldungen und Systemstarts bereitzustellen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
last [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt die Hostnamen der Benutzer an.
- `-n [anzahl]`: Gibt die Anzahl der letzten Anmeldungen an, die angezeigt werden sollen.
- `-x`: Zeigt auch Systemstarts und -abschaltungen an.
- `-R`: Unterdrückt die Anzeige von Hostnamen.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `last` Befehls:

1. **Alle letzten Anmeldungen anzeigen:**
   ```bash
   last
   ```

2. **Die letzten 5 Anmeldungen anzeigen:**
   ```bash
   last -n 5
   ```

3. **Anmeldungen mit Hostnamen anzeigen:**
   ```bash
   last -a
   ```

4. **Systemstarts und -abschaltungen anzeigen:**
   ```bash
   last -x
   ```

5. **Anmeldungen ohne Hostnamen anzeigen:**
   ```bash
   last -R
   ```

## Tipps
- Verwenden Sie `last -n 10`, um schnell die letzten 10 Anmeldungen zu überprüfen.
- Kombinieren Sie `last` mit `grep`, um nach einem bestimmten Benutzer zu suchen, z.B. `last | grep username`.
- Beachten Sie, dass `last` nur Informationen anzeigt, die in der `wtmp`-Datei gespeichert sind. Wenn die Datei gelöscht oder nicht vorhanden ist, zeigt der Befehl keine Ergebnisse an.