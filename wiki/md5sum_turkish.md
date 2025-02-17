# [Linux] Bash md5sum Kullanımı: Dosya bütünlüğünü kontrol etme

## Genel Bakış
`md5sum` komutu, dosyaların MD5 hash değerlerini hesaplamak ve doğrulamak için kullanılır. Bu, dosyaların bütünlüğünü kontrol etmek ve dosya değişikliklerini tespit etmek için yaygın bir yöntemdir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
md5sum [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-b`, `--binary`: İkili dosyalar için kullanılır.
- `-c`, `--check`: MD5 hash değerlerini kontrol etmek için kullanılır.
- `-t`, `--text`: Metin dosyaları için kullanılır (varsayılan).
- `--quiet`: Sadece hatalı dosyaları gösterir.

## Yaygın Örnekler
Aşağıda `md5sum` komutunun bazı pratik kullanımları yer almaktadır:

### 1. Bir dosyanın MD5 hash değerini hesaplama
```bash
md5sum dosya.txt
```

### 2. Birden fazla dosyanın MD5 hash değerlerini hesaplama
```bash
md5sum dosya1.txt dosya2.txt
```

### 3. MD5 hash değerlerini bir dosyaya yazma
```bash
md5sum dosya.txt > hash_degerleri.txt
```

### 4. Hash değerlerini kontrol etme
Önceden hesaplanmış hash değerlerini kontrol etmek için:
```bash
md5sum -c hash_degerleri.txt
```

## İpuçları
- Hash değerlerini kontrol etmek için her zaman bir dosya ile birlikte hash dosyası kullanın.
- Dosyaların bütünlüğünü sağlamak için hash değerlerini düzenli olarak kontrol edin.
- `md5sum` komutunu kullanmadan önce dosyaların yedeğini almak iyi bir uygulamadır.