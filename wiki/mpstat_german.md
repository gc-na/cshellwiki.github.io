# [Linux] C Shell (csh) mpstat Verwendung: Überwachung der CPU-Auslastung

## Übersicht
Der Befehl `mpstat` wird verwendet, um die CPU-Auslastung auf einem System anzuzeigen. Er liefert Informationen über die Leistung der einzelnen CPUs und ermöglicht es Benutzern, Engpässe und Probleme bei der CPU-Nutzung zu identifizieren.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
mpstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-P ALL`: Zeigt Statistiken für alle CPUs an.
- `-u`: Zeigt die CPU-Nutzung in Prozent an.
- `-h`: Gibt die Ausgabe in einem menschenlesbaren Format aus.
- `interval`: Gibt das Intervall in Sekunden an, in dem die Statistiken aktualisiert werden sollen.
- `count`: Gibt die Anzahl der gewünschten Berichte an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `mpstat`:

1. **CPU-Nutzung für alle CPUs anzeigen:**
   ```bash
   mpstat -P ALL
   ```

2. **CPU-Nutzung alle 5 Sekunden anzeigen:**
   ```bash
   mpstat 5
   ```

3. **CPU-Nutzung mit menschenlesbarem Format:**
   ```bash
   mpstat -h
   ```

4. **CPU-Nutzung für eine bestimmte CPU anzeigen:**
   ```bash
   mpstat -P 0 5 3
   ```

## Tipps
- Verwenden Sie `mpstat -P ALL`, um eine umfassende Übersicht über die Leistung aller CPUs zu erhalten.
- Kombinieren Sie `mpstat` mit anderen Überwachungstools wie `top` oder `htop`, um ein vollständiges Bild der Systemleistung zu erhalten.
- Achten Sie darauf, die Intervalle und die Anzahl der Berichte so zu wählen, dass sie Ihren Überwachungsanforderungen entsprechen, um die Ausgabe übersichtlich zu halten.