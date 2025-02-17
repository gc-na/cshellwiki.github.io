# [Linux] Bash mpstat Penggunaan: Memantau statistik pemprosesan

## Overview
Perintah `mpstat` digunakan untuk memantau statistik pemprosesan dalam sistem Linux. Ia memberikan maklumat tentang penggunaan CPU untuk setiap pemproses secara berasingan, membolehkan pengguna menganalisis prestasi sistem dan mengenal pasti potensi masalah.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `mpstat`:

```bash
mpstat [options] [arguments]
```

## Common Options
- `-P ALL` : Menunjukkan statistik untuk semua pemproses.
- `-u` : Menunjukkan penggunaan CPU dalam bentuk peratusan.
- `-h` : Menunjukkan maklumat dalam format yang lebih mudah dibaca.
- `-o` : Menentukan format output (contohnya, CSV).
- `interval` : Menentukan selang masa antara laporan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mpstat`:

1. **Menunjukkan statistik untuk semua pemproses:**
   ```bash
   mpstat -P ALL
   ```

2. **Menunjukkan penggunaan CPU setiap 5 saat:**
   ```bash
   mpstat 5
   ```

3. **Menunjukkan penggunaan CPU dalam format yang lebih mudah dibaca:**
   ```bash
   mpstat -h
   ```

4. **Menunjukkan statistik CPU dalam format CSV:**
   ```bash
   mpstat -o CSV
   ```

## Tips
- Gunakan `mpstat -P ALL` untuk mendapatkan gambaran keseluruhan prestasi semua pemproses dalam sistem.
- Pertimbangkan untuk menggabungkan `mpstat` dengan alat pemantauan lain seperti `top` atau `htop` untuk analisis yang lebih mendalam.
- Simpan output `mpstat` ke dalam fail untuk analisis lanjut menggunakan arahan pengalihan, contohnya:
  ```bash
  mpstat -P ALL > statistik_cpu.txt
  ```