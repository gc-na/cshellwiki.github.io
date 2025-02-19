# [Linux] C Shell (csh) hostname Verwendung: Zeigt den Hostnamen des Systems an

## Übersicht
Der Befehl `hostname` wird verwendet, um den Namen des aktuellen Hosts (Rechners) anzuzeigen oder zu ändern. Dies ist besonders nützlich, um den Computer in einem Netzwerk zu identifizieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
hostname [optionen] [argumente]
```

## Häufige Optionen
- `-f`: Zeigt den vollständigen qualifizierten Domainnamen (FQDN) des Hosts an.
- `-s`: Gibt nur den kurzen Hostnamen aus.
- `-i`: Zeigt die IP-Adresse des Hosts an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `hostname`-Befehls:

1. **Aktuellen Hostnamen anzeigen:**
   ```csh
   hostname
   ```

2. **Vollständigen qualifizierten Domainnamen anzeigen:**
   ```csh
   hostname -f
   ```

3. **Kurzen Hostnamen anzeigen:**
   ```csh
   hostname -s
   ```

4. **IP-Adresse des Hosts anzeigen:**
   ```csh
   hostname -i
   ```

5. **Hostnamen ändern:**
   ```csh
   hostname neuer-hostname
   ```

## Tipps
- Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen verfügen, um den Hostnamen zu ändern.
- Verwenden Sie den Befehl `hostname` ohne Optionen, um schnell den aktuellen Hostnamen zu überprüfen.
- Der Hostname sollte einfach und einprägsam sein, insbesondere in Netzwerken mit vielen Geräten.