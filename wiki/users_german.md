# [Linux] Bash-Benutzerbefehl: Benutzerinformationen anzeigen

## Übersicht
Der Befehl `users` zeigt eine Liste der aktuell angemeldeten Benutzer auf dem System an. Er gibt die Benutzernamen in einer kompakten Form aus, was nützlich ist, um schnell zu sehen, wer gerade aktiv ist.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
users [Optionen]
```

## Häufige Optionen
- `-n`: Gibt die Anzahl der angemeldeten Benutzer an.
- `-r`: Zeigt nur die Benutzernamen an, die mit einer bestimmten Shell angemeldet sind.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `users`:

1. **Einfacher Befehl**: Zeigt alle aktuell angemeldeten Benutzer an.
   ```bash
   users
   ```

2. **Anzahl der Benutzer**: Zeigt die Anzahl der aktuell angemeldeten Benutzer an.
   ```bash
   users -n
   ```

3. **Benutzer mit spezifischer Shell**: Zeigt nur die Benutzer an, die mit einer bestimmten Shell angemeldet sind (z.B. `/bin/bash`).
   ```bash
   users -r /bin/bash
   ```

## Tipps
- Verwenden Sie den Befehl regelmäßig, um einen Überblick über die Benutzeraktivität auf Ihrem System zu erhalten.
- Kombinieren Sie `users` mit anderen Befehlen wie `who` oder `w`, um detailliertere Informationen über die angemeldeten Benutzer zu erhalten.
- Beachten Sie, dass `users` nur die Benutzernamen anzeigt und keine weiteren Informationen wie Anmeldezeiten oder IP-Adressen bereitstellt.