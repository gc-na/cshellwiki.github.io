# [Linux] Bash dmesg Penggunaan: Memaparkan mesej kernel

## Overview
Perintah `dmesg` digunakan untuk memaparkan mesej log kernel yang berkaitan dengan pelbagai peristiwa sistem, termasuk pengesanan perkakasan, pemulaan sistem, dan ralat. Ia sangat berguna untuk penyelesaian masalah dan pemantauan sistem.

## Usage
Sintaks asas bagi perintah `dmesg` adalah seperti berikut:

```bash
dmesg [options] [arguments]
```

## Common Options
- `-C` : Mengosongkan buffer log kernel.
- `-c` : Memaparkan mesej dan kemudian mengosongkan buffer.
- `-n level` : Mengubah tahap keamatan mesej yang akan dipaparkan.
- `-T` : Menunjukkan timestamp dalam format yang lebih mesra pengguna.
- `--help` : Memaparkan bantuan untuk perintah dmesg.

## Common Examples
Berikut adalah beberapa contoh penggunaan `dmesg`:

1. **Memaparkan semua mesej log kernel:**
   ```bash
   dmesg
   ```

2. **Memaparkan mesej log kernel dengan timestamp:**
   ```bash
   dmesg -T
   ```

3. **Mengosongkan buffer log kernel selepas memaparkan mesej:**
   ```bash
   dmesg -c
   ```

4. **Mengubah tahap keamatan mesej yang dipaparkan:**
   ```bash
   dmesg -n 1
   ```

5. **Mengosongkan buffer log kernel:**
   ```bash
   dmesg -C
   ```

## Tips
- Gunakan `dmesg | less` untuk menatal melalui mesej log yang panjang dengan lebih mudah.
- Untuk mencari mesej tertentu, anda boleh menggunakan `grep`. Contohnya, untuk mencari mesej berkaitan dengan USB:
  ```bash
  dmesg | grep usb
  ```
- Sentiasa periksa mesej log selepas melakukan perubahan pada sistem, seperti memasang perkakasan baru, untuk memastikan semuanya berfungsi dengan baik.