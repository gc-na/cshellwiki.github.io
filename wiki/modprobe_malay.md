# [Linux] Bash modprobe penggunaan: Mengurus modul kernel

## Overview
Perintah `modprobe` digunakan untuk memuat dan mengeluarkan modul kernel dalam sistem Linux. Modul ini adalah komponen yang boleh dimuatkan secara dinamik ke dalam kernel untuk memberikan sokongan bagi perkakasan atau fungsi tertentu.

## Usage
Sintaks asas untuk perintah `modprobe` adalah seperti berikut:

```
modprobe [options] [arguments]
```

## Common Options
- `-r` : Mengeluarkan modul dari kernel.
- `-n` : Menunjukkan apa yang akan dilakukan tanpa melaksanakannya.
- `-v` : Menunjukkan maklumat lebih terperinci semasa pelaksanaan.
- `--show-depends` : Menunjukkan kebergantungan modul yang diperlukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `modprobe`:

1. **Memuatkan modul**:
   ```bash
   modprobe nama_modul
   ```

2. **Mengeluarkan modul**:
   ```bash
   modprobe -r nama_modul
   ```

3. **Menunjukkan kebergantungan modul**:
   ```bash
   modprobe --show-depends nama_modul
   ```

4. **Menjalankan modprobe dalam mod simulasi**:
   ```bash
   modprobe -n nama_modul
   ```

5. **Menunjukkan maklumat terperinci semasa memuatkan**:
   ```bash
   modprobe -v nama_modul
   ```

## Tips
- Sentiasa semak kebergantungan modul sebelum memuatkan modul baru untuk mengelakkan masalah.
- Gunakan pilihan `-v` untuk mendapatkan maklumat tambahan yang berguna semasa debug.
- Pastikan anda mempunyai hak akses yang diperlukan untuk memuat dan mengeluarkan modul kernel.