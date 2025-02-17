# [Linux] Bash uptime Kullanımı: Sistemin çalışma süresini gösterir

## Genel Bakış
`uptime` komutu, bir Linux sisteminin ne kadar süredir çalıştığını gösterir. Ayrıca, sistemin yük ortalamasını ve bağlı kullanıcı sayısını da sağlar. Bu bilgiler, sistem yöneticileri için sistemin sağlığı hakkında hızlı bir genel bakış sunar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
uptime [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Sistemin ne kadar süredir çalıştığını daha okunabilir bir formatta gösterir.
- `-s`: Sistemin ne zaman başladığını gösterir.

## Yaygın Örnekler
Aşağıda `uptime` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Temel uptime bilgisi
```bash
uptime
```
Bu komut, sistemin çalışma süresi, yük ortalaması ve bağlı kullanıcı sayısını gösterir.

### Örnek 2: Daha okunabilir formatta çalışma süresi
```bash
uptime -p
```
Bu komut, sistemin ne kadar süredir çalıştığını daha anlaşılır bir şekilde gösterir (örneğin, "1 gün, 2 saat").

### Örnek 3: Sistemin başlangıç zamanını gösterme
```bash
uptime -s
```
Bu komut, sistemin ne zaman başlatıldığını tarih ve saat formatında gösterir.

## İpuçları
- `uptime` komutunu düzenli olarak kontrol ederek sisteminizin performansını izleyebilirsiniz.
- Yük ortalamasını göz önünde bulundurarak, sistemin yoğunluk durumunu değerlendirebilir ve gerektiğinde önlemler alabilirsiniz.
- Uzun süreli çalışmalarda, sistemin yeniden başlatılması gerektiğini belirlemek için `uptime` çıktısını kullanabilirsiniz.