# [Linux] C Shell (csh) renice Verwendung: Ändern der Priorität von Prozessen

## Übersicht
Der Befehl `renice` wird verwendet, um die Priorität von laufenden Prozessen in einem Unix-ähnlichen Betriebssystem zu ändern. Durch die Anpassung der Priorität kann die CPU-Zuteilung für bestimmte Prozesse beeinflusst werden, was besonders nützlich ist, um ressourcenintensive Anwendungen zu steuern.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
renice [Optionen] [Wert] [PID]
```

Hierbei steht `Wert` für den neuen Prioritätswert und `PID` für die Prozess-ID des Prozesses, dessen Priorität geändert werden soll.

## Häufige Optionen
- `-n`: Gibt den neuen Prioritätswert an.
- `-p`: Gibt die Prozess-ID an, deren Priorität geändert werden soll.
- `-g`: Ändert die Priorität aller Prozesse einer bestimmten Gruppe.
- `-u`: Ändert die Priorität aller Prozesse eines bestimmten Benutzers.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `renice`:

1. Ändern der Priorität eines Prozesses mit der PID 1234 auf 10:
   ```csh
   renice -n 10 -p 1234
   ```

2. Ändern der Priorität aller Prozesse eines bestimmten Benutzers (z.B. `username`) auf 5:
   ```csh
   renice -n 5 -u username
   ```

3. Ändern der Priorität aller Prozesse einer bestimmten Gruppe (z.B. Gruppe 5678) auf 15:
   ```csh
   renice -n 15 -g 5678
   ```

4. Überprüfen der aktuellen Priorität eines Prozesses (z.B. PID 1234) vor der Änderung:
   ```csh
   ps -o pid,ni,comm -p 1234
   ```

## Tipps
- Verwenden Sie `renice` mit Bedacht, da das Setzen einer zu hohen Priorität für einen Prozess andere wichtige Prozesse beeinträchtigen kann.
- Überprüfen Sie regelmäßig die Prioritäten Ihrer Prozesse, um sicherzustellen, dass Ihr System effizient läuft.
- Nutzen Sie den Befehl `top` oder `htop`, um die aktuellen Prozesse und deren Prioritäten in Echtzeit zu überwachen.