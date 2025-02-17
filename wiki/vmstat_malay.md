# [Linux] Bash vmstat Penggunaan: Memantau Statistik Sistem

## Overview
Perintah `vmstat` digunakan untuk memantau statistik sistem, termasuk penggunaan memori, proses, dan aktiviti I/O. Ia memberikan gambaran keseluruhan tentang keadaan sistem dalam bentuk yang mudah dibaca.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `vmstat`:

```bash
vmstat [options] [arguments]
```

## Common Options
- `-a`: Menunjukkan statistik memori yang lebih terperinci.
- `-m`: Menunjukkan statistik memori untuk cache dan buffer.
- `-s`: Menunjukkan statistik sistem dalam format yang lebih ringkas.
- `-t`: Menunjukkan cap waktu untuk setiap baris output.

## Common Examples
Berikut adalah beberapa contoh penggunaan `vmstat`:

1. **Menampilkan statistik sistem secara ringkas:**
   ```bash
   vmstat
   ```

2. **Menunjukkan statistik dengan interval 2 saat:**
   ```bash
   vmstat 2
   ```

3. **Menunjukkan statistik memori terperinci:**
   ```bash
   vmstat -a
   ```

4. **Menunjukkan statistik sistem dengan cap waktu:**
   ```bash
   vmstat -t
   ```

## Tips
- Gunakan `vmstat` bersama dengan perintah lain seperti `top` untuk mendapatkan gambaran yang lebih lengkap tentang prestasi sistem.
- Perhatikan nilai `si` dan `so` dalam output, yang menunjukkan pertukaran memori. Nilai yang tinggi mungkin menunjukkan masalah dengan memori.
- Jalankan `vmstat` dalam jangka masa yang lebih lama untuk memantau perubahan dalam prestasi sistem secara berterusan.