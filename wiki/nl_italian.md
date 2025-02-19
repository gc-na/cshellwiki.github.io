# [Linux] C Shell (csh) nl uso: numerare le righe di un file

## Overview
Il comando `nl` in C Shell (csh) è utilizzato per numerare le righe di un file di testo. Questo comando è utile per visualizzare il contenuto di un file con i numeri di riga, facilitando la lettura e la referenziazione.

## Usage
La sintassi di base del comando è la seguente:

```csh
nl [options] [arguments]
```

## Common Options
- `-b`: Specifica il tipo di numerazione da utilizzare (ad esempio, `-b a` per numerare tutte le righe).
- `-f`: Indica il numero di righe da saltare prima di iniziare la numerazione.
- `-n`: Definisce il formato della numerazione (ad esempio, `-n ln` per numerazione a sinistra).
- `-w`: Specifica la larghezza del numero di riga.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `nl`:

1. Numerare tutte le righe di un file:
   ```csh
   nl file.txt
   ```

2. Numerare solo le righe non vuote:
   ```csh
   nl -b a file.txt
   ```

3. Saltare le prime 2 righe e numerare il resto:
   ```csh
   nl -f 2 file.txt
   ```

4. Usare una larghezza di 5 caratteri per i numeri di riga:
   ```csh
   nl -w 5 file.txt
   ```

5. Numerare le righe e formattare la numerazione a sinistra:
   ```csh
   nl -n ln file.txt
   ```

## Tips
- Utilizza l'opzione `-b` per personalizzare quali righe numerare, a seconda delle tue esigenze.
- Sperimenta con l'opzione `-w` per migliorare la leggibilità, specialmente in file con molte righe.
- Ricorda che `nl` non modifica il file originale; crea solo un output numerato sul terminale.