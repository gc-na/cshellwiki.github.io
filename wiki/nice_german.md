# [Linux] Bash nice Verwendung: Steuern der Prozesspriorität

## Übersicht
Der Befehl `nice` wird verwendet, um die Priorität eines Prozesses beim Ausführen eines Befehls in der Bash zu steuern. Er ermöglicht es Benutzern, die CPU-Zeit, die ein Prozess erhält, zu beeinflussen, indem sie eine "Nettigkeit" (nice value) angeben. Ein niedrigerer Wert bedeutet eine höhere Priorität, während ein höherer Wert eine niedrigere Priorität bedeutet.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
nice [Optionen] [Befehl]
```

## Häufige Optionen
- `-n, --adjustment=N`: Setzt den Nettigkeitswert auf N. Der Standardwert ist 10.
- `-h, --help`: Zeigt eine Hilfenachricht an.
- `--version`: Gibt die Versionsnummer des Befehls aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `nice`-Befehls:

1. **Einen Prozess mit Standard-Nettigkeit starten:**
   ```bash
   nice myscript.sh
   ```

2. **Einen Prozess mit einer spezifischen Nettigkeit starten:**
   ```bash
   nice -n 5 myscript.sh
   ```

3. **Einen Prozess mit niedrigerer Priorität ausführen:**
   ```bash
   nice -n 19 myscript.sh
   ```

4. **Einen Prozess mit höherer Priorität ausführen (erfordert Root-Rechte):**
   ```bash
   sudo nice -n -5 myscript.sh
   ```

## Tipps
- Verwenden Sie `nice`, um ressourcenintensive Prozesse zu starten, ohne die Leistung anderer wichtiger Anwendungen zu beeinträchtigen.
- Überprüfen Sie die aktuelle Nettigkeit eines laufenden Prozesses mit dem Befehl `ps -o pid,ni,cmd`.
- Seien Sie vorsichtig, wenn Sie negative Nettigkeitswerte verwenden, da dies die Systemleistung beeinträchtigen kann, wenn zu viele Prozesse mit hoher Priorität laufen.