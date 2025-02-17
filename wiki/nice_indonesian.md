# [Linux] Bash nice Penggunaan: Mengatur Prioritas Proses

## Overview
Perintah `nice` digunakan untuk mengatur prioritas eksekusi proses di sistem operasi berbasis Unix. Dengan menggunakan `nice`, pengguna dapat menentukan seberapa besar sumber daya CPU yang akan diberikan kepada proses tertentu, yang berguna untuk menghindari penggunaan CPU yang berlebihan oleh proses tertentu.

## Usage
Sintaks dasar dari perintah `nice` adalah sebagai berikut:

```bash
nice [options] [command]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `nice`:

- `-n, --adjustment=N`: Menentukan nilai prioritas yang ingin diterapkan, di mana N adalah angka dari -20 (prioritas tertinggi) hingga 19 (prioritas terendah).
- `-h, --help`: Menampilkan bantuan penggunaan perintah `nice`.
- `--version`: Menampilkan versi dari perintah `nice`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `nice`:

1. Menjalankan perintah `sleep` dengan prioritas default:
   ```bash
   nice sleep 10
   ```

2. Menjalankan perintah `gzip` dengan prioritas yang lebih rendah (nilai 10):
   ```bash
   nice -n 10 gzip file.txt
   ```

3. Menjalankan perintah `make` dengan prioritas yang lebih tinggi (nilai -5):
   ```bash
   nice -n -5 make
   ```

4. Menjalankan skrip dengan prioritas yang ditentukan:
   ```bash
   nice -n 15 ./script.sh
   ```

## Tips
- Gunakan nilai prioritas negatif untuk memberikan lebih banyak sumber daya CPU kepada proses penting.
- Sebaiknya gunakan `nice` untuk proses yang tidak mendesak agar tidak mengganggu proses lain yang lebih penting.
- Periksa prioritas proses yang sedang berjalan dengan menggunakan perintah `ps` atau `top` untuk memastikan pengaturan prioritas yang tepat.