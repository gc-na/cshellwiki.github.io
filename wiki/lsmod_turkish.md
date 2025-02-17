# [Linux] Bash lsmod Kullanımı: Modülleri Listeleme

## Genel Bakış
`lsmod` komutu, Linux işletim sistemlerinde yüklü olan çekirdek modüllerini listelemek için kullanılır. Bu komut, sistemde hangi modüllerin aktif olduğunu ve bunların bellek üzerindeki durumunu gösterir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
lsmod [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`, `--help`: Yardım bilgilerini gösterir.
- `-n`, `--no-heading`: Başlık satırını göstermez.
- `-o`, `--output`: Çıktı formatını belirler.

## Yaygın Örnekler
Aşağıda `lsmod` komutunun bazı pratik örnekleri bulunmaktadır:

1. Tüm yüklü modülleri listeleme:
   ```bash
   lsmod
   ```

2. Başlık satırını gizleyerek modülleri listeleme:
   ```bash
   lsmod -n
   ```

3. Belirli bir modülün durumunu kontrol etme:
   ```bash
   lsmod | grep <modül_adı>
   ```

4. Çıktıyı belirli bir formatta gösterme:
   ```bash
   lsmod --output=modname
   ```

## İpuçları
- `lsmod` çıktısını daha iyi analiz etmek için `grep` komutunu kullanarak belirli modülleri arayabilirsiniz.
- Modül yükleme ve kaldırma işlemleri yapmadan önce `lsmod` ile mevcut durumu kontrol etmek iyi bir uygulamadır.
- Yüklü modüllerin sistem performansına etkisini anlamak için `lsmod` çıktısını düzenli olarak gözden geçirin.