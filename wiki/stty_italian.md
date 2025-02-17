# [Linux] Bash stty utilizzo: Configurazione delle impostazioni del terminale

## Overview
Il comando `stty` in Bash è utilizzato per modificare e visualizzare le impostazioni del terminale. Permette di configurare vari aspetti del comportamento del terminale, come il controllo del flusso, la gestione dei caratteri e le opzioni di input/output.

## Usage
La sintassi di base del comando `stty` è la seguente:

```bash
stty [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `stty`:

- `-a`: Mostra tutte le impostazioni correnti del terminale.
- `-g`: Restituisce le impostazioni correnti in un formato che può essere riutilizzato.
- `erase`: Imposta il carattere di cancellazione.
- `kill`: Imposta il carattere di cancellazione della linea.
- `intr`: Imposta il carattere di interruzione.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `stty`:

1. **Visualizzare tutte le impostazioni del terminale:**

   ```bash
   stty -a
   ```

2. **Impostare il carattere di cancellazione su Ctrl+H:**

   ```bash
   stty erase ^H
   ```

3. **Impostare il carattere di interruzione su Ctrl+C:**

   ```bash
   stty intr ^C
   ```

4. **Salvare le impostazioni correnti in una variabile:**

   ```bash
   settings=$(stty -g)
   ```

5. **Ripristinare le impostazioni da una variabile:**

   ```bash
   stty $settings
   ```

## Tips
- Utilizza `stty -a` per avere una panoramica completa delle impostazioni correnti prima di apportare modifiche.
- Fai attenzione quando modifichi le impostazioni, poiché alcune possono influenzare il comportamento del terminale in modi imprevisti.
- Se non sei sicuro di un'impostazione, considera di salvarne una copia con `stty -g` prima di modificarla, in modo da poterla ripristinare facilmente.