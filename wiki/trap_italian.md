# [Linux] Bash trap uso: Gestire i segnali e le uscite

## Overview
Il comando `trap` in Bash viene utilizzato per catturare segnali e gestire le uscite di uno script. Permette di eseguire comandi specifici quando si ricevono determinati segnali o quando si esce dallo script, migliorando così il controllo e la gestione degli errori.

## Usage
La sintassi di base del comando `trap` è la seguente:

```bash
trap [azioni] [segnali]
```

## Common Options
- `EXIT`: Specifica un'azione da eseguire quando lo script termina.
- `SIGINT`: Cattura il segnale di interruzione (Ctrl+C).
- `SIGTERM`: Cattura il segnale di terminazione.
- `SIGQUIT`: Cattura il segnale di uscita (Ctrl+\).

## Common Examples

### Eseguire un comando all'uscita
Ecco come eseguire un comando quando lo script termina:

```bash
trap 'echo "Script terminato."' EXIT
```

### Catturare un'interruzione
Per gestire l'interruzione dello script con Ctrl+C:

```bash
trap 'echo "Interruzione ricevuta!"; exit' SIGINT
```

### Pulire i file temporanei
È possibile utilizzare `trap` per rimuovere file temporanei all'uscita dello script:

```bash
trap 'rm -f /tmp/tempfile' EXIT
```

### Catturare più segnali
Puoi catturare più segnali e specificare azioni diverse:

```bash
trap 'echo "Interruzione"; exit' SIGINT
trap 'echo "Terminazione"; exit' SIGTERM
```

## Tips
- Utilizza `trap` per garantire che le risorse vengano sempre liberate, anche in caso di errori.
- Testa sempre il comportamento del tuo script con i segnali per assicurarti che le azioni siano eseguite come previsto.
- Ricorda che le azioni specificate in `trap` possono contenere comandi complessi, ma è consigliabile mantenerle semplici per evitare confusione.