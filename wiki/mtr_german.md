# [Linux] Bash mtr Verwendung: Netzwerkverbindung testen

## Übersicht
Der `mtr`-Befehl (My Traceroute) kombiniert die Funktionen von `ping` und `traceroute`, um die Netzwerkverbindung zu einem Ziel zu analysieren. Er zeigt die Route von Ihrem Computer zu einem bestimmten Host und misst die Latenz und Paketverluste auf jedem Hop.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
mtr [Optionen] [Ziel]
```

## Häufige Optionen
- `-r`: Führt einen Report-Modus aus, der die Ergebnisse in einer zusammenfassenden Form anzeigt.
- `-c [Anzahl]`: Gibt die Anzahl der gesendeten Pakete an.
- `-i [Intervall]`: Setzt das Intervall zwischen den gesendeten Paketen in Sekunden.
- `-p`: Führt den Befehl im "Ping"-Modus aus, ohne die Route anzuzeigen.

## Häufige Beispiele
1. **Einfaches MTR zu einem Ziel:**
   ```bash
   mtr example.com
   ```

2. **MTR im Report-Modus:**
   ```bash
   mtr -r example.com
   ```

3. **MTR mit einer bestimmten Anzahl von Paketen:**
   ```bash
   mtr -c 10 example.com
   ```

4. **MTR mit einem Intervall von 1 Sekunde:**
   ```bash
   mtr -i 1 example.com
   ```

5. **MTR im Ping-Modus:**
   ```bash
   mtr -p example.com
   ```

## Tipps
- Verwenden Sie den Report-Modus (`-r`), wenn Sie eine schnelle Zusammenfassung der Netzwerkverbindung benötigen.
- Experimentieren Sie mit der Anzahl der Pakete (`-c`), um ein besseres Bild der Netzwerkstabilität zu erhalten.
- Nutzen Sie das Intervall (`-i`), um die Häufigkeit der gesendeten Pakete anzupassen, besonders bei der Fehlersuche in Echtzeit.
- Achten Sie darauf, dass einige Netzwerke ICMP-Pakete blockieren können, was die Ergebnisse von `mtr` beeinflussen könnte.