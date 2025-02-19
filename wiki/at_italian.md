# [Linux] C Shell (csh) at: Pianificazione di comandi

## Overview
Il comando `at` consente di pianificare l'esecuzione di comandi o script a un orario specifico nel futuro. È utile per automatizzare attività che devono essere eseguite in un momento preciso.

## Usage
La sintassi di base del comando `at` è la seguente:

```
at [options] [arguments]
```

## Common Options
- `-f`: Specifica un file di input da cui leggere i comandi da eseguire.
- `-l`: Elenca i lavori pianificati per l'utente corrente.
- `-d`: Elimina un lavoro pianificato.
- `-m`: Invia un'email all'utente anche se non ci sono output.

## Common Examples

### Pianificare un comando per eseguirlo tra 5 minuti
```bash
echo "echo 'Ciao, mondo!'" | at now + 5 minutes
```

### Pianificare un comando per un'ora specifica
```bash
echo "backup.sh" | at 14:00
```

### Pianificare un comando per domani
```bash
echo "cleanup.sh" | at tomorrow
```

### Elencare i lavori pianificati
```bash
at -l
```

### Eliminare un lavoro pianificato
```bash
at -d 1
```
*(dove "1" è l'ID del lavoro che si desidera eliminare)*

## Tips
- Assicurati di avere i permessi necessari per utilizzare il comando `at`.
- Controlla frequentemente i lavori pianificati con `at -l` per gestire le tue attività.
- Utilizza l'opzione `-m` se desideri ricevere notifiche via email sui risultati dei comandi eseguiti.