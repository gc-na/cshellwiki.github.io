# [Linux] Bash minikube Penggunaan: Mengurus kluster Kubernetes tempatan

## Overview
Minikube adalah alat yang membolehkan pengguna menjalankan kluster Kubernetes secara tempatan. Ia sangat berguna untuk pengembangan dan pengujian aplikasi yang menggunakan Kubernetes tanpa perlu mengatur infrastruktur yang lebih kompleks.

## Usage
Sintaks asas untuk menggunakan minikube adalah seperti berikut:

```
minikube [options] [arguments]
```

## Common Options
- `start`: Memulakan kluster minikube.
- `stop`: Menghentikan kluster minikube yang sedang berjalan.
- `status`: Menunjukkan status kluster minikube.
- `delete`: Menghapus kluster minikube.
- `dashboard`: Membuka antaramuka pengguna web untuk Kubernetes.

## Common Examples
Berikut adalah beberapa contoh penggunaan minikube:

1. **Memulakan kluster minikube:**
   ```bash
   minikube start
   ```

2. **Menghentikan kluster minikube:**
   ```bash
   minikube stop
   ```

3. **Memeriksa status kluster:**
   ```bash
   minikube status
   ```

4. **Menghapus kluster minikube:**
   ```bash
   minikube delete
   ```

5. **Membuka dashboard Kubernetes:**
   ```bash
   minikube dashboard
   ```

## Tips
- Sentiasa pastikan anda menggunakan versi terkini minikube untuk mendapatkan ciri dan pembaikan terbaru.
- Gunakan `minikube addons` untuk mengaktifkan pelbagai tambahan yang boleh membantu dalam pembangunan aplikasi.
- Jika mengalami masalah, gunakan `minikube logs` untuk mendapatkan maklumat lanjut tentang kesalahan yang berlaku.