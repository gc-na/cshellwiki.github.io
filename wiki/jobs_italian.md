# [Linux] Bash jobs utilizzo: Gestire i processi in background

## Overview
Il comando `jobs` in Bash è utilizzato per visualizzare i processi in background e in sospensione che sono stati avviati dalla shell corrente. Questo comando è utile per monitorare e gestire i lavori che non sono attualmente in esecuzione in primo piano.

## Usage
La sintassi di base del comando `jobs` è la seguente:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Mostra il PID (Process ID) dei processi.
- `-n`: Mostra solo i lavori che sono cambiati di stato dall'ultima esecuzione del comando.
- `-p`: Mostra solo i PID dei processi in background.

## Common Examples

### Visualizzare i lavori attivi
Per visualizzare i processi in background e in sospensione, basta eseguire:

```bash
jobs
```

### Visualizzare i lavori con PID
Per ottenere informazioni sui lavori attivi insieme ai loro PID, usa l'opzione `-l`:

```bash
jobs -l
```

### Mostrare solo i lavori modificati
Se desideri vedere solo i lavori che hanno cambiato stato dall'ultima volta che hai eseguito il comando, utilizza:

```bash
jobs -n
```

### Mostrare solo i PID dei processi
Per visualizzare solo i PID dei processi in background, puoi usare:

```bash
jobs -p
```

## Tips
- Ricorda che il comando `jobs` mostra solo i processi avviati dalla shell corrente. Se hai aperto più shell, dovrai eseguire `jobs` in ciascuna di esse per vedere i relativi processi.
- Utilizza `fg` per riportare un lavoro in primo piano e `bg` per continuare un lavoro in background.
- È utile eseguire `jobs` frequentemente per tenere traccia dei processi in esecuzione e gestirli in modo efficace.