# [Linux] Bash umask Verwendung: Festlegung der Standardberechtigungen für neue Dateien und Verzeichnisse

## Übersicht
Der Befehl `umask` wird verwendet, um die Standardberechtigungen für neu erstellte Dateien und Verzeichnisse in einem Unix-ähnlichen Betriebssystem festzulegen. Er bestimmt, welche Berechtigungen beim Erstellen neuer Dateien und Verzeichnisse standardmäßig entzogen werden.

## Verwendung
Die grundlegende Syntax des `umask`-Befehls lautet:

```bash
umask [Optionen] [Argumente]
```

## Häufige Optionen
- `-S`: Zeigt die aktuelle umask in symbolischer Form an.
- `-p`: Zeigt die aktuelle umask für die aktuelle Shell an.

## Häufige Beispiele
1. **Aktuelle umask anzeigen**:
   ```bash
   umask
   ```

2. **Umask in symbolischer Form anzeigen**:
   ```bash
   umask -S
   ```

3. **Umask auf 022 setzen** (entzieht Schreibberechtigungen für Gruppen und andere):
   ```bash
   umask 022
   ```

4. **Umask auf 077 setzen** (entzieht alle Berechtigungen für Gruppen und andere):
   ```bash
   umask 077
   ```

5. **Umask für die aktuelle Shell temporär ändern**:
   ```bash
   umask 002
   # Erstellen Sie eine Datei, um die neuen Berechtigungen zu testen
   touch testfile
   ls -l testfile
   ```

## Tipps
- Überprüfen Sie regelmäßig Ihre umask-Einstellungen, um sicherzustellen, dass sie den Sicherheitsanforderungen Ihrer Umgebung entsprechen.
- Setzen Sie eine restriktive umask (z.B. 077) für sensible Projekte, um unbefugten Zugriff zu verhindern.
- Denken Sie daran, dass die umask nur für neue Dateien und Verzeichnisse gilt; bestehende Dateien bleiben unverändert.