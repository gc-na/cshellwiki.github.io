# [Linux] C Shell (csh) nohup Verwendung: Befehle im Hintergrund ausführen

## Übersicht
Der Befehl `nohup` (no hang up) wird verwendet, um Prozesse im Hintergrund auszuführen, die auch nach dem Abmelden des Benutzers weiterlaufen. Dies ist besonders nützlich, wenn lange laufende Aufgaben nicht unterbrochen werden sollen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
nohup [Optionen] [Argumente]
```

## Häufige Optionen
- `&`: Führt den Befehl im Hintergrund aus.
- `-o [Datei]`: Leitet die Ausgabe in die angegebene Datei um (standardmäßig `nohup.out`).
- `-h`: Zeigt eine Hilfe zu den Optionen an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `nohup`:

1. **Ein einfaches Skript im Hintergrund ausführen:**
   ```csh
   nohup ./mein_skript.sh &
   ```

2. **Ein lang laufender Befehl mit Ausgabeumleitung:**
   ```csh
   nohup long_running_command > ausgabe.log &
   ```

3. **Einen Python-Prozess im Hintergrund starten:**
   ```csh
   nohup python mein_programm.py &
   ```

4. **Einen Befehl im Hintergrund ausführen und die Ausgabe in eine Datei umleiten:**
   ```csh
   nohup ls -l > dateiliste.txt &
   ```

## Tipps
- Verwenden Sie `tail -f nohup.out`, um die Ausgabe eines laufenden Prozesses in Echtzeit zu überwachen.
- Überprüfen Sie regelmäßig die Ausgabedatei, um sicherzustellen, dass der Prozess wie erwartet läuft.
- Kombinieren Sie `nohup` mit `screen` oder `tmux`, um eine noch bessere Kontrolle über Ihre Hintergrundprozesse zu haben.