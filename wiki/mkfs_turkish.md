# [Linux] Bash mkfs Kullanımı: Dosya sistemi oluşturma aracı

## Overview
`mkfs`, bir dosya sistemini oluşturmak için kullanılan bir Bash komutudur. Bu komut, belirli bir depolama aygıtında veya dosya sisteminde yeni bir dosya sistemi oluşturmanıza olanak tanır.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
mkfs [options] [arguments]
```

## Common Options
- `-t`: Oluşturulacak dosya sisteminin türünü belirtir (örneğin, ext4, vfat).
- `-L`: Dosya sistemine bir etiket atar.
- `-n`: Dosya sistemini oluştururken herhangi bir yazma işlemi yapmadan sadece test eder.
- `-V`: Ayrıntılı bilgi verir; işlem sırasında hangi adımların atıldığını gösterir.

## Common Examples
Aşağıda `mkfs` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **ext4 dosya sistemi oluşturma:**
   ```bash
   mkfs -t ext4 /dev/sdb1
   ```

2. **vfat dosya sistemi oluşturma ve etiket verme:**
   ```bash
   mkfs -t vfat -L MYLABEL /dev/sdc1
   ```

3. **Dosya sistemini test etme:**
   ```bash
   mkfs -n -t ext4 /dev/sdd1
   ```

4. **Ayrıntılı bilgi ile ext3 dosya sistemi oluşturma:**
   ```bash
   mkfs -V -t ext3 /dev/sde1
   ```

## Tips
- `mkfs` komutunu kullanmadan önce, oluşturmak istediğiniz dosya sisteminin üzerine yazılacak olan aygıtın yedeğini aldığınızdan emin olun.
- Yanlış bir aygıtı seçmek, verilerinizi kaybetmenize neden olabilir; bu nedenle dikkatli olun.
- Dosya sistemi oluşturduktan sonra, bu dosya sistemini bağlamak için `mount` komutunu kullanmayı unutmayın.