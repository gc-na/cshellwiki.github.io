# [Linux] Bash fc <Utilizare echivalentă>: [revizuirea comenzilor anterioare]

## Overview
Comanda `fc` în Bash este utilizată pentru a edita și a reexecuta comenzile anterioare din istoria shell-ului. Aceasta permite utilizatorilor să acceseze rapid comenzile anterioare, să le modifice și să le ruleze din nou.

## Usage
Sintaxa de bază a comenzii `fc` este următoarea:
```bash
fc [opțiuni] [argumente]
```

## Common Options
- `-l`: Listează comenzile anterioare.
- `-s`: Execută comanda specificată fără a o deschide în editor.
- `-n`: Nu afișează numerele comenzilor în listă.

## Common Examples
1. **Listarea comenzilor anterioare:**
   ```bash
   fc -l
   ```
   Aceasta va lista ultimele comenzi executate.

2. **Editarea ultimei comenzi:**
   ```bash
   fc
   ```
   Aceasta va deschide ultima comandă în editorul de text configurat.

3. **Executarea unei comenzi anterioare fără editare:**
   ```bash
   fc -s 123
   ```
   Aceasta va executa comanda cu numărul 123 din istoria comenzilor.

4. **Listarea comenzilor cu numere:**
   ```bash
   fc -ln -5
   ```
   Aceasta va lista ultimele 5 comenzi fără a le edita.

## Tips
- Utilizați `fc` pentru a corecta rapid greșelile din comenzile anterioare fără a le reintroduce manual.
- Puteți personaliza editorul de text utilizat de `fc` setând variabila de mediu `EDITOR`.
- Familiarizați-vă cu comenzile anterioare folosind `fc -l` pentru a îmbunătăți eficiența în utilizarea terminalului.