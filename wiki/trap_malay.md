# [Linux] Bash trap Penggunaan: Mengendalikan sinyal dan kejadian

## Overview
Perintah `trap` dalam Bash digunakan untuk menangani sinyal dan kejadian tertentu yang berlaku semasa skrip dijalankan. Ia membolehkan pengguna untuk menentukan tindakan yang perlu diambil apabila sinyal tertentu diterima, seperti menghentikan skrip atau menjalankan fungsi tertentu sebelum skrip berakhir.

## Usage
Berikut adalah sintaks asas untuk perintah `trap`:

```bash
trap [options] [arguments]
```

## Common Options
- `SIGINT`: Menangkap isyarat interupsi (biasanya Ctrl+C).
- `SIGTERM`: Menangkap isyarat untuk menghentikan proses.
- `EXIT`: Menjalankan arahan tertentu apabila skrip selesai.
- `ERR`: Menjalankan arahan tertentu apabila terdapat ralat dalam skrip.

## Common Examples

### Menangkap Sinyal SIGINT
Untuk menangkap sinyal interupsi dan menjalankan fungsi tertentu:

```bash
trap 'echo "Skrip dihentikan"; exit' SIGINT
while true; do
    echo "Skrip berjalan..."
    sleep 1
done
```

### Menjalankan Arahan pada Keluar
Menjalankan arahan tertentu apabila skrip selesai:

```bash
trap 'echo "Skrip telah selesai."' EXIT
echo "Melakukan beberapa kerja..."
sleep 2
```

### Menangkap Ralat
Menangkap ralat dan menjalankan arahan tertentu:

```bash
trap 'echo "Terdapat ralat!"' ERR
false  # Ini akan menyebabkan ralat
```

## Tips
- Sentiasa gunakan `trap` untuk memastikan skrip anda dapat menangani situasi yang tidak dijangka dengan lebih baik.
- Gunakan `trap` dengan `EXIT` untuk membersihkan sumber atau menyimpan status sebelum skrip berakhir.
- Uji skrip anda dengan dan tanpa `trap` untuk memahami bagaimana ia mempengaruhi aliran kerja.