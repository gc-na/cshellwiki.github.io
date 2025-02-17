# [Linux] Bash kubectl Penggunaan: Mengelola Kubernetes

## Overview
Perintah `kubectl` adalah alat baris perintah yang digunakan untuk berinteraksi dengan kluster Kubernetes. Dengan `kubectl`, pengguna dapat mengelola aplikasi yang berjalan di dalam kluster, memeriksa status sumber daya, dan melakukan berbagai operasi administrasi.

## Usage
Sintaks dasar dari perintah `kubectl` adalah sebagai berikut:

```
kubectl [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang sering digunakan dengan `kubectl`:

- `get`: Mengambil informasi tentang sumber daya tertentu.
- `create`: Membuat sumber daya baru di kluster.
- `delete`: Menghapus sumber daya yang ada.
- `apply`: Menerapkan perubahan konfigurasi pada sumber daya.
- `describe`: Menampilkan detail lengkap tentang sumber daya tertentu.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `kubectl`:

1. **Mengambil daftar pod yang berjalan:**
   ```bash
   kubectl get pods
   ```

2. **Membuat sebuah pod dari file YAML:**
   ```bash
   kubectl create -f pod.yaml
   ```

3. **Menghapus sebuah deployment:**
   ```bash
   kubectl delete deployment nama-deployment
   ```

4. **Menerapkan perubahan dari file konfigurasi:**
   ```bash
   kubectl apply -f config.yaml
   ```

5. **Menampilkan detail tentang sebuah service:**
   ```bash
   kubectl describe service nama-service
   ```

## Tips
- Selalu gunakan opsi `--namespace` jika Anda bekerja dengan beberapa namespace untuk menghindari kebingungan.
- Gunakan `kubectl get all` untuk mendapatkan informasi tentang semua sumber daya dalam namespace saat ini.
- Manfaatkan file YAML untuk mendefinisikan konfigurasi sumber daya, sehingga memudahkan pengelolaan dan penerapan perubahan.
- Gunakan `kubectl logs [pod-name]` untuk melihat log dari pod tertentu, yang sangat berguna untuk debugging.