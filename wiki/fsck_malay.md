# [Linux] Bash fsck Penggunaan: Memeriksa dan membetulkan sistem fail

## Overview
Perintah `fsck` (file system check) digunakan untuk memeriksa dan membetulkan kesilapan dalam sistem fail pada sistem operasi Linux. Ia membantu memastikan integriti dan kestabilan sistem fail, yang penting untuk mengelakkan kehilangan data.

## Usage
Sintaks asas untuk menggunakan perintah `fsck` adalah seperti berikut:

```bash
fsck [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan `fsck`:

- `-a` : Membetulkan kesilapan secara automatik tanpa meminta pengesahan.
- `-n` : Melakukan pemeriksaan tanpa membetulkan kesilapan.
- `-y` : Menganggap jawapan "ya" untuk semua pertanyaan semasa proses pembetulan.
- `-t` : Menunjukkan masa yang diambil untuk setiap sistem fail yang diperiksa.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `fsck`:

1. Memeriksa sistem fail pada partisi tertentu:
   ```bash
   fsck /dev/sda1
   ```

2. Membetulkan kesilapan secara automatik:
   ```bash
   fsck -a /dev/sda1
   ```

3. Melakukan pemeriksaan tanpa membetulkan kesilapan:
   ```bash
   fsck -n /dev/sda1
   ```

4. Menganggap "ya" untuk semua pertanyaan semasa pembetulan:
   ```bash
   fsck -y /dev/sda1
   ```

## Tips
- Sentiasa pastikan anda mempunyai salinan sandaran data penting sebelum menjalankan `fsck`, terutamanya jika anda menggunakan pilihan yang membetulkan kesilapan.
- Jalankan `fsck` pada sistem fail yang tidak sedang digunakan, biasanya dalam mod pemulihan atau dari Live CD/USB.
- Periksa dokumentasi sistem fail yang anda gunakan untuk memahami lebih lanjut tentang kesilapan yang mungkin berlaku dan cara terbaik untuk menanganinya.