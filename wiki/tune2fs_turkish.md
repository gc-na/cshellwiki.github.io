# [Linux] C Shell (csh) tune2fs Kullanımı: Dosya sistemi ayarlarını değiştirme

## Genel Bakış
`tune2fs`, Linux işletim sistemlerinde kullanılan bir komuttur ve ext2, ext3 ve ext4 dosya sistemlerinin ayarlarını değiştirmek için kullanılır. Bu komut, dosya sisteminin performansını ve davranışını optimize etmek amacıyla çeşitli parametreleri ayarlamanıza olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
tune2fs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c <değer>`: Dosya sisteminin maksimum dosya sayısını ayarlar.
- `-i <değer>`: Dosya sisteminin kontrol aralığını ayarlar.
- `-m <yüzde>`: Kullanıcı alanı için ayrılan minimum yüzdelik alanı ayarlar.
- `-O <özellik>`: Dosya sistemine yeni özellikler ekler.
- `-L <etiket>`: Dosya sistemine bir etiket atar.

## Yaygın Örnekler
Aşağıda `tune2fs` komutunun bazı pratik örnekleri verilmiştir:

1. **Maksimum dosya sayısını ayarlama:**
   ```bash
   tune2fs -c 100000 /dev/sda1
   ```

2. **Kontrol aralığını ayarlama:**
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. **Minimum kullanıcı alanı yüzdesini ayarlama:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Dosya sistemine etiket atama:**
   ```bash
   tune2fs -L mylabel /dev/sda1
   ```

5. **Yeni özellik ekleme:**
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

## İpuçları
- `tune2fs` komutunu kullanmadan önce dosya sisteminin yedeğini almak iyi bir uygulamadır.
- Değişikliklerin etkili olması için dosya sisteminin montajının kaldırılması gerekebilir.
- Herhangi bir değişiklik yapmadan önce mevcut ayarları görmek için `tune2fs -l /dev/sda1` komutunu kullanabilirsiniz.