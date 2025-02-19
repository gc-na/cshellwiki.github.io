# [Linux] C Shell (csh) mount Kullanımı: Dosya sistemlerini bağlama

## Overview
`mount` komutu, bir dosya sistemini belirli bir dizine bağlamak için kullanılır. Bu işlem, dosya sisteminin içeriğine erişimi sağlar ve sistemin dosya yapısında görünür hale getirir.

## Usage
Temel sözdizimi şu şekildedir:
```
mount [options] [arguments]
```

## Common Options
- `-t type`: Bağlanacak dosya sisteminin türünü belirtir.
- `-o options`: Bağlama işlemi için özel seçenekler tanımlar.
- `-r`: Dosya sistemini sadece okunur modda bağlar.
- `-w`: Dosya sistemini yazılabilir modda bağlar.

## Common Examples
Aşağıda `mount` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. Bir dosya sistemini bağlamak:
   ```bash
   mount /dev/sdb1 /mnt/mydrive
   ```

2. Belirli bir dosya sistemi türü ile bağlamak:
   ```bash
   mount -t ext4 /dev/sdb1 /mnt/mydrive
   ```

3. Sadece okunur modda bağlamak:
   ```bash
   mount -o ro /dev/sdb1 /mnt/mydrive
   ```

4. Bir ağ dosya sistemini bağlamak (NFS örneği):
   ```bash
   mount -t nfs server:/export /mnt/nfs
   ```

## Tips
- Bağlama işlemi yapmadan önce, hedef dizinin var olduğundan emin olun.
- Dosya sistemini bağladıktan sonra, içeriğini kontrol etmek için `ls` komutunu kullanabilirsiniz.
- Bağlı dosya sistemlerini görmek için `mount` komutunu tek başına çalıştırabilirsiniz.