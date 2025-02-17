# [Linux] Bash du Uso: Calcolare l'uso dello spazio su disco

## Overview
Il comando `du` (disk usage) è utilizzato per stimare e visualizzare l'uso dello spazio su disco delle directory e dei file nel sistema. Fornisce informazioni su quanto spazio occupano i file e le cartelle, permettendo agli utenti di gestire meglio le risorse di archiviazione.

## Usage
La sintassi di base del comando `du` è la seguente:

```bash
du [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `du`:

- `-h`: Mostra le dimensioni in un formato leggibile dall'uomo (es. KB, MB, GB).
- `-s`: Mostra solo il totale per ogni argomento, senza elencare le dimensioni delle sottodirectory.
- `-a`: Include anche i file oltre alle directory.
- `-c`: Mostra un totale cumulativo alla fine dell'output.
- `--max-depth=N`: Limita la profondità della visualizzazione delle directory a N livelli.

## Common Examples

### Esempio 1: Visualizzare l'uso dello spazio su disco di una directory
```bash
du -h /percorso/della/directory
```

### Esempio 2: Mostrare solo il totale per una directory
```bash
du -sh /percorso/della/directory
```

### Esempio 3: Includere file e directory
```bash
du -ah /percorso/della/directory
```

### Esempio 4: Mostrare un totale cumulativo
```bash
du -ch /percorso/della/directory/*
```

### Esempio 5: Limitare la profondità della visualizzazione
```bash
du -h --max-depth=1 /percorso/della/directory
```

## Tips
- Utilizza l'opzione `-h` per rendere l'output più leggibile, specialmente quando lavori con grandi quantità di dati.
- Combinare `du` con `sort` può aiutarti a identificare rapidamente le directory che occupano più spazio:
  ```bash
  du -h /percorso/della/directory | sort -hr
  ```
- Ricorda che `du` calcola l'uso dello spazio su disco, quindi potrebbe non riflettere immediatamente le modifiche se ci sono operazioni di scrittura in corso.