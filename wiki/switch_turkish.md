# [Linux] Bash switch Kullanımı: Komutları değiştirme

## Genel Bakış
`switch` komutu, belirli bir koşula bağlı olarak farklı komutların çalıştırılmasını sağlayan bir yapıdır. Genellikle birden fazla durumu kontrol etmek ve her duruma göre farklı işlemler gerçekleştirmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
switch [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Belirtilen ifadeyi değerlendirmek için kullanılır.
- `-d`: Varsayılan durumu belirtir.
- `-h`: Yardım bilgilerini görüntüler.

## Yaygın Örnekler
Aşağıda `switch` komutunun bazı pratik örnekleri bulunmaktadır:

### Örnek 1: Basit bir switch yapısı
```bash
case $1 in
    "bir")
        echo "Bir seçildi."
        ;;
    "iki")
        echo "İki seçildi."
        ;;
    *)
        echo "Geçersiz seçim."
        ;;
esac
```

### Örnek 2: Kullanıcıdan seçim alma
```bash
echo "Lütfen bir sayı girin (1-3):"
read sayi
case $sayi in
    1)
        echo "Seçim 1."
        ;;
    2)
        echo "Seçim 2."
        ;;
    3)
        echo "Seçim 3."
        ;;
    *)
        echo "Geçersiz seçim."
        ;;
esac
```

### Örnek 3: Dosya uzantısına göre işlem yapma
```bash
dosya="belge.txt"
case "${dosya##*.}" in
    "txt")
        echo "Bu bir metin dosyası."
        ;;
    "jpg" | "png")
        echo "Bu bir resim dosyası."
        ;;
    *)
        echo "Tanımlanamayan dosya türü."
        ;;
esac
```

## İpuçları
- `switch` yapısını kullanırken her durumu net bir şekilde tanımlamak, kodun okunabilirliğini artırır.
- `case` yapısında her durumu bitirmek için `;;` kullanmayı unutmayın.
- Kullanıcıdan alınan girdileri doğrulamak, hatalı seçimlerin önüne geçer.