# [Linux] Bash iconv Penggunaan: Mengonversi encoding teks

## Overview
Perintah `iconv` digunakan untuk mengonversi encoding karakter dari file teks. Ini sangat berguna saat Anda perlu mengubah format encoding dari satu jenis ke jenis lainnya, seperti dari UTF-8 ke ISO-8859-1.

## Usage
Berikut adalah sintaks dasar dari perintah `iconv`:

```bash
iconv [options] [arguments]
```

## Common Options
- `-f, --from-code=CODE` : Menentukan encoding asal.
- `-t, --to-code=CODE` : Menentukan encoding tujuan.
- `-o, --output=FILE` : Menentukan nama file output.
- `-c` : Mengabaikan karakter yang tidak dapat dikonversi.

## Common Examples
1. Mengonversi file dari UTF-8 ke ISO-8859-1:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. Mengonversi file dan menampilkan hasil di terminal:
   ```bash
   iconv -f UTF-8 -t ASCII//TRANSLIT input.txt
   ```

3. Mengonversi file sambil mengabaikan karakter yang tidak dapat dikonversi:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1//IGNORE input.txt -o output.txt
   ```

4. Mengonversi file dengan output ke file baru:
   ```bash
   iconv -f WINDOWS-1252 -t UTF-8 input.txt -o output.txt
   ```

## Tips
- Selalu periksa encoding file asal sebelum melakukan konversi untuk menghindari kehilangan data.
- Gunakan opsi `-c` atau `--ignore` jika Anda ingin mengabaikan karakter yang tidak dapat dikonversi.
- Cobalah untuk melakukan konversi pada salinan file terlebih dahulu untuk memastikan hasilnya sesuai harapan.