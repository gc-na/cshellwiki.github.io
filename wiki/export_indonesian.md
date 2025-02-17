# [Linux] Bash export Penggunaan: Mengatur Variabel Lingkungan

## Overview
Perintah `export` dalam Bash digunakan untuk menetapkan variabel lingkungan yang dapat diakses oleh proses anak yang dijalankan dari shell saat ini. Dengan menggunakan `export`, Anda dapat membuat variabel yang sebelumnya hanya tersedia di shell saat ini menjadi tersedia untuk program lain yang dijalankan dari shell tersebut.

## Usage
Berikut adalah sintaks dasar dari perintah `export`:

```bash
export [options] [arguments]
```

## Common Options
- `-n`: Menghapus variabel dari daftar variabel yang diekspor.
- `-p`: Menampilkan semua variabel yang diekspor saat ini.
- `VAR=value`: Menetapkan nilai untuk variabel dan mengekspornya sekaligus.

## Common Examples
Berikut adalah beberapa contoh penggunaan `export`:

1. Menetapkan dan mengekspor variabel:
   ```bash
   export MY_VAR="Hello World"
   ```

2. Menampilkan semua variabel yang diekspor:
   ```bash
   export -p
   ```

3. Menghapus variabel dari ekspor:
   ```bash
   export -n MY_VAR
   ```

4. Menetapkan dan mengekspor variabel dalam satu langkah:
   ```bash
   export PATH="$PATH:/usr/local/bin"
   ```

## Tips
- Selalu periksa variabel yang diekspor dengan `export -p` untuk memastikan bahwa variabel yang Anda butuhkan tersedia.
- Gunakan `unset VAR` untuk menghapus variabel jika Anda tidak lagi membutuhkannya.
- Pastikan untuk mengekspor variabel sebelum menjalankan program yang membutuhkannya agar program tersebut dapat mengakses nilai variabel tersebut.