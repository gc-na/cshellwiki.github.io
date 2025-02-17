# [Linux] Bash mount penggunaan: Menghubungkan sistem fail

## Overview
Perintah `mount` dalam Bash digunakan untuk menghubungkan sistem fail ke dalam struktur direktori yang sedia ada. Ini membolehkan pengguna mengakses fail dan direktori yang terdapat pada peranti penyimpanan seperti pemacu keras, pemacu USB, dan lain-lain.

## Usage
Berikut adalah sintaks asas untuk perintah `mount`:

```
mount [options] [arguments]
```

## Common Options
- `-t` : Menentukan jenis sistem fail (contohnya, ext4, ntfs).
- `-o` : Menyediakan pilihan tambahan seperti `ro` (read-only) atau `rw` (read-write).
- `-a` : Menghubungkan semua sistem fail yang dinyatakan dalam fail `/etc/fstab`.
- `-v` : Mengaktifkan mod verbose untuk menunjukkan maklumat lebih terperinci semasa proses penghubungan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `mount`:

1. **Menghubungkan sistem fail ext4 dari pemacu keras:**
   ```bash
   mount -t ext4 /dev/sda1 /mnt/mydrive
   ```

2. **Menghubungkan pemacu USB secara read-only:**
   ```bash
   mount -o ro /dev/sdb1 /mnt/usb
   ```

3. **Menghubungkan semua sistem fail yang dinyatakan dalam fstab:**
   ```bash
   mount -a
   ```

4. **Menghubungkan sistem fail NTFS dari pemacu USB:**
   ```bash
   mount -t ntfs-3g /dev/sdc1 /mnt/usbdrive
   ```

## Tips
- Pastikan anda mempunyai hak akses yang diperlukan untuk menghubungkan sistem fail, biasanya anda memerlukan akses root.
- Sentiasa semak titik pemasangan sebelum menghubungkan untuk mengelakkan kehilangan data.
- Gunakan pilihan `-v` untuk mendapatkan maklumat lebih lanjut jika anda menghadapi masalah semasa menghubungkan.