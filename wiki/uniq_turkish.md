# [Linux] Bash uniq Kullanımı: Tekrar eden satırları kaldırma

## Overview
`uniq` komutu, bir dosyadaki veya bir akıştaki tekrar eden satırları kaldırmak için kullanılır. Genellikle, sıralı verilerle birlikte kullanıldığında etkili olur, çünkü yalnızca ardışık tekrarları kaldırır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
uniq [options] [arguments]
```

## Common Options
- `-c`: Her satırın önüne tekrar sayısını ekler.
- `-d`: Sadece tekrar eden satırları gösterir.
- `-u`: Tekrar etmeyen satırları gösterir.
- `-i`: Büyük/küçük harf duyarsız karşılaştırma yapar.

## Common Examples
Aşağıda `uniq` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Bir dosyadaki tekrar eden satırları kaldırma:**
   ```bash
   uniq dosya.txt
   ```

2. **Tekrar sayısını gösterme:**
   ```bash
   uniq -c dosya.txt
   ```

3. **Sadece tekrar eden satırları gösterme:**
   ```bash
   uniq -d dosya.txt
   ```

4. **Büyük/küçük harf duyarsız karşılaştırma ile tekrarları kaldırma:**
   ```bash
   uniq -i dosya.txt
   ```

## Tips
- `uniq` komutunu kullanmadan önce verilerinizi sıralamak için `sort` komutunu kullanmayı unutmayın; aksi takdirde, yalnızca ardışık tekrarlar kaldırılacaktır.
- Uzun dosyalarla çalışırken, `uniq` komutunu bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz.
- Tekrar eden satırları kaldırdıktan sonra sonuçları incelemek için `less` veya `more` gibi komutları kullanabilirsiniz.