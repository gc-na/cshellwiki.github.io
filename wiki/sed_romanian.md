# [Linux] C Shell (csh) sed utilizare: Modificarea textului în flux

## Overview
Comanda `sed` (stream editor) este un editor de fluxuri care permite manipularea și transformarea textului din fișiere sau din intrări standard. Aceasta este utilizată frecvent pentru a efectua căutări și înlocuiri rapide de text, precum și pentru a modifica conținutul fișierelor fără a le deschide manual.

## Usage
Sintaxa de bază a comenzii `sed` este următoarea:

```bash
sed [opțiuni] [argumente]
```

## Common Options
- `-e`: Permite specificarea unei comenzi `sed` direct în linia de comandă.
- `-i`: Modifică fișierul direct, fără a crea un fișier temporar.
- `-n`: Suprimă ieșirea implicită, permițându-vă să controlați ce linii sunt afișate.
- `s`: Comanda de substituție, folosită pentru a înlocui un text specificat cu altul.

## Common Examples
1. **Înlocuirea unui cuvânt într-un fișier**:
   ```bash
   sed 's/cuvânt_vechi/cuvânt_nou/' fisier.txt
   ```

2. **Înlocuirea tuturor aparițiilor unui cuvânt**:
   ```bash
   sed 's/cuvânt_vechi/cuvânt_nou/g' fisier.txt
   ```

3. **Modificarea fișierului direct**:
   ```bash
   sed -i 's/cuvânt_vechi/cuvânt_nou/g' fisier.txt
   ```

4. **Afișarea doar a liniilor care conțin un anumit cuvânt**:
   ```bash
   sed -n '/cuvânt/p' fisier.txt
   ```

5. **Ștergerea liniilor goale dintr-un fișier**:
   ```bash
   sed '/^$/d' fisier.txt
   ```

## Tips
- Utilizați opțiunea `-i` cu precauție, deoarece modificările sunt permanente.
- Testați comenzile `sed` fără opțiunea `-i` pentru a verifica rezultatul înainte de a face modificări permanente.
- Folosiți `-n` împreună cu comanda `p` pentru a controla ce linii sunt afișate, ceea ce poate fi util pentru filtrarea rezultatelor.