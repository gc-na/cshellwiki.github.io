# [Linux] Bash dnf Penggunaan: Pengurus pakej untuk sistem Linux

## Overview
Perintah `dnf` (Dandified YUM) adalah pengurus pakej untuk sistem operasi Linux yang menggunakan format RPM. Ia membolehkan pengguna untuk memasang, menghapus, dan mengurus pakej perisian dengan mudah.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `dnf`:

```bash
dnf [options] [arguments]
```

## Common Options
- `install`: Memasang pakej baru.
- `remove`: Menghapuskan pakej yang sedia ada.
- `update`: Mengemas kini pakej yang telah dipasang.
- `search`: Mencari pakej dalam repositori.
- `info`: Menunjukkan maklumat tentang pakeg tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan `dnf`:

1. **Memasang pakej baru**:
   ```bash
   dnf install nama-pakej
   ```

2. **Menghapuskan pakej**:
   ```bash
   dnf remove nama-pakej
   ```

3. **Mengemas kini semua pakej**:
   ```bash
   dnf update
   ```

4. **Mencari pakej**:
   ```bash
   dnf search nama-pakej
   ```

5. **Menunjukkan maklumat tentang pakej**:
   ```bash
   dnf info nama-pakej
   ```

## Tips
- Sentiasa gunakan `dnf update` secara berkala untuk memastikan sistem anda sentiasa terkini.
- Gunakan `dnf search` untuk mencari pakej yang mungkin tidak anda ingati nama penuhnya.
- Untuk melihat semua pilihan yang tersedia, anda boleh menggunakan `dnf --help`.