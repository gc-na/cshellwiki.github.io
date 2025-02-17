# [macOS] Bash brew kullanımı: Paket yönetimi aracı

## Genel Bakış
`brew` komutu, macOS üzerinde yazılım paketlerini yönetmek için kullanılan bir araçtır. Homebrew adıyla bilinen bu paket yöneticisi, kullanıcıların kolayca yazılım yüklemesine, güncellemesine ve kaldırmasına olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
brew [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `install`: Belirtilen paketi yükler.
- `uninstall`: Belirtilen paketi kaldırır.
- `update`: Homebrew ve yüklü paketlerin güncellemelerini kontrol eder.
- `upgrade`: Yüklü paketleri en son sürüme günceller.
- `list`: Yüklenmiş paketlerin listesini gösterir.

## Yaygın Örnekler
Aşağıda `brew` komutunun bazı pratik kullanımları verilmiştir:

### 1. Bir paket yüklemek
```bash
brew install wget
```
Bu komut, `wget` adlı paketi yükler.

### 2. Bir paketi kaldırmak
```bash
brew uninstall wget
```
Bu komut, daha önce yüklenmiş olan `wget` paketini kaldırır.

### 3. Paket güncellemelerini kontrol etmek
```bash
brew update
```
Bu komut, Homebrew ve yüklü paketlerin güncellemelerini kontrol eder.

### 4. Yüklü paketleri güncellemek
```bash
brew upgrade
```
Bu komut, sistemde yüklü olan tüm paketleri en son sürümlerine günceller.

### 5. Yüklenmiş paketlerin listesini görüntülemek
```bash
brew list
```
Bu komut, sistemde yüklü olan tüm Homebrew paketlerini listeler.

## İpuçları
- Homebrew'ü güncel tutmak için düzenli olarak `brew update` komutunu çalıştırın.
- Yüklemek istediğiniz paketlerin bağımlılıklarını kontrol etmek için `brew info [paket_adı]` komutunu kullanın.
- Paketleri kaldırmadan önce, hangi dosyaların yüklendiğini görmek için `brew list [paket_adı]` komutunu kullanabilirsiniz.