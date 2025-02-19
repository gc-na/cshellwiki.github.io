# [Sistem Operasi] C Shell (csh) basename Penggunaan: Mengambil nama file tanpa path

## Overview
Perintah `basename` digunakan untuk mengambil nama file dari sebuah path lengkap, menghilangkan direktori dan ekstensi file jika diinginkan. Ini sangat berguna ketika Anda hanya ingin menampilkan nama file tanpa informasi tambahan tentang lokasi atau jenis file.

## Usage
Berikut adalah sintaks dasar dari perintah `basename`:

```csh
basename [options] [arguments]
```

## Common Options
- `-s, --suffix`: Menghapus sufiks tertentu dari nama file.
- `-a, --multiple`: Mengambil nama dari beberapa argumen sekaligus.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `basename`:

1. Mengambil nama file dari path lengkap:
    ```csh
    basename /home/user/documents/file.txt
    ```
    Output: `file.txt`

2. Mengambil nama file tanpa ekstensi:
    ```csh
    basename /home/user/documents/file.txt .txt
    ```
    Output: `file`

3. Mengambil nama dari beberapa file:
    ```csh
    basename -a /home/user/documents/file1.txt /home/user/documents/file2.txt
    ```
    Output:
    ```
    file1.txt
    file2.txt
    ```

4. Menghapus sufiks dari nama file:
    ```csh
    basename /home/user/documents/report.pdf .pdf
    ```
    Output: `report`

## Tips
- Gunakan `basename` dalam skrip untuk memproses nama file secara otomatis.
- Kombinasikan `basename` dengan perintah lain seperti `find` untuk mendapatkan nama file dari hasil pencarian.
- Pastikan untuk menyertakan ekstensi yang tepat saat menggunakan opsi `-s` untuk menghindari hasil yang tidak diinginkan.