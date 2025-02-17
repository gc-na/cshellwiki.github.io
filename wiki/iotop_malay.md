# [Linux] Bash iotop Penggunaan: Memantau penggunaan I/O proses

## Overview
Perintah `iotop` digunakan untuk memantau penggunaan input/output (I/O) oleh proses yang sedang berjalan di sistem Linux. Ia memberikan gambaran yang jelas tentang proses mana yang menggunakan sumber daya I/O paling banyak, membantu dalam pengoptimuman dan penyelesaian masalah.

## Usage
Sintaks asas untuk menggunakan `iotop` adalah seperti berikut:

```bash
iotop [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `iotop` beserta penjelasan ringkas:

- `-o`, `--only`: Hanya menunjukkan proses yang sedang melakukan I/O.
- `-b`, `--batch`: Menjalankan `iotop` dalam mod batch, sesuai untuk output ke fail.
- `-n NUM`, `--iter NUM`: Menentukan berapa kali `iotop` akan mengulangi pengukuran sebelum berhenti.
- `-d SEC`, `--delay SEC`: Menentukan selang masa (dalam saat) antara pengukuran.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `iotop`:

1. **Menjalankan iotop dalam mod interaktif:**
   ```bash
   iotop
   ```

2. **Menunjukkan hanya proses yang aktif dalam I/O:**
   ```bash
   iotop -o
   ```

3. **Menjalankan iotop dalam mod batch selama 10 iterasi dengan selang 2 saat:**
   ```bash
   iotop -b -n 10 -d 2
   ```

4. **Menyimpan output iotop ke dalam fail:**
   ```bash
   iotop -b -n 10 > output.txt
   ```

## Tips
- Gunakan pilihan `-o` untuk fokus pada proses yang sedang melakukan I/O, ini membantu dalam mengenal pasti masalah dengan lebih cepat.
- Jika anda ingin memantau sistem secara berterusan, pertimbangkan untuk menggunakan mod batch dengan output ke fail untuk analisis lebih lanjut.
- Pastikan anda menjalankan `iotop` dengan hak akses yang sesuai (biasanya sebagai root) untuk melihat semua proses.