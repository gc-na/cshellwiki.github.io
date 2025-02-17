# [Linux] Bash e2fsck Penggunaan: Memeriksa dan membaiki sistem fail ext2/ext3/ext4

## Overview
Perintah `e2fsck` digunakan untuk memeriksa dan membaiki sistem fail yang menggunakan format ext2, ext3, atau ext4. Ia adalah alat penting untuk memastikan integriti data dan mengatasi masalah yang mungkin timbul dalam sistem fail.

## Usage
Sintaks asas untuk menggunakan perintah `e2fsck` adalah seperti berikut:

```bash
e2fsck [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `e2fsck` beserta penjelasannya:

- `-p`: Memeriksa sistem fail secara automatik dan membaiki kesilapan tanpa meminta pengesahan.
- `-f`: Memaksa pemeriksaan walaupun sistem fail kelihatan bersih.
- `-n`: Melakukan pemeriksaan tanpa membaiki sebarang kesilapan.
- `-y`: Menganggap "ya" untuk semua soalan semasa pemeriksaan dan pembaikan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `e2fsck`:

1. Memeriksa sistem fail tanpa membaiki:
    ```bash
    e2fsck /dev/sda1
    ```

2. Memeriksa dan membaiki sistem fail secara automatik:
    ```bash
    e2fsck -p /dev/sda1
    ```

3. Memaksa pemeriksaan walaupun sistem fail kelihatan bersih:
    ```bash
    e2fsck -f /dev/sda1
    ```

4. Melakukan pemeriksaan tanpa membaiki:
    ```bash
    e2fsck -n /dev/sda1
    ```

5. Menganggap "ya" untuk semua soalan semasa pemeriksaan:
    ```bash
    e2fsck -y /dev/sda1
    ```

## Tips
- Sentiasa lakukan sandaran data penting sebelum menjalankan `e2fsck`, terutama jika anda merancang untuk membaiki sistem fail.
- Gunakan pilihan `-n` untuk melakukan pemeriksaan tanpa risiko membaiki kesilapan secara tidak sengaja.
- Jalankan `e2fsck` semasa sistem tidak aktif (offline) untuk mengelakkan kerosakan data.