# [Linux] C Shell (csh) umask Verwendung: Legt die Standardberechtigungen für neu erstellte Dateien und Verzeichnisse fest

## Übersicht
Der Befehl `umask` in der C Shell (csh) wird verwendet, um die Standardberechtigungen für neu erstellte Dateien und Verzeichnisse festzulegen. Er bestimmt, welche Berechtigungen beim Erstellen neuer Dateien und Verzeichnisse standardmäßig entzogen werden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
umask [Optionen] [Argumente]
```

## Häufige Optionen
- `-S`: Zeigt die aktuelle umask in symbolischer Form an.
- `-p`: Gibt die aktuelle umask für den aktuellen Benutzer aus.

## Häufige Beispiele

1. **Aktuelle umask anzeigen:**
   ```csh
   umask
   ```

2. **Umask auf 022 setzen:**
   ```csh
   umask 022
   ```
   Dies bedeutet, dass neue Dateien mit Berechtigungen von 644 (rw-r--r--) und neue Verzeichnisse mit 755 (rwxr-xr-x) erstellt werden.

3. **Umask auf 007 setzen:**
   ```csh
   umask 007
   ```
   Hierbei erhalten neue Dateien die Berechtigungen 660 (rw-rw----) und neue Verzeichnisse 770 (rwxrwx---).

4. **Umask in symbolischer Form anzeigen:**
   ```csh
   umask -S
   ```

## Tipps
- Überprüfen Sie regelmäßig Ihre umask-Einstellungen, um sicherzustellen, dass sie den gewünschten Sicherheitsanforderungen entsprechen.
- Setzen Sie die umask in Ihren Shell-Startdateien (z.B. `.cshrc`), um sicherzustellen, dass die Einstellungen bei jedem Start der Shell angewendet werden.
- Seien Sie vorsichtig beim Setzen einer umask, die zu lockere Berechtigungen gewährt, da dies Sicherheitsrisiken mit sich bringen kann.