# [Linux] Bash lvs Penggunaan: Menampilkan informasi tentang logical volumes

## Overview
Perintah `lvs` digunakan untuk menampilkan informasi tentang logical volumes dalam sistem manajemen volume logis (LVM). Dengan menggunakan perintah ini, pengguna dapat melihat detail mengenai logical volumes yang ada, termasuk ukuran, status, dan atribut lainnya.

## Usage
Berikut adalah sintaks dasar untuk menggunakan perintah `lvs`:

```bash
lvs [options] [arguments]
```

## Common Options
- `-o` : Menentukan kolom yang ingin ditampilkan.
- `-a` : Menampilkan semua logical volumes, termasuk yang tidak aktif.
- `-n` : Menampilkan nama logical volume saja.
- `--units` : Menentukan satuan ukuran yang ingin ditampilkan (misalnya, kB, MB, GB).

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `lvs`:

1. **Menampilkan semua logical volumes:**
   ```bash
   lvs
   ```

2. **Menampilkan informasi dengan kolom tertentu:**
   ```bash
   lvs -o +devices
   ```

3. **Menampilkan semua logical volumes, termasuk yang tidak aktif:**
   ```bash
   lvs -a
   ```

4. **Menampilkan nama logical volume:**
   ```bash
   lvs -n
   ```

5. **Menampilkan informasi dengan satuan GB:**
   ```bash
   lvs --units g
   ```

## Tips
- Gunakan opsi `-o` untuk menyesuaikan informasi yang ditampilkan sesuai kebutuhan Anda.
- Kombinasikan `lvs` dengan perintah lain seperti `grep` untuk memfilter hasil yang ditampilkan.
- Selalu periksa status logical volumes secara berkala untuk memastikan sistem berfungsi dengan baik.