# [Linux] Bash scp Kullanımı: Dosyaları güvenli bir şekilde kopyalama

## Genel Bakış
`scp` (Secure Copy Protocol), dosyaları bir ağ üzerinden güvenli bir şekilde kopyalamak için kullanılan bir komuttur. SSH protokolünü kullanarak, yerel ve uzak sistemler arasında dosya transferi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
scp [seçenekler] [kaynak] [hedef]
```

## Yaygın Seçenekler
- `-r`: Dizini ve içindeki tüm dosyaları kopyalamak için kullanılır.
- `-P`: Uzak sunucunun port numarasını belirtmek için kullanılır (büyük P).
- `-i`: Belirli bir SSH anahtar dosyası kullanmak için kullanılır.
- `-v`: Ayrıntılı çıktı almak için kullanılır; hata ayıklama için faydalıdır.

## Yaygın Örnekler
1. **Yerel bir dosyayı uzak bir sunucuya kopyalama:**
   ```bash
   scp dosya.txt kullanıcı@sunucu:/hedef/klasör/
   ```

2. **Uzak bir dosyayı yerel makineye kopyalama:**
   ```bash
   scp kullanıcı@sunucu:/uzak/dosya.txt /yerel/klasör/
   ```

3. **Bir dizini ve içindeki tüm dosyaları kopyalama:**
   ```bash
   scp -r yerel_klasör/ kullanıcı@sunucu:/hedef/
   ```

4. **Belirli bir port üzerinden kopyalama:**
   ```bash
   scp -P 2222 dosya.txt kullanıcı@sunucu:/hedef/
   ```

## İpuçları
- Uzak sunucuya bağlanmadan önce SSH bağlantısının çalıştığından emin olun.
- Dosya transferi sırasında bağlantı kesilirse, işlemi yeniden başlatmak için `-C` seçeneğini kullanarak sıkıştırmayı etkinleştirebilirsiniz.
- Güvenlik nedeniyle, mümkünse SSH anahtarları kullanarak kimlik doğrulaması yapın.