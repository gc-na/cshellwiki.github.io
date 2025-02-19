# [Linux] C Shell (csh) sha512sum Verwendung: Berechnung von SHA-512-Prüfziffern

## Übersicht
Der Befehl `sha512sum` wird verwendet, um den SHA-512-Hashwert einer Datei zu berechnen. Dieser Hashwert kann zur Überprüfung der Integrität von Dateien oder zur sicheren Speicherung von Passwörtern verwendet werden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
sha512sum [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Berechnet den Hashwert für eine Binärdatei.
- `-c`: Überprüft die Hashwerte von Dateien anhand einer Prüfziffern-Datei.
- `-h`: Zeigt eine Hilfe mit den verfügbaren Optionen an.
- `--tag`: Fügt einen Tag für die Ausgabe hinzu, um die Ausgabe zu formatieren.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `sha512sum`:

1. Berechnung des SHA-512-Hashwerts einer Datei:
   ```csh
   sha512sum datei.txt
   ```

2. Berechnung des Hashwerts einer Binärdatei:
   ```csh
   sha512sum -b binärdatei.bin
   ```

3. Überprüfung von Hashwerten mit einer Prüfziffern-Datei:
   ```csh
   sha512sum -c prüfziffern.txt
   ```

4. Ausgabe des Hashwerts mit einem Tag:
   ```csh
   sha512sum --tag datei.txt
   ```

## Tipps
- Achten Sie darauf, die Prüfziffern-Datei regelmäßig zu aktualisieren, um die Integrität Ihrer Dateien zu gewährleisten.
- Verwenden Sie `sha512sum` in Kombination mit anderen Befehlen wie `find`, um Hashwerte für mehrere Dateien auf einmal zu berechnen.
- Speichern Sie die Hashwerte an einem sicheren Ort, um sicherzustellen, dass sie nicht manipuliert werden können.