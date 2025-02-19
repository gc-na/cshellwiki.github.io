# [Linux] C Shell (csh) tee utilizare: Scrierea datelor în fișiere și pe ecran

## Overview
Comanda `tee` în C Shell (csh) este utilizată pentru a citi date de la standard input și a le scrie simultan atât pe standard output (ecran), cât și în unul sau mai multe fișiere. Aceasta este utilă pentru a vizualiza datele în timp ce le salvăm.

## Usage
Sintaxa de bază a comenzii `tee` este următoarea:

```csh
tee [opțiuni] [argumente]
```

## Common Options
- `-a`: Adaugă datele la sfârșitul fișierului existent, în loc să suprascrie.
- `-i`: Ignoră semnalul de întrerupere (SIGINT) și continuă să scrie datele.

## Common Examples
1. **Scrierea datelor într-un fișier:**
   ```csh
   echo "Salut, lume!" | tee fisier.txt
   ```
   Aceasta va scrie "Salut, lume!" atât pe ecran, cât și în `fisier.txt`.

2. **Adăugarea datelor la un fișier existent:**
   ```csh
   echo "Adăugare de text" | tee -a fisier.txt
   ```
   Aceasta va adăuga "Adăugare de text" la sfârșitul fișierului `fisier.txt`.

3. **Scrierea în mai multe fișiere:**
   ```csh
   echo "Mesaj pentru toți" | tee fisier1.txt fisier2.txt
   ```
   Aceasta va scrie "Mesaj pentru toți" în ambele fișiere `fisier1.txt` și `fisier2.txt`.

4. **Ignorarea semnalului de întrerupere:**
   ```csh
   some_command | tee -i fisier.txt
   ```
   Aceasta va continua să scrie în `fisier.txt` chiar dacă se primește un semnal de întrerupere.

## Tips
- Folosiți opțiunea `-a` pentru a evita pierderea datelor existente în fișiere.
- Combinați `tee` cu alte comenzi folosind pipe (`|`) pentru a crea fluxuri de lucru eficiente.
- Verificați conținutul fișierelor după utilizarea `tee` pentru a vă asigura că datele au fost scrise corect.