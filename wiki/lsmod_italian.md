# [Linux] Bash lsmod utilizzo: visualizzare i moduli del kernel caricati

## Overview
Il comando `lsmod` viene utilizzato per visualizzare i moduli del kernel attualmente caricati nel sistema Linux. I moduli del kernel sono componenti che possono essere caricati e scaricati dal kernel per estenderne le funzionalità senza dover riavviare il sistema.

## Usage
La sintassi di base del comando `lsmod` è la seguente:

```bash
lsmod [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per `lsmod`:

- **(none)**: Non ci sono opzioni specifiche per `lsmod`; il comando viene eseguito senza argomenti per visualizzare l'elenco dei moduli caricati.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `lsmod`:

1. **Visualizzare tutti i moduli caricati**:
   ```bash
   lsmod
   ```

2. **Filtrare l'output per un modulo specifico** (utilizzando `grep`):
   ```bash
   lsmod | grep <nome_modulo>
   ```

3. **Visualizzare i moduli e le loro dipendenze**:
   ```bash
   lsmod
   ```

## Tips
- Utilizza `lsmod` in combinazione con `grep` per trovare rapidamente un modulo specifico.
- Ricorda che `lsmod` mostra solo i moduli attualmente caricati; per caricarne uno nuovo, puoi usare `modprobe` o `insmod`.
- Se hai bisogno di ulteriori informazioni su un modulo specifico, puoi consultare la pagina man di `modinfo <nome_modulo>`.