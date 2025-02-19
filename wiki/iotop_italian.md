# [Linux] C Shell (csh) iotop Utilizzo: Monitorare l'uso del disco in tempo reale

## Overview
Il comando `iotop` è uno strumento utile per monitorare l'input/output del disco in tempo reale. Mostra quali processi stanno utilizzando il disco e quanto, permettendo agli utenti di identificare eventuali colli di bottiglia nelle prestazioni del sistema.

## Usage
La sintassi di base del comando è la seguente:

```csh
iotop [options] [arguments]
```

## Common Options
- `-o` : Mostra solo i processi che stanno attualmente utilizzando il disco.
- `-b` : Esegue `iotop` in modalità batch, utile per l'output su file.
- `-n NUM` : Specifica il numero di aggiornamenti da eseguire in modalità batch.
- `-d SECONDS` : Imposta il tempo di attesa tra gli aggiornamenti in modalità interattiva.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `iotop`:

1. **Visualizzare l'uso del disco in tempo reale**:
   ```csh
   iotop
   ```

2. **Mostrare solo i processi attivi**:
   ```csh
   iotop -o
   ```

3. **Eseguire `iotop` in modalità batch per 10 aggiornamenti**:
   ```csh
   iotop -b -n 10
   ```

4. **Impostare un intervallo di aggiornamento di 2 secondi**:
   ```csh
   iotop -d 2
   ```

## Tips
- Utilizza l'opzione `-o` per concentrarti solo sui processi che stanno attivamente utilizzando il disco, rendendo più facile l'identificazione dei problemi.
- In modalità batch, considera di reindirizzare l'output a un file per analisi successive.
- Ricorda che `iotop` richiede privilegi di root per visualizzare tutte le informazioni sui processi. Assicurati di eseguirlo con `sudo` se necessario.