# [Linux] Bash foreach penggunaan: Melaksanakan arahan untuk setiap item dalam senarai

## Overview
Perintah `foreach` dalam Bash digunakan untuk melaksanakan satu set arahan untuk setiap item dalam senarai. Ia membolehkan pengguna untuk mengulangi operasi tanpa perlu menulis semula arahan berulang kali, menjadikannya alat yang berguna untuk automasi tugas.

## Usage
Sintaks asas bagi perintah `foreach` adalah seperti berikut:

```bash
foreach [options] [arguments]
```

## Common Options
- `-n` : Menjalankan arahan tanpa mencetak output.
- `-p` : Menjalankan arahan dalam mod interaktif, membolehkan pengguna memberikan input.
- `-v` : Mengaktifkan mod verbose, yang menunjukkan lebih banyak maklumat tentang apa yang sedang dilakukan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `foreach`:

### Contoh 1: Mengulangi senarai fail
```bash
foreach file in *.txt
  echo "Mengolah fail: $file"
end
```
Dalam contoh ini, perintah akan mencetak nama setiap fail dengan sambungan `.txt` dalam direktori semasa.

### Contoh 2: Menghitung nombor
```bash
foreach num in {1..5}
  echo "Nombor: $num"
end
```
Perintah ini akan mencetak nombor dari 1 hingga 5.

### Contoh 3: Menjalankan arahan pada pelbagai direktori
```bash
foreach dir in /path/to/dir1 /path/to/dir2
  cd $dir
  ls
end
```
Contoh ini menunjukkan bagaimana untuk menukar direktori dan menyenaraikan kandungannya untuk beberapa direktori.

## Tips
- Gunakan `foreach` dalam skrip untuk mengautomasi tugas berulang.
- Pastikan untuk menggunakan `end` untuk menandakan akhir blok arahan.
- Pertimbangkan untuk menggunakan `foreach` dalam kombinasi dengan perintah lain untuk meningkatkan kecekapan skrip anda.