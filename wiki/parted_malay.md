# [Linux] Bash parted Penggunaan: Mengurus partition cakera

## Overview
Perintah `parted` digunakan untuk mengurus partition pada cakera keras. Ia membolehkan pengguna untuk membuat, mengubah, dan menghapus partition dengan mudah. `parted` menyokong pelbagai sistem fail dan memberikan kawalan yang lebih baik berbanding alat lain.

## Usage
Berikut adalah sintaks asas untuk menggunakan `parted`:

```bash
parted [options] [arguments]
```

## Common Options
- `-l`, `--list`: Menunjukkan senarai semua peranti dan partition.
- `-s`, `--script`: Menjalankan dalam mod skrip tanpa interaksi pengguna.
- `mkpart`: Membuat partition baru.
- `rm`: Menghapus partition.
- `resizepart`: Mengubah saiz partition yang sedia ada.

## Common Examples
Berikut adalah beberapa contoh penggunaan `parted`:

1. **Menunjukkan senarai partition**:
   ```bash
   parted -l
   ```

2. **Membuat partition baru**:
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Menghapus partition**:
   ```bash
   parted /dev/sda rm 1
   ```

4. **Mengubah saiz partition**:
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

## Tips
- Sentiasa buat salinan data penting sebelum mengubah partition.
- Gunakan `--script` jika anda menjalankan `parted` dalam skrip untuk mengelakkan prompt interaksi.
- Periksa semula saiz dan jenis partition sebelum menyimpan perubahan untuk mengelakkan kehilangan data.