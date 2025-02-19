# [Linux] C Shell (csh) scp Kullanımı: Dosya transferi için güvenli bir yol

## Genel Bakış
`scp` (Secure Copy Protocol), ağ üzerinden dosyaları güvenli bir şekilde kopyalamak için kullanılan bir komuttur. SSH (Secure Shell) protokolünü kullanarak, yerel ve uzak sistemler arasında dosya transferi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
scp [seçenekler] [kaynak] [hedef]
```

## Yaygın Seçenekler
- `-r`: Dizini ve içindeki tüm dosyaları kopyalamak için kullanılır.
- `-P`: Uzak sunucunun port numarasını belirtmek için kullanılır (büyük P).
- `-i`: Belirtilen özel anahtar dosyasını kullanarak kimlik doğrulama yapar.
- `-v`: Ayrıntılı çıktı almak için kullanılır; hata ayıklama amacıyla faydalıdır.

## Yaygın Örnekler
1. Yerel bir dosyayı uzak bir sunucuya kopyalamak:
   ```bash
   scp dosya.txt kullanıcı@sunucu:/hedef/dizin/
   ```

2. Uzak bir dosyayı yerel makineye indirmek:
   ```bash
   scp kullanıcı@sunucu:/uzak/dosya.txt /yerel/dizin/
   ```

3. Bir dizini ve içindeki tüm dosyaları kopyalamak:
   ```bash
   scp -r /yerel/dizin/ kullanıcı@sunucu:/hedef/dizin/
   ```

4. Belirli bir port üzerinden dosya kopyalamak:
   ```bash
   scp -P 2222 dosya.txt kullanıcı@sunucu:/hedef/dizin/
   ```

## İpuçları
- Uzak sunucuya bağlanmadan önce SSH bağlantınızın çalıştığından emin olun.
- Dosya transferi sırasında ağ bağlantınızın stabil olduğundan emin olun; büyük dosyalar için bağlantı kopmaları sorun yaratabilir.
- Güvenlik nedeniyle, özel anahtar dosyalarınızı doğru bir şekilde yönetin ve paylaşmayın.