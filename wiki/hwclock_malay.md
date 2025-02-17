# [Linux] Bash hwclock Penggunaan: Mengurus jam sistem

## Overview
Perintah `hwclock` digunakan untuk mengakses dan mengurus jam perkakasan (hardware clock) pada sistem Linux. Ia membolehkan pengguna untuk membaca dan menetapkan waktu jam perkakasan, yang berfungsi secara berasingan daripada jam sistem operasi.

## Usage
Berikut adalah sintaks asas untuk perintah `hwclock`:

```bash
hwclock [options] [arguments]
```

## Common Options
- `--show`: Menunjukkan waktu semasa dari jam perkakasan.
- `--set`: Menetapkan waktu jam perkakasan kepada waktu yang ditentukan.
- `--hctosys`: Menetapkan waktu sistem berdasarkan waktu jam perkakasan.
- `--systohc`: Menetapkan waktu jam perkakasan berdasarkan waktu sistem.
- `--utc`: Menganggap waktu jam perkakasan dalam format UTC.

## Common Examples
1. **Menunjukkan waktu semasa dari jam perkakasan:**
   ```bash
   hwclock --show
   ```

2. **Menetapkan waktu jam perkakasan kepada waktu sistem semasa:**
   ```bash
   hwclock --systohc
   ```

3. **Menetapkan waktu sistem berdasarkan waktu jam perkakasan:**
   ```bash
   hwclock --hctosys
   ```

4. **Menetapkan waktu jam perkakasan kepada waktu tertentu:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

5. **Menunjukkan waktu jam perkakasan dalam format UTC:**
   ```bash
   hwclock --show --utc
   ```

## Tips
- Pastikan untuk menggunakan `--systohc` selepas mengubah waktu sistem untuk memastikan jam perkakasan sentiasa tepat.
- Gunakan `--utc` jika anda menjalankan sistem dual-boot dengan Windows untuk mengelakkan masalah dengan waktu.
- Sentiasa semak waktu jam perkakasan secara berkala untuk memastikan ketepatan waktu pada sistem anda.