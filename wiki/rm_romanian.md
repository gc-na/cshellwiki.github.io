# [Linux] C Shell (csh) rm utilizare: Șterge fișiere și directoare

## Overview
Comanda `rm` este utilizată în C Shell (csh) pentru a șterge fișiere și directoare. Aceasta este o comandă puternică, care elimină permanent fișierele specificate, fără a le muta în coșul de reciclare.

## Usage
Sintaxa de bază a comenzii `rm` este următoarea:

```csh
rm [options] [arguments]
```

## Common Options
- `-f`: Forțează ștergerea fișierelor fără a solicita confirmarea utilizatorului.
- `-i`: Cere confirmarea utilizatorului înainte de a șterge fiecare fișier.
- `-r`: Șterge recursiv directoare și conținutul acestora.
- `-v`: Afișează numele fișierelor pe măsură ce sunt șterse.

## Common Examples
1. Ștergerea unui singur fișier:
   ```csh
   rm fisier.txt
   ```

2. Ștergerea mai multor fișiere:
   ```csh
   rm fisier1.txt fisier2.txt fisier3.txt
   ```

3. Ștergerea unui director și a conținutului său:
   ```csh
   rm -r director/
   ```

4. Ștergerea unui fișier fără confirmare:
   ```csh
   rm -f fisier.txt
   ```

5. Ștergerea fișierelor cu confirmare:
   ```csh
   rm -i fisier.txt
   ```

## Tips
- Folosește opțiunea `-i` pentru a evita ștergerea accidentală a fișierelor importante.
- Verifică întotdeauna calea fișierului înainte de a executa comanda `rm`, mai ales când folosești opțiunea `-r`.
- Consideră utilizarea comenzii `ls` pentru a lista fișierele dintr-un director înainte de a le șterge, pentru a te asigura că știi exact ce fișiere sunt afectate.