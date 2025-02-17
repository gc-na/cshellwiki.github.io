# [Linux] Bash getopts Penggunaan: Mengelola opsi baris perintah

## Overview
Perintah `getopts` digunakan dalam skrip Bash untuk memproses opsi dan argumen dari baris perintah. Ini memungkinkan pengguna untuk menangani input yang lebih kompleks dengan cara yang terstruktur, sehingga memudahkan pengelolaan opsi yang diberikan saat menjalankan skrip.

## Usage
Berikut adalah sintaks dasar dari perintah `getopts`:

```bash
getopts [options] [arguments]
```

## Common Options
Beberapa opsi umum yang digunakan dengan `getopts` adalah:

- `-a`: Menetapkan opsi untuk menerima argumen.
- `-b`: Menetapkan opsi untuk menerima beberapa argumen.
- `-c`: Menetapkan opsi untuk mengatur nilai default.
- `-d`: Menetapkan opsi untuk menampilkan pesan bantuan.

## Common Examples

### Contoh 1: Menggunakan getopts untuk opsi sederhana
```bash
#!/bin/bash

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Opsi -a diaktifkan"
      ;;
    b)
      echo "Opsi -b dengan argumen: $OPTARG"
      ;;
    c)
      echo "Opsi -c dengan argumen: $OPTARG"
      ;;
    *)
      echo "Opsi tidak valid"
      ;;
  esac
done
```

### Contoh 2: Menangani beberapa argumen
```bash
#!/bin/bash

while getopts "a:b:c:" opt; do
  case $opt in
    a)
      echo "Opsi -a diaktifkan"
      ;;
    b)
      echo "Opsi -b dengan argumen: $OPTARG"
      ;;
    c)
      echo "Opsi -c dengan argumen: $OPTARG"
      ;;
    *)
      echo "Opsi tidak valid"
      ;;
  esac
done

echo "Selesai memproses opsi."
```

### Contoh 3: Menampilkan pesan bantuan
```bash
#!/bin/bash

show_help() {
  echo "Penggunaan: $0 [-a] [-b arg] [-c arg]"
  echo "  -a        Aktifkan opsi a"
  echo "  -b arg   Opsi b dengan argumen"
  echo "  -c arg   Opsi c dengan argumen"
}

while getopts "hab:c:" opt; do
  case $opt in
    h)
      show_help
      exit 0
      ;;
    a)
      echo "Opsi -a diaktifkan"
      ;;
    b)
      echo "Opsi -b dengan argumen: $OPTARG"
      ;;
    c)
      echo "Opsi -c dengan argumen: $OPTARG"
      ;;
    *)
      show_help
      exit 1
      ;;
  esac
done
```

## Tips
- Selalu sertakan opsi bantuan (`-h`) dalam skrip Anda untuk memudahkan pengguna memahami cara penggunaan.
- Gunakan `OPTARG` untuk mendapatkan nilai argumen yang terkait dengan opsi yang dipilih.
- Pastikan untuk menangani opsi yang tidak valid dengan baik agar pengguna mendapatkan umpan balik yang jelas.