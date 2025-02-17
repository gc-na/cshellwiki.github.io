# [Linux] Bash lvcreate Uso: Crea volumi logici in un gruppo di volumi

## Overview
Il comando `lvcreate` viene utilizzato per creare volumi logici all'interno di un gruppo di volumi in un sistema Linux. Questo comando è parte del Logical Volume Manager (LVM), che consente una gestione flessibile dello spazio su disco.

## Usage
La sintassi di base del comando `lvcreate` è la seguente:

```bash
lvcreate [opzioni] [argomenti]
```

## Common Options
- `-n, --name <nome>`: Specifica il nome del volume logico da creare.
- `-L, --size <dimensione>`: Imposta la dimensione del volume logico.
- `-l, --extents <numero>`: Specifica il numero di estensioni da allocare.
- `-C, --mirrors <numero>`: Crea un volume logico mirroring con il numero specificato di copie.
- `-Z, --zero n` : Imposta se il volume logico deve essere azzerato o meno.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `lvcreate`:

1. Creare un volume logico di 10 GB chiamato "mio_volume" nel gruppo di volumi "mio_gruppo":

   ```bash
   lvcreate -n mio_volume -L 10G mio_gruppo
   ```

2. Creare un volume logico di 5 estensioni nel gruppo di volumi "mio_gruppo":

   ```bash
   lvcreate -n mio_volume -l 5 mio_gruppo
   ```

3. Creare un volume logico di 20 GB e azzerarlo:

   ```bash
   lvcreate -n mio_volume -L 20G -Z y mio_gruppo
   ```

4. Creare un volume logico mirroring con 2 copie:

   ```bash
   lvcreate -n mio_volume -L 15G -m 1 mio_gruppo
   ```

## Tips
- Assicurati di avere spazio sufficiente nel gruppo di volumi prima di creare un nuovo volume logico.
- Utilizza nomi descrittivi per i volumi logici per facilitare la gestione futura.
- Considera di utilizzare il mirroring per aumentare la disponibilità dei dati, se necessario.