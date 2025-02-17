# [Linux] Bash printenv Kullanımı: Ortam değişkenlerini görüntüleme

## Overview
`printenv` komutu, mevcut ortam değişkenlerini görüntülemek için kullanılır. Bu komut, sistemdeki çeşitli ayarları ve bilgileri gösterir.

## Usage
Temel sözdizimi şu şekildedir:

```bash
printenv [options] [arguments]
```

## Common Options
- `-0`, `--null`: Çıktıyı null karakter ile ayırır.
- `NAME`: Belirtilen ortam değişkeninin değerini gösterir. Eğer değişken mevcut değilse, hiçbir şey döndürmez.

## Common Examples
Aşağıda `printenv` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Tüm ortam değişkenlerini görüntüleme:
   ```bash
   printenv
   ```

2. Belirli bir ortam değişkeninin değerini görüntüleme (örneğin, `HOME`):
   ```bash
   printenv HOME
   ```

3. Çıktıyı null karakter ile ayırarak görüntüleme:
   ```bash
   printenv -0
   ```

## Tips
- `printenv` komutunu kullanarak sistemdeki tüm ortam değişkenlerini hızlıca kontrol edebilirsiniz.
- Belirli bir değişkenin varlığını kontrol etmek için `printenv NAME` şeklinde kullanabilirsiniz.
- Ortam değişkenlerini düzenlemek için `export` komutunu kullanmayı unutmayın.