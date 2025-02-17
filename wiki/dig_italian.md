# [Linux] Bash dig uso: Strumento per interrogare server DNS

## Overview
Il comando `dig` (Domain Information Groper) è uno strumento utilizzato per interrogare i server DNS (Domain Name System). Permette di ottenere informazioni dettagliate su vari record DNS, come indirizzi IP, record MX, e altro ancora. È particolarmente utile per la risoluzione dei problemi di rete e per la verifica della configurazione DNS.

## Usage
La sintassi di base del comando `dig` è la seguente:

```bash
dig [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `dig`:

- `@server`: Specifica un server DNS da interrogare.
- `-t tipo`: Specifica il tipo di record DNS da cercare (es. A, AAAA, MX, TXT).
- `+short`: Restituisce un output più conciso, mostrando solo le informazioni essenziali.
- `+trace`: Segue la catena di risoluzione DNS fino al server autoritativo.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `dig`:

1. **Interrogare un record A di un dominio**:
   ```bash
   dig example.com
   ```

2. **Interrogare un record MX (Mail Exchange)**:
   ```bash
   dig -t MX example.com
   ```

3. **Utilizzare un server DNS specifico**:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Ottenere un output breve**:
   ```bash
   dig +short example.com
   ```

5. **Tracciare la risoluzione DNS**:
   ```bash
   dig +trace example.com
   ```

## Tips
- Utilizza l'opzione `+short` per ottenere risultati più leggibili quando hai bisogno solo di informazioni essenziali.
- Se stai risolvendo problemi di DNS, considera di utilizzare `+trace` per vedere il percorso completo della risoluzione.
- Prova a interrogare diversi server DNS pubblici, come Google (8.8.8.8) o Cloudflare (1.1.1.1), per confrontare i risultati.