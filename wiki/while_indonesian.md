# [Linux] Bash while penggunaan: Menjalankan perintah berulang kali

## Overview
Perintah `while` dalam Bash digunakan untuk menjalankan blok perintah berulang kali selama kondisi tertentu terpenuhi. Ini sangat berguna untuk situasi di mana Anda ingin terus melakukan sesuatu sampai kondisi tertentu tidak lagi benar.

## Usage
Sintaks dasar dari perintah `while` adalah sebagai berikut:

```bash
while [kondisi]
do
    # perintah yang akan dijalankan
done
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `while`:

- **kondisi**: Ekspresi yang dievaluasi sebelum setiap iterasi. Jika kondisi benar (true), blok perintah di dalam `do` akan dieksekusi.
  
## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `while`:

### Contoh 1: Menghitung dari 1 hingga 5
```bash
count=1
while [ $count -le 5 ]
do
    echo "Hitung: $count"
    ((count++))
done
```

### Contoh 2: Membaca file baris demi baris
```bash
while IFS= read -r line
do
    echo "Baris: $line"
done < file.txt
```

### Contoh 3: Menunggu input pengguna
```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Masukkan perintah (ketik 'exit' untuk keluar): " input
    echo "Anda memasukkan: $input"
done
```

## Tips
- Pastikan kondisi dalam perintah `while` dapat menjadi false pada suatu saat untuk menghindari loop tak berujung.
- Gunakan `break` untuk keluar dari loop secara paksa jika diperlukan.
- Pertimbangkan untuk menggunakan `sleep` di dalam loop jika Anda melakukan polling atau menunggu kondisi tertentu untuk menghindari penggunaan CPU yang berlebihan.