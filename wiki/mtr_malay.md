# [Linux] Bash mtr Penggunaan: Menyemak laluan rangkaian

## Overview
Perintah `mtr` (My Traceroute) adalah alat yang menggabungkan fungsi `ping` dan `traceroute` untuk menganalisis laluan rangkaian dari komputer anda ke host lain. Ia memberikan maklumat tentang masa perjalanan dan kehilangan paket di setiap hop dalam laluan rangkaian.

## Usage
Sintaks asas untuk menggunakan perintah `mtr` adalah seperti berikut:

```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: Menghasilkan laporan ringkas.
- `-c <count>`: Menentukan bilangan ping yang akan dihantar.
- `-i <interval>`: Menetapkan selang masa antara ping dalam saat.
- `-p`: Menunjukkan nombor port untuk sambungan.
- `-n`: Mengelakkan resolusi nama host, hanya menunjukkan alamat IP.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mtr` yang biasa:

1. **Menggunakan mtr untuk mengesan laluan ke sebuah host:**
   ```bash
   mtr google.com
   ```

2. **Menghasilkan laporan ringkas dengan 5 ping:**
   ```bash
   mtr -r -c 5 google.com
   ```

3. **Menetapkan selang ping kepada 2 saat:**
   ```bash
   mtr -i 2 google.com
   ```

4. **Menggunakan mtr tanpa resolusi nama host:**
   ```bash
   mtr -n google.com
   ```

## Tips
- Gunakan pilihan `-r` untuk mendapatkan laporan yang lebih mudah dibaca jika anda hanya memerlukan ringkasan.
- Jika anda mengalami masalah rangkaian, cuba gunakan pilihan `-c` untuk menghantar lebih banyak ping dan mendapatkan gambaran yang lebih jelas tentang kehilangan paket.
- Untuk analisis yang lebih mendalam, pertimbangkan untuk menggunakan pilihan `-p` untuk menyemak sambungan ke port tertentu.