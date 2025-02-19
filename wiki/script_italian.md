# [Linux] C Shell (csh) script utilizzo: Registra sessioni di terminale

## Overview
Il comando `script` in C Shell (csh) viene utilizzato per registrare una sessione di terminale. Questo strumento cattura tutto ciò che viene visualizzato sullo schermo e lo salva in un file, consentendo di rivedere le attività svolte in una sessione di terminale.

## Usage
La sintassi di base del comando è la seguente:

```csh
script [options] [file]
```

## Common Options
- `-a`: Aggiunge l'output al file esistente invece di sovrascriverlo.
- `-f`: Scrive l'output immediatamente nel file, utile per sessioni lunghe.
- `-q`: Esegue il comando in modalità silenziosa, senza messaggi di avvio e chiusura.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `script`:

1. **Registrare una sessione in un file chiamato `session.log`:**
   ```csh
   script session.log
   ```
   Questo comando inizia a registrare la sessione e salva l'output in `session.log`.

2. **Aggiungere l'output a un file esistente:**
   ```csh
   script -a session.log
   ```
   Utilizzando l'opzione `-a`, l'output verrà aggiunto a `session.log` senza sovrascrivere il contenuto esistente.

3. **Eseguire il comando in modalità silenziosa:**
   ```csh
   script -q session.log
   ```
   Questo comando registra la sessione senza mostrare i messaggi di avvio e chiusura.

4. **Scrivere l'output immediatamente nel file:**
   ```csh
   script -f session.log
   ```
   Con l'opzione `-f`, l'output viene scritto nel file in tempo reale.

## Tips
- Assicurati di terminare la registrazione digitando `exit` o `Ctrl+D` per chiudere correttamente il file di output.
- Utilizza nomi di file significativi per i tuoi log, in modo da poterli identificare facilmente in seguito.
- Controlla il file di log dopo la registrazione per assicurarti che tutte le informazioni necessarie siano state catturate.