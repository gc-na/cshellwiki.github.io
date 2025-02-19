# [Linux] C Shell (csh) cp Kullanımı: Dosya kopyalama komutu

## Genel Bakış
`cp` komutu, bir veya daha fazla dosyayı veya dizini başka bir konuma kopyalamak için kullanılır. Bu komut, dosyaların yedeğini almak veya dosyaları bir yerden başka bir yere taşımak için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```
cp [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Hedef dosya zaten varsa, üzerine yazmadan önce onay ister.
- `-r`: Dizinleri kopyalamak için kullanılır. Alt dizinleri ve dosyaları da kopyalar.
- `-u`: Sadece kaynak dosya hedef dosyadan daha yeni ise kopyalar.
- `-v`: Kopyalama işlemi sırasında hangi dosyaların kopyalandığını gösterir.

## Yaygın Örnekler
Aşağıda `cp` komutunun bazı pratik kullanım örnekleri verilmiştir:

1. Basit bir dosya kopyalama:
   ```bash
   cp dosya.txt yedek_dosya.txt
   ```

2. Bir dizini ve içindeki tüm dosyaları kopyalama:
   ```bash
   cp -r kaynak_dizin/ hedef_dizin/
   ```

3. Hedef dosya zaten varsa onay istemek:
   ```bash
   cp -i dosya.txt yedek_dosya.txt
   ```

4. Sadece daha yeni dosyaları kopyalama:
   ```bash
   cp -u dosya.txt yedek_dosya.txt
   ```

5. Kopyalama işlemi sırasında hangi dosyaların kopyalandığını görmek:
   ```bash
   cp -v dosya.txt yedek_dosya.txt
   ```

## İpuçları
- `-r` seçeneğini kullanarak dizinleri kopyalarken, hedef dizinin var olduğundan emin olun ya da `-p` seçeneği ile dosya izinlerini koruyun.
- Kopyalama işlemi yapmadan önce `ls` komutunu kullanarak hedef dizinin içeriğini kontrol edin.
- Önemli dosyaları kopyalarken `-i` seçeneğini kullanarak yanlışlıkla üzerine yazmayı önleyin.