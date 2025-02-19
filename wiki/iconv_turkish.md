# [Linux] C Shell (csh) iconv Kullanımı: Karakter kodlamalarını dönüştürme

## Genel Bakış
`iconv` komutu, dosyaların karakter kodlamalarını dönüştürmek için kullanılır. Farklı platformlar veya uygulamalar arasında uyumluluğu sağlamak amacıyla metin dosyalarının karakter setlerini değiştirmek için idealdir.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
iconv [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f, --from-code=KOD`: Dönüştürülecek dosyanın mevcut karakter kodlamasını belirtir.
- `-t, --to-code=KOD`: Dönüştürülen dosyanın hedef karakter kodlamasını belirtir.
- `-o, --output=DOSYA`: Dönüştürülmüş çıktının kaydedileceği dosya adını belirtir.
- `-l, --list`: Desteklenen tüm karakter kodlamalarının listesini gösterir.

## Yaygın Örnekler
Aşağıda `iconv` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. UTF-8'den ISO-8859-1'e dönüştürme:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 dosya.txt -o dosya_donusturulmus.txt
   ```

2. UTF-16 kodlamasındaki bir dosyayı UTF-8'e dönüştürme:
   ```bash
   iconv -f UTF-16 -t UTF-8 dosya_utf16.txt -o dosya_utf8.txt
   ```

3. Desteklenen karakter kodlamalarının listesini görüntüleme:
   ```bash
   iconv -l
   ```

## İpuçları
- Dönüştürme işlemi yapmadan önce dosyanızın yedeğini almayı unutmayın.
- Hedef kodlama ile ilgili sorun yaşamamak için, dönüştürme işlemi yapmadan önce kaynak dosyanın kodlamasını kontrol edin.
- `iconv` komutunu bir betik içinde kullanarak toplu dosya dönüştürmeleri gerçekleştirebilirsiniz.