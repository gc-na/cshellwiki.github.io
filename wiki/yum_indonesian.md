# [Sistem Operasi] C Shell (csh) yum: Mengelola paket perangkat lunak

## Overview
Perintah `yum` (Yellowdog Updater Modified) adalah alat manajemen paket yang digunakan pada sistem berbasis RPM (Red Hat Package Manager). Dengan `yum`, pengguna dapat menginstal, memperbarui, dan menghapus paket perangkat lunak dengan mudah.

## Usage
Berikut adalah sintaks dasar untuk menggunakan perintah `yum`:

```
yum [options] [arguments]
```

## Common Options
- `install`: Menginstal paket baru.
- `remove`: Menghapus paket yang sudah terinstal.
- `update`: Memperbarui paket yang sudah terinstal ke versi terbaru.
- `list`: Menampilkan daftar paket yang tersedia atau yang sudah terinstal.
- `search`: Mencari paket berdasarkan nama atau deskripsi.

## Common Examples
Berikut adalah beberapa contoh penggunaan `yum`:

1. **Menginstal paket baru**:
   ```bash
   yum install nama_paket
   ```

2. **Menghapus paket**:
   ```bash
   yum remove nama_paket
   ```

3. **Memperbarui semua paket**:
   ```bash
   yum update
   ```

4. **Menampilkan daftar paket yang terinstal**:
   ```bash
   yum list installed
   ```

5. **Mencari paket tertentu**:
   ```bash
   yum search nama_paket
   ```

## Tips
- Selalu perbarui repositori sebelum menginstal atau memperbarui paket dengan menggunakan `yum update`.
- Gunakan `yum clean all` untuk membersihkan cache dan menghemat ruang disk.
- Periksa dependensi paket sebelum menginstal untuk menghindari masalah di kemudian hari.