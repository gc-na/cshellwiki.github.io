# [Linux] C Shell (csh) cmp utilizare: Compararea fișierelor binare

## Overview
Comanda `cmp` este utilizată pentru a compara două fișiere binare sau textuale, raportând diferențele dintre acestea. Aceasta este utilă pentru a verifica dacă fișierele sunt identice sau pentru a identifica locurile în care acestea diferă.

## Usage
Sintaxa de bază a comenzii `cmp` este următoarea:

```csh
cmp [opțiuni] [fișier1] [fișier2]
```

## Common Options
- `-l`: Afișează fiecare octet diferit în format numeric.
- `-s`: Nu afișează nimic, dar returnează un cod de ieșire care indică dacă fișierele sunt identice sau nu.
- `-i`: Specifică un offset de la care să înceapă compararea.
- `-n`: Compară doar un număr specificat de octeți.

## Common Examples
1. Compararea a două fișiere și afișarea diferențelor:
   ```csh
   cmp fisier1.txt fisier2.txt
   ```

2. Compararea a două fișiere fără a afișa ieșirea, doar codul de ieșire:
   ```csh
   cmp -s fisier1.txt fisier2.txt
   ```

3. Afișarea diferențelor în format numeric:
   ```csh
   cmp -l fisier1.bin fisier2.bin
   ```

4. Compararea primilor 100 de octeți din două fișiere:
   ```csh
   cmp -n 100 fisier1.txt fisier2.txt
   ```

## Tips
- Folosește opțiunea `-s` pentru a verifica rapid dacă două fișiere sunt identice fără a afișa detalii.
- Atunci când compari fișiere binare, opțiunea `-l` poate fi foarte utilă pentru a obține o listă detaliată a diferențelor.
- Asigură-te că specifici corect calea fișierelor pentru a evita erorile de acces.