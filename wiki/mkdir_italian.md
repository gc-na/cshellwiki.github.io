# [Linux] Bash mkdir Uso: Crea directory nel file system

## Overview
Il comando `mkdir` (make directory) è utilizzato per creare nuove directory nel file system. È uno strumento fondamentale per organizzare i file e le cartelle in modo efficiente.

## Usage
La sintassi di base del comando `mkdir` è la seguente:

```bash
mkdir [opzioni] [argomenti]
```

## Common Options
- `-p`: Crea directory genitore se non esistono già.
- `-v`: Mostra un messaggio per ogni directory creata.
- `-m`: Imposta i permessi della directory al valore specificato.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mkdir`:

1. **Creare una singola directory:**
   ```bash
   mkdir nuova_cartella
   ```

2. **Creare più directory contemporaneamente:**
   ```bash
   mkdir cartella1 cartella2 cartella3
   ```

3. **Creare una directory e le sue directory genitore:**
   ```bash
   mkdir -p /percorso/della/cartella/genitore/nuova_cartella
   ```

4. **Creare una directory e visualizzare un messaggio:**
   ```bash
   mkdir -v cartella_visibile
   ```

5. **Creare una directory con permessi specifici:**
   ```bash
   mkdir -m 755 cartella_permessi
   ```

## Tips
- Utilizza l'opzione `-p` quando non sei sicuro se le directory genitore esistano già, per evitare errori.
- Controlla i permessi delle directory create con il comando `ls -l` per assicurarti che siano impostati correttamente.
- Ricorda che i nomi delle directory non possono contenere caratteri speciali non validi, quindi scegli nomi semplici e descrittivi.