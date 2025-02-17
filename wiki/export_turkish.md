# [Linux] Bash export Kullanımı: Ortam Değişkenlerini Ayarlama

## Genel Bakış
`export` komutu, bir ortam değişkenini tanımlamak ve bu değişkeni alt süreçlere iletmek için kullanılır. Bu, shell oturumu boyunca değişkenlerin erişilebilir olmasını sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
export [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-p`: Mevcut ortam değişkenlerini listelemek için kullanılır.
- `VAR=value`: Yeni bir ortam değişkeni tanımlamak için kullanılır.

## Yaygın Örnekler
Aşağıda `export` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Basit bir ortam değişkeni tanımlama
```bash
export MY_VAR="Merhaba Dünya"
```

### 2. Ortam değişkenini kontrol etme
```bash
echo $MY_VAR
```

### 3. Birden fazla ortam değişkeni tanımlama
```bash
export VAR1="Değer1" VAR2="Değer2"
```

### 4. Ortam değişkenlerini listeleme
```bash
export -p
```

## İpuçları
- `export` komutunu kullanarak tanımladığınız değişkenler, yalnızca o shell oturumu ve onun alt süreçleri için geçerlidir.
- Değişkenlerinizi tanımladıktan sonra, bunları kontrol etmek için `echo` komutunu kullanmayı unutmayın.
- Ortam değişkenlerini kalıcı hale getirmek istiyorsanız, bunları `~/.bashrc` veya `~/.bash_profile` dosyalarınıza ekleyin.