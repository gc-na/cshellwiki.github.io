# [Linux] Bash dpkg Kullanımı: Paket yönetimi aracı

## Genel Bakış
`dpkg`, Debian tabanlı sistemlerde (örneğin, Ubuntu) kullanılan bir paket yönetim aracıdır. Bu komut, .deb uzantılı paketleri kurmak, kaldırmak ve yönetmek için kullanılır. `dpkg`, sistemde yüklü olan paketler hakkında bilgi almanıza ve paketleri manuel olarak yönetmenize olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
dpkg [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`, `--install`: Belirtilen .deb paketini kurar.
- `-r`, `--remove`: Belirtilen paketi kaldırır.
- `-l`, `--list`: Yüklü paketlerin listesini gösterir.
- `-s`, `--status`: Belirtilen paketin durumunu gösterir.
- `-c`, `--contents`: Belirtilen paketin içeriğini listeler.

## Yaygın Örnekler
1. Bir .deb paketini kurmak için:
   ```bash
   sudo dpkg -i paket_adi.deb
   ```

2. Yüklü paketleri listelemek için:
   ```bash
   dpkg -l
   ```

3. Belirli bir paketin durumunu kontrol etmek için:
   ```bash
   dpkg -s paket_adi
   ```

4. Bir paketin içeriğini görüntülemek için:
   ```bash
   dpkg -c paket_adi.deb
   ```

5. Bir paketi kaldırmak için:
   ```bash
   sudo dpkg -r paket_adi
   ```

## İpuçları
- `dpkg` ile kurulum sırasında bağımlılık sorunları yaşayabilirsiniz. Bu durumda, `apt-get install -f` komutunu kullanarak eksik bağımlılıkları çözebilirsiniz.
- Paketleri kurmadan önce, paket dosyasının doğru ve güvenilir bir kaynaktan geldiğinden emin olun.
- `dpkg` komutunu kullanırken `sudo` ile çalıştırmayı unutmayın, çünkü çoğu işlem için yönetici yetkileri gereklidir.