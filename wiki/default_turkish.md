# [Linux] Bash varsayılan komut: Komutları çalıştırma

## Genel Bakış
Bash, Unix benzeri işletim sistemlerinde komutları çalıştırmak için kullanılan bir komut yorumlayıcısıdır. Kullanıcılar, terminal üzerinden çeşitli komutları yazarak sistemle etkileşimde bulunabilirler. Bash, kullanıcıların dosya yönetimi, program çalıştırma ve sistem ayarlarını değiştirme gibi işlemleri gerçekleştirmesine olanak tanır.

## Kullanım
Bash komutlarının temel sözdizimi aşağıdaki gibidir:

```bash
komut [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-h`, `--help`: Komut hakkında yardım bilgisi gösterir.
- `-v`, `--verbose`: Daha ayrıntılı çıktı verir.
- `-q`, `--quiet`: Sessiz modda çalışır, minimum çıktı üretir.

## Yaygın Örnekler
Aşağıda bazı pratik örnekler verilmiştir:

### 1. Basit bir komut çalıştırma
```bash
echo "Merhaba, Dünya!"
```
Bu komut, "Merhaba, Dünya!" ifadesini terminalde görüntüler.

### 2. Dosya içeriğini görüntüleme
```bash
cat dosya.txt
```
Bu komut, `dosya.txt` dosyasının içeriğini terminalde gösterir.

### 3. Dizin değiştirme
```bash
cd /home/kullanici
```
Bu komut, kullanıcıyı belirtilen dizine taşır.

### 4. Dosya kopyalama
```bash
cp kaynak.txt hedef.txt
```
Bu komut, `kaynak.txt` dosyasını `hedef.txt` olarak kopyalar.

## İpuçları
- Komutları yazarken dikkatli olun; küçük bir hata, komutun çalışmamasına neden olabilir.
- `tab` tuşunu kullanarak otomatik tamamlama özelliğinden faydalanabilirsiniz.
- Komutların nasıl çalıştığını anlamak için `--help` seçeneğini kullanarak yardım alabilirsiniz.