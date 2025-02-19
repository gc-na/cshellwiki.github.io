# [Unix] C Shell (csh) pr: Textdateien formatieren und drucken

## Übersicht
Der Befehl `pr` wird verwendet, um Textdateien für den Druck zu formatieren. Er kann Text in Spalten aufteilen, Seitenumbrüche hinzufügen und die Ausgabe anpassen, um die Lesbarkeit zu verbessern.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
pr [Optionen] [Argumente]
```

## Häufige Optionen
- `-2`: Teilt die Ausgabe in zwei Spalten.
- `-f`: Fügt einen Seitenumbruch nach jeder Datei hinzu.
- `-h <Überschrift>`: Fügt eine benutzerdefinierte Überschrift hinzu.
- `-l <Zeilen>`: Legt die Anzahl der Zeilen pro Seite fest.
- `-s`: Verwendet Leerzeichen anstelle von Tabulatoren zur Ausrichtung.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `pr`-Befehls:

1. **Einfaches Formatieren einer Datei:**
   ```csh
   pr datei.txt
   ```

2. **Zwei Spalten ausgeben:**
   ```csh
   pr -2 datei.txt
   ```

3. **Seitenumbrüche nach jeder Datei hinzufügen:**
   ```csh
   pr -f datei1.txt datei2.txt
   ```

4. **Benutzerdefinierte Überschrift hinzufügen:**
   ```csh
   pr -h "Meine Überschrift" datei.txt
   ```

5. **Anzahl der Zeilen pro Seite festlegen:**
   ```csh
   pr -l 50 datei.txt
   ```

## Tipps
- Verwenden Sie die Option `-s`, um sicherzustellen, dass Ihre Ausgabe ordentlich ausgerichtet ist, insbesondere wenn Sie mit Tabulatoren arbeiten.
- Kombinieren Sie mehrere Optionen, um die Ausgabe nach Ihren Wünschen anzupassen, z. B. `pr -2 -h "Bericht" datei.txt`.
- Testen Sie die Ausgabe zuerst im Terminal, bevor Sie sie drucken, um sicherzustellen, dass alles korrekt formatiert ist.