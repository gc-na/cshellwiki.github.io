# [Linux] Bash hostname Verwendung: Zeigt oder setzt den Hostnamen des Systems an

## Übersicht
Der Befehl `hostname` wird verwendet, um den aktuellen Hostnamen des Systems anzuzeigen oder zu ändern. Der Hostname ist der Name, unter dem ein Computer im Netzwerk identifiziert wird.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
hostname [Optionen] [Argumente]
```

## Häufige Optionen
- `-s`: Zeigt nur den kurzen Hostnamen an (ohne Domain).
- `-f`: Zeigt den vollständigen Hostnamen (Fully Qualified Domain Name, FQDN) an.
- `-i`: Gibt die IP-Adresse des Hostnamens zurück.
- `-b`: Setzt den Hostnamen auf den angegebenen Wert.

## Häufige Beispiele
Um den aktuellen Hostnamen anzuzeigen:

```bash
hostname
```

Um den kurzen Hostnamen anzuzeigen:

```bash
hostname -s
```

Um den vollständigen Hostnamen anzuzeigen:

```bash
hostname -f
```

Um die IP-Adresse des Hostnamens zu erhalten:

```bash
hostname -i
```

Um den Hostnamen zu ändern:

```bash
sudo hostname neuer-hostname
```

## Tipps
- Verwenden Sie `sudo`, um den Hostnamen zu ändern, da Administratorrechte erforderlich sind.
- Überprüfen Sie nach dem Ändern des Hostnamens die Netzwerkeinstellungen, um sicherzustellen, dass alles korrekt konfiguriert ist.
- Denken Sie daran, dass Änderungen am Hostnamen möglicherweise einen Neustart des Systems oder der Netzwerkschnittstelle erfordern, um wirksam zu werden.