# [Linux] C Shell (csh) sha256sum utilizzo: Calcola l'hash SHA-256 di file

## Overview
Il comando `sha256sum` calcola e verifica l'hash SHA-256 di file. Questo è utile per garantire l'integrità dei dati e per confrontare file.

## Usage
La sintassi di base del comando è la seguente:

```csh
sha256sum [options] [arguments]
```

## Common Options
- `-b`: Calcola l'hash in modalità binaria.
- `-c`: Verifica gli hash SHA-256 da un file di checksum.
- `--quiet`: Non mostrare messaggi di errore per file non validi.
- `--tag`: Stampa l'output in formato "tagged".

## Common Examples
Ecco alcuni esempi pratici dell'uso di `sha256sum`:

1. Calcolare l'hash di un file:
   ```csh
   sha256sum file.txt
   ```

2. Salvare l'hash di un file in un file di checksum:
   ```csh
   sha256sum file.txt > checksum.sha256
   ```

3. Verificare un file utilizzando un file di checksum:
   ```csh
   sha256sum -c checksum.sha256
   ```

4. Calcolare l'hash di più file:
   ```csh
   sha256sum file1.txt file2.txt
   ```

## Tips
- Assicurati di utilizzare `sha256sum` su file che non sono stati modificati per ottenere un hash accurato.
- È buona pratica salvare gli hash in un file separato per future verifiche.
- Utilizza l'opzione `-c` per verificare rapidamente l'integrità di più file in una sola volta.