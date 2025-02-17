# [Linux] Bash systemctl Penggunaan: Mengurus perkhidmatan sistem

## Overview
Perintah `systemctl` adalah alat yang digunakan untuk mengurus dan mengawal perkhidmatan (services) dalam sistem Linux yang menggunakan systemd sebagai pengurus sistem. Ia membolehkan pengguna untuk memulakan, menghentikan, menghidupkan semula, dan memeriksa status perkhidmatan.

## Usage
Berikut adalah sintaks asas bagi perintah `systemctl`:

```bash
systemctl [options] [arguments]
```

## Common Options
- `start`: Memulakan perkhidmatan.
- `stop`: Menghentikan perkhidmatan.
- `restart`: Menghidupkan semula perkhidmatan.
- `status`: Menunjukkan status semasa perkhidmatan.
- `enable`: Mengaktifkan perkhidmatan untuk dimulakan secara automatik semasa boot.
- `disable`: Menonaktifkan perkhidmatan dari dimulakan secara automatik semasa boot.

## Common Examples
Berikut adalah beberapa contoh penggunaan `systemctl`:

1. **Memulakan perkhidmatan**
   ```bash
   systemctl start nama_perkhidmatan
   ```

2. **Menghentikan perkhidmatan**
   ```bash
   systemctl stop nama_perkhidmatan
   ```

3. **Menghidupkan semula perkhidmatan**
   ```bash
   systemctl restart nama_perkhidmatan
   ```

4. **Memeriksa status perkhidmatan**
   ```bash
   systemctl status nama_perkhidmatan
   ```

5. **Mengaktifkan perkhidmatan untuk dimulakan secara automatik**
   ```bash
   systemctl enable nama_perkhidmatan
   ```

6. **Menonaktifkan perkhidmatan dari dimulakan secara automatik**
   ```bash
   systemctl disable nama_perkhidmatan
   ```

## Tips
- Sentiasa periksa status perkhidmatan selepas melakukan tindakan untuk memastikan ia berfungsi seperti yang diharapkan.
- Gunakan `systemctl list-units --type=service` untuk melihat senarai semua perkhidmatan yang sedang berjalan.
- Untuk mendapatkan maklumat lebih lanjut tentang perkhidmatan tertentu, gunakan `systemctl show nama_perkhidmatan`.