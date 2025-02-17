# [Română] Bash hostname utilizare: Afișează sau setează numele gazdelor

## Overview
Comanda `hostname` este utilizată pentru a afișa sau a seta numele gazdelor sistemului. Acesta este un identificator unic care ajută la recunoașterea unui dispozitiv într-o rețea.

## Usage
Sintaxa de bază a comenzii este următoarea:
```bash
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: Afișează numele complet al gazdei (Fully Qualified Domain Name).
- `-i`, `--ip-address`: Afișează adresa IP a gazdei.
- `-s`, `--short`: Afișează doar numele scurt al gazdei.
- `-V`, `--version`: Afișează versiunea comenzii hostname.

## Common Examples
1. **Afișarea numelui gazdei curente:**
   ```bash
   hostname
   ```

2. **Afișarea numelui complet al gazdei:**
   ```bash
   hostname -f
   ```

3. **Afișarea adresei IP a gazdei:**
   ```bash
   hostname -i
   ```

4. **Setarea unui nou nume pentru gazdă:**
   ```bash
   sudo hostname noul_nume
   ```

5. **Afișarea numelui scurt al gazdei:**
   ```bash
   hostname -s
   ```

## Tips
- Asigurați-vă că aveți permisiuni de administrator atunci când încercați să schimbați numele gazdei.
- Utilizați comanda `hostname` fără opțiuni pentru a verifica rapid numele curent al gazdei.
- După schimbarea numelui gazdei, este recomandat să reporniți sistemul pentru a aplica modificările.