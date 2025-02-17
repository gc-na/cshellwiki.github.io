# [Linux] Bash tee Kullanımı: Verileri dosyaya ve ekrana yazdırma

## Genel Bakış
`tee` komutu, standart girdi akışını hem ekrana yazdırmak hem de bir veya daha fazla dosyaya yönlendirmek için kullanılır. Bu, komut çıktısını izlemek ve aynı zamanda dosyalara kaydetmek isteyen kullanıcılar için oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```
tee [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`, `--append`: Çıktıyı dosyaya ekler, dosyanın üzerine yazmaz.
- `-i`, `--ignore-interrupts`: Kesme sinyallerini yok sayar.
- `--help`: Komutun kullanımına dair yardım bilgilerini gösterir.
- `--version`: Komutun sürüm bilgilerini gösterir.

## Yaygın Örnekler
Aşağıda `tee` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

1. **Basit Kullanım**: Bir komutun çıktısını hem ekrana yazdırmak hem de bir dosyaya kaydetmek için:
   ```bash
   echo "Merhaba Dünya" | tee dosya.txt
   ```

2. **Dosyaya Ekleme**: Çıktıyı mevcut bir dosyaya eklemek için:
   ```bash
   echo "Yeni Satır" | tee -a dosya.txt
   ```

3. **Birden Fazla Dosyaya Yazma**: Çıktıyı birden fazla dosyaya yönlendirmek için:
   ```bash
   echo "Veri" | tee dosya1.txt dosya2.txt
   ```

4. **Komut Çıktısını Kaydetme**: Bir komutun çıktısını kaydetmek için:
   ```bash
   ls -l | tee liste.txt
   ```

## İpuçları
- `tee` komutunu, uzun süren işlemler sırasında çıktıyı kaydetmek için kullanabilirsiniz.
- Çıktıyı izlemek için `tail -f` komutuyla birlikte kullanmak, dosyadaki güncellemeleri gerçek zamanlı olarak görmenizi sağlar.
- `tee` komutunu bir boru hattında (pipeline) kullanarak, birden fazla komutun çıktısını aynı anda yönetebilirsiniz.