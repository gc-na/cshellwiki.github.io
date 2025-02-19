# [Linux] C Shell (csh) df Verwendung: Zeigt den verfügbaren Speicherplatz auf Dateisystemen an

## Übersicht
Der Befehl `df` (disk free) wird verwendet, um Informationen über den verfügbaren und verwendeten Speicherplatz auf Dateisystemen anzuzeigen. Er gibt eine Übersicht über die Speicherkapazität der verschiedenen Laufwerke und Partitionen des Systems.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
df [Optionen] [Argumente]
```

## Häufige Optionen
- `-h`: Zeigt die Größen in einem menschenlesbaren Format (z.B. KB, MB, GB) an.
- `-T`: Zeigt den Typ des Dateisystems an.
- `-i`: Zeigt die Anzahl der inodes an, die verwendet und verfügbar sind.
- `-a`: Zeigt alle Dateisysteme an, einschließlich derjenigen, die keinen Speicherplatz verwenden.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `df`-Befehls:

1. **Standardnutzung**: Zeigt den verfügbaren Speicherplatz für alle gemounteten Dateisysteme an.
   ```csh
   df
   ```

2. **Menschenlesbares Format**: Zeigt die Speicherkapazität in einem leicht verständlichen Format an.
   ```csh
   df -h
   ```

3. **Dateisystemtyp anzeigen**: Zeigt zusätzlich den Typ des Dateisystems an.
   ```csh
   df -T
   ```

4. **Inodes anzeigen**: Gibt Informationen über die verwendeten und verfügbaren inodes aus.
   ```csh
   df -i
   ```

5. **Alle Dateisysteme anzeigen**: Listet auch die Dateisysteme auf, die keinen Speicherplatz verwenden.
   ```csh
   df -a
   ```

## Tipps
- Verwenden Sie die Option `-h`, um die Ausgabe leichter lesbar zu machen, insbesondere wenn Sie mit großen Speichermengen arbeiten.
- Kombinieren Sie Optionen, um spezifischere Informationen zu erhalten, z.B. `df -hT`, um sowohl die Größe als auch den Typ des Dateisystems anzuzeigen.
- Überprüfen Sie regelmäßig den Speicherplatz, um sicherzustellen, dass Ihr System nicht überlastet ist, was zu Leistungsproblemen führen kann.