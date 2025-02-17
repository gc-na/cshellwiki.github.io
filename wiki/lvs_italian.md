# [Linux] Bash lvs utilizzo: visualizzare informazioni sui volumi logici

## Overview
Il comando `lvs` è utilizzato per visualizzare informazioni sui volumi logici in un sistema Linux che utilizza LVM (Logical Volume Manager). Questo comando fornisce dettagli come il nome del volume, il gruppo di volumi a cui appartiene, la dimensione e lo stato.

## Usage
La sintassi di base del comando è la seguente:

```bash
lvs [opzioni] [argomenti]
```

## Common Options
- `-o, --options`: Specifica quali colonne visualizzare.
- `-a, --all`: Mostra anche i volumi logici inattivi.
- `-h, --units`: Mostra le dimensioni in unità leggibili (KB, MB, GB).
- `--noheadings`: Nasconde l'intestazione della tabella nell'output.
- `-S, --select`: Filtra i volumi logici in base a criteri specifici.

## Common Examples

1. **Visualizzare tutti i volumi logici**:
   ```bash
   lvs
   ```

2. **Visualizzare volumi logici con dettagli specifici**:
   ```bash
   lvs -o +devices
   ```

3. **Mostrare volumi logici inattivi**:
   ```bash
   lvs -a
   ```

4. **Visualizzare le dimensioni in unità leggibili**:
   ```bash
   lvs -h
   ```

5. **Filtrare i volumi logici in base a criteri**:
   ```bash
   lvs -S 'lv_size > 10G'
   ```

## Tips
- Utilizza l'opzione `--noheadings` se desideri un output più pulito, adatto per l'elaborazione automatica.
- Combina `lvs` con altri comandi come `grep` per filtrare ulteriormente i risultati.
- Familiarizza con le opzioni di visualizzazione per ottenere informazioni più dettagliate sui tuoi volumi logici.