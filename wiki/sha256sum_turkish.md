# [Linux] C Shell (csh) sha256sum Kullanımı: Dosyaların SHA-256 Hash Değerini Hesaplama

## Genel Bakış
`sha256sum` komutu, dosyaların SHA-256 hash değerlerini hesaplamak için kullanılır. Bu, dosyaların bütünlüğünü kontrol etmek ve dosya karşılaştırmaları yapmak için yararlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
sha256sum [options] [arguments]
```

## Yaygın Seçenekler
- `-b`: İkili dosyalar için hash hesaplar.
- `-c`: Belirtilen dosyadaki hash değerlerini kontrol eder.
- `-o`: Çıktıyı belirtilen dosyaya yönlendirir.
- `--quiet`: Çıktıyı sessiz modda gösterir, sadece hatalar görünür.

## Yaygın Örnekler

1. Bir dosyanın SHA-256 hash değerini hesaplama:
   ```bash
   sha256sum dosya.txt
   ```

2. Birden fazla dosyanın hash değerlerini hesaplama:
   ```bash
   sha256sum dosya1.txt dosya2.txt
   ```

3. Hash değerlerini bir dosyaya yazma:
   ```bash
   sha256sum dosya.txt > hash_degeri.txt
   ```

4. Hash değerlerini kontrol etme:
   ```bash
   sha256sum -c hash_degeri.txt
   ```

## İpuçları
- Hash değerlerini kontrol etmek için, hash değerlerini ve dosyaları aynı dizinde tutmak iyi bir uygulamadır.
- Dosya bütünlüğünü sağlamak için hash değerlerini düzenli olarak kontrol edin.
- Büyük dosyalarla çalışırken, işlemin tamamlanmasını bekleyin; işlem süresi dosyanın boyutuna bağlıdır.