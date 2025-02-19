# [Linux] C Shell (csh) sed Kullanımı: Metin düzenleme aracı

## Genel Bakış
`sed`, akış düzenleyici olarak bilinen bir komuttur. Metin dosyaları üzerinde düzenleme yapmanıza olanak tanır. `sed`, metin akışını okur ve belirli kurallara göre değişiklikler yaparak çıktıyı oluşturur. Bu, dosyaları otomatik olarak düzenlemek için oldukça kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
sed [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Birden fazla komut belirtmek için kullanılır.
- `-i`: Dosyayı yerinde düzenler; değişiklikler dosyaya kaydedilir.
- `-n`: Varsayılan çıktıyı bastırır; yalnızca belirtilen satırları gösterir.
- `s/pattern/replacement/`: Belirli bir deseni değiştirir.

## Yaygın Örnekler
Aşağıda `sed` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Basit Metin Değiştirme
Bir dosyadaki "eski" kelimesini "yeni" ile değiştirmek için:

```bash
sed 's/eski/yeni/' dosya.txt
```

### 2. Yerinde Değiştirme
Değişiklikleri doğrudan dosyaya kaydetmek için:

```bash
sed -i 's/eski/yeni/' dosya.txt
```

### 3. Belirli Satırları Gösterme
Sadece 2. satırı göstermek için:

```bash
sed -n '2p' dosya.txt
```

### 4. Birden Fazla Değişiklik Yapma
Birden fazla değişiklik yapmak için:

```bash
sed -e 's/eski/yeni/' -e 's/başka/yeni2/' dosya.txt
```

## İpuçları
- `sed` komutunu test etmek için `-n` seçeneğini kullanarak çıktıyı kontrol edin.
- Değişikliklerinizi kaydetmeden önce yedek almak iyi bir uygulamadır.
- Karmaşık düzenlemeler için `sed` komutunu bir dosyaya yazabilir ve daha sonra çalıştırabilirsiniz.