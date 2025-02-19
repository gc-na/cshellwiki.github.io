# [Linux] C Shell (csh) shift Kullanımı: Argümanları sola kaydırma

## Overview
`shift` komutu, C Shell (csh) ortamında, komut satırında tanımlı argümanları sola kaydırmak için kullanılır. Bu, argümanların sırasını değiştirerek, belirli bir argümanı işlemek için diğerlerini kolayca atlamanızı sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```csh
shift [options] [arguments]
```

## Common Options
- `n`: Argümanları `n` kadar sola kaydırır. Eğer `n` belirtilmezse, varsayılan olarak 1 kaydırma yapılır.

## Common Examples

### Örnek 1: Basit kaydırma
Aşağıdaki komut, ilk argümanı kaydırarak ikinci argümanı ilk pozisyona getirir.

```csh
set args = (arg1 arg2 arg3)
echo $args[1]  # Çıktı: arg1
shift
echo $args[1]  # Çıktı: arg2
```

### Örnek 2: Birden fazla kaydırma
`shift` komutunu birden fazla argümanı kaydırmak için kullanabilirsiniz.

```csh
set args = (arg1 arg2 arg3 arg4)
echo $args[1]  # Çıktı: arg1
shift 2
echo $args[1]  # Çıktı: arg3
```

### Örnek 3: Argümanları döngü ile işleme
`shift` komutunu bir döngü içinde kullanarak tüm argümanları işleyebilirsiniz.

```csh
set args = (arg1 arg2 arg3 arg4)
while ($#args > 0)
    echo $args[1]
    shift
end
```

## Tips
- `shift` komutunu kullanmadan önce argümanların sayısını kontrol etmek için `$#args` ifadesini kullanın.
- Argümanları kaydırmadan önce, hangi argümanın işleneceğini belirlemek için `echo` komutunu kullanarak argümanları görüntüleyin.
- `shift` komutunu, scriptlerinizde argümanları yönetmek için etkili bir yöntem olarak kullanabilirsiniz.