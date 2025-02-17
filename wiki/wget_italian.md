# [Linux] Bash wget utilizzo: Scarica file da URL

## Overview
Il comando `wget` è uno strumento potente per il download di file da Internet. Supporta vari protocolli come HTTP, HTTPS e FTP, consentendo di scaricare file in modo semplice e veloce.

## Usage
La sintassi di base del comando `wget` è la seguente:

```bash
wget [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni di `wget`:

- `-O [file]`: Specifica il nome del file di output.
- `-q`: Esegue il download in modalità silenziosa, senza output.
- `-c`: Riprende un download interrotto.
- `--limit-rate=[rate]`: Limita la velocità di download.
- `-r`: Abilita il download ricorsivo di directory.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `wget`:

### Scaricare un file
Per scaricare un file da un URL specifico:

```bash
wget http://example.com/file.zip
```

### Scaricare un file con un nome specifico
Per scaricare un file e salvarlo con un nome diverso:

```bash
wget -O nuovo_nome.zip http://example.com/file.zip
```

### Riprendere un download interrotto
Se un download è stato interrotto, puoi riprenderlo con:

```bash
wget -c http://example.com/file.zip
```

### Scaricare una pagina web in modalità silenziosa
Per scaricare una pagina web senza output:

```bash
wget -q http://example.com
```

### Scaricare ricorsivamente una directory
Per scaricare tutti i file da una directory:

```bash
wget -r http://example.com/directory/
```

## Tips
- Utilizza l'opzione `-q` per evitare output eccessivo durante il download di file di grandi dimensioni.
- Se hai bisogno di scaricare più file, considera di utilizzare un file di testo con gli URL e il comando `wget -i file.txt`.
- Controlla sempre i termini di servizio del sito web prima di scaricare contenuti in modo massivo.