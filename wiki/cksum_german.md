# [Linux] C Shell (csh) cksum: Berechnung von Prüfzahlen für Dateien

## Übersicht
Der Befehl `cksum` wird verwendet, um die Prüfzahlen und die Byte-Anzahl von Dateien zu berechnen. Er gibt eine Prüfziffer, die Dateigröße und den Dateinamen aus, was nützlich ist, um die Integrität von Dateien zu überprüfen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
cksum [Optionen] [Argumente]
```

## Häufige Optionen
- `-a, --algorithm`: Gibt den Algorithmus an, der zur Berechnung der Prüfziffer verwendet werden soll.
- `-h, --help`: Zeigt eine Hilfenachricht mit den verfügbaren Optionen an.
- `-o, --output`: Gibt die Ausgabedatei an, in die die Prüfzahlen geschrieben werden sollen.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `cksum`:

1. Berechnung der Prüfziffer für eine einzelne Datei:
   ```csh
   cksum datei.txt
   ```

2. Berechnung der Prüfziffer für mehrere Dateien:
   ```csh
   cksum datei1.txt datei2.txt datei3.txt
   ```

3. Ausgabe der Prüfziffer in eine Datei:
   ```csh
   cksum datei.txt > pruefziffer.txt
   ```

4. Verwendung einer spezifischen Prüfziffer-Algorithmus:
   ```csh
   cksum -a md5 datei.txt
   ```

## Tipps
- Überprüfen Sie regelmäßig die Prüfziffern wichtiger Dateien, um sicherzustellen, dass sie nicht beschädigt wurden.
- Nutzen Sie die Ausgabe von `cksum`, um eine einfache Integritätsprüfung in Skripten zu implementieren.
- Speichern Sie Prüfziffern in einer Datei, um sie später zur Überprüfung der Dateiintegrität verwenden zu können.