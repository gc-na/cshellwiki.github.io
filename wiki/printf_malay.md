# [Linux] Bash printf Penggunaan: Menampilkan format teks

## Overview
Perintah `printf` dalam Bash digunakan untuk mencetak teks dengan format yang ditentukan. Ia membolehkan pengguna untuk mengawal cara output ditampilkan, termasuk pengaturan lebar, pemisahan desimal, dan banyak lagi.

## Usage
Berikut adalah sintaks asas bagi perintah `printf`:

```bash
printf [options] [arguments]
```

## Common Options
- `-v var`: Menyimpan hasil output ke dalam pembolehubah `var` tanpa mencetaknya ke skrin.
- `-f format`: Menggunakan format yang ditentukan untuk output.
- `--help`: Menunjukkan maklumat bantuan mengenai penggunaan `printf`.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `printf`:

1. **Mencetak teks biasa:**
   ```bash
   printf "Hello, World!\n"
   ```

2. **Mencetak nombor dengan format:**
   ```bash
   printf "Nombor: %.2f\n" 3.14159
   ```

3. **Mencetak teks dengan lebar tertentu:**
   ```bash
   printf "|%-10s|%10s|\n" "Kiri" "Kanan"
   ```

4. **Menggunakan pembolehubah dalam output:**
   ```bash
   name="Ali"
   age=30
   printf "%s berumur %d tahun.\n" "$name" "$age"
   ```

5. **Menyimpan output ke dalam pembolehubah:**
   ```bash
   printf -v result "Hasil: %.1f" 5.678
   echo "$result"
   ```

## Tips
- Gunakan `\n` untuk menambah baris baru dalam output.
- Pastikan untuk menggunakan format yang sesuai untuk jenis data yang ingin dicetak.
- Eksperimen dengan lebar dan pemisahan untuk mendapatkan hasil yang lebih baik dalam laporan atau output yang lebih teratur.