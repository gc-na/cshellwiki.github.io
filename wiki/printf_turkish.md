# [Linux] Bash printf Kullanımı: Formatlı çıktı üretme aracı

## Overview
`printf` komutu, formatlı metin çıktısı üretmek için kullanılan bir Bash komutudur. C dilindeki `printf` fonksiyonuna benzer şekilde çalışarak, belirli bir formatta verileri ekrana yazdırmanıza olanak tanır.

## Usage
Temel sözdizimi şu şekildedir:
```bash
printf [seçenekler] [argümanlar]
```

## Common Options
- `-v`: Değişkeni formatlı çıktı olarak ayarlamak için kullanılır.
- `-f`: Format belirtmek için kullanılır.
- `-n`: Yeni satıra geçmeden çıktı üretir.

## Common Examples
Aşağıda `printf` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### Örnek 1: Basit metin yazdırma
```bash
printf "Merhaba, Dünya!\n"
```

### Örnek 2: Değişken ile yazdırma
```bash
isim="Ali"
printf "Merhaba, %s!\n" "$isim"
```

### Örnek 3: Sayı formatlama
```bash
printf "Sayı: %d\n" 42
```

### Örnek 4: Ondalık sayılar
```bash
printf "Ondalık: %.2f\n" 3.14159
```

### Örnek 5: Birden fazla argüman
```bash
printf "Ad: %s, Yaş: %d\n" "Ayşe" 30
```

## Tips
- Format belirlerken `%` işaretini kullanmayı unutmayın; bu, hangi tür verinin yazdırılacağını belirtir.
- `printf` komutu, `echo` komutuna göre daha fazla kontrol ve formatlama seçeneği sunar, bu nedenle karmaşık çıktılar için tercih edilebilir.
- Çıktıyı dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz. Örneğin: `printf "Veri" > dosya.txt`