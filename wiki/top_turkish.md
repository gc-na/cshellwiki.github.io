# [Linux] C Shell (csh) top Kullanımı: Sistem kaynaklarını görüntüleme

## Genel Bakış
`top` komutu, sistemdeki işlemleri ve kaynak kullanımını gerçek zamanlı olarak görüntülemek için kullanılır. Bu komut, CPU ve bellek kullanımı gibi bilgileri takip etmek isteyen kullanıcılar için oldukça yararlıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```csh
top [options] [arguments]
```

## Yaygın Seçenekler
- `-d <saniye>`: Güncellemelerin ne sıklıkla yapılacağını belirler.
- `-n <sayı>`: Belirtilen sayıda güncelleme yapıldıktan sonra çıkış yapar.
- `-u <kullanıcı>`: Sadece belirtilen kullanıcıya ait işlemleri gösterir.

## Yaygın Örnekler
Aşağıda `top` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Varsayılan Kullanım**: `top` komutunu basitçe çalıştırmak için:
   ```csh
   top
   ```

2. **Güncellemeleri 5 Saniyede Bir Yapmak**:
   ```csh
   top -d 5
   ```

3. **Sadece Belirli Bir Kullanıcının İşlemlerini Görüntülemek**:
   ```csh
   top -u kullanıcı_adı
   ```

4. **10 Güncellemeden Sonra Çıkmak**:
   ```csh
   top -n 10
   ```

## İpuçları
- `top` komutunu kullanırken, işlemleri sıralamak için `Shift + M` (bellek kullanımı) veya `Shift + P` (CPU kullanımı) tuşlarına basabilirsiniz.
- `top` arayüzünde, `h` tuşuna basarak yardım alabilirsiniz.
- Çıkmak için `q` tuşuna basmayı unutmayın.