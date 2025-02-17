# [Linux] Bash case Kullanımı: Değişkenlerin Değerine Göre Koşullu İşlem Yapma

## Genel Bakış
`case` komutu, bir değişkenin değerine göre farklı komutlar çalıştırmak için kullanılan bir kontrol yapısıdır. Bu komut, özellikle birden fazla koşulun kontrol edilmesi gereken durumlarda oldukça kullanışlıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
case [değişken] in
    [değer1])
        # Komutlar
        ;;
    [değer2])
        # Komutlar
        ;;
    *)
        # Varsayılan komutlar
        ;;
esac
```

## Yaygın Seçenekler
`case` komutunun kendine özgü seçenekleri yoktur, ancak kullanıldığı yerlerde değişkenlerin ve değerlerin doğru bir şekilde tanımlanması önemlidir.

## Yaygın Örnekler
Aşağıda `case` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Örnek 1: Basit Değişken Kontrolü
```bash
deger="merhaba"

case $deger in
    "merhaba")
        echo "Selam!"
        ;;
    "güle güle")
        echo "Hoşça kal!"
        ;;
    *)
        echo "Tanımlı bir değer değil."
        ;;
esac
```

### Örnek 2: Kullanıcı Girişi Kontrolü
```bash
read -p "Bir renk girin: " renk

case $renk in
    "kırmızı")
        echo "Kırmızı seçtiniz."
        ;;
    "mavi")
        echo "Mavi seçtiniz."
        ;;
    "yeşil")
        echo "Yeşil seçtiniz."
        ;;
    *)
        echo "Bilinmeyen bir renk."
        ;;
esac
```

### Örnek 3: Dosya Uzantısına Göre İşlem
```bash
dosya="belge.pdf"

case $dosya in
    *.pdf)
        echo "PDF dosyası."
        ;;
    *.txt)
        echo "Metin dosyası."
        ;;
    *.jpg)
        echo "Resim dosyası."
        ;;
    *)
        echo "Bilinmeyen dosya türü."
        ;;
esac
```

## İpuçları
- `case` komutunu kullanırken, her bir durum için `;;` ile sonlandırmayı unutmayın.
- Değişkenlerinizi doğru bir şekilde tanımlamak, `case` komutunun doğru çalışması için kritik öneme sahiptir.
- `*` ifadesini kullanarak varsayılan bir durum belirlemek, beklenmeyen değerler için iyi bir uygulamadır.