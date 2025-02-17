# [Linux] Bash who Verwendung: Zeigt angemeldete Benutzer an

## Übersicht
Der Befehl `who` wird verwendet, um eine Liste der Benutzer anzuzeigen, die derzeit am System angemeldet sind. Er liefert Informationen wie den Benutzernamen, das Terminal, von dem aus der Benutzer angemeldet ist, sowie das Datum und die Uhrzeit der Anmeldung.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
who [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle verfügbaren Informationen an, einschließlich der Benutzer, die sich nicht mehr angemeldet haben.
- `-b`: Gibt die letzte Systemstartzeit aus.
- `-q`: Zeigt nur die Benutzernamen und die Anzahl der angemeldeten Benutzer an.
- `--help`: Zeigt eine Hilfeübersicht für den Befehl an.

## Häufige Beispiele

1. **Einfacher Aufruf von who:**
   ```bash
   who
   ```

2. **Anzeigen aller verfügbaren Informationen:**
   ```bash
   who -a
   ```

3. **Letzte Systemstartzeit anzeigen:**
   ```bash
   who -b
   ```

4. **Nur Benutzernamen und Anzahl der angemeldeten Benutzer anzeigen:**
   ```bash
   who -q
   ```

## Tipps
- Verwenden Sie `who -b`, um schnell zu überprüfen, wann das System zuletzt neu gestartet wurde.
- Kombinieren Sie `who` mit anderen Befehlen wie `grep`, um gezielt nach bestimmten Benutzern zu suchen. Beispiel:
  ```bash
  who | grep username
  ```
- Nutzen Sie `who --help`, um eine vollständige Liste der verfügbaren Optionen und deren Erklärungen zu erhalten.