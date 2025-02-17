# [Linux] Bash rsync utilizzo: Sincronizzazione di file e directory

## Overview
Il comando `rsync` è uno strumento potente per la sincronizzazione di file e directory tra diverse posizioni, sia locali che remote. È particolarmente utile per il backup e il trasferimento di dati, poiché solo i file modificati vengono copiati, riducendo il tempo e la larghezza di banda necessari.

## Usage
La sintassi di base del comando `rsync` è la seguente:

```bash
rsync [opzioni] [origine] [destinazione]
```

## Common Options
Ecco alcune opzioni comuni per `rsync`:

- `-a`: Modalità archivio; copia in modo ricorsivo e preserva i permessi, le date e i link simbolici.
- `-v`: Verboso; mostra i dettagli del processo di copia.
- `-z`: Comprimi i dati durante il trasferimento.
- `-r`: Copia in modo ricorsivo le directory.
- `--delete`: Elimina i file nella destinazione che non esistono più nell'origine.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `rsync`:

1. **Sincronizzare una directory locale con un'altra directory locale:**

   ```bash
   rsync -av /percorso/origine/ /percorso/destinazione/
   ```

2. **Sincronizzare una directory locale con un server remoto:**

   ```bash
   rsync -av /percorso/origine/ utente@server:/percorso/destinazione/
   ```

3. **Sincronizzare una directory remota con una directory locale:**

   ```bash
   rsync -av utente@server:/percorso/origine/ /percorso/destinazione/
   ```

4. **Sincronizzare e comprimere i dati durante il trasferimento:**

   ```bash
   rsync -avz /percorso/origine/ utente@server:/percorso/destinazione/
   ```

5. **Sincronizzare e eliminare i file non più presenti nell'origine:**

   ```bash
   rsync -av --delete /percorso/origine/ /percorso/destinazione/
   ```

## Tips
- Utilizza l'opzione `-n` (dry run) per simulare il comando senza eseguire effettivamente la copia. Questo è utile per verificare quali file verrebbero copiati o eliminati.
- Assicurati di avere i permessi necessari per accedere alle directory di origine e destinazione.
- Considera di utilizzare `rsync` su una rete sicura o tramite SSH per garantire la sicurezza dei dati durante il trasferimento.