# [Linux] Bash tune2fs Kullanımı: Dosya sistemi ayarlarını değiştirme

## Genel Bakış
`tune2fs`, Linux işletim sistemlerinde kullanılan bir komut olup, ext2, ext3 ve ext4 dosya sistemlerinin ayarlarını değiştirmek için kullanılır. Bu komut, dosya sisteminin performansını ve güvenliğini optimize etmek amacıyla çeşitli parametrelerin ayarlanmasına olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
tune2fs [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c <değer>`: Dosya sisteminin maksimum dosya sayısını ayarlar.
- `-i <tarih>`: Dosya sistemi kontrolü için minimum süreyi ayarlar.
- `-m <yüzde>`: Kullanıcı alanı için ayrılan minimum yüzdelik alanı ayarlar.
- `-O <özellik>`: Dosya sistemine yeni özellikler ekler.
- `-L <etiket>`: Dosya sistemine bir etiket atar.

## Yaygın Örnekler
Aşağıda `tune2fs` komutunun bazı pratik örnekleri verilmiştir:

1. **Dosya sisteminin maksimum dosya sayısını ayarlamak:**
   ```bash
   tune2fs -c 50 /dev/sda1
   ```

2. **Dosya sistemi kontrolü için minimum süreyi ayarlamak:**
   ```bash
   tune2fs -i 2w /dev/sda1
   ```

3. **Kullanıcı alanı için minimum yüzdelik alanı ayarlamak:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Dosya sistemine yeni bir etiket atamak:**
   ```bash
   tune2fs -L mylabel /dev/sda1
   ```

5. **Dosya sistemine yeni bir özellik eklemek:**
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

## İpuçları
- `tune2fs` komutunu kullanmadan önce dosya sisteminin yedeğini almak iyi bir uygulamadır.
- Komutları çalıştırmadan önce, dosya sisteminin durumunu kontrol etmek için `dumpe2fs` komutunu kullanabilirsiniz.
- Değişikliklerin etkili olabilmesi için dosya sistemini yeniden monte etmeniz gerekebilir.