# [Linux] C Shell (csh) cksum Kullanımı: Dosya kontrol toplamını hesaplama

## Genel Bakış
`cksum` komutu, dosyaların kontrol toplamını (checksum) hesaplamak için kullanılır. Bu, dosyanın içeriğinin bütünlüğünü doğrulamak için faydalıdır. Kontrol toplamı, dosyanın içeriği değiştiğinde değişen bir sayıdır ve bu sayede dosyanın bozulup bozulmadığını anlayabilirsiniz.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
cksum [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a, --algorithm=ALGORITHM`: Kullanılacak algoritmayı belirtir.
- `-h, --help`: Yardım mesajını gösterir.
- `-v, --version`: Versiyon bilgisini gösterir.

## Yaygın Örnekler
Aşağıda `cksum` komutunun bazı pratik örnekleri verilmiştir:

### Örnek 1: Basit kontrol toplamı hesaplama
Bir dosyanın kontrol toplamını hesaplamak için:
```bash
cksum dosya.txt
```

### Örnek 2: Birden fazla dosya için kontrol toplamı hesaplama
Birden fazla dosyanın kontrol toplamını hesaplamak için:
```bash
cksum dosya1.txt dosya2.txt
```

### Örnek 3: Çıktıyı bir dosyaya yönlendirme
Kontrol toplamı çıktısını bir dosyaya kaydetmek için:
```bash
cksum dosya.txt > kontrol_toplami.txt
```

## İpuçları
- Kontrol toplamlarını düzenli olarak kontrol ederek dosyalarınızın bütünlüğünü sağlamak iyi bir uygulamadır.
- Dosya yedekleme işlemlerinde kontrol toplamlarını kullanarak yedeklerin doğruluğunu kontrol edebilirsiniz.
- `cksum` komutunu, dosya transferleri sırasında dosya bütünlüğünü doğrulamak için de kullanabilirsiniz.