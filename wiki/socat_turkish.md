# [Linux] C Shell (csh) socat Kullanımı: Veri akışlarını yönlendirme

## Genel Bakış
socat, iki veri akışını birleştiren ve yönlendiren bir komut satırı aracıdır. Ağ bağlantıları, dosyalar veya diğer veri akışları arasında iletişim kurmak için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
socat [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-u`: İletişim için UDP protokolünü kullanır.
- `-l`: Yerel bir bağlantı noktası dinler.
- `-d`: Hata ayıklama bilgilerini gösterir.
- `-v`: Ayrıntılı bilgi verir.
- `tcp:<host>:<port>`: Belirtilen ana bilgisayara ve bağlantı noktasına TCP bağlantısı kurar.

## Yaygın Örnekler
Aşağıda, socat komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. TCP Bağlantısı Kurma
```csh
socat tcp:example.com:80 -
```
Bu komut, example.com üzerindeki 80 numaralı bağlantı noktasına bir TCP bağlantısı kurar.

### 2. Yerel Bir Port Dinleme
```csh
socat -l tcp-listen:1234,fork -
```
Bu komut, 1234 numaralı bağlantı noktasında dinleme yapar ve her yeni bağlantı için yeni bir işlem oluşturur.

### 3. Dosyadan TCP'ye Veri Gönderme
```csh
socat tcp:example.com:80 < myfile.txt
```
Bu komut, myfile.txt dosyasındaki verileri example.com üzerindeki 80 numaralı bağlantı noktasına gönderir.

### 4. İki TCP Bağlantısını Birleştirme
```csh
socat tcp-listen:1234,fork tcp:anotherhost:5678
```
Bu komut, 1234 numaralı bağlantı noktasında dinleyerek gelen verileri anotherhost üzerindeki 5678 numaralı bağlantı noktasına yönlendirir.

## İpuçları
- Socat kullanırken, bağlantı noktalarının ve protokollerin doğru ayarlandığından emin olun.
- Hata ayıklama için `-d` ve `-v` seçeneklerini kullanarak daha fazla bilgi edinebilirsiniz.
- Güvenlik açısından, açık bağlantı noktalarını dikkatli bir şekilde yönetin ve yalnızca güvenilir kaynaklarla iletişim kurun.