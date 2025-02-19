# [Linux] C Shell (csh) mpstat Utilizzo: Monitorare le statistiche della CPU

## Overview
Il comando `mpstat` è utilizzato per visualizzare le statistiche di utilizzo della CPU in un sistema. Fornisce informazioni dettagliate sulle prestazioni della CPU, consentendo agli utenti di monitorare l'attività della CPU in tempo reale.

## Usage
La sintassi di base del comando `mpstat` è la seguente:

```csh
mpstat [options] [arguments]
```

## Common Options
- `-P ALL`: Mostra le statistiche per tutte le CPU.
- `-u`: Visualizza l'utilizzo della CPU in percentuale.
- `-w`: Mostra le statistiche di attesa della CPU.
- `-h`: Mostra l'help con le opzioni disponibili.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `mpstat`:

1. **Visualizzare le statistiche di utilizzo della CPU per tutte le CPU:**
   ```csh
   mpstat -P ALL
   ```

2. **Visualizzare l'utilizzo della CPU ogni 5 secondi:**
   ```csh
   mpstat 5
   ```

3. **Mostrare solo l'utilizzo della CPU:**
   ```csh
   mpstat -u
   ```

4. **Visualizzare le statistiche di attesa della CPU:**
   ```csh
   mpstat -w
   ```

## Tips
- Utilizza l'opzione `-P ALL` per avere una visione completa dell'utilizzo della CPU su sistemi multi-core.
- Esegui `mpstat` in combinazione con altri strumenti di monitoraggio per ottenere un quadro più dettagliato delle prestazioni del sistema.
- Considera di impostare un intervallo di aggiornamento per monitorare le tendenze nel tempo, ad esempio utilizzando `mpstat 1` per aggiornamenti ogni secondo.