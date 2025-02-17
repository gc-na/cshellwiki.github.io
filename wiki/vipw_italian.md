# [Linux] Bash vipw uso equivalente: Modifica il file delle password in modo sicuro

## Overview
Il comando `vipw` viene utilizzato per modificare in modo sicuro il file delle password di sistema, solitamente `/etc/passwd` e `/etc/shadow`. Questo comando garantisce che nessun altro processo possa modificare questi file mentre sono aperti, prevenendo così la corruzione dei dati.

## Usage
La sintassi di base del comando è la seguente:

```bash
vipw [opzioni]
```

## Common Options
- `-s`: Utilizza l'editor di testo per modificare il file `/etc/shadow` invece di `/etc/passwd`.
- `-f <file>`: Specifica un file diverso da modificare, utile per gestire file di password personalizzati.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `vipw`:

1. **Modificare il file delle password:**
   ```bash
   vipw
   ```

2. **Modificare il file delle password shadow:**
   ```bash
   vipw -s
   ```

3. **Modificare un file di password personalizzato:**
   ```bash
   vipw -f /path/to/custom/passwd
   ```

## Tips
- Assicurati di avere i privilegi di superutente (root) per eseguire `vipw`, poiché richiede permessi elevati per modificare i file di sistema.
- Usa un editor di testo che conosci bene; `vipw` utilizzerà l'editor predefinito del tuo sistema, che può essere modificato tramite la variabile d'ambiente `EDITOR`.
- Fai sempre un backup dei file di configurazione prima di apportare modifiche, per evitare problemi in caso di errori.