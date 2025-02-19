# [Linux] C Shell (csh) killall Verwendung: Prozesse beenden

## Übersicht
Der Befehl `killall` wird verwendet, um alle Prozesse mit einem bestimmten Namen zu beenden. Dies ist nützlich, wenn Sie mehrere Instanzen eines Programms laufen haben und alle gleichzeitig schließen möchten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
killall [optionen] [argumente]
```

## Häufige Optionen
- `-u [benutzer]`: Beendet nur die Prozesse, die von dem angegebenen Benutzer ausgeführt werden.
- `-i`: Fragt vor dem Beenden jedes Prozesses nach Bestätigung.
- `-q`: Unterdrückt die Ausgabe von Fehlermeldungen, wenn kein Prozess gefunden wird.
- `-s [signal]`: Gibt das Signal an, das an die Prozesse gesendet werden soll (z.B. `SIGTERM`, `SIGKILL`).

## Häufige Beispiele
Um alle Instanzen eines Programms namens `firefox` zu beenden, verwenden Sie:

```csh
killall firefox
```

Um alle `python`-Prozesse zu beenden und vorher um Bestätigung zu bitten, verwenden Sie:

```csh
killall -i python
```

Um alle Prozesse eines bestimmten Benutzers zu beenden, verwenden Sie:

```csh
killall -u username
```

Um ein spezifisches Signal, wie `SIGKILL`, an alle `gedit`-Prozesse zu senden, verwenden Sie:

```csh
killall -s SIGKILL gedit
```

## Tipps
- Seien Sie vorsichtig mit `killall`, da es alle Prozesse mit dem angegebenen Namen beendet. Vergewissern Sie sich, dass Sie den richtigen Prozess angeben.
- Nutzen Sie die `-i`-Option, um versehentliche Beendigungen zu vermeiden, besonders in produktiven Umgebungen.
- Überprüfen Sie die laufenden Prozesse mit `ps` oder `top`, um sicherzustellen, dass Sie die richtigen Prozesse beenden.