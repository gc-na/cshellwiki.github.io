# [Linux] C Shell (csh) uniq Utilizare: Elimină liniile duplicate din fișiere

## Overview
Comanda `uniq` este utilizată pentru a elimina liniile duplicate consecutive dintr-un fișier sau dintr-un flux de date. Aceasta este utilă pentru a curăța datele și a obține o listă unică de intrări.

## Usage
Sintaxa de bază a comenzii `uniq` este următoarea:

```csh
uniq [opțiuni] [argumente]
```

## Common Options
- `-c`: Numără liniile unice și afișează numărul de apariții înaintea fiecărei linii.
- `-d`: Afișează doar liniile care sunt duplicate.
- `-u`: Afișează doar liniile care sunt unice (nu sunt duplicate).
- `-i`: Ignoră diferențele dintre majuscule și minuscule.

## Common Examples
1. **Eliminarea liniilor duplicate dintr-un fișier:**
   ```csh
   uniq fisier.txt
   ```

2. **Numărarea liniilor unice:**
   ```csh
   uniq -c fisier.txt
   ```

3. **Afișarea doar a liniilor duplicate:**
   ```csh
   uniq -d fisier.txt
   ```

4. **Afișarea liniilor unice:**
   ```csh
   uniq -u fisier.txt
   ```

5. **Ignorarea diferențelor dintre majuscule și minuscule:**
   ```csh
   uniq -i fisier.txt
   ```

## Tips
- Asigurați-vă că datele sunt sortate înainte de a folosi `uniq`, deoarece aceasta elimină doar liniile duplicate consecutive.
- Puteți combina `uniq` cu comanda `sort` pentru a obține o listă completă de linii unice dintr-un fișier nesortat:
  ```csh
  sort fisier.txt | uniq
  ```
- Folosiți opțiunea `-c` pentru a obține o idee despre frecvența apariției fiecărei linii, ceea ce poate fi util în analiza datelor.