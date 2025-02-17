# [Linux] Bash blkid Uso: Identificare i dispositivi di archiviazione

## Overview
Il comando `blkid` è utilizzato per identificare i dispositivi di archiviazione e visualizzare le informazioni sui loro file system. Fornisce dettagli come l'UUID (Identificatore Universale Unico), il tipo di file system e altre informazioni utili sui dispositivi di blocco.

## Usage
La sintassi di base del comando `blkid` è la seguente:

```bash
blkid [options] [arguments]
```

## Common Options
- `-o, --output`: Specifica il formato dell'output. Può essere `value`, `full`, `list`, ecc.
- `-s, --match-tag`: Filtra l'output per mostrare solo i tag specificati.
- `-p, --probe`: Prova a rilevare il tipo di file system.
- `-c, --cache`: Utilizza la cache per migliorare le prestazioni.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `blkid`:

1. **Visualizzare tutte le informazioni sui dispositivi di archiviazione:**

   ```bash
   blkid
   ```

2. **Visualizzare informazioni specifiche su un dispositivo:**

   ```bash
   blkid /dev/sda1
   ```

3. **Mostrare solo l'UUID di un dispositivo:**

   ```bash
   blkid -s UUID -o value /dev/sda1
   ```

4. **Filtrare l'output per mostrare solo i dispositivi con un file system ext4:**

   ```bash
   blkid -t TYPE=ext4
   ```

## Tips
- Utilizza `blkid` con i permessi di superutente (sudo) per ottenere informazioni complete sui dispositivi.
- Puoi combinare `blkid` con altri comandi come `grep` per filtrare ulteriormente i risultati.
- Ricorda che `blkid` può essere utile per configurare file di sistema come `/etc/fstab`, dove è necessario specificare UUID e tipi di file system.