# [Linux] Bash vgs Penggunaan: Menunjukkan maklumat kumpulan volum

## Overview
Perintah `vgs` digunakan dalam sistem pengurusan storan LVM (Logical Volume Manager) untuk menunjukkan maklumat mengenai kumpulan volum yang ada. Ia memberikan gambaran keseluruhan tentang kapasiti, penggunaan, dan status kumpulan volum dalam sistem.

## Usage
Sintaks asas untuk menggunakan perintah `vgs` adalah seperti berikut:

```
vgs [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `vgs`:

- `-o` : Menentukan lajur yang ingin ditunjukkan.
- `-n` : Menunjukkan nama kumpulan volum sahaja.
- `--units` : Menentukan unit untuk kapasiti yang ditunjukkan.
- `-h` : Menunjukkan maklumat dalam format yang lebih mudah dibaca.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `vgs`:

1. **Menunjukkan semua kumpulan volum:**
   ```bash
   vgs
   ```

2. **Menunjukkan maklumat dengan lajur tertentu:**
   ```bash
   vgs -o vg_name,lv_count,vg_size
   ```

3. **Menunjukkan nama kumpulan volum sahaja:**
   ```bash
   vgs -n
   ```

4. **Menunjukkan maklumat dalam format yang lebih mudah dibaca:**
   ```bash
   vgs -h
   ```

5. **Menunjukkan maklumat dengan unit tertentu:**
   ```bash
   vgs --units g
   ```

## Tips
- Gunakan pilihan `-o` untuk menyesuaikan maklumat yang ditunjukkan mengikut keperluan anda.
- Sentiasa periksa status kumpulan volum secara berkala untuk memastikan tiada masalah dengan storan anda.
- Jika anda baru menggunakan LVM, luangkan masa untuk memahami konsep kumpulan volum dan logik di sebaliknya untuk penggunaan yang lebih berkesan.