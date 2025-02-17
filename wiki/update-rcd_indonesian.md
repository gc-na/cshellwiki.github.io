# [Linux] Bash update-rc.d: [mengelola skrip inisialisasi]

## Overview
Perintah `update-rc.d` digunakan untuk mengelola skrip inisialisasi di sistem Linux. Perintah ini memungkinkan pengguna untuk menambahkan, menghapus, atau mengubah prioritas skrip yang dijalankan saat booting.

## Usage
Berikut adalah sintaks dasar dari perintah `update-rc.d`:

```bash
update-rc.d [options] [arguments]
```

## Common Options
- `defaults`: Menambahkan skrip dengan prioritas default.
- `remove`: Menghapus skrip dari direktori inisialisasi.
- `enable`: Mengaktifkan skrip untuk dijalankan saat boot.
- `disable`: Menonaktifkan skrip agar tidak dijalankan saat boot.
- `start <N>`: Menentukan urutan saat skrip dijalankan pada saat boot.
- `stop <N>`: Menentukan urutan saat skrip dihentikan pada saat shutdown.

## Common Examples
1. **Menambahkan skrip dengan prioritas default:**
   ```bash
   sudo update-rc.d myscript defaults
   ```

2. **Menghapus skrip dari direktori inisialisasi:**
   ```bash
   sudo update-rc.d myscript remove
   ```

3. **Mengaktifkan skrip untuk dijalankan saat boot:**
   ```bash
   sudo update-rc.d myscript enable
   ```

4. **Menonaktifkan skrip agar tidak dijalankan saat boot:**
   ```bash
   sudo update-rc.d myscript disable
   ```

5. **Menentukan urutan saat skrip dijalankan:**
   ```bash
   sudo update-rc.d myscript start 20 2 3 4 5 .
   ```

## Tips
- Pastikan untuk menjalankan perintah ini dengan hak akses superuser (`sudo`) agar dapat mengubah skrip inisialisasi.
- Selalu periksa apakah skrip yang akan ditambahkan sudah sesuai dengan standar dan dapat dijalankan tanpa error.
- Gunakan opsi `remove` dengan hati-hati, karena ini akan menghapus skrip dari semua runlevel.