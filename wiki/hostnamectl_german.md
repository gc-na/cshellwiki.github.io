# [Linux] Bash hostnamectl Verwendung: Systeminformationen verwalten

## Übersicht
Der Befehl `hostnamectl` wird verwendet, um den Hostnamen und andere systembezogene Informationen in Linux-basierten Betriebssystemen zu verwalten. Mit diesem Befehl können Sie den aktuellen Hostnamen anzeigen, ändern und verschiedene Eigenschaften des Systems abfragen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
hostnamectl [Optionen] [Argumente]
```

## Häufige Optionen
- `set-hostname`: Ändert den Hostnamen des Systems.
- `status`: Zeigt den aktuellen Status des Systems an, einschließlich Hostname, Betriebssystem und Kernel-Version.
- `set-icon-name`: Setzt den Symbolnamen des Systems.
- `set-chassis`: Legt den Chassis-Typ des Systems fest (z. B. "desktop", "laptop").
- `help`: Zeigt eine Hilfeseite mit verfügbaren Optionen und deren Beschreibungen an.

## Häufige Beispiele
Um den aktuellen Hostnamen anzuzeigen, verwenden Sie:

```bash
hostnamectl status
```

Um den Hostnamen auf "neuer-hostname" zu ändern, führen Sie den folgenden Befehl aus:

```bash
sudo hostnamectl set-hostname neuer-hostname
```

Um den Chassis-Typ auf "laptop" zu setzen, verwenden Sie:

```bash
sudo hostnamectl set-chassis laptop
```

Um den Symbolnamen auf "computer-laptop" zu setzen, führen Sie aus:

```bash
sudo hostnamectl set-icon-name computer-laptop
```

## Tipps
- Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen verfügen (z. B. als Root-Benutzer oder mit `sudo`), um den Hostnamen zu ändern.
- Überprüfen Sie nach der Änderung des Hostnamens, ob die Änderung erfolgreich war, indem Sie `hostnamectl status` erneut ausführen.
- Beachten Sie, dass einige Anwendungen möglicherweise neu gestartet werden müssen, um den neuen Hostnamen zu erkennen.