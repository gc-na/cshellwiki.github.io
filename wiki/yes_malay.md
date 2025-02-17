# [Linux] Bash yes Penggunaan: Mengulangi teks secara berterusan

## Overview
Perintah `yes` dalam Bash digunakan untuk mencetak satu atau lebih rentetan teks secara berterusan ke output standard. Ia sering digunakan untuk memberikan input automatik kepada perintah lain yang memerlukan pengesahan atau input berulang.

## Usage
Sintaks asas untuk perintah `yes` adalah seperti berikut:

```bash
yes [options] [arguments]
```

## Common Options
- `-h`, `--help`: Menunjukkan maklumat bantuan tentang perintah `yes`.
- `-V`, `--version`: Menunjukkan versi perintah `yes`.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `yes`:

1. **Mengulangi teks "yes" secara berterusan**:
   ```bash
   yes
   ```
   Ini akan mencetak "yes" tanpa henti.

2. **Mengulangi teks tertentu**:
   ```bash
   yes "Saya suka Bash"
   ```
   Ini akan mencetak "Saya suka Bash" berulang kali.

3. **Menggunakan `yes` untuk memberikan input kepada perintah lain**:
   ```bash
   yes | rm -i *.tmp
   ```
   Dalam contoh ini, `yes` akan memberikan jawapan "yes" secara automatik kepada semua pengesahan yang diperlukan oleh perintah `rm`.

4. **Mengulangi pelbagai rentetan teks**:
   ```bash
   yes "Pilihan 1" "Pilihan 2"
   ```
   Ini akan mencetak "Pilihan 1" dan "Pilihan 2" secara berterusan.

## Tips
- Gunakan `yes` dengan berhati-hati, terutama dengan perintah yang boleh mengubah atau memadam data, kerana ia akan memberikan jawapan secara automatik tanpa pengesahan.
- Anda boleh menghentikan output `yes` dengan menekan `Ctrl + C`.
- Pertimbangkan untuk menggunakan `yes` dalam skrip untuk automasi tugas yang memerlukan input berulang.