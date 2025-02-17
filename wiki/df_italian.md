# [Linux] Bash df utilizzo: Visualizza lo spazio su disco disponibile

## Overview
Il comando `df` (disk free) è utilizzato per mostrare la quantità di spazio su disco disponibile e utilizzato sui file system montati. È uno strumento utile per monitorare lo stato del disco e gestire le risorse di archiviazione.

## Usage
La sintassi di base del comando `df` è la seguente:

```bash
df [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `df`:

- `-h`: Mostra le dimensioni in un formato leggibile dall'uomo (ad esempio, KB, MB, GB).
- `-T`: Mostra il tipo di file system.
- `-a`: Mostra anche i file system che hanno zero blocchi.
- `-i`: Mostra l'uso degli inode invece dello spazio su disco.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `df`:

1. **Visualizzare lo spazio su disco in formato leggibile:**

   ```bash
   df -h
   ```

2. **Visualizzare il tipo di file system insieme allo spazio disponibile:**

   ```bash
   df -hT
   ```

3. **Mostrare anche i file system con zero blocchi:**

   ```bash
   df -a
   ```

4. **Controllare l'uso degli inode:**

   ```bash
   df -i
   ```

## Tips
- Utilizza l'opzione `-h` per rendere le informazioni più comprensibili, specialmente quando lavori con file system di grandi dimensioni.
- Controlla regolarmente lo spazio su disco per evitare problemi di archiviazione.
- Puoi combinare più opzioni, ad esempio `df -hT` per ottenere informazioni dettagliate in un formato leggibile.