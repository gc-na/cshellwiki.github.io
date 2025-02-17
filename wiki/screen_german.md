# [Linux] Bash screen Verwendung: Sitzungen verwalten und im Hintergrund laufen lassen

## Übersicht
Der Befehl `screen` ermöglicht es Benutzern, mehrere Terminal-Sitzungen zu erstellen und zu verwalten. Mit `screen` können Sie Programme im Hintergrund ausführen und die Kontrolle über diese Sitzungen wiedererlangen, selbst wenn die Verbindung zum Terminal unterbrochen wird.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
screen [Optionen] [Argumente]
```

## Häufige Optionen
- `-S <name>`: Gibt einen Namen für die neue Sitzung an.
- `-d -r`: Trennen Sie eine Sitzung und stellen Sie sie wieder her.
- `-list`: Zeigt alle aktiven `screen`-Sitzungen an.
- `-X <Befehl>`: Sendet einen Befehl an eine laufende Sitzung.

## Häufige Beispiele
1. **Neue Sitzung erstellen**:
   ```bash
   screen -S meineSitzung
   ```

2. **Sitzung trennen** (Sie können die Sitzung später wiederherstellen):
   Drücken Sie `Ctrl + A`, gefolgt von `D`.

3. **Wiederherstellen einer getrennten Sitzung**:
   ```bash
   screen -r meineSitzung
   ```

4. **Liste aller aktiven Sitzungen anzeigen**:
   ```bash
   screen -list
   ```

5. **Befehl an eine Sitzung senden**:
   ```bash
   screen -S meineSitzung -X quit
   ```

## Tipps
- Verwenden Sie `screen` für lang laufende Prozesse, um sicherzustellen, dass sie nicht unterbrochen werden, wenn Sie die Verbindung verlieren.
- Benennen Sie Ihre Sitzungen mit `-S`, um die Verwaltung zu erleichtern.
- Nutzen Sie die Möglichkeit, mehrere Fenster innerhalb einer Sitzung zu erstellen, um verschiedene Aufgaben gleichzeitig zu erledigen. Drücken Sie `Ctrl + A`, gefolgt von `C`, um ein neues Fenster zu erstellen.