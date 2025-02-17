# [Linux] Bash hexdump Penggunaan: Menunjukkan data dalam format heksadesimal

## Overview
Perintah `hexdump` digunakan untuk menampilkan kandungan fail dalam format heksadesimal. Ia berguna untuk menganalisis fail binari dan memahami struktur data dengan lebih baik.

## Usage
Sintaks asas bagi perintah `hexdump` adalah seperti berikut:

```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: Menunjukkan output dalam format heksadesimal dan ASCII.
- `-n N`: Menunjukkan hanya N bait pertama dari fail.
- `-v`: Menunjukkan semua data, termasuk nilai yang berulang.
- `-e FORMAT`: Menentukan format output yang khusus.

## Common Examples
Berikut adalah beberapa contoh penggunaan `hexdump`:

1. Menunjukkan kandungan fail dalam format heksadesimal:
   ```bash
   hexdump fail.bin
   ```

2. Menunjukkan output dalam format heksadesimal dan ASCII:
   ```bash
   hexdump -C fail.bin
   ```

3. Menunjukkan hanya 16 bait pertama dari fail:
   ```bash
   hexdump -n 16 fail.bin
   ```

4. Menggunakan format khusus untuk output:
   ```bash
   hexdump -e '16/1 "%02x " "\n"' fail.bin
   ```

## Tips
- Gunakan pilihan `-C` untuk mendapatkan pandangan yang lebih jelas tentang data binari, termasuk representasi ASCII.
- Jika anda hanya perlu melihat sebahagian kecil fail, gunakan pilihan `-n` untuk mengelakkan output yang terlalu panjang.
- Eksperimen dengan pilihan `-e` untuk menyesuaikan format output mengikut keperluan analisis anda.