# [Linux] Bash yum Penggunaan: Mengurus pakej perisian

## Overview
Perintah `yum` (Yellowdog Updater Modified) adalah alat pengurusan pakej untuk sistem operasi berasaskan RPM, seperti CentOS dan Fedora. Ia membolehkan pengguna untuk memasang, mengemas kini, dan menghapuskan perisian dengan mudah dari repositori dalam talian.

## Usage
Sintaks asas untuk menggunakan perintah `yum` adalah seperti berikut:

```bash
yum [options] [arguments]
```

## Common Options
- `install`: Memasang pakej baru.
- `remove`: Menghapuskan pakej yang sedia ada.
- `update`: Mengemas kini pakej yang telah dipasang.
- `list`: Menyenaraikan pakej yang tersedia atau yang telah dipasang.
- `search`: Mencari pakej berdasarkan nama atau keterangan.

## Common Examples
1. **Memasang pakej**:
   ```bash
   yum install nama-pakej
   ```

2. **Menghapuskan pakej**:
   ```bash
   yum remove nama-pakej
   ```

3. **Mengemas kini semua pakej**:
   ```bash
   yum update
   ```

4. **Menyenaraikan semua pakej yang dipasang**:
   ```bash
   yum list installed
   ```

5. **Mencari pakej tertentu**:
   ```bash
   yum search nama-pakej
   ```

## Tips
- Sentiasa kemas kini repositori sebelum memasang atau mengemas kini pakej dengan menggunakan `yum update`.
- Gunakan `yum clean all` untuk membersihkan cache dan ruang yang tidak diperlukan.
- Periksa kebergantungan pakej sebelum memasang untuk mengelakkan masalah dengan sistem anda.