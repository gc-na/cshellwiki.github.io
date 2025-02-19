# [Linux] C Shell (csh) trap utilizzo: Gestire i segnali nel terminale

## Overview
Il comando `trap` nel C Shell (csh) viene utilizzato per gestire i segnali e le interruzioni nel terminale. Permette di specificare azioni da eseguire quando il processo riceve determinati segnali, consentendo una gestione più controllata degli eventi nel programma.

## Usage
La sintassi di base del comando `trap` è la seguente:

```csh
trap [azioni] [segnali]
```

## Common Options
- `SIGINT`: Interruzione (Ctrl+C).
- `SIGTERM`: Richiesta di terminazione.
- `SIGQUIT`: Uscita dal programma (Ctrl+\).
- `EXIT`: Azione da eseguire quando lo script termina.

## Common Examples

### Esempio 1: Intercettare SIGINT
Questo esempio mostra come utilizzare `trap` per gestire l'interruzione del programma quando si preme Ctrl+C.

```csh
trap 'echo "Interruzione ricevuta!"' SIGINT
while (1)
    echo "In esecuzione..."
    sleep 1
end
```

### Esempio 2: Pulizia alla chiusura
In questo esempio, `trap` viene utilizzato per eseguire un comando di pulizia quando lo script termina.

```csh
trap 'rm -f temp_file.txt; echo "File temporaneo rimosso."' EXIT
echo "Esecuzione dello script..."
sleep 5
```

### Esempio 3: Gestire SIGTERM
Questo esempio mostra come gestire un segnale di terminazione.

```csh
trap 'echo "Ricevuto SIGTERM, terminazione in corso..."' SIGTERM
while (1)
    echo "In esecuzione..."
    sleep 1
end
```

## Tips
- Utilizza `trap` per garantire che le risorse vengano sempre liberate, anche in caso di interruzione.
- Testa sempre il comportamento del tuo script con i segnali per assicurarti che le azioni di `trap` vengano eseguite come previsto.
- Ricorda che `trap` può essere utilizzato anche per gestire segnali personalizzati, migliorando la robustezza del tuo script.