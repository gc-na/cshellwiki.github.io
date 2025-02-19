# [Linux] C Shell (csh) df Uso: Visualizza informazioni sullo spazio su disco

## Overview
Il comando `df` in C Shell (csh) viene utilizzato per visualizzare informazioni sullo spazio su disco disponibile e utilizzato sui filesystem montati. È uno strumento utile per monitorare l'uso del disco e gestire lo spazio di archiviazione.

## Usage
La sintassi di base del comando `df` è la seguente:

```csh
df [options] [arguments]
```

## Common Options
- `-h`: Mostra le dimensioni in un formato leggibile dall'utente (ad esempio, KB, MB, GB).
- `-T`: Mostra il tipo di filesystem.
- `-i`: Mostra informazioni sull'uso degli inode invece dello spazio su disco.
- `-a`: Include i filesystem con zero blocchi.
- `-l`: Limita l'output ai filesystem locali.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `df`:

1. **Visualizzare lo spazio su disco in formato leggibile**:
   ```csh
   df -h
   ```

2. **Visualizzare il tipo di filesystem**:
   ```csh
   df -T
   ```

3. **Controllare l'uso degli inode**:
   ```csh
   df -i
   ```

4. **Visualizzare informazioni su tutti i filesystem, compresi quelli con zero blocchi**:
   ```csh
   df -a
   ```

5. **Limitare l'output ai filesystem locali**:
   ```csh
   df -l
   ```

## Tips
- Utilizza l'opzione `-h` per rendere i dati più comprensibili, specialmente quando lavori con grandi volumi di dati.
- Controlla regolarmente lo spazio su disco per evitare problemi di archiviazione.
- Usa `df` insieme ad altri comandi come `du` per avere una visione più completa dell'uso dello spazio su disco.