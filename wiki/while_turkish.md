# [Linux] Bash while Kullanımı: Döngüsel işlemler gerçekleştirme

## Overview
`while` komutu, belirli bir koşul doğru olduğu sürece bir komut veya komutlar dizisini tekrar eden bir döngü oluşturur. Bu, belirli bir koşul sağlandığı sürece işlemlerin devam etmesini sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
while [koşul]
do
    [komutlar]
done
```

## Common Options
`while` komutunun kendisi için özel bir seçenek yoktur, ancak koşul ifadelerinde kullanılabilecek bazı yaygın operatörler şunlardır:
- `-eq`: Eşitlik kontrolü.
- `-ne`: Eşit olmama kontrolü.
- `-lt`: Küçüklük kontrolü.
- `-le`: Küçük veya eşitlik kontrolü.
- `-gt`: Büyüklük kontrolü.
- `-ge`: Büyük veya eşitlik kontrolü.

## Common Examples

### Örnek 1: Basit bir sayma döngüsü
Aşağıdaki örnekte, 1'den 5'e kadar olan sayılar yazdırılmaktadır.

```bash
count=1
while [ $count -le 5 ]
do
    echo $count
    count=$((count + 1))
done
```

### Örnek 2: Kullanıcıdan giriş alma
Bu örnekte, kullanıcıdan "exit" yazana kadar sürekli olarak giriş alınmaktadır.

```bash
input=""
while [ "$input" != "exit" ]
do
    read -p "Bir şey yazın (çıkmak için 'exit' yazın): " input
    echo "Girdiğiniz: $input"
done
```

### Örnek 3: Dosya kontrolü
Aşağıdaki örnekte, belirli bir dosya mevcut olduğu sürece döngü devam eder.

```bash
filename="test.txt"
while [ ! -f "$filename" ]
do
    echo "$filename dosyası henüz mevcut değil."
    sleep 2
done
echo "$filename dosyası mevcut!"
```

## Tips
- Koşul ifadelerinizi dikkatlice oluşturun; sonsuz döngülerden kaçının.
- `sleep` komutu kullanarak döngülerinizi yavaşlatabilir ve sistem kaynaklarını koruyabilirsiniz.
- Giriş almak için `read` komutunu kullanarak kullanıcı etkileşimini artırabilirsiniz.