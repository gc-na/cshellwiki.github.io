# [Linux] Bash tcpdump Penggunaan: Menangkap dan menganalisis paket rangkaian

## Overview
Perintah `tcpdump` adalah alat yang digunakan untuk menangkap dan menganalisis paket data yang melalui rangkaian. Ia sangat berguna untuk pemantauan rangkaian dan penyelesaian masalah, membolehkan pengguna melihat lalu lintas rangkaian secara langsung.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `tcpdump`:

```bash
tcpdump [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan `tcpdump`:

- `-i <interface>`: Menentukan antaramuka rangkaian yang ingin dipantau.
- `-n`: Menghalang penukaran alamat IP kepada nama host.
- `-v`, `-vv`, `-vvv`: Menambah tahap butiran output.
- `-c <count>`: Menangkap hanya bilangan paket yang ditentukan.
- `-w <file>`: Menyimpan output ke dalam fail untuk analisis kemudian.
- `-r <file>`: Membaca paket dari fail yang telah disimpan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `tcpdump`:

1. Menangkap semua paket pada antaramuka rangkaian tertentu:
   ```bash
   tcpdump -i eth0
   ```

2. Menangkap paket tanpa menukarkan alamat IP kepada nama host:
   ```bash
   tcpdump -i eth0 -n
   ```

3. Menangkap hanya 10 paket:
   ```bash
   tcpdump -i eth0 -c 10
   ```

4. Menyimpan hasil tangkapan ke dalam fail:
   ```bash
   tcpdump -i eth0 -w output.pcap
   ```

5. Membaca paket dari fail yang telah disimpan:
   ```bash
   tcpdump -r output.pcap
   ```

## Tips
- Sentiasa gunakan pilihan `-n` untuk mengelakkan kelewatan yang disebabkan oleh penukaran nama host.
- Gunakan pilihan `-v` untuk mendapatkan maklumat lebih terperinci tentang paket yang ditangkap.
- Simpan hasil tangkapan ke dalam fail menggunakan pilihan `-w` jika anda merancang untuk menganalisis data tersebut kemudian.
- Pastikan anda menjalankan `tcpdump` dengan hak akses yang sesuai, biasanya sebagai pengguna root, untuk dapat menangkap paket.