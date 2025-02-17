# [Linux] Bash hash penggunaan: Menyimpan dan mengurus lokasi perintah

## Overview
Perintah `hash` dalam Bash digunakan untuk menyimpan dan mengurus lokasi perintah yang telah dijalankan. Ia membantu mempercepat proses pencarian perintah dengan menyimpan jalur ke executable yang telah digunakan sebelum ini.

## Usage
Berikut adalah sintaks asas untuk perintah `hash`:

```bash
hash [options] [arguments]
```

## Common Options
- `-r`: Mengosongkan cache hash, membolehkan sistem untuk mencari semula lokasi perintah.
- `-p`: Menetapkan lokasi tertentu untuk perintah yang diberikan.
- `-l`: Menunjukkan semua perintah yang telah di-cache.

## Common Examples

1. **Menunjukkan semua perintah yang telah di-cache:**
   ```bash
   hash -l
   ```

2. **Mengosongkan cache hash:**
   ```bash
   hash -r
   ```

3. **Menetapkan lokasi khusus untuk perintah:**
   ```bash
   hash -p /usr/local/bin/mycommand mycommand
   ```

4. **Menunjukkan lokasi perintah tertentu:**
   ```bash
   hash mycommand
   ```

## Tips
- Gunakan `hash -r` selepas mengubah atau menambah perintah baru untuk memastikan sistem mengenali lokasi terkini.
- Perintah `hash` berguna dalam skrip untuk mengelakkan pencarian berulang bagi perintah yang sama, meningkatkan kecekapan.
- Sentiasa semak cache hash jika anda menghadapi masalah dengan perintah yang tidak dijumpai.