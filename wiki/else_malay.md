# [Linux] Bash else Penggunaan: Menyediakan alternatif dalam pengendalian aliran

## Overview
Perintah `else` dalam Bash digunakan sebagai sebahagian daripada struktur kawalan `if`. Ia membolehkan pengguna untuk menentukan tindakan alternatif yang akan diambil jika syarat dalam pernyataan `if` tidak dipenuhi. Ini membolehkan pengaturcara untuk mengawal aliran program dengan lebih baik.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `else`:

```bash
if [ condition ]; then
    # arahan jika condition benar
else
    # arahan jika condition salah
fi
```

## Common Options
Perintah `else` tidak mempunyai pilihan khusus, tetapi ia biasanya digunakan bersama dengan perintah `if`. Berikut adalah beberapa elemen yang sering digunakan dalam konteks ini:

- `if`: Memulakan blok kawalan.
- `then`: Menandakan permulaan arahan yang akan dilaksanakan jika syarat benar.
- `fi`: Menandakan akhir blok kawalan `if`.

## Common Examples

### Contoh 1: Memeriksa sama ada fail wujud
```bash
if [ -f "fail.txt" ]; then
    echo "Fail wujud."
else
    echo "Fail tidak wujud."
fi
```

### Contoh 2: Memeriksa nombor genap atau ganjil
```bash
nombor=5
if [ $((nombor % 2)) -eq 0 ]; then
    echo "Nombor adalah genap."
else
    echo "Nombor adalah ganjil."
fi
```

### Contoh 3: Memeriksa status perintah
```bash
mkdir direktori_baru
if [ $? -eq 0 ]; then
    echo "Direktori berjaya dibuat."
else
    echo "Gagal membuat direktori."
fi
```

## Tips
- Sentiasa gunakan tanda kurung untuk mengelakkan kekeliruan dalam syarat.
- Gunakan `elif` untuk menambah lebih banyak syarat sebelum mencapai `else`.
- Pastikan untuk menutup blok kawalan dengan `fi` untuk mengelakkan ralat sintaks.