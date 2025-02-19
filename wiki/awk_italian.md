# [Linux] C Shell (csh) awk Utilizzo: Elaborazione di testo e reportistica

## Overview
Il comando `awk` è uno strumento potente per l'elaborazione di testo e la generazione di report. Viene utilizzato per analizzare e manipolare dati strutturati, come file di testo e output di comandi, consentendo di estrarre informazioni specifiche e formattare i risultati in modo utile.

## Usage
La sintassi di base del comando `awk` è la seguente:

```bash
awk [options] [arguments]
```

## Common Options
- `-F`: Specifica il delimitatore di campo. Ad esempio, `-F,` per i file CSV.
- `-v`: Permette di definire variabili da utilizzare all'interno del programma `awk`.
- `-f`: Indica un file contenente uno script `awk` da eseguire.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `awk`:

### Esempio 1: Stampare la prima colonna di un file
```bash
awk '{print $1}' file.txt
```
Questo comando stampa il contenuto della prima colonna di `file.txt`.

### Esempio 2: Usare un delimitatore personalizzato
```bash
awk -F, '{print $2}' file.csv
```
In questo caso, il comando stampa la seconda colonna di un file CSV, utilizzando la virgola come delimitatore.

### Esempio 3: Filtrare righe in base a una condizione
```bash
awk '$3 > 100' file.txt
```
Questo comando restituisce solo le righe in cui il valore della terza colonna è maggiore di 100.

### Esempio 4: Sommare i valori di una colonna
```bash
awk '{sum += $2} END {print sum}' file.txt
```
Qui, il comando somma tutti i valori della seconda colonna e stampa il risultato alla fine.

## Tips
- Utilizza `-F` per gestire file con delimitatori diversi, come tabulazioni o punti e virgola.
- Sfrutta le variabili definite con `-v` per rendere i tuoi script più flessibili e riutilizzabili.
- Ricorda che `awk` tratta le righe come record e le colonne come campi, il che rende facile l'accesso ai dati strutturati.