# [Linux] Bash unset Kullanımı: Değişkenleri Silme

## Genel Bakış
`unset` komutu, Bash kabuğunda tanımlı olan değişkenleri veya fonksiyonları silmek için kullanılır. Bu komut, bir değişkenin veya fonksiyonun bellekteki yerini temizleyerek, daha fazla kullanılmasını engeller.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
unset [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-f`: Belirtilen bir fonksiyonu silmek için kullanılır.
- `-v`: Belirtilen bir değişkeni silmek için kullanılır. Bu seçenek varsayılan olarak kullanılır.

## Yaygın Örnekler
Aşağıda `unset` komutunun bazı pratik örnekleri bulunmaktadır:

### Değişken Silme
Bir değişkeni silmek için:

```bash
my_var="Merhaba"
echo $my_var  # Çıktı: Merhaba
unset my_var
echo $my_var  # Çıktı: (boş)
```

### Fonksiyon Silme
Bir fonksiyonu silmek için:

```bash
my_function() {
    echo "Bu bir fonksiyon."
}
my_function  # Çıktı: Bu bir fonksiyon.
unset -f my_function
my_function  # Çıktı: bash: my_function: command not found
```

### Birden Fazla Değişken Silme
Birden fazla değişkeni aynı anda silmek için:

```bash
var1="Değer 1"
var2="Değer 2"
unset var1 var2
echo $var1  # Çıktı: (boş)
echo $var2  # Çıktı: (boş)
```

## İpuçları
- `unset` komutunu dikkatli kullanın; bir değişkeni sildiğinizde geri alınamaz.
- Değişkenlerinizi silmeden önce, onları kullanıp kullanmadığınızı kontrol edin.
- `unset` komutunu bir script içinde kullanıyorsanız, değişkenlerin kapsamını göz önünde bulundurun; global ve yerel değişkenler arasında farklılıklar olabilir.