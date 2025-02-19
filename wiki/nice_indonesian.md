# [Sistem Operasi] C Shell (csh) nice Penggunaan: Mengatur Prioritas Proses

## Overview
Perintah `nice` digunakan dalam C Shell (csh) untuk mengatur prioritas eksekusi proses. Dengan menggunakan `nice`, pengguna dapat menentukan seberapa besar sumber daya CPU yang akan dialokasikan untuk proses tertentu, yang memungkinkan pengelolaan beban kerja yang lebih baik di sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `nice`:

```
nice [options] [arguments]
```

## Common Options
- `-n <nilai>`: Menentukan nilai nice yang ingin diterapkan. Nilai ini dapat berkisar antara -20 (prioritas tertinggi) hingga 19 (prioritas terendah).
- `-h`: Menampilkan pesan bantuan tentang penggunaan perintah `nice`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `nice`:

1. Menjalankan proses dengan prioritas lebih rendah:
   ```csh
   nice -n 10 ./programku
   ```

2. Menjalankan perintah `make` dengan prioritas lebih tinggi:
   ```csh
   nice -n -5 make
   ```

3. Menjalankan skrip shell dengan prioritas normal:
   ```csh
   nice ./script.sh
   ```

4. Menampilkan prioritas dari proses yang sedang berjalan:
   ```csh
   ps -o pid,nice,cmd
   ```

## Tips
- Gunakan nilai nice yang lebih rendah (misalnya, -10) untuk proses yang memerlukan lebih banyak sumber daya, seperti kompilasi atau rendering.
- Sebaiknya tidak menggunakan nilai nice yang terlalu tinggi (misalnya, 19) untuk proses penting, karena dapat memperlambat eksekusi.
- Periksa prioritas proses yang sedang berjalan secara berkala untuk memastikan sistem tetap responsif.