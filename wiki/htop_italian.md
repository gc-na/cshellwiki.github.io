# [Linux] C Shell (csh) htop Utilizzo: Monitorare i processi di sistema

## Overview
Il comando `htop` è un visualizzatore interattivo dei processi in esecuzione su un sistema Unix-like. A differenza del comando `top`, `htop` offre un'interfaccia più user-friendly e consente di gestire i processi in modo più semplice.

## Usage
La sintassi di base del comando `htop` è la seguente:

```csh
htop [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per `htop`:

- `-d [delay]`: Imposta il ritardo tra gli aggiornamenti della visualizzazione (in decimi di secondo).
- `-u [utente]`: Mostra solo i processi appartenenti a un determinato utente.
- `-p [pid]`: Mostra solo il processo con l'ID specificato.
- `--sort-key [chiave]`: Ordina i processi in base alla chiave specificata (ad esempio, `PID`, `MEM`, `CPU`).

## Common Examples
Ecco alcuni esempi pratici di utilizzo di `htop`:

1. Avviare `htop` senza opzioni:
   ```csh
   htop
   ```

2. Visualizzare i processi di un utente specifico:
   ```csh
   htop -u nome_utente
   ```

3. Impostare un ritardo di aggiornamento di 2 secondi:
   ```csh
   htop -d 20
   ```

4. Mostrare solo un processo specifico con PID 1234:
   ```csh
   htop -p 1234
   ```

5. Ordinare i processi per utilizzo della memoria:
   ```csh
   htop --sort-key MEM
   ```

## Tips
- Usa le frecce direzionali per navigare tra i processi e `F9` per terminare un processo selezionato.
- Puoi personalizzare la visualizzazione premendo `F2` per accedere alle impostazioni.
- Ricorda che `htop` richiede i permessi di root per visualizzare tutti i processi di sistema. Usa `sudo htop` se necessario.