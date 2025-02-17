# [Linux] Bash tac <Utilizare echivalentă>: inversarea liniilor dintr-un fișier

## Overview
Comanda `tac` este utilizată în Bash pentru a citi un fișier și a afișa conținutul acestuia în ordine inversă, linie cu linie. Aceasta este o comandă utilă atunci când doriți să vizualizați ultimele linii ale unui fișier înainte de cele anterioare.

## Usage
Sintaxa de bază a comenzii `tac` este următoarea:

```bash
tac [opțiuni] [argumente]
```

## Common Options
- `-r`, `--regex`: Permite utilizarea expresiilor regulate pentru delimitarea liniilor.
- `-s`, `--separator`: Specifică un separator personalizat între linii.
- `-b`, `--before`: Afișează separatorul înainte de fiecare linie.

## Common Examples
1. **Inversarea liniilor dintr-un fișier**:
   ```bash
   tac fisier.txt
   ```

2. **Inversarea liniilor și utilizarea unui separator personalizat**:
   ```bash
   tac -s "," fisier.txt
   ```

3. **Inversarea liniilor dintr-un fișier și salvarea rezultatului într-un alt fișier**:
   ```bash
   tac fisier.txt > fisier_inversat.txt
   ```

4. **Inversarea liniilor cu un separator specificat**:
   ```bash
   tac -s ";" fisier.txt
   ```

## Tips
- Folosiți `tac` împreună cu `grep` pentru a căuta linii specifice în ordine inversă.
- Comanda `tac` poate fi combinată cu alte comenzi prin intermediul pipe-urilor pentru a crea fluxuri de lucru mai complexe.
- Verificați dimensiunea fișierului înainte de a utiliza `tac` pe fișiere mari, deoarece inversarea poate consuma resurse semnificative.