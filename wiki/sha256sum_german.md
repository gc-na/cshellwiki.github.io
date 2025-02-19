# [Linux] C Shell (csh) sha256sum Verwendung: Berechnung von SHA-256-Hashwerten

## Übersicht
Der Befehl `sha256sum` wird verwendet, um den SHA-256-Hashwert einer Datei zu berechnen. Dieser Hashwert dient oft zur Überprüfung der Integrität von Dateien, da selbst kleinste Änderungen an einer Datei zu einem völlig anderen Hashwert führen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
sha256sum [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Berechnet den Hashwert für eine Binärdatei.
- `-c`: Überprüft die Hashwerte einer Datei gegen die in einer anderen Datei gespeicherten Hashwerte.
- `--help`: Zeigt eine Hilfeseite mit Informationen zur Verwendung des Befehls an.
- `--version`: Gibt die Versionsnummer des Programms aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung von `sha256sum`:

1. Berechnung des SHA-256-Hashwerts einer Datei:
   ```csh
   sha256sum datei.txt
   ```

2. Berechnung des Hashwerts für eine Binärdatei:
   ```csh
   sha256sum -b datei.bin
   ```

3. Überprüfung von Hashwerten aus einer Datei:
   ```csh
   sha256sum -c hashes.txt
   ```

4. Anzeige der Hilfe:
   ```csh
   sha256sum --help
   ```

## Tipps
- Verwenden Sie `sha256sum` in Kombination mit `>`, um den Hashwert in eine Datei zu speichern:
  ```csh
  sha256sum datei.txt > hash.txt
  ```
- Achten Sie darauf, die Hashwerte regelmäßig zu überprüfen, insbesondere bei wichtigen Dateien.
- Nutzen Sie die Option `-c`, um sicherzustellen, dass Ihre Dateien nicht verändert wurden, indem Sie die Hashwerte mit einer vorher gespeicherten Liste vergleichen.