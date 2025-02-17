# [Linux] Bash renice Verwendung: Ändern der Priorität von Prozessen

## Übersicht
Der Befehl `renice` wird verwendet, um die Priorität von laufenden Prozessen in einem Linux-System zu ändern. Mit diesem Befehl können Benutzer die CPU-Zuteilung für bestimmte Prozesse anpassen, um die Systemleistung zu optimieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
renice [Optionen] [Wert] [PID...]
```

Hierbei steht `Wert` für den neuen Prioritätswert, und `PID` ist die Prozess-ID des Prozesses, dessen Priorität geändert werden soll.

## Häufige Optionen
- `-n`: Gibt den neuen Prioritätswert an.
- `-p`: Gibt die PID des Prozesses an, dessen Priorität geändert werden soll.
- `-g`: Ändert die Priorität aller Prozesse einer bestimmten Gruppe.
- `-u`: Ändert die Priorität aller Prozesse eines bestimmten Benutzers.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `renice`:

1. **Ändern der Priorität eines einzelnen Prozesses:**
   ```bash
   renice -n 10 -p 1234
   ```
   In diesem Beispiel wird die Priorität des Prozesses mit der PID 1234 auf 10 gesetzt.

2. **Ändern der Priorität mehrerer Prozesse:**
   ```bash
   renice -n 5 -p 1234 5678
   ```
   Hier wird die Priorität der Prozesse mit den PIDs 1234 und 5678 auf 5 gesetzt.

3. **Ändern der Priorität aller Prozesse eines Benutzers:**
   ```bash
   renice -n 15 -u benutzername
   ```
   In diesem Beispiel wird die Priorität aller Prozesse des Benutzers `benutzername` auf 15 gesetzt.

4. **Ändern der Priorität aller Prozesse einer Gruppe:**
   ```bash
   renice -n -5 -g gruppenname
   ```
   Hier wird die Priorität aller Prozesse der Gruppe `gruppenname` auf -5 gesetzt.

## Tipps
- Verwenden Sie `renice` mit Bedacht, da das Setzen einer zu niedrigen Priorität dazu führen kann, dass wichtige Prozesse nicht genügend CPU-Ressourcen erhalten.
- Um die aktuelle Priorität eines Prozesses zu überprüfen, können Sie den Befehl `ps` verwenden:
  ```bash
  ps -o pid,ni,cmd
  ```
- Beachten Sie, dass nur der Benutzer, der den Prozess gestartet hat, oder der Root-Benutzer die Priorität eines Prozesses ändern kann.