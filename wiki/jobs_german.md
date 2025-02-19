# [Linux] C Shell (csh) jobs Verwendung: Zeigt aktive Jobs an

## Übersicht
Der Befehl `jobs` in der C Shell (csh) wird verwendet, um eine Liste der aktuell aktiven Jobs anzuzeigen, die im Hintergrund oder im Vordergrund laufen. Dies ist nützlich, um den Status von Prozessen zu überwachen, die von der Shell gestartet wurden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```csh
jobs [optionen] [argumente]
```

## Häufige Optionen
- `-l`: Zeigt die Prozess-ID (PID) für jeden Job an.
- `-n`: Zeigt nur die Jobs an, die seit dem letzten Aufruf von `jobs` geändert wurden.
- `-p`: Gibt nur die Prozess-IDs der Jobs aus.

## Häufige Beispiele

1. **Einfaches Anzeigen aktiver Jobs:**
   ```csh
   jobs
   ```

2. **Anzeigen von Jobs mit Prozess-IDs:**
   ```csh
   jobs -l
   ```

3. **Anzeigen von nur neuen oder geänderten Jobs:**
   ```csh
   jobs -n
   ```

4. **Anzeigen von nur den Prozess-IDs der Jobs:**
   ```csh
   jobs -p
   ```

## Tipps
- Verwenden Sie `jobs -l`, um eine bessere Übersicht über die Jobs zu erhalten, insbesondere wenn Sie die Prozess-IDs benötigen.
- Kombinieren Sie `jobs` mit anderen Befehlen wie `fg` oder `bg`, um Jobs im Vordergrund oder Hintergrund fortzusetzen.
- Überprüfen Sie regelmäßig den Status Ihrer Jobs, um sicherzustellen, dass keine unerwarteten Prozesse laufen, die Ressourcen beanspruchen.