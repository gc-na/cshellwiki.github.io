# [Linux] Bash shift Kullanımı: Komut satırındaki argümanları kaydırma

## Overview
`shift` komutu, Bash kabuğunda komut satırındaki argümanları sola kaydırmak için kullanılır. Bu, birden fazla argümanla çalışırken, ilk argümanı kaldırarak geri kalan argümanlara erişimi kolaylaştırır.

## Usage
Temel sözdizimi şu şekildedir:

```bash
shift [n]
```

Burada `n`, kaç adet argümanın kaydırılacağını belirtir. Eğer `n` verilmezse, varsayılan olarak 1 kabul edilir.

## Common Options
- `n`: Kaç argümanın kaydırılacağını belirtir. Örneğin, `shift 2` komutu, ilk iki argümanı kaydırır.

## Common Examples

### Örnek 1: Basit Kaydırma
Aşağıdaki örnekte, iki argümanla `shift` komutunun nasıl çalıştığını görebilirsiniz.

```bash
#!/bin/bash
echo "İlk argüman: $1"
echo "İkinci argüman: $2"
shift
echo "Kaydırmadan sonra ilk argüman: $1"
```

Bu script çalıştırıldığında, ilk argüman kaydırılır ve ikinci argüman birinci argüman haline gelir.

### Örnek 2: Birden Fazla Argümanı Kaydırma
Birden fazla argümanı kaydırmak için `n` parametresini kullanabilirsiniz.

```bash
#!/bin/bash
echo "Argümanlar: $@"
shift 2
echo "Kaydırmadan sonra argümanlar: $@"
```

Bu script, iki argümanı kaydırarak geri kalan argümanları gösterir.

### Örnek 3: Döngü ile Argümanları İşleme
`shift` komutunu bir döngü içinde kullanarak tüm argümanları işleyebilirsiniz.

```bash
#!/bin/bash
while [ "$#" -gt 0 ]; do
    echo "İşlenen argüman: $1"
    shift
done
```

Bu script, verilen tüm argümanları sırayla işler.

## Tips
- `shift` komutunu kullanmadan önce argüman sayısını kontrol etmek için `"$#"` değişkenini kullanabilirsiniz.
- Argümanları kaydırmadan önce önemli bilgileri kaydetmek istiyorsanız, argümanları bir diziye atayarak daha sonra kullanabilirsiniz.
- `shift` komutunu kullanırken dikkatli olun; yanlış kaydırma, beklenmeyen sonuçlara yol açabilir.