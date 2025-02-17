# [Linux] Bash docker penggunaan: Mengurus kontena aplikasi

## Overview
Perintah `docker` digunakan untuk mengurus dan menjalankan kontena aplikasi. Docker membolehkan pengguna untuk membina, menghantar, dan menjalankan aplikasi dalam persekitaran yang terasing, menjadikannya lebih mudah untuk mengurus kebergantungan dan persekitaran aplikasi.

## Usage
Berikut adalah sintaks asas untuk perintah docker:

```bash
docker [options] [arguments]
```

## Common Options
- `run`: Menjalankan kontena baru.
- `ps`: Menunjukkan senarai kontena yang sedang berjalan.
- `images`: Menunjukkan senarai imej yang tersedia.
- `pull`: Memuat turun imej dari Docker Hub.
- `build`: Membina imej dari Dockerfile.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah docker:

1. **Menjalankan kontena baru**:
   ```bash
   docker run hello-world
   ```

2. **Melihat kontena yang sedang berjalan**:
   ```bash
   docker ps
   ```

3. **Memuat turun imej**:
   ```bash
   docker pull ubuntu
   ```

4. **Membina imej dari Dockerfile**:
   ```bash
   docker build -t my-image .
   ```

5. **Menghentikan kontena yang sedang berjalan**:
   ```bash
   docker stop <container_id>
   ```

## Tips
- Sentiasa gunakan tag untuk imej anda agar mudah dikenali dan diurus.
- Gunakan `docker-compose` untuk mengurus aplikasi yang terdiri daripada beberapa kontena.
- Pastikan untuk membersihkan kontena dan imej yang tidak digunakan dengan `docker system prune` untuk mengelakkan penggunaan ruang yang tidak perlu.