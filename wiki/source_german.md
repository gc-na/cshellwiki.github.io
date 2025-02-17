# [Linux] Bash source Verwendung: Skripte ausführen und Umgebungsvariablen laden

## Übersicht
Der Befehl `source` wird in der Bash verwendet, um ein Skript oder eine Datei in die aktuelle Shell-Umgebung zu laden und auszuführen. Dies ermöglicht es, Funktionen und Variablen, die im Skript definiert sind, in der aktuellen Shell-Sitzung zu verwenden, ohne eine neue Shell zu starten.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
source [Optionen] [Argumente]
```

Alternativ kann auch der Punkt (`.`) verwendet werden, um dasselbe zu erreichen:

```bash
. [Optionen] [Argumente]
```

## Häufige Optionen
- `-e`: Beendet die Ausführung des Skripts, wenn ein Fehler auftritt.
- `-u`: Behandelt nicht definierte Variablen als Fehler.

## Häufige Beispiele

### Beispiel 1: Ein einfaches Skript ausführen
Angenommen, Sie haben ein Skript namens `mein_skript.sh`, das einige Variablen definiert:

```bash
source mein_skript.sh
```

### Beispiel 2: Umgebungsvariablen laden
Wenn Sie Umgebungsvariablen aus einer Datei namens `env.sh` laden möchten:

```bash
source env.sh
```

### Beispiel 3: Fehlerbehandlung aktivieren
Um sicherzustellen, dass das Skript bei einem Fehler sofort abbricht:

```bash
source -e mein_skript.sh
```

### Beispiel 4: Mit Punkt-Syntax
Die Verwendung des Punktes ist eine kürzere Schreibweise:

```bash
. mein_skript.sh
```

## Tipps
- Verwenden Sie `source`, um Konfigurationsdateien zu laden, die häufig in der Shell verwendet werden, wie `.bashrc` oder `.bash_profile`.
- Achten Sie darauf, dass das Skript ausführbare Berechtigungen hat, wenn Sie es mit `source` verwenden, da es in der aktuellen Shell ausgeführt wird.
- Testen Sie Skripte in einer separaten Shell, bevor Sie sie in Ihre Hauptumgebung laden, um unerwartete Änderungen zu vermeiden.