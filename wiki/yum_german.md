# [Linux] Bash yum Verwendung: Paketverwaltung unter Linux

## Übersicht
Der `yum`-Befehl (Yellowdog Updater, Modified) ist ein Paketverwaltungstool für Linux-Distributionen, die auf RPM basieren. Er ermöglicht das Installieren, Aktualisieren und Entfernen von Softwarepaketen sowie das Verwalten von Abhängigkeiten.

## Verwendung
Die grundlegende Syntax des `yum`-Befehls lautet:

```bash
yum [Optionen] [Argumente]
```

## Häufige Optionen
- `install`: Installiert ein oder mehrere Pakete.
- `remove`: Entfernt ein oder mehrere Pakete.
- `update`: Aktualisiert alle installierten Pakete auf die neueste Version.
- `list`: Zeigt eine Liste von Paketen an.
- `search`: Sucht nach Paketen, die einem bestimmten Muster entsprechen.
- `info`: Zeigt Informationen über ein bestimmtes Paket an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `yum`:

### Paket installieren
Um ein Paket zu installieren, verwenden Sie den folgenden Befehl:

```bash
yum install paketname
```

### Paket entfernen
Um ein Paket zu entfernen, verwenden Sie:

```bash
yum remove paketname
```

### Pakete aktualisieren
Um alle installierten Pakete zu aktualisieren, führen Sie aus:

```bash
yum update
```

### Verfügbare Pakete auflisten
Um eine Liste aller verfügbaren Pakete anzuzeigen, verwenden Sie:

```bash
yum list available
```

### Nach einem Paket suchen
Um nach einem bestimmten Paket zu suchen, verwenden Sie:

```bash
yum search suchbegriff
```

### Informationen zu einem Paket anzeigen
Um Informationen über ein bestimmtes Paket zu erhalten, verwenden Sie:

```bash
yum info paketname
```

## Tipps
- Verwenden Sie `yum clean all`, um den Cache zu leeren und Speicherplatz freizugeben.
- Überprüfen Sie regelmäßig auf Updates, um sicherzustellen, dass Ihr System sicher und stabil bleibt.
- Nutzen Sie `yum groupinstall`, um eine Gruppe von Paketen zu installieren, die zusammengehören, z.B. Entwicklungswerkzeuge.