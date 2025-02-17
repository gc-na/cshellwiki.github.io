# [Linux] Bash fmt Utilizzo: Riformattare il testo

## Overview
Il comando `fmt` è utilizzato per riformattare il testo in modo che le righe abbiano una lunghezza uniforme. È particolarmente utile per preparare documenti di testo per la stampa o per migliorare la leggibilità.

## Usage
La sintassi di base del comando è la seguente:

```bash
fmt [options] [arguments]
```

## Common Options
- `-w NUM`: Imposta la larghezza massima delle righe a NUM caratteri.
- `-s`: Riduce gli spazi bianchi tra le righe.
- `-u`: Rimuove le righe vuote e le righe che contengono solo spazi bianchi.

## Common Examples

### Esempio 1: Riformattare un file di testo
Per riformattare un file di testo chiamato `documento.txt` con una larghezza massima di 50 caratteri, puoi usare:

```bash
fmt -w 50 documento.txt
```

### Esempio 2: Riformattare l'output di un comando
Puoi riformattare l'output di un comando, ad esempio `cat`, e inviarlo a `fmt`:

```bash
cat documento.txt | fmt -w 60
```

### Esempio 3: Rimuovere righe vuote
Per riformattare un file e rimuovere le righe vuote, utilizza l'opzione `-u`:

```bash
fmt -u documento.txt
```

## Tips
- Quando utilizzi `fmt`, considera di specificare una larghezza che si adatti al tuo formato di output desiderato.
- Puoi combinare più opzioni per ottenere il risultato desiderato, ad esempio `fmt -w 80 -s documento.txt`.
- Se stai lavorando con file di testo molto lunghi, prova a utilizzare `less` insieme a `fmt` per visualizzare il testo riformattato in modo più gestibile.