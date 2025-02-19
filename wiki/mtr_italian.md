# [Linux] C Shell (csh) mtr Uso: Strumento di diagnostica di rete

## Overview
Il comando `mtr` (My Traceroute) combina le funzionalità di `ping` e `traceroute` per fornire informazioni dettagliate sul percorso e sulla latenza dei pacchetti tra il tuo computer e un host remoto. È utile per diagnosticare problemi di rete e per analizzare la qualità della connessione.

## Usage
La sintassi di base del comando è la seguente:

```
mtr [opzioni] [argomenti]
```

## Common Options
- `-r`: Esegue un test in modalità report e termina dopo un numero specificato di ping.
- `-c <count>`: Specifica il numero di pacchetti da inviare.
- `-i <interval>`: Imposta l'intervallo di tempo tra i ping.
- `-p`: Mostra le porte utilizzate per il test.
- `-w`: Abilita la modalità "wide", che espande la visualizzazione.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mtr`:

1. Eseguire un test di mtr su un host specifico:
   ```bash
   mtr example.com
   ```

2. Eseguire un test in modalità report e limitare il numero di ping a 10:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Eseguire mtr con un intervallo di 2 secondi tra i ping:
   ```bash
   mtr -i 2 example.com
   ```

4. Utilizzare la modalità "wide" per una visualizzazione più ampia:
   ```bash
   mtr -w example.com
   ```

## Tips
- Utilizza l'opzione `-r` per ottenere un report finale, utile per la documentazione.
- Se stai diagnosticando problemi di rete, prova a eseguire `mtr` da diversi punti della rete per identificare dove si verifica il problema.
- Ricorda che l'esecuzione di `mtr` può richiedere privilegi di amministratore in alcune configurazioni di rete.