# [Linux] C Shell (csh) comm utilizzo: confronta file riga per riga

## Overview
Il comando `comm` è utilizzato per confrontare due file ordinati riga per riga. Esso produce un output che mostra le righe uniche a ciascun file e le righe comuni tra di essi.

## Usage
La sintassi di base del comando è la seguente:

```csh
comm [options] [file1] [file2]
```

## Common Options
- `-1`: sopprime le righe uniche del primo file.
- `-2`: sopprime le righe uniche del secondo file.
- `-3`: sopprime le righe comuni.
- `-i`: ignora la distinzione tra maiuscole e minuscole.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `comm`:

1. **Confrontare due file e visualizzare tutte le righe:**

```csh
comm file1.txt file2.txt
```

2. **Mostrare solo le righe uniche del primo file:**

```csh
comm -13 file1.txt file2.txt
```

3. **Mostrare solo le righe comuni tra i due file:**

```csh
comm -12 file1.txt file2.txt
```

4. **Confrontare due file ignorando la distinzione tra maiuscole e minuscole:**

```csh
comm -i file1.txt file2.txt
```

## Tips
- Assicurati che i file siano ordinati prima di utilizzare `comm`, poiché il comando funziona correttamente solo con file ordinati.
- Puoi utilizzare `sort` per ordinare i file prima di confrontarli, se necessario.
- Considera di utilizzare le opzioni `-1`, `-2`, e `-3` in combinazione per personalizzare l'output secondo le tue esigenze.