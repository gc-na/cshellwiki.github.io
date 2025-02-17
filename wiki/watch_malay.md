# [Linux] Bash watch penggunaan: Memantau perintah secara berkala

## Overview
Perintah `watch` dalam Bash digunakan untuk menjalankan perintah tertentu secara berkala dan memaparkan hasilnya di terminal. Ini sangat berguna untuk memantau perubahan dalam output perintah tanpa perlu menjalankannya secara manual setiap kali.

## Usage
Sintaks asas untuk perintah `watch` adalah seperti berikut:

```bash
watch [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `watch` beserta penjelasan ringkas:

- `-n <seconds>`: Menentukan selang waktu dalam saat untuk menjalankan perintah. Defaultnya adalah 2 saat.
- `-d`: Menyoroti perubahan dalam output antara setiap pengulangan.
- `-t`: Menyembunyikan header yang menunjukkan perintah yang sedang dijalankan.
- `-x`: Menjalankan perintah dengan argumen yang diberikan.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `watch`:

1. **Memantau penggunaan CPU**:
   ```bash
   watch -n 1 mpstat
   ```
   Ini akan menjalankan perintah `mpstat` setiap saat untuk memantau penggunaan CPU.

2. **Memantau direktori untuk perubahan**:
   ```bash
   watch -d ls -l /path/to/directory
   ```
   Ini akan menunjukkan senarai fail dalam direktori tertentu dan menyoroti sebarang perubahan.

3. **Memantau penggunaan memori**:
   ```bash
   watch free -h
   ```
   Ini akan memaparkan penggunaan memori sistem secara berkala.

4. **Memantau status perkhidmatan**:
   ```bash
   watch systemctl status apache2
   ```
   Ini akan memaparkan status perkhidmatan Apache secara berkala.

## Tips
- Gunakan pilihan `-d` untuk lebih mudah melihat perubahan dalam output.
- Sesuaikan selang waktu dengan pilihan `-n` untuk mengelakkan terlalu banyak output yang tidak perlu.
- Jika anda ingin menghentikan perintah `watch`, tekan `Ctrl+C`.