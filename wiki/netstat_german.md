# [Linux] Bash netstat Verwendung: Netzwerkverbindungen anzeigen

## Übersicht
Der Befehl `netstat` wird verwendet, um Netzwerkverbindungen, Routing-Tabellen, Schnittstellenstatistiken und andere Netzwerkinformationen auf einem System anzuzeigen. Er ist ein nützliches Werkzeug zur Diagnose von Netzwerkproblemen und zur Überwachung von Netzwerkaktivitäten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
netstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle Verbindungen und Listening-Ports an.
- `-t`: Zeigt nur TCP-Verbindungen an.
- `-u`: Zeigt nur UDP-Verbindungen an.
- `-n`: Zeigt Adressen und Portnummern numerisch an, anstatt sie in Namen aufzulösen.
- `-l`: Zeigt nur Listening-Ports an.
- `-p`: Zeigt den Prozess an, der die Verbindung verwendet.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `netstat`:

1. **Alle Verbindungen anzeigen:**
   ```bash
   netstat -a
   ```

2. **Nur aktive TCP-Verbindungen anzeigen:**
   ```bash
   netstat -t
   ```

3. **Nur Listening-Ports anzeigen:**
   ```bash
   netstat -l
   ```

4. **Verbindungen mit numerischen Adressen anzeigen:**
   ```bash
   netstat -n
   ```

5. **Verbindungen mit Prozessinformationen anzeigen:**
   ```bash
   netstat -p
   ```

## Tipps
- Verwenden Sie die Option `-n`, um die Ausgabe zu beschleunigen, da die Namensauflösung umgangen wird.
- Kombinieren Sie Optionen, um spezifischere Informationen zu erhalten, z.B. `netstat -tunlp` für alle aktiven TCP- und UDP-Verbindungen mit Prozessinformationen.
- Nutzen Sie `grep`, um die Ausgabe zu filtern, z.B. `netstat -a | grep LISTEN`, um nur die Listening-Ports anzuzeigen.