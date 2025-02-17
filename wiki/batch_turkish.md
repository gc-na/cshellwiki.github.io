# [Linux] Bash batch kullanımı: Arka planda komut çalıştırma

## Genel Bakış
`batch` komutu, kullanıcıların belirli komutları veya betikleri, sistemin yükü düşük olduğunda arka planda çalıştırmalarını sağlar. Bu, özellikle yoğun zamanlarda sistem kaynaklarını daha verimli kullanmak için yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
batch [options] [arguments]
```

## Yaygın Seçenekler
- `-f`: Belirtilen dosyayı çalıştırır.
- `-q`: Çıktıyı bastırır, yalnızca hata mesajlarını gösterir.
- `-l`: Komutun çalıştırılacağı zaman dilimini belirler.

## Yaygın Örnekler
Aşağıda `batch` komutunun bazı pratik kullanımları verilmiştir:

1. Basit bir komut çalıştırma:
   ```bash
   echo "Hello, World!" | batch
   ```

2. Bir betik dosyasını arka planda çalıştırma:
   ```bash
   batch < my_script.sh
   ```

3. Belirli bir zaman diliminde çalıştırma:
   ```bash
   echo "python my_script.py" | batch -l "10:00"
   ```

4. Çıktıyı bastırma:
   ```bash
   echo "Backup started" | batch -q
   ```

## İpuçları
- `batch` komutunu kullanmadan önce, çalıştırmak istediğiniz komutların doğru olduğundan emin olun.
- Komutlarınızın çıktısını kontrol etmek için, `mail` veya `cron` gibi araçları kullanarak hata mesajlarını takip edebilirsiniz.
- Sistem yükünü izlemek için `top` veya `htop` gibi araçları kullanarak, `batch` komutunu en uygun zamanda çalıştırabilirsiniz.