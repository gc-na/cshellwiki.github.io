# [Linux] C Shell (csh) script Verwendung: Erstellen von Terminalaufzeichnungen

## Übersicht
Der `script` Befehl wird verwendet, um eine Aufzeichnung aller Terminalausgaben in einer Datei zu erstellen. Dies ist nützlich, um eine Sitzung zu protokollieren oder um Befehle und deren Ausgaben für spätere Referenz zu speichern.

## Verwendung
Die grundlegende Syntax des `script` Befehls lautet:

```csh
script [Optionen] [Dateiname]
```

## Häufige Optionen
- `-a`: Fügt die Ausgabe an eine bestehende Datei an, anstatt sie zu überschreiben.
- `-q`: Unterdrückt die Ausgabe von Start- und Endenachrichten.
- `-t`: Erstellt eine Timing-Datei, die die Zeitstempel für die Eingaben und Ausgaben aufzeichnet.

## Häufige Beispiele

1. **Einfaches Aufzeichnen einer Sitzung:**
   Um eine neue Sitzung aufzuzeichnen, können Sie den folgenden Befehl verwenden:

   ```csh
   script aufzeichnung.txt
   ```

   Dies startet die Aufzeichnung und speichert die Ausgabe in `aufzeichnung.txt`. Um die Aufzeichnung zu beenden, geben Sie `exit` ein.

2. **An eine bestehende Datei anhängen:**
   Wenn Sie eine bestehende Datei aktualisieren möchten, verwenden Sie die `-a` Option:

   ```csh
   script -a aufzeichnung.txt
   ```

3. **Aufzeichnung ohne Start- und Endenachrichten:**
   Um die Start- und Endenachrichten zu unterdrücken, verwenden Sie die `-q` Option:

   ```csh
   script -q aufzeichnung.txt
   ```

4. **Aufzeichnung mit Timing:**
   Um eine Timing-Datei zu erstellen, verwenden Sie die `-t` Option:

   ```csh
   script -t timing.txt aufzeichnung.txt
   ```

## Tipps
- Überprüfen Sie die Größe der Aufzeichnungsdatei regelmäßig, um sicherzustellen, dass sie nicht zu groß wird.
- Nutzen Sie die `-a` Option, um mehrere Sitzungen in einer Datei zu kombinieren, wenn Sie eine fortlaufende Dokumentation benötigen.
- Denken Sie daran, die Aufzeichnung zu beenden, indem Sie `exit` eingeben, um sicherzustellen, dass alle Daten korrekt gespeichert werden.