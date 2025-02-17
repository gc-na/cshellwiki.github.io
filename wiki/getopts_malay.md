# [Linux] Bash getopts Penggunaan: Mengendalikan Pilihan dalam Skrip Bash

## Overview
Perintah `getopts` digunakan dalam skrip Bash untuk memproses pilihan dan argumen yang diberikan kepada skrip. Ia membolehkan pengguna untuk menangkap pilihan seperti `-a`, `-b`, dan seterusnya, serta argumen yang berkaitan dengan pilihan tersebut.

## Usage
Berikut adalah sintaks asas untuk menggunakan `getopts`:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: Menandakan pilihan yang akan diproses.
- `-b`: Menandakan pilihan lain yang boleh diterima.
- `:`: Menunjukkan bahawa pilihan memerlukan argumen.

## Common Examples

### Contoh 1: Menggunakan Pilihan Tunggal
```bash
#!/bin/bash
while getopts "a:" opt; do
  case $opt in
    a)
      echo "Pilihan -a diterima dengan argumen: $OPTARG"
      ;;
    \?)
      echo "Pilihan tidak sah: -$OPTARG" >&2
      ;;
  esac
done
```

### Contoh 2: Menggunakan Beberapa Pilihan
```bash
#!/bin/bash
while getopts "ab:" opt; do
  case $opt in
    a)
      echo "Pilihan -a diterima"
      ;;
    b)
      echo "Pilihan -b diterima dengan argumen: $OPTARG"
      ;;
    \?)
      echo "Pilihan tidak sah: -$OPTARG" >&2
      ;;
  esac
done
```

### Contoh 3: Mengendalikan Pilihan Tanpa Argumen
```bash
#!/bin/bash
while getopts "abc" opt; do
  case $opt in
    a)
      echo "Pilihan -a diterima"
      ;;
    b)
      echo "Pilihan -b diterima"
      ;;
    c)
      echo "Pilihan -c diterima"
      ;;
    \?)
      echo "Pilihan tidak sah: -$OPTARG" >&2
      ;;
  esac
done
```

## Tips
- Sentiasa gunakan `:` selepas pilihan yang memerlukan argumen untuk mengelakkan kekeliruan.
- Gunakan `OPTIND` untuk mengawal indeks pilihan yang sedang diproses, terutamanya jika anda juga ingin memproses argumen selepas pilihan.
- Uji skrip anda dengan pelbagai kombinasi pilihan untuk memastikan ia berfungsi seperti yang diharapkan.