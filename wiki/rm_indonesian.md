# [Linux] Bash rm Penggunaan: Menghapus file dan direktori

## Overview
Perintah `rm` digunakan dalam Bash untuk menghapus file dan direktori. Ini adalah alat yang sangat berguna, tetapi harus digunakan dengan hati-hati karena file yang dihapus tidak dapat dipulihkan dengan mudah.

## Usage
Berikut adalah sintaks dasar dari perintah `rm`:

```bash
rm [options] [arguments]
```

## Common Options
- `-f`: Menghapus file tanpa meminta konfirmasi, bahkan jika file tersebut tidak dapat dihapus.
- `-i`: Meminta konfirmasi sebelum menghapus setiap file.
- `-r`: Menghapus direktori dan semua isinya secara rekursif.
- `-v`: Menampilkan nama file yang sedang dihapus.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `rm`:

1. Menghapus file tunggal:
    ```bash
    rm file.txt
    ```

2. Menghapus beberapa file sekaligus:
    ```bash
    rm file1.txt file2.txt file3.txt
    ```

3. Menghapus direktori beserta isinya:
    ```bash
    rm -r direktori/
    ```

4. Menghapus file tanpa konfirmasi:
    ```bash
    rm -f file.txt
    ```

5. Menghapus file dengan konfirmasi:
    ```bash
    rm -i file.txt
    ```

## Tips
- Selalu periksa kembali nama file atau direktori yang akan dihapus untuk menghindari kehilangan data yang tidak disengaja.
- Gunakan opsi `-i` jika Anda tidak yakin untuk menghapus file, agar Anda dapat mengonfirmasi setiap tindakan.
- Pertimbangkan untuk menggunakan perintah `mv` untuk memindahkan file ke direktori sampah jika Anda ingin menghindari penghapusan permanen.