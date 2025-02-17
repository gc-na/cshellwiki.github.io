# [Linux] Bash tune2fs uso: Modifica parametri del filesystem ext2/ext3/ext4

## Overview
Il comando `tune2fs` è utilizzato per modificare i parametri di un filesystem di tipo ext2, ext3 o ext4. Permette di ottimizzare e configurare vari aspetti del filesystem, come le opzioni di montaggio e le caratteristiche di journaling.

## Usage
La sintassi di base del comando è la seguente:

```bash
tune2fs [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `tune2fs`:

- `-c <numero>`: Imposta il numero massimo di montaggi prima che il filesystem venga controllato.
- `-i <intervallo>`: Imposta l'intervallo di tempo tra i controlli automatici del filesystem.
- `-m <percentuale>`: Imposta la percentuale di spazio riservato per l'utente root.
- `-O <opzione>`: Abilita una specifica opzione del filesystem.
- `-L <etichetta>`: Cambia l'etichetta del filesystem.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `tune2fs`:

1. **Impostare il numero massimo di montaggi**:
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

2. **Impostare un intervallo di controllo di 30 giorni**:
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. **Riservare il 5% dello spazio per l'utente root**:
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Abilitare l'opzione di journaling**:
   ```bash
   tune2fs -O journal_data /dev/sda1
   ```

5. **Cambiare l'etichetta del filesystem**:
   ```bash
   tune2fs -L "NuovaEtichetta" /dev/sda1
   ```

## Tips
- Assicurati di eseguire `tune2fs` su filesystem smontati o in modalità di sola lettura per evitare danni.
- Controlla sempre lo stato del filesystem con `fsck` prima di apportare modifiche significative.
- Utilizza l'opzione `-l` per visualizzare le informazioni correnti del filesystem prima di modificarlo:
  ```bash
  tune2fs -l /dev/sda1
  ```