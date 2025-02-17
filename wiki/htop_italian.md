# [Linux] Bash htop utilizzo: Monitorare le risorse di sistema in tempo reale

## Overview
Il comando `htop` è un visualizzatore interattivo dei processi in esecuzione su un sistema Linux. A differenza del comando `top`, `htop` offre un'interfaccia utente più amichevole e consente di gestire i processi in modo più semplice e intuitivo.

## Usage
La sintassi di base del comando `htop` è la seguente:

```bash
htop [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `htop`:

- `-h`, `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `-s`, `--sort`: Permette di ordinare i processi in base a un criterio specifico (es. CPU, memoria).
- `-p`, `--pid`: Mostra solo i processi con gli ID specificati.
- `-u`, `--user`: Mostra solo i processi appartenenti a un utente specifico.

## Common Examples

Ecco alcuni esempi pratici di utilizzo di `htop`:

1. **Avviare htop senza opzioni**:
   ```bash
   htop
   ```

2. **Ordinare i processi per utilizzo della CPU**:
   ```bash
   htop -s PERCENT_CPU
   ```

3. **Mostrare solo i processi di un utente specifico**:
   ```bash
   htop -u nome_utente
   ```

4. **Mostrare solo processi specifici per ID**:
   ```bash
   htop -p 1234,5678
   ```

## Tips
- Usa le frecce direzionali per navigare tra i processi e `F9` per terminare un processo selezionato.
- Puoi personalizzare la visualizzazione premendo `F2` per accedere al menu di configurazione.
- Per aggiornare manualmente la visualizzazione, premi `F5` per passare alla vista ad albero dei processi.

Utilizzare `htop` è un modo efficace per monitorare le risorse del sistema e gestire i processi in modo più efficiente.