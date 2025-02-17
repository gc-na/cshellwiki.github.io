# [Linux] Bash last penggunaan: Menunjukkan log masuk pengguna

## Overview
Perintah `last` digunakan untuk memaparkan senarai log masuk pengguna yang telah dilakukan pada sistem. Ia mengambil data dari fail `/var/log/wtmp`, yang menyimpan maklumat tentang sesi log masuk dan log keluar pengguna.

## Usage
Berikut adalah sintaks asas untuk perintah `last`:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Menunjukkan alamat IP atau nama host pengguna yang log masuk.
- `-n [number]`: Menentukan bilangan entri yang ingin dipaparkan.
- `-x`: Menunjukkan maklumat tentang sesi yang tidak aktif dan perkhidmatan yang telah dimulakan.
- `-R`: Menghilangkan nama host dari output.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `last`:

1. **Menunjukkan semua log masuk pengguna:**

    ```bash
    last
    ```

2. **Menunjukkan log masuk pengguna terkini (10 entri):**

    ```bash
    last -n 10
    ```

3. **Menunjukkan log masuk dengan alamat IP:**

    ```bash
    last -a
    ```

4. **Menunjukkan sesi yang tidak aktif dan perkhidmatan yang dimulakan:**

    ```bash
    last -x
    ```

5. **Menunjukkan log masuk untuk pengguna tertentu:**

    ```bash
    last username
    ```

## Tips
- Gunakan `last -n 20` untuk melihat 20 log masuk terkini, yang berguna jika anda ingin mendapatkan gambaran ringkas tentang aktiviti terkini.
- Jika anda ingin menyemak log masuk dari alamat IP tertentu, gunakan `last -a | grep [IP_ADDRESS]`.
- Perintah `last` boleh digabungkan dengan `less` untuk meneliti output yang panjang: `last | less`.