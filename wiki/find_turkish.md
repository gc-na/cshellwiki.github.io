# [Linux] Bash find Kullanımı: Dosya adlarını bulma

## Genel Bakış
`find` komutu, belirli bir dizin içinde dosya ve dizinleri aramak için kullanılır. Kullanıcıların belirli kriterlere göre dosyaları bulmasına olanak tanır, bu da dosya yönetimini kolaylaştırır.

## Kullanım
Temel sözdizimi şu şekildedir:

```
find [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-name`: Belirtilen isimle eşleşen dosyaları bulur.
- `-type`: Belirli bir dosya türünü (örneğin, dosya veya dizin) arar.
- `-size`: Belirli bir boyutta dosyaları bulur.
- `-mtime`: Son değişiklik tarihine göre dosyaları arar.
- `-exec`: Bulunan dosyalar üzerinde belirli bir komut çalıştırır.

## Yaygın Örnekler
Aşağıda `find` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Belirli bir isimle dosya bulma
```bash
find /home/kullanici -name "belge.txt"
```
Bu komut, `/home/kullanici` dizininde "belge.txt" adlı dosyayı arar.

### 2. Sadece dizinleri bulma
```bash
find /var -type d
```
Bu komut, `/var` dizininde bulunan tüm dizinleri listeler.

### 3. Belirli bir boyutta dosyaları bulma
```bash
find /tmp -size +10M
```
Bu komut, `/tmp` dizininde 10 MB'den büyük dosyaları arar.

### 4. Son 7 günde değiştirilen dosyaları bulma
```bash
find /home/kullanici -mtime -7
```
Bu komut, son 7 gün içinde değiştirilen dosyaları bulur.

### 5. Bulunan dosyalar üzerinde komut çalıştırma
```bash
find /home/kullanici -name "*.log" -exec rm {} \;
```
Bu komut, `/home/kullanici` dizininde bulunan tüm `.log` dosyalarını siler.

## İpuçları
- `find` komutunu kullanırken, arama alanını daraltmak için seçenekleri birleştirmek faydalıdır.
- Arama işlemlerini hızlandırmak için, belirli bir dizinle sınırlı kalmaya özen gösterin.
- `-print` seçeneğini kullanarak bulunan dosyaların listesini görmek isteyebilirsiniz; bu, varsayılan olarak etkin olsa da, bazen açıkça belirtmek faydalı olabilir.