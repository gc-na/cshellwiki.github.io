# [Linux] C Shell (csh) tail utilizare: Afișează ultimele linii ale unui fișier

## Overview
Comanda `tail` este utilizată pentru a afișa ultimele linii ale unui fișier. Este utilă în special pentru monitorizarea fișierelor de jurnal sau pentru a vizualiza rapid conținutul recent al unui fișier.

## Usage
Sintaxa de bază a comenzii `tail` este următoarea:

```csh
tail [options] [arguments]
```

## Common Options
- `-n [număr]`: Afișează ultimele [număr] de linii din fișier.
- `-f`: Monitorizează fișierul în timp real, afișând noi linii pe măsură ce sunt adăugate.
- `-c [număr]`: Afișează ultimele [număr] de octeți din fișier.

## Common Examples
1. Afișează ultimele 10 linii dintr-un fișier:
   ```csh
   tail nume_fisier.txt
   ```

2. Afișează ultimele 20 de linii dintr-un fișier:
   ```csh
   tail -n 20 nume_fisier.txt
   ```

3. Monitorizează un fișier de jurnal în timp real:
   ```csh
   tail -f jurnal.log
   ```

4. Afișează ultimele 50 de octeți dintr-un fișier:
   ```csh
   tail -c 50 nume_fisier.txt
   ```

## Tips
- Utilizați opțiunea `-f` pentru a urmări fișierele de jurnal în timp real, ceea ce este foarte util pentru depanare.
- Comanda `tail` poate fi combinată cu alte comenzi prin pipe (`|`) pentru a filtra sau procesa datele afișate.
- Dacă doriți să salvați ieșirea comenzii `tail` într-un fișier, puteți redirecționa ieșirea folosind `>`:
  ```csh
  tail nume_fisier.txt > iesire.txt
  ```