# [Sistem Operasi] C Shell (csh) sha256sum Penggunaan: Menghitung checksum SHA-256

## Overview
Perintah `sha256sum` digunakan untuk menghitung dan memverifikasi checksum SHA-256 dari file. Ini berguna untuk memastikan integritas file dengan membandingkan checksum yang dihasilkan dengan checksum yang diketahui.

## Usage
Sintaks dasar dari perintah `sha256sum` adalah sebagai berikut:

```csh
sha256sum [options] [arguments]
```

## Common Options
- `-b`: Menghitung checksum untuk file biner.
- `-c`: Memeriksa checksum dari file yang telah dihitung sebelumnya.
- `-o`: Menentukan file output untuk menyimpan hasil checksum.
- `--help`: Menampilkan bantuan tentang penggunaan perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sha256sum`:

1. Menghitung checksum dari file:
   ```csh
   sha256sum file.txt
   ```

2. Menghitung checksum untuk file biner:
   ```csh
   sha256sum -b file.bin
   ```

3. Memeriksa checksum dari file menggunakan file daftar:
   ```csh
   sha256sum -c checksum.txt
   ```

4. Menyimpan hasil checksum ke dalam file:
   ```csh
   sha256sum file.txt -o hasil.txt
   ```

## Tips
- Selalu simpan checksum yang dihasilkan untuk referensi di masa mendatang.
- Gunakan opsi `-c` untuk memverifikasi file setelah diunduh atau dipindahkan.
- Pastikan untuk menggunakan file yang sesuai (biner atau teks) saat menghitung checksum untuk hasil yang akurat.