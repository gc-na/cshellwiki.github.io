# [Linux] Bash sha256sum utilizzo: Calcola e verifica checksum SHA-256

## Overview
Il comando `sha256sum` è utilizzato per calcolare e verificare il checksum SHA-256 di file. Questo è utile per garantire l'integrità dei dati, poiché un piccolo cambiamento nel file produce un checksum completamente diverso.

## Usage
La sintassi di base del comando è la seguente:

```bash
sha256sum [opzioni] [argomenti]
```

## Common Options
- `-b`: Calcola il checksum in modalità binaria.
- `-c`: Verifica i checksum da un file.
- `-o FILE`: Scrive l'output in un file specificato.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `sha256sum`:

1. **Calcolare il checksum di un file:**
   ```bash
   sha256sum file.txt
   ```

2. **Calcolare il checksum di più file:**
   ```bash
   sha256sum file1.txt file2.txt
   ```

3. **Verificare un checksum da un file:**
   Supponiamo di avere un file `checksums.txt` che contiene i checksum e i nomi dei file.
   ```bash
   sha256sum -c checksums.txt
   ```

4. **Calcolare il checksum in modalità binaria:**
   ```bash
   sha256sum -b file.bin
   ```

5. **Scrivere l'output in un file:**
   ```bash
   sha256sum file.txt -o checksum.txt
   ```

## Tips
- Assicurati di utilizzare `sha256sum` su file che non sono stati modificati per ottenere risultati accurati.
- Quando verifichi i checksum, utilizza sempre l'opzione `-c` per confrontare i checksum con i file originali.
- È buona pratica generare e conservare i checksum dei file scaricati per garantire la loro integrità nel tempo.