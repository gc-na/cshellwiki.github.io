# [Linux] Bash who utilizzo: mostra gli utenti connessi

## Overview
Il comando `who` in Bash viene utilizzato per visualizzare gli utenti attualmente connessi al sistema. Fornisce informazioni come il nome dell'utente, il terminale utilizzato, la data e l'ora di accesso.

## Usage
La sintassi di base del comando è la seguente:

```bash
who [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `who`:

- `-a`: Mostra tutte le informazioni disponibili, inclusi gli utenti inattivi.
- `-b`: Mostra l'ultima volta che il sistema è stato avviato.
- `-q`: Mostra solo i nomi degli utenti connessi e il numero totale di utenti.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `who`:

1. **Visualizzare gli utenti connessi:**
   ```bash
   who
   ```

2. **Mostrare tutte le informazioni sugli utenti:**
   ```bash
   who -a
   ```

3. **Visualizzare l'ultima volta che il sistema è stato avviato:**
   ```bash
   who -b
   ```

4. **Mostrare solo i nomi degli utenti connessi:**
   ```bash
   who -q
   ```

## Tips
- Utilizza `who -b` per monitorare la stabilità del sistema, assicurandoti che non ci siano riavvii frequenti.
- Combinare `who` con altri comandi come `grep` può aiutarti a filtrare le informazioni. Ad esempio, per trovare un utente specifico:
  ```bash
  who | grep nome_utente
  ```
- Ricorda che `who` mostra solo gli utenti connessi attivamente e non fornisce informazioni sugli utenti disconnessi.