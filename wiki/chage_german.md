# [Linux] Bash chage Verwendung: Benutzerpasswort-Ablauf verwalten

## Übersicht
Der Befehl `chage` wird verwendet, um die Passwortablauf- und Änderungsrichtlinien für Benutzerkonten in Linux-Systemen zu verwalten. Mit `chage` können Administratoren festlegen, wie oft ein Benutzer sein Passwort ändern muss und wann das Passwort abläuft.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
chage [Optionen] [Benutzername]
```

## Häufige Optionen
- `-l`: Zeigt die aktuellen Passwortablaufinformationen für den angegebenen Benutzer an.
- `-m`: Legt die minimale Anzahl von Tagen fest, die zwischen Passwortänderungen liegen müssen.
- `-M`: Legt die maximale Anzahl von Tagen fest, die ein Passwort gültig ist.
- `-I`: Legt die Anzahl der Tage fest, nach denen das Konto inaktiv wird, nachdem das Passwort abgelaufen ist.
- `-E`: Setzt das Ablaufdatum des Kontos.

## Häufige Beispiele

1. **Aktuelle Passwortablaufinformationen anzeigen:**
   ```bash
   chage -l benutzername
   ```

2. **Minimale Tage zwischen Passwortänderungen auf 7 setzen:**
   ```bash
   chage -m 7 benutzername
   ```

3. **Maximale Gültigkeitsdauer des Passworts auf 30 Tage setzen:**
   ```bash
   chage -M 30 benutzername
   ```

4. **Inaktivitätszeit auf 15 Tage setzen:**
   ```bash
   chage -I 15 benutzername
   ```

5. **Ablaufdatum des Kontos auf den 1. Januar 2024 setzen:**
   ```bash
   chage -E 2024-01-01 benutzername
   ```

## Tipps
- Überprüfen Sie regelmäßig die Passwortablaufinformationen für alle Benutzer, um die Sicherheit zu gewährleisten.
- Setzen Sie angemessene Fristen für Passwortänderungen, um die Benutzer nicht unnötig zu belasten.
- Dokumentieren Sie Änderungen an den Passwortrichtlinien, um die Nachverfolgbarkeit zu gewährleisten.