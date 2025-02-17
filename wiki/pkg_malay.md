# [Linux] Bash pkg Penggunaan: Mengurus pakej perisian

## Overview
Perintah `pkg` digunakan untuk mengurus pakej perisian dalam sistem operasi yang berasaskan Unix, khususnya dalam FreeBSD. Ia membolehkan pengguna untuk memasang, mengemas kini, dan menghapuskan pakej perisian dengan mudah.

## Usage
Sintaks asas untuk menggunakan perintah `pkg` adalah seperti berikut:

```bash
pkg [options] [arguments]
```

## Common Options
- `install`: Memasang pakej baru.
- `remove`: Menghapuskan pakej yang sedia ada.
- `update`: Mengemas kini senarai pakej yang tersedia.
- `upgrade`: Mengemas kini semua pakej yang telah dipasang.
- `search`: Mencari pakej dalam repositori.

## Common Examples
1. **Memasang pakej baru**
   ```bash
   pkg install nama-pakej
   ```

2. **Menghapuskan pakej**
   ```bash
   pkg remove nama-pakej
   ```

3. **Mengemas kini senarai pakej**
   ```bash
   pkg update
   ```

4. **Mengemas kini semua pakej**
   ```bash
   pkg upgrade
   ```

5. **Mencari pakej**
   ```bash
   pkg search nama-pakej
   ```

## Tips
- Sentiasa jalankan `pkg update` sebelum memasang atau mengemas kini pakej untuk memastikan anda mempunyai senarai terkini.
- Gunakan `pkg info` untuk mendapatkan maklumat terperinci tentang pakej yang telah dipasang.
- Untuk mengelakkan konflik, pastikan untuk menghapuskan pakej yang tidak diperlukan sebelum memasang yang baru.