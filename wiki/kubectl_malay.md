# [Linux] Bash kubectl Penggunaan: Mengurus kluster Kubernetes

## Overview
Perintah `kubectl` adalah alat baris perintah yang digunakan untuk berinteraksi dengan kluster Kubernetes. Ia membolehkan pengguna untuk mengurus sumber daya dalam kluster, seperti pod, servis, dan pengaturan lain yang berkaitan dengan aplikasi yang berjalan di Kubernetes.

## Usage
Berikut adalah sintaks asas untuk menggunakan `kubectl`:

```bash
kubectl [options] [arguments]
```

## Common Options
- `get`: Mengambil maklumat tentang sumber daya tertentu.
- `create`: Membuat sumber daya baru dalam kluster.
- `delete`: Menghapus sumber daya yang ada.
- `apply`: Mengaplikasikan perubahan pada sumber daya yang ada.
- `describe`: Menunjukkan maklumat terperinci tentang sumber daya tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan `kubectl`:

1. **Mengambil senarai pod dalam kluster:**
   ```bash
   kubectl get pods
   ```

2. **Membuat pod baru menggunakan fail konfigurasi:**
   ```bash
   kubectl create -f pod.yaml
   ```

3. **Menghapus pod tertentu:**
   ```bash
   kubectl delete pod nama-pod
   ```

4. **Mengaplikasikan perubahan pada sumber daya:**
   ```bash
   kubectl apply -f deployment.yaml
   ```

5. **Menunjukkan maklumat terperinci tentang sebuah servis:**
   ```bash
   kubectl describe service nama-servis
   ```

## Tips
- Sentiasa gunakan `kubectl get` untuk memeriksa status sumber daya selepas melakukan perubahan.
- Gunakan fail YAML untuk mendefinisikan sumber daya secara terperinci dan memudahkan pengurusan.
- Manfaatkan `kubectl context` untuk beralih antara kluster yang berbeza dengan mudah.
- Gunakan `kubectl logs` untuk melihat log dari pod tertentu, yang sangat berguna untuk debugging.