# [Linux] C Shell (csh) netstat Verwendung: Netzwerkverbindungen anzeigen

## Übersicht
Der Befehl `netstat` wird verwendet, um Netzwerkverbindungen, Routing-Tabellen, Schnittstellenstatistiken und andere Netzwerkinformationen anzuzeigen. Er ist ein nützliches Werkzeug zur Diagnose von Netzwerkproblemen und zur Überwachung von Netzwerkaktivitäten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
netstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle Verbindungen und Listening-Ports an.
- `-n`: Zeigt Adressen und Portnummern in numerischer Form an, anstatt sie in Namen aufzulösen.
- `-t`: Zeigt nur TCP-Verbindungen an.
- `-u`: Zeigt nur UDP-Verbindungen an.
- `-l`: Zeigt nur Listening-Ports an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `netstat`:

1. **Alle aktiven Verbindungen anzeigen:**
   ```csh
   netstat -a
   ```

2. **TCP-Verbindungen in numerischer Form anzeigen:**
   ```csh
   netstat -tn
   ```

3. **Nur Listening-Ports anzeigen:**
   ```csh
   netstat -l
   ```

4. **UDP-Verbindungen anzeigen:**
   ```csh
   netstat -u
   ```

5. **Statistiken für alle Schnittstellen anzeigen:**
   ```csh
   netstat -i
   ```

## Tipps
- Verwenden Sie die Option `-n`, um die Ausgabe zu beschleunigen, da die Namensauflösung vermieden wird.
- Kombinieren Sie Optionen, um spezifischere Informationen zu erhalten, z.B. `netstat -tunl` für alle aktiven TCP- und UDP-Verbindungen, die auf Ports lauschen.
- Überprüfen Sie regelmäßig die Netzwerkverbindungen, um unautorisierte Zugriffe oder ungewöhnliche Aktivitäten zu erkennen.