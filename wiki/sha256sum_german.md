# [Linux] Bash sha256sum Verwendung: Berechnung von SHA-256-Hashwerten

## Übersicht
Der Befehl `sha256sum` wird verwendet, um den SHA-256-Hashwert einer Datei zu berechnen. Dieser Hashwert wird häufig zur Überprüfung der Integrität von Dateien verwendet, da selbst kleinste Änderungen an der Datei zu einem völlig anderen Hashwert führen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
sha256sum [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Behandelt die Eingabedatei als Binärdatei.
- `-c`: Überprüft die Hashwerte einer Datei gegen die in einer anderen Datei gespeicherten Hashwerte.
- `--help`: Zeigt eine Hilfeübersicht mit verfügbaren Optionen an.
- `--version`: Gibt die Versionsnummer des Programms aus.

## Häufige Beispiele

### Beispiel 1: Berechnung des SHA-256-Hashwerts einer Datei
Um den SHA-256-Hashwert einer Datei zu berechnen, verwenden Sie den folgenden Befehl:

```bash
sha256sum dateiname.txt
```

### Beispiel 2: Berechnung des Hashwerts mehrerer Dateien
Sie können auch den Hashwert mehrerer Dateien gleichzeitig berechnen:

```bash
sha256sum datei1.txt datei2.txt
```

### Beispiel 3: Überprüfung von Hashwerten
Um die Integrität einer Datei zu überprüfen, können Sie eine Datei mit Hashwerten erstellen und dann die Überprüfung durchführen:

1. Erstellen Sie eine Datei mit Hashwerten:

```bash
sha256sum dateiname.txt > hashes.txt
```

2. Überprüfen Sie die Datei gegen die Hashwerte:

```bash
sha256sum -c hashes.txt
```

## Tipps
- Verwenden Sie die Option `-b`, wenn Sie mit Binärdateien arbeiten, um sicherzustellen, dass der Hashwert korrekt berechnet wird.
- Speichern Sie die Hashwerte in einer Datei, um die Integrität Ihrer Dateien regelmäßig zu überprüfen.
- Nutzen Sie die `--help`-Option, um sich schnell über alle verfügbaren Optionen zu informieren, falls Sie sich nicht sicher sind.