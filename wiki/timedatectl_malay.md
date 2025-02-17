# [Linux] Bash timedatectl Penggunaan: Mengurus waktu dan tarikh sistem

## Overview
Perintah `timedatectl` digunakan untuk mengurus dan mengkonfigurasi waktu serta tarikh pada sistem Linux. Ia membolehkan pengguna untuk melihat dan mengubah seting waktu, zon waktu, serta status penyelarasan waktu rangkaian.

## Usage
Berikut adalah sintaks asas untuk perintah `timedatectl`:

```bash
timedatectl [options] [arguments]
```

## Common Options
- `status`: Menunjukkan status waktu dan tarikh semasa.
- `set-time`: Mengubah waktu sistem kepada waktu yang ditentukan.
- `set-timezone`: Mengubah zon waktu sistem.
- `set-ntp`: Menghidupkan atau mematikan penyelarasan waktu rangkaian.
- `list-timezones`: Menyenaraikan semua zon waktu yang tersedia.

## Common Examples
1. **Menunjukkan status waktu dan tarikh semasa:**
   ```bash
   timedatectl status
   ```

2. **Mengubah waktu sistem kepada 15:30 pada 1 Januari 2023:**
   ```bash
   timedatectl set-time '2023-01-01 15:30:00'
   ```

3. **Mengubah zon waktu kepada Asia/Kuala_Lumpur:**
   ```bash
   timedatectl set-timezone Asia/Kuala_Lumpur
   ```

4. **Menghidupkan penyelarasan waktu rangkaian:**
   ```bash
   timedatectl set-ntp true
   ```

5. **Menyenaraikan semua zon waktu yang tersedia:**
   ```bash
   timedatectl list-timezones
   ```

## Tips
- Pastikan anda mempunyai hak akses yang mencukupi (biasanya sebagai root) untuk mengubah waktu dan zon waktu.
- Gunakan `timedatectl list-timezones` untuk mencari zon waktu yang tepat sebelum mengubahnya.
- Selalu semak status waktu selepas melakukan perubahan untuk memastikan ia telah diterapkan dengan betul.