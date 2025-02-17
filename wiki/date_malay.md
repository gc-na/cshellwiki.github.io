# [Linux] Bash date penggunaan: Menunjukkan dan mengubah tarikh dan masa

## Overview
Perintah `date` dalam Bash digunakan untuk memaparkan tarikh dan masa semasa. Ia juga membolehkan pengguna untuk mengubah format tarikh dan masa yang dipaparkan, serta menetapkan tarikh dan masa sistem.

## Usage
Sintaks asas untuk perintah `date` adalah seperti berikut:

```bash
date [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk perintah `date`:

- `+FORMAT`: Menentukan format output tarikh dan masa.
- `-u`: Memaparkan tarikh dan masa dalam waktu Universal Coordinated Time (UTC).
- `-d STRING`: Menggunakan STRING untuk menentukan tarikh dan masa yang ingin dipaparkan.
- `-s STRING`: Menetapkan tarikh dan masa sistem kepada STRING yang diberikan.

## Common Examples

1. **Memaparkan tarikh dan masa semasa:**

   ```bash
   date
   ```

2. **Memaparkan tarikh dalam format tertentu:**

   ```bash
   date "+%Y-%m-%d %H:%M:%S"
   ```

3. **Memaparkan tarikh dalam waktu UTC:**

   ```bash
   date -u
   ```

4. **Menetapkan tarikh dan masa sistem:**

   ```bash
   sudo date -s "2023-10-01 12:00:00"
   ```

5. **Menggunakan STRING untuk memaparkan tarikh tertentu:**

   ```bash
   date -d "next Friday"
   ```

## Tips
- Sentiasa gunakan pilihan `-u` jika anda memerlukan waktu dalam format UTC untuk mengelakkan kekeliruan dengan zon waktu tempatan.
- Untuk format yang lebih kompleks, rujuk kepada dokumentasi `date` untuk senarai penuh format yang boleh digunakan.
- Pastikan anda mempunyai hak akses yang sesuai jika anda ingin menetapkan tarikh dan masa sistem menggunakan pilihan `-s`.