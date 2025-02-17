# [Linux] Bash iconv Kullanımı: Karakter kodlamalarını dönüştürme aracı

## Genel Bakış
`iconv`, bir dosyanın karakter kodlamasını dönüştürmek için kullanılan bir komut satırı aracıdır. Farklı karakter setleri arasında dönüşüm yaparak, metin dosyalarının uyumluluğunu artırır ve veri kaybını önler.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
iconv [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f, --from-code`: Dönüştürülecek dosyanın mevcut karakter kodlamasını belirtir.
- `-t, --to-code`: Dönüştürülmek istenen hedef karakter kodlamasını belirtir.
- `-o, --output`: Dönüştürülmüş çıktının kaydedileceği dosya adını belirtir.
- `-l, --list`: Desteklenen karakter kodlamalarının listesini gösterir.

## Yaygın Örnekler
Aşağıda `iconv` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. UTF-8'den ISO-8859-1'e dönüştürme:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 dosya.txt -o dosya_iso.txt
   ```

2. UTF-16'dan UTF-8'e dönüştürme:
   ```bash
   iconv -f UTF-16 -t UTF-8 dosya_utf16.txt -o dosya_utf8.txt
   ```

3. Desteklenen karakter kodlamalarını listeleme:
   ```bash
   iconv -l
   ```

4. Standart çıktıya yazdırma (dosya kaydetmeden):
   ```bash
   iconv -f WINDOWS-1254 -t UTF-8 dosya.txt
   ```

## İpuçları
- Dönüştürme işlemi yapmadan önce dosyanızın mevcut karakter kodlamasını kontrol edin.
- Dönüştürme işlemi sırasında veri kaybını önlemek için hedef kodlamanın kaynak kodlamayla uyumlu olduğundan emin olun.
- `iconv` komutunu bir betik içinde kullanarak toplu dosya dönüştürmeleri gerçekleştirebilirsiniz.