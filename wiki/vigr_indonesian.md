# [Linux] Bash vigr Penggunaan: Mengedit file konfigurasi sistem

## Overview
Perintah `vigr` digunakan untuk mengedit file konfigurasi sistem, khususnya file `/etc/passwd` dan `/etc/group`, dengan cara yang aman. Perintah ini membuka editor teks yang ditentukan dalam variabel lingkungan `EDITOR`, dan melakukan pemeriksaan sintaksis sebelum menyimpan perubahan, sehingga membantu mencegah kesalahan yang dapat merusak sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `vigr`:

```
vigr [options] [arguments]
```

## Common Options
- `-h`, `--help`: Menampilkan bantuan dan informasi tentang penggunaan perintah.
- `-s`, `--safe`: Mengaktifkan mode aman yang memeriksa kesalahan sintaksis sebelum menyimpan file.
- `-f`, `--file`: Menentukan file yang akan diedit (default adalah `/etc/passwd`).

## Common Examples
Berikut adalah beberapa contoh penggunaan `vigr`:

1. **Mengedit file passwd**:
   ```bash
   vigr
   ```

2. **Mengedit file group**:
   ```bash
   vigr /etc/group
   ```

3. **Menggunakan mode aman**:
   ```bash
   vigr -s
   ```

4. **Menentukan editor yang berbeda**:
   ```bash
   EDITOR=nano vigr
   ```

## Tips
- Selalu gunakan `vigr` untuk mengedit file konfigurasi sistem daripada editor teks biasa, karena `vigr` melakukan pemeriksaan kesalahan.
- Pastikan untuk memahami struktur file yang sedang diedit untuk menghindari kesalahan yang dapat menyebabkan masalah pada sistem.
- Jika Anda tidak yakin, gunakan opsi `-s` untuk memastikan tidak ada kesalahan sintaksis sebelum menyimpan perubahan.