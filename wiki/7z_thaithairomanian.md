# [Română] Bash 7z Utilizare: Comprimarea și decomprimarea fișierelor

## Overview
Comanda `7z` este un instrument puternic de arhivare care permite utilizatorilor să comprime și să decompună fișiere și directoare. Este parte din pachetul 7-Zip, cunoscut pentru eficiența sa în reducerea dimensiunii fișierelor.

## Usage
Sintaxa de bază a comenzii `7z` este următoarea:

```
7z [options] [arguments]
```

## Common Options
- `a`: Adaugă fișiere într-o arhivă.
- `x`: Extrage fișiere dintr-o arhivă.
- `l`: Listează conținutul unei arhive.
- `d`: Șterge fișiere dintr-o arhivă.
- `t`: Verifică integritatea arhivei.

## Common Examples
1. **Crearea unei arhive**:
   ```bash
   7z a arhiva.7z /cale/catre/fișiere/*
   ```

2. **Extracția fișierelor**:
   ```bash
   7z x arhiva.7z
   ```

3. **Listarea conținutului unei arhive**:
   ```bash
   7z l arhiva.7z
   ```

4. **Ștergerea unui fișier dintr-o arhivă**:
   ```bash
   7z d arhiva.7z fișier_de_sters.txt
   ```

5. **Verificarea integrității arhivei**:
   ```bash
   7z t arhiva.7z
   ```

## Tips
- Asigurați-vă că aveți suficiente permisiuni pentru a accesa fișierele pe care doriți să le arhivați sau să le extrageți.
- Utilizați opțiunea `-p` pentru a adăuga o parolă arhivei, sporind astfel securitatea datelor.
- Verificați dimensiunea arhivei după compresie pentru a evalua eficiența procesului.