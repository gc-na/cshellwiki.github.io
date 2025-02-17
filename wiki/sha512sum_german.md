# [Linux] Bash sha512sum Verwendung: Berechnung von SHA-512-Prüfziffern

## Übersicht
Der Befehl `sha512sum` wird verwendet, um den SHA-512-Hashwert von Dateien zu berechnen. Dies ist nützlich, um die Integrität von Dateien zu überprüfen oder um sicherzustellen, dass Dateien nicht verändert wurden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
sha512sum [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Berechnet den Hashwert im Binärmodus.
- `-c`: Überprüft die Prüfziffern aus einer Datei.
- `-h`: Zeigt die Hilfe an und listet alle Optionen auf.
- `--tag`: Gibt den Hashwert im "tagged" Format aus.

## Häufige Beispiele

### 1. Berechnung des SHA-512-Hashwerts einer Datei
Um den SHA-512-Hashwert einer Datei zu berechnen, verwenden Sie:

```bash
sha512sum dateiname.txt
```

### 2. Berechnung des Hashwerts mehrerer Dateien
Um den Hashwert mehrerer Dateien in einem Befehl zu berechnen, können Sie Folgendes tun:

```bash
sha512sum datei1.txt datei2.txt
```

### 3. Überprüfung von Prüfziffern
Wenn Sie eine Datei mit Prüfziffern haben, können Sie diese mit dem folgenden Befehl überprüfen:

```bash
sha512sum -c pruefziffern.txt
```

### 4. Ausgabe im "tagged" Format
Um den Hashwert im "tagged" Format auszugeben, verwenden Sie:

```bash
sha512sum --tag dateiname.txt
```

## Tipps
- Stellen Sie sicher, dass Sie die Prüfziffern regelmäßig überprüfen, insbesondere bei wichtigen Dateien.
- Nutzen Sie `-c`, um sicherzustellen, dass Ihre Dateien nicht verändert wurden, nachdem Sie die Prüfziffern erstellt haben.
- Speichern Sie die Prüfziffern in einer separaten Datei, um die Integrität Ihrer Daten langfristig zu gewährleisten.