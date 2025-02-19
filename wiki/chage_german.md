# [Linux] C Shell (csh) chage Verwendung: Benutzerpasswortalter verwalten

## Übersicht
Der Befehl `chage` wird verwendet, um die Passwortablaufrichtlinien für Benutzerkonten in einem Linux-System zu verwalten. Mit `chage` können Administratoren festlegen, wie lange ein Passwort gültig bleibt und wann der Benutzer gezwungen wird, ein neues Passwort zu wählen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
chage [Optionen] [Argumente]
```

## Häufige Optionen
- `-l, --list`: Zeigt die aktuellen Passwortablaufrichtlinien für den angegebenen Benutzer an.
- `-m, --mindays`: Legt die minimale Anzahl von Tagen fest, die zwischen Passwortänderungen liegen müssen.
- `-M, --maxdays`: Legt die maximale Anzahl von Tagen fest, die ein Passwort gültig ist.
- `-I, --inactive`: Legt die Anzahl der Tage fest, nach denen ein Konto inaktiv wird, nachdem das Passwort abgelaufen ist.
- `-E, --expire`: Legt das Ablaufdatum für das Benutzerkonto fest.

## Häufige Beispiele
- Um die aktuellen Passwortablaufrichtlinien für einen Benutzer namens `max` anzuzeigen:

```bash
chage -l max
```

- Um die maximale Gültigkeitsdauer eines Passworts für den Benutzer `max` auf 90 Tage festzulegen:

```bash
chage -M 90 max
```

- Um die minimale Anzahl von Tagen zwischen Passwortänderungen für den Benutzer `max` auf 7 Tage festzulegen:

```bash
chage -m 7 max
```

- Um das Ablaufdatum für das Benutzerkonto `max` auf den 31. Dezember 2023 festzulegen:

```bash
chage -E 2023-12-31 max
```

## Tipps
- Überprüfen Sie regelmäßig die Passwortablaufrichtlinien Ihrer Benutzer, um die Sicherheit zu gewährleisten.
- Verwenden Sie die Option `-l`, um sicherzustellen, dass die Einstellungen korrekt angewendet wurden.
- Informieren Sie Benutzer im Voraus über bevorstehende Passwortablaufdaten, um Unterbrechungen zu vermeiden.