# [Linux] Bash dirname Kullanımı: Dosya yolundan dizin adını çıkarma

## Genel Bakış
`dirname` komutu, bir dosya yolundan dizin adını çıkarmak için kullanılır. Bu komut, verilen bir dosya yolunun dizin kısmını ayırarak yalnızca dizin adını döndürür.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
dirname [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-z`, `--zero`: Girdi dosyası yollarını sıfır karakteri ile ayırarak işleme alır.
- `--help`: Komut hakkında yardım bilgilerini gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `dirname` komutunun bazı pratik kullanımları verilmiştir:

1. Basit bir dosya yolu için dizin adını alma:
   ```bash
   dirname /home/kullanici/dosya.txt
   ```
   Çıktı:
   ```
   /home/kullanici
   ```

2. Bir dosya yolunda son dizin adını almak:
   ```bash
   dirname /var/log/syslog
   ```
   Çıktı:
   ```
   /var/log
   ```

3. Birden fazla dosya yolu için dizin adlarını alma:
   ```bash
   dirname /usr/local/bin/script.sh /etc/nginx/nginx.conf
   ```
   Çıktı:
   ```
   /usr/local/bin
   /etc/nginx
   ```

## İpuçları
- `dirname` komutunu, dosya yollarını işleyen betiklerinizde kullanarak dizinleri kolayca ayırabilirsiniz.
- Birden fazla dosya yolu ile çalışırken, çıktıların her birinin ayrı satırlarda olacağını unutmayın.
- `dirname` komutunu diğer komutlarla birleştirerek daha karmaşık dosya işlemleri gerçekleştirebilirsiniz. Örneğin, bir dosyanın bulunduğu dizine gitmek için `cd $(dirname dosya_yolu)` komutunu kullanabilirsiniz.