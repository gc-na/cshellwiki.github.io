# [Linux] Bash docker Verwendung: Container verwalten und ausführen

## Übersicht
Der `docker` Befehl ist ein leistungsstarkes Werkzeug zur Verwaltung von Containern. Mit Docker können Entwickler Anwendungen in Containern isoliert ausführen, was die Bereitstellung und Skalierung von Software vereinfacht.

## Verwendung
Die grundlegende Syntax des `docker` Befehls lautet:

```bash
docker [optionen] [argumente]
```

## Häufige Optionen
- `run`: Startet einen neuen Container.
- `ps`: Listet alle laufenden Container auf.
- `stop`: Stoppt einen laufenden Container.
- `rm`: Entfernt einen Container.
- `images`: Listet alle verfügbaren Images auf.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `docker` Befehls:

### 1. Einen neuen Container starten
```bash
docker run hello-world
```
Dieser Befehl startet einen neuen Container mit dem Image `hello-world`, das eine einfache Bestätigung ausgibt.

### 2. Alle laufenden Container auflisten
```bash
docker ps
```
Mit diesem Befehl können Sie alle aktuell laufenden Container anzeigen.

### 3. Einen Container stoppen
```bash
docker stop <container_id>
```
Ersetzen Sie `<container_id>` durch die ID des Containers, den Sie stoppen möchten.

### 4. Einen Container entfernen
```bash
docker rm <container_id>
```
Dieser Befehl entfernt den angegebenen Container. Stellen Sie sicher, dass der Container gestoppt ist, bevor Sie ihn entfernen.

### 5. Alle verfügbaren Images auflisten
```bash
docker images
```
Mit diesem Befehl können Sie alle Images auf Ihrem System anzeigen.

## Tipps
- Verwenden Sie `docker-compose`, um mehrere Container gleichzeitig zu verwalten und zu orchestrieren.
- Halten Sie Ihre Docker-Images klein, um die Ladezeiten zu verkürzen.
- Nutzen Sie Volumes, um Daten persistent zu speichern und zwischen Container-Neustarts zu erhalten.
- Überprüfen Sie regelmäßig die Sicherheit Ihrer Images, um Schwachstellen zu vermeiden.