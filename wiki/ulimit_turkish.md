# [Linux] Bash ulimit Kullanımı: Sistem kaynaklarını sınırlama

## Overview
`ulimit` komutu, bir shell oturumu için sistem kaynaklarının kullanımını sınırlamak amacıyla kullanılır. Bu komut, kullanıcıların belirli kaynakların (örneğin, dosya boyutu, süreç sayısı) kullanımını kontrol etmelerine olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
ulimit [options] [arguments]
```

## Common Options
- `-c`: Çekirdek dosyası boyutunu ayarlar.
- `-d`: Veri segmenti boyutunu ayarlar.
- `-f`: Oluşturulacak dosyaların maksimum boyutunu ayarlar.
- `-l`: Kilitlenmiş bellek boyutunu ayarlar.
- `-n`: Açık dosya tanımlayıcılarının maksimum sayısını ayarlar.
- `-s`: Yığın boyutunu ayarlar.
- `-t`: Süreçlerin maksimum çalışma süresini ayarlar.
- `-u`: Kullanıcının oluşturabileceği maksimum süreç sayısını ayarlar.

## Common Examples
1. Açık dosya tanımlayıcılarının maksimum sayısını görüntüleme:
   ```bash
   ulimit -n
   ```

2. Açık dosya tanımlayıcılarının maksimum sayısını 1024 olarak ayarlama:
   ```bash
   ulimit -n 1024
   ```

3. Çekirdek dosyası boyutunu 0 olarak ayarlayarak çekirdek dökümünü devre dışı bırakma:
   ```bash
   ulimit -c 0
   ```

4. Kullanıcının oluşturabileceği maksimum süreç sayısını 50 olarak ayarlama:
   ```bash
   ulimit -u 50
   ```

5. Yığın boyutunu 1 MB olarak ayarlama:
   ```bash
   ulimit -s 1024
   ```

## Tips
- `ulimit` ayarları, yalnızca mevcut shell oturumu için geçerlidir. Yeni bir oturum açıldığında varsayılan ayarlar geri yüklenir.
- Ayarları kalıcı hale getirmek için, bu komutları kullanıcı profil dosyalarına (örneğin, `~/.bashrc`) ekleyebilirsiniz.
- Sistem kaynaklarını aşırı şekilde sınırlamak, uygulamaların beklenmedik şekilde çalışmamasına neden olabilir; bu nedenle dikkatli olunmalıdır.