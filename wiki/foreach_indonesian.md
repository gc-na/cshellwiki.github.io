# [Sistem Operasi] C Shell (csh) foreach Penggunaan: Menjalankan perintah untuk setiap elemen dalam daftar

## Overview
Perintah `foreach` dalam C Shell (csh) digunakan untuk menjalankan serangkaian perintah untuk setiap elemen dalam daftar. Ini sangat berguna ketika Anda perlu melakukan operasi yang sama pada beberapa item tanpa harus menulis ulang perintah untuk setiap item.

## Usage
Berikut adalah sintaks dasar dari perintah `foreach`:

```
foreach variable (list)
    command
end
```

## Common Options
Perintah `foreach` tidak memiliki banyak opsi, tetapi berikut adalah beberapa yang umum digunakan:
- `variable`: Nama variabel yang akan menyimpan setiap elemen dari daftar saat iterasi.
- `list`: Daftar elemen yang ingin Anda iterasi.

## Common Examples

### Contoh 1: Mencetak Nama File
Menampilkan nama file dalam direktori saat ini.

```csh
foreach file (*)
    echo $file
end
```

### Contoh 2: Mengganti Ekstensi File
Mengganti ekstensi file dari `.txt` menjadi `.bak`.

```csh
foreach file (*.txt)
    mv $file `basename $file .txt`.bak
end
```

### Contoh 3: Menjalankan Perintah pada Daftar Angka
Menampilkan kuadrat dari angka 1 hingga 5.

```csh
foreach num (1 2 3 4 5)
    @ square = $num * $num
    echo "Kuadrat dari $num adalah $square"
end
```

## Tips
- Pastikan untuk menutup blok `foreach` dengan `end` untuk menghindari kesalahan sintaks.
- Gunakan wildcard (`*`) untuk menangani banyak file atau elemen dengan mudah.
- Periksa nilai variabel dengan `echo` sebelum menjalankan perintah yang lebih kompleks untuk memastikan bahwa iterasi berjalan dengan benar.