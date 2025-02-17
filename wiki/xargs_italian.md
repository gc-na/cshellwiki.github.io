# [Linux] Bash xargs utilizzo: Esegue comandi con input da stdin

## Overview
Il comando `xargs` è uno strumento potente in Bash che consente di costruire e eseguire comandi da input standard. È particolarmente utile per elaborare output di altri comandi, permettendo di passare argomenti a comandi che normalmente non accettano input diretto.

## Usage
La sintassi di base del comando `xargs` è la seguente:

```bash
xargs [options] [arguments]
```

## Common Options
Ecco alcune opzioni comuni per `xargs` con brevi spiegazioni:

- `-n N`: Specifica il numero massimo di argomenti da utilizzare per ogni invocazione del comando.
- `-d DELIMITER`: Imposta un delimitatore personalizzato per separare gli argomenti.
- `-p`: Chiede conferma prima di eseguire ogni comando.
- `-0`: Legge gli input separati da null invece che da spazi o nuove righe, utile per gestire file con spazi nei nomi.

## Common Examples

### Eseguire un comando su file trovati
Per eliminare tutti i file `.tmp` nella directory corrente:

```bash
find . -name "*.tmp" | xargs rm
```

### Limitare il numero di argomenti
Per copiare file in un'altra directory, limitando a 2 file per comando:

```bash
ls | xargs -n 2 cp -t /path/to/destination/
```

### Usare un delimitatore personalizzato
Se si ha un file di testo con nomi separati da virgole, si può usare:

```bash
cat file.txt | xargs -d ',' echo
```

### Eseguire un comando con conferma
Per visualizzare i file prima di eliminarli:

```bash
find . -name "*.log" | xargs -p rm
```

## Tips
- Utilizza `-0` con `find` per gestire file con nomi complessi: `find . -print0 | xargs -0 rm`.
- Fai attenzione all'uso di `xargs` con comandi distruttivi come `rm` per evitare cancellazioni accidentali.
- Considera di utilizzare `-n` per evitare di superare i limiti di argomenti del sistema operativo, specialmente con file di grandi dimensioni.