# [Linux] C Shell (csh) Benutzerbefehl: Benutzerinformationen anzeigen

## Übersicht
Der `users` Befehl in der C Shell (csh) zeigt die Benutzernamen der aktuell angemeldeten Benutzer an. Dies ist nützlich, um schnell zu überprüfen, welche Benutzer derzeit im System aktiv sind.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
users [Optionen] [Argumente]
```

## Häufige Optionen
- `-n`: Gibt die Anzahl der angemeldeten Benutzer aus.
- `-r`: Zeigt nur die Benutzernamen der Benutzer an, die auf dem aktuellen Terminal angemeldet sind.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `users` Befehls:

1. **Alle angemeldeten Benutzer anzeigen:**
   ```csh
   users
   ```

2. **Anzahl der angemeldeten Benutzer anzeigen:**
   ```csh
   users -n
   ```

3. **Benutzer auf dem aktuellen Terminal anzeigen:**
   ```csh
   users -r
   ```

## Tipps
- Verwenden Sie den `users` Befehl regelmäßig, um einen Überblick über die Benutzeraktivität auf Ihrem System zu erhalten.
- Kombinieren Sie den `users` Befehl mit anderen Befehlen wie `who` oder `w`, um detailliertere Informationen über die Benutzer zu erhalten.
- Beachten Sie, dass der `users` Befehl nur die Benutzernamen anzeigt und keine weiteren Informationen wie Anmeldezeiten oder aktive Prozesse liefert.