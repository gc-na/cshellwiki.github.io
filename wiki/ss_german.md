# [Linux] Bash ss Verwendung: Netzwerkverbindungen anzeigen

## Übersicht
Der Befehl `ss` (Socket Statictics) wird verwendet, um Informationen über Netzwerkverbindungen und Sockets auf einem Linux-System anzuzeigen. Er ist ein leistungsfähiges Werkzeug zur Überwachung von Netzwerkverbindungen und bietet detaillierte Informationen über aktive Verbindungen, Ports und Protokolle.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
ss [Optionen] [Argumente]
```

## Häufige Optionen
- `-t`: Zeigt nur TCP-Verbindungen an.
- `-u`: Zeigt nur UDP-Verbindungen an.
- `-l`: Listet nur die Listening-Sockets auf.
- `-p`: Zeigt die zugehörigen Prozesse an.
- `-n`: Zeigt die numerischen Adressen und Ports an, anstatt sie aufzulösen.

## Häufige Beispiele

1. **Alle aktiven Verbindungen anzeigen:**
   ```bash
   ss
   ```

2. **Nur TCP-Verbindungen anzeigen:**
   ```bash
   ss -t
   ```

3. **Nur UDP-Verbindungen anzeigen:**
   ```bash
   ss -u
   ```

4. **Listening-Sockets anzeigen:**
   ```bash
   ss -l
   ```

5. **Verbindungen mit zugehörigen Prozessen anzeigen:**
   ```bash
   ss -p
   ```

6. **Numerische Adressen und Ports anzeigen:**
   ```bash
   ss -n
   ```

## Tipps
- Verwenden Sie die Kombination von Optionen, um spezifischere Informationen zu erhalten, z.B. `ss -tunlp`, um alle aktiven TCP- und UDP-Verbindungen mit Prozessinformationen anzuzeigen.
- Nutzen Sie `man ss`, um die vollständige Dokumentation und alle verfügbaren Optionen zu lesen.
- `ss` ist in der Regel schneller und ressourcenschonender als der ältere Befehl `netstat`, daher ist es empfehlenswert, `ss` für die Netzwerküberwachung zu verwenden.