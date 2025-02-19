# [Linux] C Shell (csh) pr: Stampa file in formato leggibile

## Overview
Il comando `pr` viene utilizzato per formattare file di testo in modo che siano più leggibili quando stampati. Questo comando suddivide il contenuto in colonne e aggiunge intestazioni e numeri di pagina, rendendo più facile la lettura e la stampa dei documenti.

## Usage
La sintassi di base del comando `pr` è la seguente:

```csh
pr [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per il comando `pr`:

- `-l [numero]`: Imposta il numero di righe per pagina.
- `-w [numero]`: Imposta la larghezza della pagina in caratteri.
- `-h [stringa]`: Aggiunge un'intestazione personalizzata.
- `-n`: Non numerare le pagine.
- `-s`: Usa uno spazio in bianco tra le colonne.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `pr`:

1. **Stampare un file con intestazione e numerazione delle pagine:**
   ```csh
   pr file.txt
   ```

2. **Impostare il numero di righe per pagina a 50:**
   ```csh
   pr -l 50 file.txt
   ```

3. **Impostare la larghezza della pagina a 80 caratteri:**
   ```csh
   pr -w 80 file.txt
   ```

4. **Aggiungere un'intestazione personalizzata:**
   ```csh
   pr -h "Il mio documento" file.txt
   ```

5. **Stampare due file in colonne:**
   ```csh
   pr file1.txt file2.txt
   ```

## Tips
- Utilizza l'opzione `-s` per migliorare la leggibilità quando stampi più file in colonne.
- Prova diverse combinazioni di opzioni per ottenere il formato di stampa desiderato.
- Ricorda di visualizzare l'output su schermo prima di stampare, per assicurarti che sia formattato correttamente. Puoi farlo reindirizzando l'output a `less`:
  ```csh
  pr file.txt | less
  ```