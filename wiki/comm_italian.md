# [Linux] Bash comm uso: confronta file riga per riga

## Overview
Il comando `comm` è utilizzato per confrontare due file ordinati riga per riga. Esso produce un output che mostra le righe uniche a ciascun file e le righe comuni.

## Usage
La sintassi di base del comando è la seguente:

```bash
comm [opzioni] [file1] [file2]
```

## Common Options
- `-1`: Sopprime l'output delle righe uniche nel primo file.
- `-2`: Sopprime l'output delle righe uniche nel secondo file.
- `-3`: Sopprime l'output delle righe comuni a entrambi i file.
- `-i`: Ignora la differenza tra maiuscole e minuscole.

## Common Examples

### Esempio 1: Confrontare due file
Per confrontare due file chiamati `file1.txt` e `file2.txt`, usa il seguente comando:

```bash
comm file1.txt file2.txt
```

### Esempio 2: Mostrare solo righe uniche nel secondo file
Se vuoi vedere solo le righe che sono uniche a `file2.txt`, puoi usare:

```bash
comm -13 file1.txt file2.txt
```

### Esempio 3: Ignorare le maiuscole
Per confrontare due file ignorando le differenze di maiuscole e minuscole, utilizza l'opzione `-i`:

```bash
comm -i file1.txt file2.txt
```

## Tips
- Assicurati che i file siano ordinati prima di utilizzare `comm`, altrimenti il risultato potrebbe non essere corretto.
- Puoi utilizzare `sort` per ordinare i file prima di passarli a `comm`, ad esempio:

```bash
comm <(sort file1.txt) <(sort file2.txt)
```
- Usa le opzioni in combinazione per ottenere l'output desiderato in modo più efficiente.