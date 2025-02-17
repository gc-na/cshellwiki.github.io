# [Linux] Bash rehash Kullanımı: Komutları güncelleme

## Genel Bakış
`rehash` komutu, Bash kabuğunda kullanılan bir komut olup, mevcut komutların ve yürütülebilir dosyaların güncellenmesini sağlar. Bu komut, özellikle yeni yüklenen veya değiştirilen komutların tanınmasını sağlamak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
rehash [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Yalnızca PATH değişkeninde bulunan dizinlerdeki komutları günceller.
- `-a`: Tüm dizinlerdeki komutları günceller.

## Yaygın Örnekler
Aşağıda `rehash` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Basit rehash kullanımı
```bash
rehash
```
Bu komut, mevcut komutları güncelleyerek yeni eklenen veya değiştirilen komutların tanınmasını sağlar.

### Örnek 2: PATH dizinlerinde rehash
```bash
rehash -p
```
Bu komut, yalnızca PATH değişkeninde bulunan dizinlerdeki komutları günceller.

### Örnek 3: Tüm dizinlerde rehash
```bash
rehash -a
```
Bu komut, tüm dizinlerdeki komutları güncelleyerek daha geniş bir güncelleme sağlar.

## İpuçları
- `rehash` komutunu sık sık kullanarak, yeni yüklenen programların hemen tanınmasını sağlayabilirsiniz.
- Eğer bir komut eklediyseniz ve hala çalışmıyorsa, `rehash` komutunu çalıştırmayı deneyin.
- `rehash` komutunu, özellikle sık sık yeni yazılımlar yükleyen kullanıcılar için önerilir.