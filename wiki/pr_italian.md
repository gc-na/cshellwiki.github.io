# [Linux] Bash pr: Stampa file in formato leggibile

## Overview
Il comando `pr` in Bash è utilizzato per formattare e stampare file di testo in un modo leggibile, suddividendo il contenuto in colonne e aggiungendo intestazioni e numeri di pagina. È particolarmente utile per preparare documenti da stampare.

## Usage
La sintassi di base del comando è la seguente:

```bash
pr [opzioni] [argomenti]
```

## Common Options
- `-h, --header=STRING`: Specifica un'intestazione personalizzata per il documento.
- `-n, --number`: Aggiunge numeri di pagina al documento.
- `-t, --omit-header`: Ommette l'intestazione predefinita.
- `-s, --separator=CHAR`: Specifica un carattere di separazione tra le colonne.
- `-w, --width=N`: Imposta la larghezza totale delle colonne.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `pr`:

### Esempio 1: Formattare un file di testo
```bash
pr file.txt
```
Questo comando formatterà e stamperà il contenuto di `file.txt` in un formato leggibile.

### Esempio 2: Aggiungere un'intestazione personalizzata
```bash
pr -h "Il mio documento" file.txt
```
In questo caso, il comando stamperà `file.txt` con l'intestazione "Il mio documento".

### Esempio 3: Numerare le pagine
```bash
pr -n file.txt
```
Questo comando stamperà `file.txt` con numeri di pagina aggiunti.

### Esempio 4: Formattare in colonne
```bash
pr -s, -w 80 file.txt
```
Qui, il file verrà stampato in colonne separate da una virgola e con una larghezza totale di 80 caratteri.

## Tips
- Utilizza l'opzione `-t` se desideri un output senza intestazioni, utile per documenti più puliti.
- Sperimenta con l'opzione `-w` per trovare la larghezza ottimale per la tua stampante.
- Considera di combinare `pr` con altri comandi come `less` o `more` per visualizzare il contenuto formattato direttamente nel terminale.