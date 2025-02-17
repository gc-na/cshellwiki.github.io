# [Linux] Bash stty Kullanımı: Terminal ayarlarını yapılandırma

## Genel Bakış
`stty` komutu, terminal ayarlarını yapılandırmak ve kontrol etmek için kullanılır. Bu komut, terminalin davranışını değiştirmek ve giriş/çıkış ayarlarını yönetmek için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
stty [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm terminal ayarlarını gösterir.
- `-g`: Terminal ayarlarını bir dize olarak gösterir, bu dize daha sonra geri yüklenebilir.
- `erase`: Silme karakterini ayarlar.
- `kill`: Satırı silmek için kullanılan karakteri ayarlar.
- `intr`: Kesme karakterini ayarlar.

## Yaygın Örnekler
Aşağıda `stty` komutunun bazı pratik örnekleri bulunmaktadır:

### 1. Tüm Terminal Ayarlarını Görüntüleme
```bash
stty -a
```

### 2. Silme Karakterini Ayarlama
```bash
stty erase ^H
```
Bu komut, silme karakterini `^H` (backspace) olarak ayarlar.

### 3. Kesme Karakterini Ayarlama
```bash
stty intr ^C
```
Bu komut, kesme karakterini `^C` olarak ayarlar.

### 4. Terminal Ayarlarını Dize Olarak Kaydetme
```bash
stty -g > ayarlar.txt
```
Bu komut, mevcut terminal ayarlarını `ayarlar.txt` dosyasına kaydeder.

### 5. Terminal Ayarlarını Geri Yükleme
```bash
stty $(cat ayarlar.txt)
```
Bu komut, daha önce kaydedilmiş ayarları geri yükler.

## İpuçları
- Terminal ayarlarını değiştirmeden önce mevcut ayarları kaydetmek iyi bir uygulamadır.
- `stty` komutunu kullanarak terminalinizin davranışını özelleştirebilir, böylece daha verimli çalışabilirsiniz.
- Değişikliklerinizi test etmek için terminali kapatıp açmayı unutmayın; bazı ayarlar kalıcı olmayabilir.