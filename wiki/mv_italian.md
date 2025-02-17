# [Linux] Bash mv Utilizzo: Spostare o rinominare file e directory

## Overview
Il comando `mv` in Bash è utilizzato per spostare file e directory da una posizione a un'altra o per rinominarli. È uno strumento fondamentale per la gestione dei file nel sistema operativo.

## Usage
La sintassi di base del comando `mv` è la seguente:

```bash
mv [opzioni] [argomenti]
```

## Common Options
- `-i`: Chiede conferma prima di sovrascrivere file esistenti.
- `-u`: Sposta solo i file che sono più recenti rispetto ai file di destinazione o che non esistono.
- `-v`: Mostra i dettagli delle operazioni eseguite, utile per il debug.
- `-n`: Non sovrascrive i file esistenti.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `mv`:

1. **Spostare un file in una directory**:
   ```bash
   mv documento.txt /home/utente/documenti/
   ```

2. **Rinominare un file**:
   ```bash
   mv vecchio_nome.txt nuovo_nome.txt
   ```

3. **Spostare e rinominare un file**:
   ```bash
   mv /home/utente/documento.txt /home/utente/documenti/nuovo_documento.txt
   ```

4. **Spostare più file in una directory**:
   ```bash
   mv file1.txt file2.txt /home/utente/documenti/
   ```

5. **Usare l'opzione interattiva per evitare sovrascritture**:
   ```bash
   mv -i file.txt /home/utente/documenti/
   ```

## Tips
- Utilizza l'opzione `-v` per avere un feedback visivo su ciò che stai spostando o rinominando.
- Fai attenzione quando usi `mv` senza opzioni, poiché i file esistenti nella destinazione possono essere sovrascritti senza preavviso.
- Considera di usare `-n` se desideri evitare di sovrascrivere file esistenti accidentalmente.