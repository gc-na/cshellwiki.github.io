# [Linux] Bash cut utilizzo: Estrazione di porzioni di testo

## Overview
Il comando `cut` in Bash è utilizzato per estrarre sezioni specifiche da ogni riga di un file o di un input standard. È particolarmente utile per lavorare con file di testo delimitati, come CSV o TSV, dove è necessario isolare colonne specifiche.

## Usage
La sintassi di base del comando `cut` è la seguente:

```bash
cut [options] [arguments]
```

## Common Options
- `-f`: Specifica i campi da estrarre, separati da virgole.
- `-d`: Definisce il delimitatore da utilizzare per separare i campi (il delimitatore predefinito è il tab).
- `-c`: Estrae caratteri specifici da ogni riga.
- `--complement`: Restituisce tutto tranne i campi o i caratteri specificati.

## Common Examples

### Estrazione di colonne da un file CSV
Per estrarre la seconda colonna da un file CSV utilizzando la virgola come delimitatore:

```bash
cut -d ',' -f 2 file.csv
```

### Estrazione di caratteri specifici
Per estrarre i primi 5 caratteri di ogni riga in un file di testo:

```bash
cut -c 1-5 file.txt
```

### Estrazione di più colonne
Per estrarre la prima e la terza colonna da un file TSV (tab-separated values):

```bash
cut -d $'\t' -f 1,3 file.tsv
```

### Utilizzo con input standard
Puoi anche utilizzare `cut` con input standard. Ad esempio, per estrarre il primo campo da una lista di nomi separati da spazi:

```bash
echo "Mario Rossi Giovanni Bianchi" | cut -d ' ' -f 1
```

## Tips
- Quando lavori con file delimitati, assicurati di specificare correttamente il delimitatore con l'opzione `-d`.
- Usa l'opzione `--complement` se desideri escludere determinati campi invece di includerli.
- Per visualizzare l'output in modo più leggibile, puoi combinare `cut` con altri comandi come `sort` o `uniq`.