# [Linux] C Shell (csh) tput Verwendung: Terminalsteuerung und -formatierung

## Übersicht
Der Befehl `tput` wird verwendet, um terminalbezogene Informationen abzurufen und Terminalsteuerungen durchzuführen. Er ermöglicht es Benutzern, die Anzeige von Text im Terminal zu formatieren, Farben zu setzen und verschiedene Terminalfunktionen zu steuern.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
tput [Optionen] [Argumente]
```

## Häufige Optionen
- `clear`: Löscht den Bildschirm des Terminals.
- `setaf [FARBE]`: Setzt die Vordergrundfarbe auf die angegebene Farbe (z.B. `setaf 1` für rot).
- `setab [FARBE]`: Setzt die Hintergrundfarbe auf die angegebene Farbe (z.B. `setab 2` für grün).
- `bold`: Aktiviert den fetten Text.
- `smso`: Aktiviert den unterstrichenen Text.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `tput`:

1. **Bildschirm löschen**:
   ```csh
   tput clear
   ```

2. **Text in roter Farbe ausgeben**:
   ```csh
   tput setaf 1
   echo "Dies ist roter Text"
   tput sgr0  # Setzt die Farben zurück
   ```

3. **Text fett formatieren**:
   ```csh
   tput bold
   echo "Dies ist fetter Text"
   tput sgr0  # Setzt die Formatierung zurück
   ```

4. **Text unterstreichen**:
   ```csh
   tput smso
   echo "Dies ist unterstrichener Text"
   tput rmso  # Entfernt die Unterstreichung
   ```

5. **Hintergrundfarbe ändern**:
   ```csh
   tput setab 4  # Setzt die Hintergrundfarbe auf blau
   echo "Text mit blauem Hintergrund"
   tput sgr0  # Setzt die Farben zurück
   ```

## Tipps
- Verwenden Sie `tput sgr0`, um alle Formatierungen und Farben zurückzusetzen, bevor Sie neuen Text ausgeben.
- Experimentieren Sie mit verschiedenen Farbnummern, um die gewünschten Farben für Vorder- und Hintergrund zu finden.
- Kombinieren Sie mehrere `tput` Befehle, um komplexe Formatierungen zu erstellen, z.B. fetter und roter Text gleichzeitig.