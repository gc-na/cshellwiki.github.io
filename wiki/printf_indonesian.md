# [Linux] Bash printf Penggunaan: Menampilkan format teks

## Overview
Perintah `printf` dalam Bash digunakan untuk mencetak teks ke terminal dengan format yang ditentukan. Ini mirip dengan fungsi `printf` di bahasa pemrograman lain, memungkinkan pengguna untuk mengontrol bagaimana data ditampilkan.

## Usage
Berikut adalah sintaks dasar dari perintah `printf`:

```bash
printf [options] [arguments]
```

## Common Options
- `-v var`: Menyimpan output ke dalam variabel yang ditentukan.
- `--help`: Menampilkan informasi bantuan tentang penggunaan `printf`.
- `--version`: Menampilkan versi dari perintah `printf`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `printf`:

1. **Mencetak teks sederhana:**
   ```bash
   printf "Hello, World!\n"
   ```

2. **Mencetak angka dengan format:**
   ```bash
   printf "Nilai: %.2f\n" 3.14159
   ```

3. **Mencetak beberapa argumen:**
   ```bash
   printf "Nama: %s, Umur: %d\n" "Alice" 30
   ```

4. **Menggunakan opsi untuk menyimpan output ke variabel:**
   ```bash
   printf -v myVar "Hasil: %.1f" 9.876
   echo "$myVar"
   ```

5. **Mencetak tabel sederhana:**
   ```bash
   printf "%-10s %-10s\n" "Nama" "Umur"
   printf "%-10s %-10d\n" "Bob" 25
   printf "%-10s %-10d\n" "Charlie" 30
   ```

## Tips
- Gunakan `\n` untuk menambahkan baris baru dalam output.
- Format angka dengan spesifikasi seperti `%.2f` untuk mengontrol jumlah desimal.
- Manfaatkan opsi `-v` untuk menyimpan output ke dalam variabel jika diperlukan untuk penggunaan lebih lanjut.