# [Linux] C Shell (csh) du: Speicherplatznutzung anzeigen

## Overview
Der `du`-Befehl (Disk Usage) wird verwendet, um die Speicherplatznutzung von Dateien und Verzeichnissen anzuzeigen. Er gibt an, wie viel Speicherplatz von Dateien und Unterverzeichnissen belegt wird.

## Usage
Die grundlegende Syntax des `du`-Befehls lautet:

```csh
du [Optionen] [Argumente]
```

## Common Options
Hier sind einige gängige Optionen für den `du`-Befehl:

- `-h`: Gibt die Größe in einem menschenlesbaren Format aus (z.B. KB, MB).
- `-s`: Zeigt nur die Gesamtsumme für jedes angegebene Argument an.
- `-a`: Listet die Größe aller Dateien und Verzeichnisse auf, nicht nur der Verzeichnisse.
- `-c`: Gibt eine Gesamtsumme am Ende der Ausgabe aus.

## Common Examples
Hier sind einige praktische Beispiele für die Verwendung des `du`-Befehls:

1. **Speicherplatznutzung eines Verzeichnisses anzeigen:**

   ```csh
   du /pfad/zum/verzeichnis
   ```

2. **Größen in einem menschenlesbaren Format anzeigen:**

   ```csh
   du -h /pfad/zum/verzeichnis
   ```

3. **Nur die Gesamtsumme eines Verzeichnisses anzeigen:**

   ```csh
   du -s /pfad/zum/verzeichnis
   ```

4. **Speicherplatznutzung aller Dateien und Verzeichnisse auflisten:**

   ```csh
   du -a /pfad/zum/verzeichnis
   ```

5. **Gesamtsumme aller Verzeichnisse und Dateien anzeigen:**

   ```csh
   du -c /pfad/zum/verzeichnis/*
   ```

## Tips
- Verwenden Sie die `-h`-Option, um die Ausgabe leichter lesbar zu machen, insbesondere bei großen Verzeichnissen.
- Kombinieren Sie `du` mit dem `sort`-Befehl, um die größten Verzeichnisse anzuzeigen:
  
  ```csh
  du -h /pfad/zum/verzeichnis | sort -hr
  ```

- Achten Sie darauf, dass `du` rekursiv durch Unterverzeichnisse geht, was bei großen Verzeichnissen zu längeren Wartezeiten führen kann.