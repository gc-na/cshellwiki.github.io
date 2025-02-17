# [Linux] Bash sha256sum Kullanımı: Dosyaların SHA-256 Hash Değerini Hesaplama

## Genel Bakış
`sha256sum` komutu, dosyaların SHA-256 hash değerlerini hesaplamak için kullanılır. Bu hash değeri, dosyanın içeriğini temsil eden benzersiz bir dizi oluşturur ve dosyanın bütünlüğünü kontrol etmek için sıklıkla kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
sha256sum [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-b`, `--binary`: İkili dosyalar için hash hesaplamak üzere kullanılır.
- `-c`, `--check`: Daha önce hesaplanmış hash değerlerini kontrol etmek için kullanılır.
- `-h`, `--help`: Komut hakkında yardım bilgilerini gösterir.
- `-o`, `--output`: Çıktının yazılacağı dosyayı belirtir.

## Yaygın Örnekler
Aşağıda `sha256sum` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Bir Dosyanın SHA-256 Hash Değerini Hesaplama
```bash
sha256sum dosya.txt
```

### 2. Birden Fazla Dosyanın Hash Değerlerini Hesaplama
```bash
sha256sum dosya1.txt dosya2.txt
```

### 3. Hash Değerlerini Bir Dosyaya Yazma
```bash
sha256sum dosya.txt > hash_degerleri.txt
```

### 4. Daha Önce Hesaplanmış Hash Değerlerini Kontrol Etme
```bash
sha256sum -c hash_degerleri.txt
```

## İpuçları
- Hash değerlerini kontrol etmek için, her zaman hash değerlerini bir dosyaya kaydedin ve bu dosyayı daha sonra kontrol edin.
- İkili dosyalar için `-b` seçeneğini kullanmayı unutmayın, aksi takdirde yanlış sonuçlar alabilirsiniz.
- Hash değerlerini karşılaştırarak dosyaların değiştirilip değiştirilmediğini kolayca kontrol edebilirsiniz.