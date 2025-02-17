# [Linux] Bash update-rc.d: [mengurus skrip permulaan]

## Overview
Perintah `update-rc.d` digunakan untuk mengurus skrip permulaan (init scripts) pada sistem Linux. Ia membolehkan pengguna untuk menambah, menghapus, atau mengubah cara skrip permulaan dijalankan semasa proses boot.

## Usage
Berikut adalah sintaks asas bagi perintah `update-rc.d`:

```bash
update-rc.d [options] [arguments]
```

## Common Options
- `defaults`: Menambah skrip permulaan dengan tetapan lalai.
- `remove`: Menghapus skrip permulaan dari sistem.
- `enable`: Mengaktifkan skrip permulaan untuk dijalankan semasa boot.
- `disable`: Menonaktifkan skrip permulaan dari dijalankan semasa boot.

## Common Examples
1. **Menambah skrip permulaan dengan tetapan lalai:**
   ```bash
   update-rc.d myscript defaults
   ```

2. **Menghapus skrip permulaan:**
   ```bash
   update-rc.d myscript remove
   ```

3. **Mengaktifkan skrip permulaan:**
   ```bash
   update-rc.d myscript enable
   ```

4. **Menonaktifkan skrip permulaan:**
   ```bash
   update-rc.d myscript disable
   ```

## Tips
- Sentiasa pastikan anda mempunyai hak akses yang mencukupi (biasanya sebagai root) untuk menggunakan perintah ini.
- Semak skrip permulaan anda sebelum menambah atau mengubahnya untuk mengelakkan masalah semasa boot.
- Gunakan `update-rc.d -n` untuk melakukan ujian tanpa membuat sebarang perubahan pada sistem.