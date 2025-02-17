# [Linux] Bash lsblk Utilizzo: Visualizzare le informazioni sui dispositivi a blocchi

## Overview
Il comando `lsblk` è utilizzato per elencare i dispositivi a blocchi presenti nel sistema, come dischi rigidi, partizioni e dispositivi di archiviazione USB. Mostra una rappresentazione gerarchica dei dispositivi e delle loro relazioni, rendendo facile identificare come sono organizzati.

## Usage
La sintassi di base del comando `lsblk` è la seguente:

```bash
lsblk [options] [arguments]
```

## Common Options
- `-a`, `--all`: Mostra tutti i dispositivi, inclusi quelli non montati.
- `-f`, `--fs`: Mostra informazioni sul filesystem, come tipo e UUID.
- `-l`, `--list`: Mostra l'output in formato elenco piuttosto che in formato ad albero.
- `-o`, `--output`: Specifica quali colonne visualizzare nell'output.
- `-p`, `--paths`: Mostra i percorsi completi dei dispositivi.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `lsblk`:

1. **Elencare tutti i dispositivi a blocchi:**
   ```bash
   lsblk
   ```

2. **Mostrare tutti i dispositivi, compresi quelli non montati:**
   ```bash
   lsblk -a
   ```

3. **Mostrare informazioni sul filesystem:**
   ```bash
   lsblk -f
   ```

4. **Visualizzare l'output in formato elenco:**
   ```bash
   lsblk -l
   ```

5. **Mostrare solo colonne specifiche (ad esempio, NAME e SIZE):**
   ```bash
   lsblk -o NAME,SIZE
   ```

## Tips
- Utilizza l'opzione `-f` per ottenere informazioni dettagliate sui filesystem, utile per la gestione delle partizioni.
- Se hai bisogno di un output più leggibile, considera di utilizzare l'opzione `-l` per visualizzare i dispositivi in formato elenco.
- Ricorda che l'output di `lsblk` può variare a seconda dei permessi dell'utente; esegui il comando come root se hai bisogno di visualizzare tutti i dispositivi.