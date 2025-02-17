# [Linux] Bash tput utilizzo: Controlla le proprietà del terminale

## Overview
Il comando `tput` è utilizzato per impostare le proprietà del terminale, come colori, formattazione del testo e altre caratteristiche. Permette di interagire con il terminale in modo da migliorare l'aspetto e la leggibilità dell'output.

## Usage
La sintassi di base del comando `tput` è la seguente:

```bash
tput [opzioni] [argomenti]
```

## Common Options
- `setaf [n]`: Imposta il colore del testo foreground (dove n è il numero del colore).
- `setab [n]`: Imposta il colore di sfondo (dove n è il numero del colore).
- `bold`: Attiva il testo in grassetto.
- `smso`: Attiva il testo in modalità sottolineata.
- `rmso`: Disattiva la modalità sottolineata.
- `clear`: Pulisce lo schermo del terminale.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `tput`:

1. **Impostare il colore del testo su rosso:**
   ```bash
   tput setaf 1
   echo "Questo testo è rosso"
   ```

2. **Impostare il colore di sfondo su blu e il testo in bianco:**
   ```bash
   tput setab 4
   tput setaf 7
   echo "Testo bianco su sfondo blu"
   ```

3. **Attivare il testo in grassetto:**
   ```bash
   tput bold
   echo "Questo testo è in grassetto"
   tput sgr0  # Ripristina le impostazioni predefinite
   ```

4. **Pulisci lo schermo del terminale:**
   ```bash
   tput clear
   ```

5. **Attivare e disattivare la modalità sottolineata:**
   ```bash
   tput smso
   echo "Questo testo è sottolineato"
   tput rmso
   ```

## Tips
- Utilizza `tput sgr0` per ripristinare le impostazioni predefinite del terminale dopo aver applicato formattazioni.
- Puoi combinare più comandi `tput` in un'unica riga per ottenere effetti complessi.
- Verifica la compatibilità del tuo terminale con i colori e le opzioni di formattazione supportate, poiché potrebbero variare.