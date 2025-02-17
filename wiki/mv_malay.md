# [Linux] Bash mv Penggunaan: Memindahkan atau menamakan semula fail

## Overview
Perintah `mv` dalam Bash digunakan untuk memindahkan fail atau direktori dari satu lokasi ke lokasi lain. Selain itu, ia juga boleh digunakan untuk menamakan semula fail atau direktori.

## Usage
Sintaks asas untuk perintah `mv` adalah seperti berikut:

```bash
mv [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `mv`:

- `-i`: Mengaktifkan mod interaktif. Jika fail yang sama wujud di lokasi sasaran, pengguna akan diminta untuk mengesahkan sebelum menimpa.
- `-u`: Memindahkan fail hanya jika fail sumber lebih baru daripada fail sasaran atau jika fail sasaran tidak wujud.
- `-v`: Menunjukkan maklumat tentang fail yang sedang dipindahkan atau dinamakan semula.

## Common Examples

1. **Memindahkan fail ke direktori lain:**
   ```bash
   mv fail.txt /home/user/dokumen/
   ```

2. **Menamakan semula fail:**
   ```bash
   mv fail_lama.txt fail_baru.txt
   ```

3. **Memindahkan dan menamakan semula fail dalam satu arahan:**
   ```bash
   mv /home/user/fail.txt /home/user/dokumen/fail_baru.txt
   ```

4. **Menggunakan pilihan interaktif:**
   ```bash
   mv -i fail.txt /home/user/dokumen/
   ```

5. **Memindahkan fail hanya jika lebih baru:**
   ```bash
   mv -u fail.txt /home/user/dokumen/
   ```

## Tips
- Sentiasa gunakan pilihan `-i` jika anda bimbang tentang menimpa fail yang sedia ada.
- Periksa lokasi sasaran sebelum memindahkan fail untuk mengelakkan kehilangan data.
- Gunakan pilihan `-v` untuk mendapatkan maklumat tambahan semasa proses pemindahan, terutamanya jika anda memindahkan banyak fail.