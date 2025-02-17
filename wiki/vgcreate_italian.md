# [Linux] Bash vgcreate Uso: Crea un gruppo di volumi logici

## Overview
Il comando `vgcreate` viene utilizzato per creare un nuovo gruppo di volumi (VG) in un sistema Linux che utilizza LVM (Logical Volume Manager). Questo comando è fondamentale per gestire lo spazio di archiviazione in modo flessibile, consentendo di aggregare più volumi fisici in un'unica entità logica.

## Usage
La sintassi di base del comando `vgcreate` è la seguente:

```bash
vgcreate [options] [nome_del_gruppo] [volumi_fisici]
```

## Common Options
- `-s, --stripes <n>`: Specifica il numero di strisce per i volumi logici.
- `-p, --maxlogicalvolumes <n>`: Imposta il numero massimo di volumi logici che possono essere creati nel gruppo.
- `-y, --yes`: Risponde automaticamente "sì" a tutte le domande durante l'esecuzione del comando.

## Common Examples

### Creare un nuovo gruppo di volumi
Per creare un gruppo di volumi chiamato `vg1` utilizzando i volumi fisici `/dev/sda1` e `/dev/sdb1`, puoi utilizzare il seguente comando:

```bash
vgcreate vg1 /dev/sda1 /dev/sdb1
```

### Creare un gruppo di volumi con opzioni
Se desideri specificare il numero massimo di volumi logici e il numero di strisce, puoi farlo in questo modo:

```bash
vgcreate -p 10 -s 64K vg2 /dev/sdc1 /dev/sdd1
```

### Verificare la creazione del gruppo di volumi
Dopo aver creato un gruppo di volumi, puoi verificarne l'esistenza con il comando:

```bash
vgs
```

## Tips
- Assicurati che i volumi fisici siano già inizializzati con `pvcreate` prima di utilizzare `vgcreate`.
- Controlla sempre lo stato del tuo gruppo di volumi dopo la creazione per confermare che tutto sia andato a buon fine.
- Considera di utilizzare opzioni come `--yes` se stai eseguendo script automatizzati per evitare interruzioni.