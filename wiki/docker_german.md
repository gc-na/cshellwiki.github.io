# [Linux] C Shell (csh) docker Verwendung: Container verwalten und orchestrieren

## Übersicht
Der `docker` Befehl wird verwendet, um Container zu verwalten und zu orchestrieren. Mit Docker können Sie Anwendungen in Containern isoliert ausführen, was eine konsistente Umgebung für die Entwicklung und Bereitstellung schafft.

## Verwendung
Die grundlegende Syntax des `docker` Befehls lautet:

```csh
docker [optionen] [argumente]
```

## Häufige Optionen
- `run`: Startet einen neuen Container.
- `ps`: Listet alle laufenden Container auf.
- `stop`: Stoppt einen laufenden Container.
- `rm`: Entfernt einen gestoppten Container.
- `images`: Zeigt alle verfügbaren Images an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `docker` Befehls:

### 1. Einen neuen Container starten
```csh
docker run -d --name mein_container nginx
```
Dieser Befehl startet einen neuen Container mit dem Namen `mein_container` basierend auf dem `nginx` Image.

### 2. Laufende Container auflisten
```csh
docker ps
```
Mit diesem Befehl können Sie alle derzeit laufenden Container anzeigen.

### 3. Einen Container stoppen
```csh
docker stop mein_container
```
Dieser Befehl stoppt den Container mit dem Namen `mein_container`.

### 4. Einen gestoppten Container entfernen
```csh
docker rm mein_container
```
Hiermit wird der gestoppte Container `mein_container` entfernt.

### 5. Verfügbare Images anzeigen
```csh
docker images
```
Dieser Befehl listet alle lokal gespeicherten Docker-Images auf.

## Tipps
- Verwenden Sie `docker-compose`, um mehrere Container als Dienst zu verwalten.
- Halten Sie Ihre Images klein, um die Ladezeiten zu verbessern.
- Nutzen Sie Tags, um verschiedene Versionen Ihrer Images zu verwalten und zu kennzeichnen.