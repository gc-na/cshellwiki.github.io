# [Linux] Bash lsof Kullanımı: Açık dosyaları listeleme

## Genel Bakış
`lsof` (List Open Files), sistemde açık olan dosyaları ve bu dosyaları kullanan süreçleri listeleyen bir komuttur. Bu komut, dosya tanımlayıcıları, ağ bağlantıları ve daha fazlası hakkında bilgi edinmek için kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
lsof [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-i`: Ağ bağlantılarını listelemek için kullanılır.
- `-u [kullanıcı]`: Belirtilen kullanıcıya ait açık dosyaları gösterir.
- `-p [PID]`: Belirtilen süreç kimliğine (PID) ait açık dosyaları listeler.
- `+D [dizin]`: Belirtilen dizindeki tüm açık dosyaları gösterir.

## Yaygın Örnekler
Aşağıda `lsof` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### Tüm Açık Dosyaları Listeleme
```bash
lsof
```

### Belirli Bir Kullanıcının Açık Dosyalarını Listeleme
```bash
lsof -u kullanıcı_adı
```

### Belirli Bir Sürecin Açık Dosyalarını Listeleme
```bash
lsof -p 1234
```

### Ağ Bağlantılarını Listeleme
```bash
lsof -i
```

### Belirli Bir Dizin Altındaki Açık Dosyaları Listeleme
```bash
lsof +D /path/to/directory
```

## İpuçları
- `lsof` komutunu `grep` ile birleştirerek belirli dosya türlerini veya süreçleri filtreleyebilirsiniz. Örneğin:
  ```bash
  lsof | grep .txt
  ```
- `lsof` çıktısını bir dosyaya yönlendirmek için `>` operatörünü kullanabilirsiniz:
  ```bash
  lsof > acik_dosyalar.txt
  ```
- `lsof` komutunu çalıştırmak için genellikle yönetici (root) izinlerine ihtiyaç duyulabilir, bu nedenle `sudo` kullanmayı unutmayın.