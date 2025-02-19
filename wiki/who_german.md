# [Linux] C Shell (csh) who Verwendung: Zeigt angemeldete Benutzer an

## Übersicht
Der Befehl `who` zeigt eine Liste der Benutzer an, die derzeit am System angemeldet sind. Diese Informationen umfassen den Benutzernamen, das Terminal, von dem aus sie angemeldet sind, sowie das Datum und die Uhrzeit ihrer Anmeldung.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
who [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle verfügbaren Informationen über die Benutzer an.
- `-b`: Gibt die letzte Systemstartzeit aus.
- `-q`: Zeigt nur die Benutzernamen und die Anzahl der angemeldeten Benutzer an.
- `-r`: Zeigt die aktuelle Runlevel-Nummer des Systems an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `who`-Befehls:

1. **Einfaches Anzeigen der angemeldeten Benutzer:**
   ```csh
   who
   ```

2. **Anzeigen aller verfügbaren Informationen:**
   ```csh
   who -a
   ```

3. **Anzeigen der letzten Systemstartzeit:**
   ```csh
   who -b
   ```

4. **Anzeigen der Anzahl der angemeldeten Benutzer:**
   ```csh
   who -q
   ```

5. **Anzeigen der aktuellen Runlevel-Nummer:**
   ```csh
   who -r
   ```

## Tipps
- Verwenden Sie `who -a`, um umfassende Informationen zu erhalten, die Ihnen helfen können, das System besser zu verstehen.
- Kombinieren Sie `who` mit anderen Befehlen wie `grep`, um spezifische Benutzer zu finden.
- Nutzen Sie `who -q`, wenn Sie schnell die Anzahl der Benutzer überprüfen möchten, ohne eine vollständige Liste anzuzeigen.