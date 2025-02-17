# [Linux] Bash mpstat Utilizzo: Monitoraggio delle statistiche CPU

## Overview
Il comando `mpstat` è utilizzato per visualizzare le statistiche di utilizzo della CPU su sistemi Linux. Fornisce informazioni dettagliate sull'attività della CPU, consentendo agli utenti di monitorare le prestazioni del sistema e identificare eventuali colli di bottiglia.

## Usage
La sintassi di base del comando `mpstat` è la seguente:

```bash
mpstat [options] [arguments]
```

## Common Options
- `-P ALL`: Mostra le statistiche per tutte le CPU.
- `-u`: Visualizza le statistiche di utilizzo della CPU in percentuale.
- `-h`: Mostra l'output in un formato leggibile.
- `-o`: Specifica il formato di output (es. CSV).
- `interval`: Specifica l'intervallo di tempo tra le misurazioni (in secondi).
- `count`: Numero di volte che il comando deve essere eseguito.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mpstat`:

1. **Visualizzare le statistiche di utilizzo della CPU per tutte le CPU:**
   ```bash
   mpstat -P ALL
   ```

2. **Monitorare l'utilizzo della CPU ogni 2 secondi per 5 volte:**
   ```bash
   mpstat 2 5
   ```

3. **Visualizzare le statistiche di utilizzo della CPU in formato leggibile:**
   ```bash
   mpstat -h
   ```

4. **Esportare le statistiche in formato CSV:**
   ```bash
   mpstat -o CSV
   ```

## Tips
- Utilizza l'opzione `-P ALL` per ottenere una panoramica completa delle prestazioni di tutte le CPU, specialmente su sistemi multi-core.
- Monitora l'utilizzo della CPU durante i picchi di carico per identificare eventuali problemi di prestazioni.
- Considera di eseguire `mpstat` in combinazione con altri strumenti di monitoraggio per un'analisi più approfondita del sistema.