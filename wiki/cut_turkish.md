# [Linux] Bash cut Kullanımı: Metin parçalama aracı

## Genel Bakış
`cut` komutu, metin dosyalarındaki satırları kesmek ve belirli alanları veya karakterleri çıkarmak için kullanılır. Özellikle, belirli bir ayırıcıya göre bölünmüş verilerle çalışırken oldukça faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
cut [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`: Belirtilen alanları seçer. Örneğin, `-f1` ilk alanı, `-f1,3` ise birinci ve üçüncü alanları seçer.
- `-d`: Alanları ayıran karakteri belirtir. Varsayılan ayırıcı tab karakteridir.
- `-c`: Belirtilen karakter aralıklarını seçer. Örneğin, `-c1-5` ilk beş karakteri alır.
- `--complement`: Belirtilen alanların dışındaki tüm alanları seçer.

## Yaygın Örnekler
Aşağıda `cut` komutunun bazı pratik kullanımları bulunmaktadır:

### 1. Bir dosyadan belirli alanları seçme
Bir dosyadaki virgülle ayrılmış verilerden ilk ve üçüncü alanları almak için:
```bash
cut -d',' -f1,3 dosya.txt
```

### 2. Belirli karakter aralıklarını kesme
Bir dosyadaki ilk beş karakteri almak için:
```bash
cut -c1-5 dosya.txt
```

### 3. Birden fazla alanı ayırıcı ile kesme
Bir dosyadaki alanları boşluk ile ayırarak ikinci alanı almak için:
```bash
cut -d' ' -f2 dosya.txt
```

### 4. Tüm alanların dışındaki alanları alma
Bir dosyadaki tüm alanların dışındaki alanları almak için:
```bash
cut -d',' -f2 --complement dosya.txt
```

## İpuçları
- `cut` komutunu kullanmadan önce dosyanızın yapısını kontrol edin; ayırıcı karakterlerin doğru olduğundan emin olun.
- Birden fazla alanı keserken, alan numaralarını virgülle ayırarak belirtin.
- `cut` komutunu diğer komutlarla birleştirmek için `|` (pipe) operatörünü kullanarak daha karmaşık veri işleme görevleri gerçekleştirebilirsiniz. Örneğin, `cat dosya.txt | cut -d',' -f1` ile dosyayı okuduktan sonra kesme işlemi yapabilirsiniz.