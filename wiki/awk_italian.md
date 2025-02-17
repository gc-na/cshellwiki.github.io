# [Linux] Bash awk utilizzo: Elaborazione di testo e reportistica

## Overview
Il comando `awk` è un potente strumento di elaborazione del testo utilizzato per analizzare e manipolare dati strutturati, come file di testo e output di comandi. È particolarmente utile per l'estrazione di informazioni e la generazione di report.

## Usage
La sintassi di base del comando `awk` è la seguente:

```bash
awk [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `awk`:

- `-F` : Specifica il delimitatore di campo (ad esempio, `-F,` per i file CSV).
- `-v` : Permette di definire variabili da utilizzare all'interno del programma `awk`.
- `-f` : Indica un file contenente script `awk` da eseguire.

## Common Examples

### Esempio 1: Stampa la prima colonna di un file
```bash
awk '{print $1}' file.txt
```
Questo comando stampa il contenuto della prima colonna di `file.txt`.

### Esempio 2: Utilizzare un delimitatore personalizzato
```bash
awk -F, '{print $2}' file.csv
```
In questo caso, il comando stampa la seconda colonna di un file CSV, utilizzando la virgola come delimitatore.

### Esempio 3: Filtrare righe in base a una condizione
```bash
awk '$3 > 50' file.txt
```
Questo comando restituisce solo le righe di `file.txt` in cui il valore della terza colonna è maggiore di 50.

### Esempio 4: Somma i valori di una colonna
```bash
awk '{sum += $2} END {print sum}' file.txt
```
Qui, il comando calcola e stampa la somma di tutti i valori nella seconda colonna di `file.txt`.

### Esempio 5: Definire una variabile
```bash
awk -v threshold=100 '$1 > threshold' file.txt
```
Questo comando utilizza una variabile `threshold` per filtrare le righe in cui il valore della prima colonna è maggiore di 100.

## Tips
- Utilizza i delimitatori corretti per i tuoi file per garantire che `awk` interpreti correttamente i dati.
- Sfrutta le variabili per rendere i tuoi script più flessibili e facili da mantenere.
- Prova a combinare `awk` con altri comandi Unix per pipeline più potenti e versatili.