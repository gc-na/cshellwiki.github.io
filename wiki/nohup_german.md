# [Linux] Bash nohup Verwendung: Prozesse im Hintergrund ausführen

## Übersicht
Der `nohup`-Befehl (no hang up) wird verwendet, um Prozesse im Hintergrund auszuführen, sodass sie auch dann weiterlaufen, wenn die Sitzung beendet wird. Dies ist besonders nützlich, wenn Sie lange laufende Aufgaben haben, die nicht unterbrochen werden sollen, wenn Sie sich abmelden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
nohup [Optionen] [Befehle] &
```

Das `&` am Ende des Befehls sorgt dafür, dass der Prozess im Hintergrund ausgeführt wird.

## Häufige Optionen
- `-h`: Zeigt die Hilfe an und listet alle verfügbaren Optionen auf.
- `-v`: Aktiviert den ausführlichen Modus, um mehr Informationen über den Prozess anzuzeigen.
- `--help`: Zeigt eine Hilfeseite mit Informationen zur Verwendung von nohup an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `nohup`:

1. **Ein einfaches Skript im Hintergrund ausführen:**

   ```bash
   nohup ./mein_skript.sh &
   ```

2. **Einen Python-Server im Hintergrund starten:**

   ```bash
   nohup python3 -m http.server 8000 &
   ```

3. **Ein lang laufendes Backup-Skript ausführen und die Ausgabe in eine Datei umleiten:**

   ```bash
   nohup ./backup.sh > backup.log 2>&1 &
   ```

4. **Einen Prozess mit einer spezifischen Priorität im Hintergrund ausführen:**

   ```bash
   nohup nice -n 19 ./langlaufender_prozess &
   ```

## Tipps
- Verwenden Sie `nohup` zusammen mit `&`, um sicherzustellen, dass der Prozess im Hintergrund läuft und nicht von der Sitzung abhängt.
- Leiten Sie die Ausgabe in eine Datei um, um Protokolle zu speichern und Fehler zu überwachen.
- Überprüfen Sie regelmäßig die Ausgabedatei, um sicherzustellen, dass der Prozess wie erwartet läuft.