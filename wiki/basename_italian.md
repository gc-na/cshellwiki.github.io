# [Linux] Bash basename uso equivalente: Estrae il nome di un file da un percorso

## Overview
Il comando `basename` in Bash è utilizzato per estrarre il nome di un file da un percorso completo. Questo è particolarmente utile quando si desidera ottenere solo il nome del file senza il percorso che lo precede.

## Usage
La sintassi di base del comando `basename` è la seguente:

```bash
basename [opzioni] [argomenti]
```

## Common Options
- `-a`: Tratta ogni argomento come un file separato e restituisce il nome di base per ciascuno.
- `-s`: Rimuove una specifica estensione dal nome del file.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `basename`:

1. **Estrazione del nome di un file da un percorso**:
   ```bash
   basename /percorso/del/file/nomefile.txt
   ```
   Output: `nomefile.txt`

2. **Estrazione del nome di un file senza estensione**:
   ```bash
   basename /percorso/del/file/nomefile.txt .txt
   ```
   Output: `nomefile`

3. **Uso dell'opzione -a per più file**:
   ```bash
   basename -a /percorso/del/file/nomefile1.txt /percorso/del/file/nomefile2.txt
   ```
   Output:
   ```
   nomefile1.txt
   nomefile2.txt
   ```

4. **Rimozione di un'estensione specifica**:
   ```bash
   basename /percorso/del/file/nomefile.log .log
   ```
   Output: `nomefile`

## Tips
- Utilizza `basename` in script per semplificare la gestione dei file e dei loro nomi.
- Quando usi l'opzione `-s`, assicurati che l'estensione che stai rimuovendo corrisponda esattamente a quella del file.
- Puoi combinare `basename` con altri comandi come `find` per ottenere risultati più complessi e utili.