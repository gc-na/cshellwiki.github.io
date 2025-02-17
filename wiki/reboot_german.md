# [Linux] Bash reboot Verwendung: System neu starten

## Übersicht
Der Befehl `reboot` wird verwendet, um das System neu zu starten. Dies kann nützlich sein, um Änderungen an der Systemkonfiguration zu übernehmen oder um das System nach einem Absturz wiederherzustellen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
reboot [Optionen] [Argumente]
```

## Häufige Optionen
- `-f`: Erzwingt einen sofortigen Neustart ohne vorherige Warnung oder Herunterfahren.
- `-i`: Ignoriert alle laufenden Prozesse und startet das System sofort neu.
- `-n`: Führt einen Neustart ohne das vorherige Entladen von Dateisystemen durch.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `reboot`-Befehls:

1. **Einfacher Neustart des Systems:**
   ```bash
   reboot
   ```

2. **Erzwinge einen sofortigen Neustart:**
   ```bash
   reboot -f
   ```

3. **Neustart ohne Entladen von Dateisystemen:**
   ```bash
   reboot -n
   ```

4. **Neustart mit einer spezifischen Zeitverzögerung (z.B. 1 Minute):**
   ```bash
   shutdown -r +1
   ```

## Tipps
- Verwenden Sie den Befehl `shutdown` anstelle von `reboot`, wenn Sie eine Warnung an andere Benutzer senden möchten.
- Stellen Sie sicher, dass alle wichtigen Daten gespeichert sind, bevor Sie das System neu starten.
- Testen Sie den Befehl in einer sicheren Umgebung, um unerwartete Probleme zu vermeiden.