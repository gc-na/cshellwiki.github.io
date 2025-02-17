# [Linux] Bash apt Penggunaan: Mengurus pakej perisian

## Overview
Perintah `apt` adalah alat pengurusan pakej untuk sistem pengendalian berasaskan Debian, seperti Ubuntu. Ia membolehkan pengguna untuk memasang, mengemas kini, dan mengalih keluar perisian dengan mudah.

## Usage
Sintaks asas untuk menggunakan `apt` adalah seperti berikut:

```bash
apt [options] [arguments]
```

## Common Options
- `install`: Memasang pakej baru.
- `remove`: Mengalih keluar pakej yang telah dipasang.
- `update`: Mengemas kini senarai pakej dari repositori.
- `upgrade`: Mengemas kini semua pakej yang telah dipasang kepada versi terbaru.
- `search`: Mencari pakej dalam repositori.

## Common Examples
1. **Mengemas kini senarai pakej:**
   ```bash
   sudo apt update
   ```

2. **Memasang pakej baru (contoh: `curl`):**
   ```bash
   sudo apt install curl
   ```

3. **Mengalih keluar pakej (contoh: `curl`):**
   ```bash
   sudo apt remove curl
   ```

4. **Mengemas kini semua pakej yang dipasang:**
   ```bash
   sudo apt upgrade
   ```

5. **Mencari pakej (contoh: `git`):**
   ```bash
   apt search git
   ```

## Tips
- Sentiasa jalankan `sudo apt update` sebelum memasang atau mengemas kini pakej untuk memastikan anda mempunyai senarai terkini.
- Gunakan `apt list --upgradable` untuk melihat pakej yang boleh dikemas kini sebelum menjalankan `apt upgrade`.
- Untuk menghapuskan pakej dan semua fail konfigurasi yang berkaitan, gunakan `apt purge [package_name]`.