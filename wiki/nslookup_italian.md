# [Linux] Bash nslookup utilizzo: Risolvere nomi di dominio in indirizzi IP

## Overview
Il comando `nslookup` è uno strumento di rete utilizzato per interrogare i server DNS al fine di ottenere informazioni sui nomi di dominio. Permette di risolvere un nome di dominio in un indirizzo IP e viceversa, fornendo così un modo per diagnosticare problemi di rete e verificare la configurazione DNS.

## Usage
La sintassi di base del comando `nslookup` è la seguente:

```
nslookup [opzioni] [argomenti]
```

## Common Options
- `-type=tipo`: Specifica il tipo di record DNS da cercare (es. A, AAAA, MX).
- `-timeout=secondi`: Imposta il tempo di attesa per una risposta dal server DNS.
- `-retry=numero`: Imposta il numero di tentativi in caso di mancata risposta.
- `server`: Specifica un server DNS diverso da quello predefinito da utilizzare per la query.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `nslookup`:

### Esempio 1: Risolvere un nome di dominio
```bash
nslookup www.example.com
```

### Esempio 2: Ottenere il record MX di un dominio
```bash
nslookup -type=MX example.com
```

### Esempio 3: Utilizzare un server DNS specifico
```bash
nslookup www.example.com 8.8.8.8
```

### Esempio 4: Verificare un indirizzo IP
```bash
nslookup 93.184.216.34
```

## Tips
- Utilizza il comando `nslookup` in modalità interattiva per eseguire più query senza dover digitare nuovamente il comando.
- Ricorda di specificare il tipo di record se stai cercando informazioni specifiche, come i record MX per le email.
- Se riscontri problemi di risoluzione, prova a utilizzare un server DNS pubblico come quelli di Google (8.8.8.8) per verificare se il problema è legato al tuo server DNS locale.