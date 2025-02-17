# [Linux] Bash source penggunaan: Memuatkan skrip Bash

## Overview
Perintah `source` dalam Bash digunakan untuk menjalankan skrip shell dalam konteks shell semasa. Ini bermakna bahawa sebarang perubahan yang dibuat oleh skrip, seperti pengaturan pembolehubah atau fungsi, akan tetap ada setelah skrip selesai dijalankan.

## Usage
Berikut adalah sintaks asas untuk perintah `source`:

```bash
source [options] [arguments]
```

## Common Options
- `-`: Menunjukkan bahawa perintah `source` harus mengambil skrip dari stdin.
- `--help`: Menunjukkan maklumat bantuan untuk perintah `source`.
- `--version`: Menunjukkan versi Bash yang sedang digunakan.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `source`:

1. **Memuatkan skrip Bash**:
   Untuk memuatkan skrip bernama `myscript.sh`, anda boleh menggunakan:
   ```bash
   source myscript.sh
   ```

2. **Menggunakan titik (.) sebagai pengganti `source`**:
   Anda juga boleh menggunakan titik sebagai pengganti `source`:
   ```bash
   . myscript.sh
   ```

3. **Memuatkan fail konfigurasi**:
   Jika anda mempunyai fail konfigurasi seperti `.bashrc`, anda boleh memuatkannya dengan:
   ```bash
   source ~/.bashrc
   ```

4. **Menjalankan skrip dengan argumen**:
   Anda boleh memanggil skrip dengan argumen yang diperlukan:
   ```bash
   source myscript.sh arg1 arg2
   ```

## Tips
- Pastikan skrip yang anda muatkan mempunyai izin yang betul untuk dieksekusi.
- Gunakan `source` untuk memuatkan fail konfigurasi yang mengandungi pembolehubah persekitaran agar perubahan dapat dilihat dalam sesi shell semasa.
- Jika anda ingin menguji perubahan dalam skrip tanpa menutup dan membuka semula terminal, gunakan `source` untuk memuatkan skrip tersebut semula.