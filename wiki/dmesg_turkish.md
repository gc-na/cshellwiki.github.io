# [Linux] Bash dmesg Kullanımı: Çekirdek döküm bilgilerini görüntüleme

## Genel Bakış
`dmesg` komutu, Linux çekirdeği tarafından üretilen mesajları görüntülemek için kullanılır. Bu komut, sistem başlangıcında ve donanım ile ilgili olaylarda oluşan log kayıtlarını gösterir. Genellikle, sistem hatalarını veya donanım sorunlarını teşhis etmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
dmesg [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-C`: Dmesg tamponunu temizler.
- `-c`: Dmesg tamponunu temizler ve mevcut içeriği gösterir.
- `-n <seviye>`: Belirtilen seviyeden daha düşük olan mesajları gösterir.
- `-T`: Zaman damgalarını okunabilir bir formatta gösterir.
- `--help`: Komut hakkında yardım bilgisi gösterir.

## Yaygın Örnekler
Aşağıda `dmesg` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Tüm dmesg mesajlarını görüntüleme
```bash
dmesg
```

### 2. Zaman damgalarını okunabilir formatta gösterme
```bash
dmesg -T
```

### 3. Dmesg tamponunu temizleme
```bash
dmesg -C
```

### 4. Belirli bir hata seviyesindeki mesajları görüntüleme
```bash
dmesg -n 3
```

### 5. Dmesg çıktısını bir dosyaya yönlendirme
```bash
dmesg > dmesg_output.txt
```

## İpuçları
- `dmesg` çıktısını daha okunabilir hale getirmek için `less` veya `more` komutları ile birleştirebilirsiniz:
  ```bash
  dmesg | less
  ```
- Belirli bir anahtar kelimeyi aramak için `grep` ile birlikte kullanabilirsiniz:
  ```bash
  dmesg | grep hata
  ```
- Sistem başlangıcında oluşan hataları incelemek için `dmesg` çıktısını düzenli olarak kontrol etmek iyi bir uygulamadır.