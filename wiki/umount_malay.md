# [Linux] Bash umount Penggunaan: Menanggalkan sistem fail

## Overview
Perintah `umount` digunakan untuk menanggalkan sistem fail yang telah dipasang (mounted) dalam sistem Linux. Ini penting untuk memastikan bahawa semua data ditulis dengan betul dan untuk mengelakkan kerosakan data sebelum mematikan peranti penyimpanan atau memindahkannya.

## Usage
Berikut adalah sintaks asas untuk perintah `umount`:

```
umount [options] [arguments]
```

## Common Options
- `-a`: Menanggalkan semua sistem fail yang terdapat dalam `/etc/mtab`.
- `-r`: Menanggalkan sistem fail secara read-only jika gagal untuk menanggalkan secara biasa.
- `-f`: Memaksa penangguhan sistem fail walaupun terdapat kesalahan.
- `-l`: Menangguhkan sistem fail secara "lazy", yang membolehkan proses lain terus menggunakan sistem fail sehingga ia benar-benar ditanggalkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `umount`:

1. Menanggalkan sistem fail yang dipasang pada `/mnt/usb`:
   ```bash
   umount /mnt/usb
   ```

2. Menanggalkan semua sistem fail yang terdapat dalam `/etc/mtab`:
   ```bash
   umount -a
   ```

3. Memaksa penangguhan sistem fail yang dipasang pada `/dev/sdb1`:
   ```bash
   umount -f /dev/sdb1
   ```

4. Menangguhkan sistem fail secara "lazy":
   ```bash
   umount -l /mnt/data
   ```

## Tips
- Pastikan tiada proses yang sedang menggunakan sistem fail sebelum menanggalkannya untuk mengelakkan kehilangan data.
- Gunakan pilihan `-l` jika anda ingin menanggalkan sistem fail tetapi masih memerlukan akses ke dalamnya sehingga proses selesai.
- Sentiasa periksa status sistem fail dengan `mount` selepas menggunakan `umount` untuk memastikan ia telah ditanggalkan dengan betul.