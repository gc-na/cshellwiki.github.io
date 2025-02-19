# [Linux] C Shell (csh) w: Zeigt angemeldete Benutzer und ihre Aktivitäten an

## Übersicht
Der Befehl `w` zeigt eine Liste der aktuell angemeldeten Benutzer auf dem System sowie deren Aktivitäten an. Dies umfasst Informationen wie die Benutzer-ID, die Zeit der Anmeldung, die aktive Shell und die von den Benutzern ausgeführten Prozesse.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
w [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Unterdrückt die Anzeige der Kopfzeile.
- `-s`: Zeigt eine kurze Ausgabe an, ohne die Informationen über die Benutzerprozesse.
- `-u`: Zeigt die Benutzer-ID an, die standardmäßig nicht angezeigt wird.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `w`:

1. **Einfacher Befehl ohne Optionen:**
   ```csh
   w
   ```

2. **Kurze Ausgabe ohne Kopfzeile:**
   ```csh
   w -hs
   ```

3. **Anzeige der Benutzer-ID:**
   ```csh
   w -u
   ```

4. **Nur aktive Benutzer anzeigen:**
   ```csh
   w | grep 'pts'
   ```

## Tipps
- Verwenden Sie `w` regelmäßig, um einen Überblick über die Systemnutzung zu erhalten.
- Kombinieren Sie `w` mit anderen Befehlen wie `grep`, um spezifische Benutzer oder Aktivitäten zu filtern.
- Beachten Sie, dass die Ausgabe von `w` je nach Benutzerrechten variieren kann.