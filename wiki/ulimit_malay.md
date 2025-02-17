# [Linux] Bash ulimit Penggunaan: Mengawal had sumber sistem

## Overview
Perintah `ulimit` dalam Bash digunakan untuk menetapkan atau memaparkan had sumber sistem yang boleh digunakan oleh proses yang dijalankan dalam shell. Ini termasuk had untuk memori, fail terbuka, dan banyak lagi, yang membantu dalam menguruskan penggunaan sumber dan mencegah satu proses daripada menggunakan semua sumber yang tersedia.

## Usage
Berikut adalah sintaks asas untuk perintah `ulimit`:

```bash
ulimit [options] [arguments]
```

## Common Options
- `-a`: Memaparkan semua had sumber yang sedia ada.
- `-c`: Menetapkan had saiz fail core.
- `-d`: Menetapkan had saiz segmen data.
- `-f`: Menetapkan had saiz fail maksimum.
- `-l`: Menetapkan had saiz fail yang boleh dikunci.
- `-n`: Menetapkan had bilangan fail terbuka.
- `-s`: Menetapkan had saiz stack.
- `-t`: Menetapkan had masa CPU maksimum.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `ulimit`:

1. **Memaparkan semua had sumber:**
   ```bash
   ulimit -a
   ```

2. **Menetapkan had maksimum bilangan fail terbuka kepada 1024:**
   ```bash
   ulimit -n 1024
   ```

3. **Menetapkan had saiz fail maksimum kepada 100MB:**
   ```bash
   ulimit -f 102400
   ```

4. **Menetapkan had saiz stack kepada 8MB:**
   ```bash
   ulimit -s 8192
   ```

5. **Menetapkan had saiz fail core kepada 0 (tidak membenarkan fail core):**
   ```bash
   ulimit -c 0
   ```

## Tips
- Sentiasa periksa had sumber semasa sebelum menjalankan aplikasi berat untuk memastikan ia tidak terhad oleh `ulimit`.
- Gunakan `ulimit -a` untuk mendapatkan gambaran keseluruhan tentang had sumber yang ada sebelum membuat perubahan.
- Jika anda perlu menetapkan had secara kekal, pertimbangkan untuk menambah perintah `ulimit` dalam fail konfigurasi shell seperti `.bashrc` atau `.bash_profile`.