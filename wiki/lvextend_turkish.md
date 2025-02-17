# [Linux] Bash lvextend Kullanımı: Mantıksal birimlerin boyutunu artırma

## Genel Bakış
`lvextend` komutu, Linux sistemlerinde mantıksal birimlerin (logical volumes) boyutunu artırmak için kullanılır. Bu komut, mevcut bir mantıksal birime daha fazla alan ekleyerek depolama kapasitesini genişletmek için idealdir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
lvextend [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-L`: Mantıksal birimin yeni boyutunu belirtir. Örneğin, `-L +10G` ile 10 GB eklenir.
- `-l`: Mantıksal birimin boyutunu, fiziksel alan sayısı cinsinden belirtir.
- `-r`: Mantıksal birimi genişlettikten sonra dosya sistemini otomatik olarak yeniden boyutlandırır.

## Yaygın Örnekler
1. Mantıksal birimin boyutunu 10 GB artırmak:
   ```bash
   lvextend -L +10G /dev/vg1/lv1
   ```

2. Mantıksal birimi maksimum boyutuna kadar genişletmek:
   ```bash
   lvextend -l +100%FREE /dev/vg1/lv1
   ```

3. Mantıksal birimi genişletip dosya sistemini otomatik olarak yeniden boyutlandırmak:
   ```bash
   lvextend -r -L +5G /dev/vg1/lv1
   ```

## İpuçları
- Mantıksal birimi genişletmeden önce mevcut alanın yeterli olduğundan emin olun.
- `-r` seçeneğini kullanarak dosya sistemini otomatik olarak yeniden boyutlandırmak, işlemi daha kolay hale getirir.
- Genişletme işlemi sırasında veri kaybını önlemek için her zaman yedekleme yapmayı unutmayın.