# [Linux] Bash fmt Kullanımı: Metin biçimlendirme aracı

## Genel Bakış
`fmt` komutu, metin dosyalarını biçimlendirmek için kullanılan bir araçtır. Bu komut, metin satırlarını belirli bir genişlikte düzenleyerek daha okunabilir hale getirir. Özellikle, metin dosyalarının düzenlenmesi ve okunabilirliğinin artırılması için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
fmt [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-w, --width`: Çıktı satırlarının maksimum genişliğini belirler.
- `-s, --split-only`: Sadece boşluk karakterlerine göre bölme yapar, satırları birleştirmez.
- `-u, --uniform`: Satır uzunluklarını eşit hale getirir.

## Yaygın Örnekler
Aşağıda `fmt` komutunun bazı pratik kullanım örnekleri verilmiştir:

1. **Temel Biçimlendirme:**
   Bir metin dosyasını varsayılan genişlikte biçimlendirmek için:
   ```bash
   fmt metin_dosyası.txt
   ```

2. **Genişlik Belirleme:**
   Çıktı satırlarının maksimum genişliğini 50 karakter olarak ayarlamak için:
   ```bash
   fmt -w 50 metin_dosyası.txt
   ```

3. **Sadece Boşluklarla Bölme:**
   Metni sadece boşluk karakterlerine göre bölmek için:
   ```bash
   fmt -s metin_dosyası.txt
   ```

4. **Eşit Satır Uzunluğu:**
   Satır uzunluklarını eşit hale getirmek için:
   ```bash
   fmt -u metin_dosyası.txt
   ```

## İpuçları
- `fmt` komutunu kullanmadan önce dosyanızın yedeğini almak iyi bir uygulamadır.
- Biçimlendirme işlemi sonrasında metin dosyasını kontrol edin, bazı durumlarda istenmeyen sonuçlar ortaya çıkabilir.
- Genişlik ayarını belirlerken, metnin okunabilirliğini göz önünde bulundurun; çok dar bir genişlik, metni zorlaştırabilir.