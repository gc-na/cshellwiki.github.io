# [Linux] C Shell (csh) yum Verwendung: Paketverwaltung unter Linux

## Übersicht
Der `yum`-Befehl (Yellowdog Updater, Modified) ist ein Paketverwaltungstool für Linux-Distributionen, das auf RPM-Paketen basiert. Er ermöglicht das Installieren, Aktualisieren und Entfernen von Softwarepaketen sowie das Verwalten von Repositories.

## Verwendung
Die grundlegende Syntax des `yum`-Befehls lautet:

```bash
yum [Optionen] [Argumente]
```

## Häufige Optionen
- `install`: Installiert ein oder mehrere Pakete.
- `remove`: Entfernt ein oder mehrere Pakete.
- `update`: Aktualisiert alle installierten Pakete auf die neueste Version.
- `search`: Sucht nach Paketen, die einem bestimmten Namen oder einer Beschreibung entsprechen.
- `info`: Zeigt Informationen über ein bestimmtes Paket an.

## Häufige Beispiele
- Um ein Paket zu installieren, verwenden Sie:

```bash
yum install paketname
```

- Um ein Paket zu entfernen, verwenden Sie:

```bash
yum remove paketname
```

- Um alle installierten Pakete zu aktualisieren, verwenden Sie:

```bash
yum update
```

- Um nach einem Paket zu suchen, verwenden Sie:

```bash
yum search suchbegriff
```

- Um Informationen über ein bestimmtes Paket anzuzeigen, verwenden Sie:

```bash
yum info paketname
```

## Tipps
- Verwenden Sie `yum clean all`, um den Cache zu leeren und Speicherplatz freizugeben.
- Überprüfen Sie regelmäßig auf Updates, um sicherzustellen, dass Ihre Software auf dem neuesten Stand ist.
- Nutzen Sie `yum list installed`, um eine Liste aller installierten Pakete anzuzeigen.