# [Linux] Bash cd Kullanımı: Dizinler arasında geçiş yapma komutu

## Genel Bakış
`cd` komutu, kullanıcıların dosya sisteminde dizinler arasında geçiş yapmalarını sağlar. Bu komut, terminalde çalışırken bulunduğunuz dizini değiştirmenize olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
cd [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `..` : Bir üst dizine geçiş yapar.
- `-` : Önceki dizine geri döner.
- `~` : Kullanıcının ana dizinine geçiş yapar.

## Yaygın Örnekler
Aşağıda `cd` komutunun bazı pratik örnekleri bulunmaktadır:

1. Bir üst dizine geçiş yapmak:
   ```bash
   cd ..
   ```

2. Kullanıcının ana dizinine geçiş yapmak:
   ```bash
   cd ~
   ```

3. Önceki dizine geri dönmek:
   ```bash
   cd -
   ```

4. Belirli bir dizine geçiş yapmak (örneğin, belgeler dizini):
   ```bash
   cd ~/Belgeler
   ```

5. Gösterim için tam yol kullanarak bir dizine geçiş yapmak:
   ```bash
   cd /home/kullanici/Belgeler/Projeler
   ```

## İpuçları
- `cd` komutunu kullanırken, dizin adlarını tam olarak yazmak yerine otomatik tamamlama özelliğinden yararlanmak için `Tab` tuşuna basabilirsiniz.
- Dizin yolunu kısaltmak için `~` sembolünü kullanarak ana dizin altındaki dizinlere hızlıca geçiş yapabilirsiniz.
- Geçiş yaptığınız dizinin içeriğini görmek için `ls` komutunu kullanabilirsiniz.