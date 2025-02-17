# [Linux] Bash tput Kullanımı: Terminalde metin biçimlendirme ve renk ayarlama

## Genel Bakış
`tput` komutu, terminalde metin biçimlendirmek ve renk ayarlarını değiştirmek için kullanılır. Bu komut, terminalin özelliklerini kontrol etmenizi ve terminaldeki çıktıyı özelleştirmenizi sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
tput [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `setaf [numara]`: Metin rengini ayarlar. Renk numarası 0-7 arasında olabilir.
- `setab [numara]`: Arka plan rengini ayarlar. Renk numarası 0-7 arasında olabilir.
- `bold`: Metni kalın yapar.
- `underline`: Metni altı çizili yapar.
- `reset`: Tüm biçimlendirmeleri sıfırlar.

## Yaygın Örnekler
Aşağıda `tput` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Metin Rengini Ayarlama
Kırmızı metin rengi ayarlamak için:

```bash
tput setaf 1
echo "Bu kırmızı bir metin."
tput sgr0  # Biçimlendirmeyi sıfırlar
```

### 2. Arka Plan Rengini Ayarlama
Yeşil arka plan rengi ayarlamak için:

```bash
tput setab 2
echo "Bu yeşil arka planlı bir metin."
tput sgr0  # Biçimlendirmeyi sıfırlar
```

### 3. Kalın Metin
Metni kalın yapmak için:

```bash
tput bold
echo "Bu kalın bir metin."
tput sgr0  # Biçimlendirmeyi sıfırlar
```

### 4. Altı Çizili Metin
Altı çizili metin oluşturmak için:

```bash
tput underline
echo "Bu altı çizili bir metin."
tput sgr0  # Biçimlendirmeyi sıfırlar
```

## İpuçları
- `tput` komutunu kullanmadan önce terminalinizin desteklediği renk ve biçimlendirme seçeneklerini kontrol edin.
- Biçimlendirmeleri sıfırlamak için `tput sgr0` kullanmayı unutmayın; aksi takdirde, sonraki metinler de biçimlendirilmiş olabilir.
- Renk ve stil kombinasyonlarını deneyerek terminal çıktınızı daha okunabilir hale getirin.