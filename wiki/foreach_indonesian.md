# [Linux] Bash foreach penggunaan: Menjalankan perintah untuk setiap item dalam daftar

## Overview
Perintah `foreach` dalam Bash digunakan untuk menjalankan serangkaian perintah untuk setiap item dalam daftar. Ini sangat berguna untuk mengulangi tugas yang sama pada beberapa file atau argumen tanpa harus menulis ulang perintah.

## Usage
Berikut adalah sintaks dasar dari perintah `foreach`:

```bash
foreach variable (list)
    command
end
```

## Common Options
- `variable`: Nama variabel yang akan menyimpan setiap item dalam daftar.
- `list`: Daftar item yang ingin Anda iterasi.
- `command`: Perintah yang akan dijalankan untuk setiap item dalam daftar.

## Common Examples

### Contoh 1: Menampilkan nama file
Menampilkan semua file dalam direktori saat ini:

```bash
foreach file (*)
    echo $file
end
```

### Contoh 2: Menghapus file sementara
Menghapus semua file dengan ekstensi `.tmp`:

```bash
foreach file (*.tmp)
    rm $file
end
```

### Contoh 3: Menyalin file
Menyalin semua file `.txt` ke direktori lain:

```bash
foreach file (*.txt)
    cp $file /path/to/destination/
end
```

## Tips
- Pastikan untuk menggunakan tanda kurung yang benar saat mendefinisikan daftar.
- Gunakan `echo` untuk menguji perintah sebelum menjalankannya untuk memastikan semuanya berjalan sesuai rencana.
- Jika Anda bekerja dengan banyak file, pertimbangkan untuk menggunakan wildcard untuk menyederhanakan daftar item.