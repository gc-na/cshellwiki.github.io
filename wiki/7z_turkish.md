# [Linux] C Shell (csh) 7z Kullanımı: Dosyaları sıkıştırma ve açma aracı

## Genel Bakış
7z, dosyaları sıkıştırmak ve açmak için kullanılan güçlü bir komut satırı aracıdır. Özellikle yüksek sıkıştırma oranları sunarak, dosya boyutunu azaltma konusunda etkilidir. 7z, 7-Zip arşiv formatını destekler ve birçok farklı dosya formatıyla çalışabilir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
7z [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `a`: Yeni bir arşiv oluşturur ve dosyaları ekler.
- `x`: Arşivden dosyaları çıkartır.
- `t`: Arşivin içeriğini test eder.
- `l`: Arşivin içeriğini listele.
- `d`: Arşivden dosyaları siler.

## Yaygın Örnekler
Aşağıda 7z komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Yeni bir arşiv oluşturma
```
7z a arşiv.7z dosya1.txt dosya2.txt
```
Bu komut, `dosya1.txt` ve `dosya2.txt` dosyalarını `arşiv.7z` adlı bir arşive ekler.

### 2. Arşivden dosyaları çıkartma
```
7z x arşiv.7z
```
Bu komut, `arşiv.7z` içindeki tüm dosyaları mevcut dizine çıkartır.

### 3. Arşivin içeriğini listeleme
```
7z l arşiv.7z
```
Bu komut, `arşiv.7z` içindeki dosyaların listesini gösterir.

### 4. Arşivin içeriğini test etme
```
7z t arşiv.7z
```
Bu komut, `arşiv.7z` dosyasının bozulup bozulmadığını kontrol eder.

### 5. Arşivden dosya silme
```
7z d arşiv.7z dosya1.txt
```
Bu komut, `arşiv.7z` içinden `dosya1.txt` dosyasını siler.

## İpuçları
- Sıkıştırma oranını artırmak için `-mx=9` seçeneğini kullanarak en yüksek sıkıştırma seviyesini seçebilirsiniz.
- Arşiv oluştururken dosya uzantılarını belirtmek, dosyaların daha kolay yönetilmesini sağlar.
- Büyük dosyalarla çalışırken, işlem tamamlanana kadar sabırlı olun; sıkıştırma işlemi zaman alabilir.