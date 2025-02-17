# [Linux] Bash grupları kullanım: Kullanıcıların ait olduğu grupları gösterir

## Genel Bakış
`groups` komutu, bir kullanıcının ait olduğu grupları listelemek için kullanılır. Bu komut, kullanıcıların sistemdeki grup üyeliklerini hızlı bir şekilde görüntülemeye olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```
groups [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`, `--help`: Komut hakkında yardım bilgisi gösterir.
- `-n`, `--no-name`: Grupların isimlerini değil, grup kimliklerini (GID) gösterir.

## Yaygın Örnekler
Aşağıda `groups` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Mevcut Kullanıcının Gruplarını Gösterme**
   ```bash
   groups
   ```

2. **Belirli Bir Kullanıcının Gruplarını Gösterme**
   ```bash
   groups kullanıcı_adı
   ```

3. **Grupların GID'lerini Gösterme**
   ```bash
   groups -n kullanıcı_adı
   ```

## İpuçları
- `groups` komutunu, kullanıcıların sistemdeki izinlerini yönetirken kontrol etmek için sıkça kullanabilirsiniz.
- Birden fazla kullanıcı için grup bilgilerini almak isterseniz, kullanıcı adlarını boşlukla ayırarak yazabilirsiniz.
- `groups` komutunu, kullanıcıların hangi gruplara ait olduğunu anlamak için bir güvenlik denetimi aracı olarak da kullanabilirsiniz.