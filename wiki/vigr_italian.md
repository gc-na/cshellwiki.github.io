# [Linux] Bash vigr Uso: Modifica i file di configurazione di vi

## Overview
Il comando `vigr` è uno strumento utile per modificare i file di configurazione di sistema, come `/etc/passwd` e `/etc/group`, utilizzando l'editor di testo `vi`. Questo comando garantisce che il file venga bloccato durante la modifica, prevenendo conflitti tra più utenti.

## Usage
La sintassi di base del comando `vigr` è la seguente:

```bash
vigr [opzioni] [file]
```

## Common Options
- `-s`: Esegue un controllo di sintassi sul file prima di aprirlo.
- `-f`: Specifica un file di configurazione diverso da quello predefinito.
- `-r`: Ripristina il file di configurazione da un backup.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `vigr`:

1. **Modificare il file passwd**:
   ```bash
   vigr /etc/passwd
   ```

2. **Modificare il file group**:
   ```bash
   vigr /etc/group
   ```

3. **Controllo di sintassi su un file specifico**:
   ```bash
   vigr -s /etc/group
   ```

4. **Usare un file di configurazione personalizzato**:
   ```bash
   vigr -f /path/to/custom_file
   ```

## Tips
- Assicurati di avere i permessi necessari per modificare i file di configurazione di sistema.
- Usa l'opzione `-s` per verificare eventuali errori di sintassi prima di salvare le modifiche.
- Fai sempre un backup del file di configurazione prima di apportare modifiche significative.