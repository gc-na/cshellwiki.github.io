# [Linux] Bash mtr Utilizzo: Strumento di diagnostica della rete

## Overview
Il comando `mtr` (My Traceroute) è uno strumento di diagnostica della rete che combina le funzionalità di `ping` e `traceroute`. Consente di monitorare e analizzare la qualità della connessione verso un host specifico, fornendo informazioni sui pacchetti persi e sui tempi di risposta.

## Usage
La sintassi di base del comando `mtr` è la seguente:

```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: Esegue una modalità report, mostrando i risultati in un formato leggibile.
- `-c <count>`: Specifica il numero di pacchetti da inviare.
- `-i <interval>`: Imposta l'intervallo tra i pacchetti inviati.
- `-p`: Mostra solo le informazioni sui pacchetti persi.
- `-n`: Non risolvere i nomi degli host, mostrando solo gli indirizzi IP.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mtr`:

1. Eseguire un semplice tracciamento verso un host:
   ```bash
   mtr example.com
   ```

2. Eseguire un report con un numero specifico di pacchetti:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Monitorare la connessione con un intervallo di 2 secondi tra i pacchetti:
   ```bash
   mtr -i 2 example.com
   ```

4. Visualizzare solo gli indirizzi IP senza risolvere i nomi:
   ```bash
   mtr -n example.com
   ```

5. Controllare solo i pacchetti persi:
   ```bash
   mtr -p example.com
   ```

## Tips
- Utilizza l'opzione `-r` per ottenere un report finale che puoi facilmente salvare o condividere.
- Se stai diagnosticando problemi di rete, prova a eseguire `mtr` durante diverse ore del giorno per vedere se ci sono variazioni nelle prestazioni.
- Ricorda che alcuni firewall possono bloccare i pacchetti ICMP, quindi i risultati potrebbero non essere sempre rappresentativi della qualità della connessione.