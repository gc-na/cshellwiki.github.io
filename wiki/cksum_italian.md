# [Linux] Bash cksum uso equivalente: Calcola il checksum di un file

## Overview
Il comando `cksum` calcola e visualizza il checksum di un file, insieme alla dimensione del file in byte. Questo è utile per verificare l'integrità dei dati e per confrontare file.

## Usage
La sintassi di base del comando è la seguente:

```bash
cksum [opzioni] [file]
```

## Common Options
- `-a, --algorithm=ALGO`: Specifica l'algoritmo da utilizzare per il calcolo del checksum.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `--version`: Mostra la versione del comando `cksum`.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `cksum`:

1. Calcolare il checksum di un file:
   ```bash
   cksum miofile.txt
   ```

2. Calcolare il checksum di più file:
   ```bash
   cksum file1.txt file2.txt
   ```

3. Usare un algoritmo specifico (se supportato):
   ```bash
   cksum --algorithm=crc32 miofile.txt
   ```

4. Visualizzare l'aiuto del comando:
   ```bash
   cksum --help
   ```

## Tips
- Utilizza `cksum` per verificare l'integrità dei file scaricati, confrontando il checksum fornito con quello calcolato.
- Ricorda che il checksum è utile per identificare modifiche nei file, ma non è infallibile; per una maggiore sicurezza, considera di utilizzare anche altri strumenti di hashing come `sha256sum`.