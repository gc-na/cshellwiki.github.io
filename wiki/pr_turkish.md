# [Linux] Bash pr Kullanımı: Dosya içeriğini sayfalara ayırma

## Genel Bakış
`pr` komutu, metin dosyalarını sayfalara ayırarak çıktı almayı sağlar. Genellikle yazdırma işlemleri için dosyaların daha okunabilir bir formatta sunulmasına yardımcı olur.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
pr [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`: Başlık ekler.
- `-l [satır sayısı]`: Her sayfada gösterilecek satır sayısını belirler.
- `-w [genişlik]`: Sayfanın genişliğini ayarlar.
- `-t`: Başlık ve sayfa numarası olmadan çıktı verir.

## Yaygın Örnekler
Aşağıda `pr` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Basit Kullanım
Bir metin dosyasını varsayılan ayarlarla sayfalara ayırmak için:
```bash
pr dosya.txt
```

### 2. Başlık Ekleme
Başlık ekleyerek dosyayı sayfalara ayırmak için:
```bash
pr -h "Başlık" dosya.txt
```

### 3. Sayfa Uzunluğunu Ayarlama
Her sayfada 20 satır göstermek için:
```bash
pr -l 20 dosya.txt
```

### 4. Sayfa Genişliğini Ayarlama
Sayfa genişliğini 100 karakter olarak ayarlamak için:
```bash
pr -w 100 dosya.txt
```

### 5. Başlık ve Sayfa Numarası Olmadan Çıktı
Başlık ve sayfa numarası olmadan çıktı almak için:
```bash
pr -t dosya.txt
```

## İpuçları
- `pr` komutunu yazdırma işlemlerinden önce kullanarak çıktıyı daha okunabilir hale getirebilirsiniz.
- Uzun dosyalar için sayfa uzunluğunu ayarlamak, çıktıyı daha düzenli hale getirebilir.
- Farklı seçenekleri bir arada kullanarak çıktıyı özelleştirebilirsiniz; örneğin, hem başlık ekleyip hem de sayfa uzunluğunu ayarlayabilirsiniz.