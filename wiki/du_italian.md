# [Linux] C Shell (csh) du uso: Calcola l'uso dello spazio su disco

## Overview
Il comando `du` (disk usage) è utilizzato per stimare e visualizzare l'uso dello spazio su disco delle directory e dei file nel sistema. È particolarmente utile per identificare quali file o directory occupano più spazio.

## Usage
La sintassi di base del comando `du` è la seguente:

```csh
du [options] [arguments]
```

## Common Options
- `-h`: Mostra le dimensioni in un formato leggibile (es. KB, MB).
- `-s`: Fornisce solo il totale per ogni argomento, senza elencare le dimensioni di ogni file o sottodirectory.
- `-a`: Mostra le dimensioni di tutti i file, non solo delle directory.
- `-c`: Fornisce un totale cumulativo alla fine dell'output.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `du`:

1. **Visualizzare l'uso dello spazio su disco di una directory specifica:**
   ```csh
   du /percorso/della/directory
   ```

2. **Visualizzare l'uso dello spazio in un formato leggibile:**
   ```csh
   du -h /percorso/della/directory
   ```

3. **Ottenere solo il totale per una directory:**
   ```csh
   du -sh /percorso/della/directory
   ```

4. **Mostrare le dimensioni di tutti i file e le directory:**
   ```csh
   du -a /percorso/della/directory
   ```

5. **Visualizzare un totale cumulativo per più directory:**
   ```csh
   du -ch /percorso/della/directory1 /percorso/della/directory2
   ```

## Tips
- Utilizza l'opzione `-h` per rendere l'output più comprensibile, specialmente quando lavori con directory di grandi dimensioni.
- Se desideri analizzare rapidamente l'uso dello spazio, l'opzione `-s` è molto utile per ottenere solo i totali senza dettagli superflui.
- Ricorda che `du` calcola lo spazio occupato, non lo spazio disponibile. Per controllare lo spazio libero, puoi usare il comando `df`.