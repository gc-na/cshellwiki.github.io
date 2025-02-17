# [Linux] Bash iconv utilizzo: Convertire file di testo tra diverse codifiche

## Overview
Il comando `iconv` è utilizzato per convertire file di testo tra diverse codifiche di caratteri. È particolarmente utile quando si lavora con file provenienti da diverse fonti che potrebbero utilizzare codifiche diverse, come UTF-8, ISO-8859-1, e altre.

## Usage
La sintassi di base del comando `iconv` è la seguente:

```bash
iconv [opzioni] [argomenti]
```

## Common Options
- `-f, --from-code=CODIFICA`: Specifica la codifica di origine.
- `-t, --to-code=CODIFICA`: Specifica la codifica di destinazione.
- `-o, --output=FILE`: Scrive l'output in un file specificato invece di stampare su stdout.
- `-c`: Ignora i caratteri non validi durante la conversione.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `iconv`:

1. **Convertire un file da UTF-8 a ISO-8859-1**:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. **Convertire un file da ISO-8859-1 a UTF-8**:
   ```bash
   iconv -f ISO-8859-1 -t UTF-8 input.txt -o output.txt
   ```

3. **Convertire e stampare l'output direttamente nel terminale**:
   ```bash
   iconv -f UTF-8 -t UTF-16 input.txt
   ```

4. **Ignorare i caratteri non validi durante la conversione**:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
   ```

## Tips
- Assicurati di conoscere le codifiche di origine e di destinazione prima di eseguire la conversione.
- Utilizza l'opzione `-o` per salvare il risultato in un file, evitando di sovrascrivere il file originale.
- Puoi utilizzare `iconv -l` per elencare tutte le codifiche supportate dal tuo sistema.