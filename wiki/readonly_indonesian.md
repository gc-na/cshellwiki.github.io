# [Linux] Bash readonly Penggunaan: Mengatur variabel sebagai tidak dapat diubah

## Overview
Perintah `readonly` dalam Bash digunakan untuk menetapkan variabel sebagai tidak dapat diubah. Setelah sebuah variabel ditetapkan sebagai readonly, nilainya tidak dapat diubah atau dihapus selama sesi shell tersebut. Ini berguna untuk melindungi variabel penting dari modifikasi yang tidak disengaja.

## Usage
Sintaks dasar dari perintah `readonly` adalah sebagai berikut:

```bash
readonly [options] [arguments]
```

## Common Options
- `-p`: Menampilkan semua variabel yang ditetapkan sebagai readonly beserta nilainya.

## Common Examples

### Menetapkan variabel sebagai readonly
```bash
readonly VAR="Ini tidak bisa diubah"
```

### Mencoba mengubah nilai variabel readonly
```bash
VAR="Coba ubah"  # Ini akan menghasilkan error
```

### Menampilkan variabel readonly
```bash
readonly -p
```

### Menghapus variabel readonly (dengan menggunakan unset)
```bash
unset VAR  # Ini akan menghasilkan error karena VAR adalah readonly
```

## Tips
- Gunakan `readonly` untuk melindungi variabel yang penting dalam skrip Anda agar tidak diubah secara tidak sengaja.
- Selalu periksa variabel readonly dengan `readonly -p` sebelum mencoba mengubahnya.
- Pertimbangkan untuk menggunakan `readonly` pada variabel yang berisi konfigurasi atau pengaturan yang tidak boleh diubah selama eksekusi skrip.