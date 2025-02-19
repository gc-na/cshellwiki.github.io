# [Sistem Operasi] C Shell (csh) expr Penggunaan: Menghitung ekspresi

## Overview
Perintah `expr` dalam C Shell (csh) digunakan untuk mengevaluasi ekspresi aritmatika, string, dan logika. Ini memungkinkan pengguna untuk melakukan perhitungan dasar dan manipulasi string dalam skrip shell.

## Usage
Sintaks dasar dari perintah `expr` adalah sebagai berikut:

```csh
expr [options] [arguments]
```

## Common Options
- `+` : Menambahkan dua angka.
- `-` : Mengurangkan satu angka dari angka lainnya.
- `*` : Mengalikan dua angka.
- `/` : Membagi satu angka dengan angka lainnya.
- `%` : Menghitung sisa dari pembagian dua angka.
- `=` : Membandingkan dua nilai untuk kesetaraan.
- `!=` : Membandingkan dua nilai untuk ketidaksetaraan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `expr`:

1. **Menjumlahkan dua angka:**
   ```csh
   set result = `expr 5 + 3`
   echo $result  # Output: 8
   ```

2. **Mengurangkan dua angka:**
   ```csh
   set result = `expr 10 - 4`
   echo $result  # Output: 6
   ```

3. **Mengalikan dua angka:**
   ```csh
   set result = `expr 7 \* 6`
   echo $result  # Output: 42
   ```

4. **Membagi dua angka:**
   ```csh
   set result = `expr 20 / 4`
   echo $result  # Output: 5
   ```

5. **Menghitung sisa pembagian:**
   ```csh
   set result = `expr 10 % 3`
   echo $result  # Output: 1
   ```

6. **Membandingkan dua nilai:**
   ```csh
   set isEqual = `expr 5 = 5`
   echo $isEqual  # Output: 1 (true)
   ```

## Tips
- Selalu gunakan tanda backticks (`` ` ``) saat menggunakan `expr` dalam skrip untuk memastikan hasilnya disimpan dalam variabel.
- Ingat untuk menghindari spasi di sekitar operator aritmatika, karena C Shell memerlukan format tertentu untuk mengenali ekspresi.
- Untuk operasi yang lebih kompleks, pertimbangkan untuk menggunakan bahasa pemrograman lain atau alat yang lebih kuat seperti `bc` atau `awk`.