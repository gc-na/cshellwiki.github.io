# [Linux] Bash mkdir Penggunaan: Membuat direktori baru

## Overview
Perintah `mkdir` digunakan untuk membuat direktori baru di sistem file. Ini adalah salah satu perintah dasar yang sering digunakan dalam manajemen file dan direktori di lingkungan Unix/Linux.

## Usage
Berikut adalah sintaks dasar dari perintah `mkdir`:

```
mkdir [options] [arguments]
```

## Common Options
- `-p`: Membuat direktori parent jika belum ada.
- `-m`: Menentukan mode izin untuk direktori yang dibuat.
- `-v`: Menampilkan pesan yang menjelaskan apa yang dilakukan perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mkdir`:

1. **Membuat direktori sederhana**:
   ```bash
   mkdir direktori_baru
   ```

2. **Membuat beberapa direktori sekaligus**:
   ```bash
   mkdir direktori1 direktori2 direktori3
   ```

3. **Membuat direktori beserta subdirektori**:
   ```bash
   mkdir -p direktori_utama/subdirektori
   ```

4. **Menentukan izin saat membuat direktori**:
   ```bash
   mkdir -m 755 direktori_dengan_izin
   ```

5. **Menampilkan pesan saat direktori dibuat**:
   ```bash
   mkdir -v direktori_dengan_pesan
   ```

## Tips
- Gunakan opsi `-p` untuk membuat struktur direktori yang kompleks tanpa harus membuat setiap direktori satu per satu.
- Selalu periksa izin direktori setelah membuatnya, terutama jika Anda menggunakan opsi `-m`.
- Jika Anda sering membuat direktori dengan nama yang sama, pertimbangkan untuk menggunakan skrip untuk mengotomatiskan proses tersebut.