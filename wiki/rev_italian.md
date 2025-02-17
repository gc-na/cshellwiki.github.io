# [Linux] Bash rev: Invertire il contenuto delle righe

## Overview
Il comando `rev` in Bash è utilizzato per invertire il contenuto di ogni riga di un file o di un input standard. Questo significa che ogni carattere di una riga viene riordinato in ordine inverso.

## Usage
La sintassi di base del comando `rev` è la seguente:

```bash
rev [opzioni] [argomenti]
```

## Common Options
- `-o, --output FILE`: Specifica un file di output in cui scrivere il risultato.
- `-h, --help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `-V, --version`: Mostra la versione del comando.

## Common Examples

### Esempio 1: Invertire il contenuto di un file
Per invertire il contenuto di un file chiamato `testo.txt`, puoi utilizzare il seguente comando:

```bash
rev testo.txt
```

### Esempio 2: Invertire l'input standard
Puoi anche utilizzare `rev` per invertire l'input direttamente dalla riga di comando. Ad esempio:

```bash
echo "Ciao Mondo" | rev
```

### Esempio 3: Scrivere l'output in un file
Se desideri salvare l'output invertito in un nuovo file, puoi utilizzare l'opzione `-o`:

```bash
rev -o output.txt testo.txt
```

## Tips
- Utilizza `rev` in combinazione con altri comandi tramite pipe per manipolare il testo in modo più complesso.
- Fai attenzione ai file di grandi dimensioni, poiché `rev` carica l'intero file in memoria.
- Ricorda che `rev` inverte solo il contenuto delle righe, non l'ordine delle righe stesse.