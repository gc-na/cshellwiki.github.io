# [Linux] Bash 7z Kullanımı: Dosyaları sıkıştırma ve açma aracı

## Genel Bakış
7z, dosyaları sıkıştırmak ve açmak için kullanılan güçlü bir komut satırı aracıdır. 7z formatı, yüksek sıkıştırma oranları sunarak dosyaların daha az yer kaplamasını sağlar. Ayrıca, birçok farklı dosya formatını destekler.

## Kullanım
Temel sözdizimi şu şekildedir:
```
7z [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `a`: Yeni bir arşiv oluşturur ve dosyaları ekler.
- `x`: Arşivden dosyaları çıkarır.
- `l`: Arşivdeki dosyaların listesini gösterir.
- `t`: Arşivin bütünlüğünü kontrol eder.
- `d`: Arşivden dosyaları siler.

## Yaygın Örnekler
1. **Yeni bir arşiv oluşturma**:
   ```bash
   7z a arşiv.7z dosya1.txt dosya2.txt
   ```
   Bu komut, `dosya1.txt` ve `dosya2.txt` dosyalarını `arşiv.7z` adlı bir arşive ekler.

2. **Arşivden dosyaları çıkarma**:
   ```bash
   7z x arşiv.7z
   ```
   Bu komut, `arşiv.7z` içindeki tüm dosyaları mevcut dizine çıkarır.

3. **Arşivdeki dosyaların listesini gösterme**:
   ```bash
   7z l arşiv.7z
   ```
   Bu komut, `arşiv.7z` içindeki dosyaların listesini görüntüler.

4. **Arşivin bütünlüğünü kontrol etme**:
   ```bash
   7z t arşiv.7z
   ```
   Bu komut, `arşiv.7z` dosyasının bozulup bozulmadığını kontrol eder.

5. **Arşivden belirli bir dosyayı silme**:
   ```bash
   7z d arşiv.7z dosya1.txt
   ```
   Bu komut, `arşiv.7z` içinden `dosya1.txt` dosyasını siler.

## İpuçları
- Sıkıştırma oranını artırmak için `-mx=9` seçeneğini kullanabilirsiniz. Örneğin:
  ```bash
  7z a -mx=9 arşiv.7z dosya.txt
  ```
- Arşivlerinizi şifrelemek için `-p` seçeneğini kullanabilirsiniz:
  ```bash
  7z a -pşifre arşiv.7z dosya.txt
  ```
- Büyük dosyaları sıkıştırırken, işlem süresinin uzayabileceğini unutmayın; sabırlı olun.