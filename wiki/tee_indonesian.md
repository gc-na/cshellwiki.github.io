# [Sistem Operasi] C Shell (csh) tee Penggunaan: Menyalin dan Menampilkan Output

## Overview
Perintah `tee` dalam C Shell (csh) digunakan untuk membaca dari input standar dan menulis ke output standar serta satu atau lebih file. Ini berguna untuk melihat output dari perintah sambil juga menyimpannya ke dalam file.

## Usage
Sintaks dasar dari perintah `tee` adalah sebagai berikut:

```csh
tee [options] [arguments]
```

## Common Options
- `-a` : Menambahkan output ke akhir file yang sudah ada, bukan menimpanya.
- `-i` : Mengabaikan sinyal interrupt (SIGINT) saat menulis ke file.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `tee`:

1. Menyimpan output dari perintah `ls` ke dalam file `daftar.txt`:
   ```csh
   ls | tee daftar.txt
   ```

2. Menyimpan output sambil menampilkan hasil di terminal:
   ```csh
   echo "Ini adalah contoh" | tee output.txt
   ```

3. Menambahkan output ke file yang sudah ada:
   ```csh
   echo "Baris tambahan" | tee -a output.txt
   ```

4. Mengabaikan interrupt saat menulis ke file:
   ```csh
   cat file.txt | tee -i output.txt
   ```

## Tips
- Gunakan opsi `-a` jika Anda ingin menambahkan data ke file yang sudah ada tanpa menghapus isinya.
- Perhatikan bahwa `tee` akan menampilkan output ke terminal secara default, jadi jika Anda hanya ingin menyimpan tanpa menampilkan, Anda bisa mengarahkan output ke `/dev/null`.
- Kombinasikan `tee` dengan perintah lain menggunakan pipe (`|`) untuk memproses data secara efisien.