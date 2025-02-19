# [Linux] C Shell (csh) wget utilizzo: Scaricare file da internet

## Overview
Il comando `wget` è uno strumento potente utilizzato per scaricare file da internet. Supporta vari protocolli come HTTP, HTTPS e FTP, ed è in grado di gestire download in background, riprendere download interrotti e scaricare interi siti web.

## Usage
La sintassi di base del comando `wget` è la seguente:

```bash
wget [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `wget`:

- `-O [file]`: Specifica il nome del file di output.
- `-c`: Riprende un download interrotto.
- `-r`: Scarica in modo ricorsivo, utile per scaricare interi siti web.
- `-p`: Scarica tutte le risorse necessarie per visualizzare una pagina web (immagini, fogli di stile, ecc.).
- `--limit-rate=[rate]`: Limita la velocità di download.

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `wget`:

1. Scaricare un file da un URL specifico:

    ```bash
    wget http://esempio.com/file.txt
    ```

2. Scaricare un file e salvarlo con un nome diverso:

    ```bash
    wget -O nuovo_nome.txt http://esempio.com/file.txt
    ```

3. Riprendere un download interrotto:

    ```bash
    wget -c http://esempio.com/file_grande.zip
    ```

4. Scaricare un intero sito web:

    ```bash
    wget -r http://esempio.com
    ```

5. Scaricare una pagina web e tutte le sue risorse:

    ```bash
    wget -p http://esempio.com/pagina.html
    ```

## Tips
- Utilizza l'opzione `-c` per evitare di scaricare nuovamente file già scaricati, risparmiando tempo e banda.
- Se stai scaricando un sito web, considera di utilizzare `--limit-rate` per non sovraccaricare il server.
- Controlla sempre i termini di servizio del sito web prima di scaricare contenuti in modo massivo.