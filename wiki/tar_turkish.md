# [Linux] C Shell (csh) tar Kullanımı: Dosyaları arşivleme ve sıkıştırma

## Genel Bakış
`tar` komutu, dosyaları bir arşiv dosyası içinde toplamak ve sıkıştırmak için kullanılan bir araçtır. Bu komut, genellikle yedekleme işlemleri veya dosyaları birleştirme amacıyla kullanılır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```csh
tar [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-c`: Yeni bir arşiv oluşturur.
- `-x`: Var olan bir arşivi çıkarır.
- `-f`: Arşiv dosyasının adını belirtir.
- `-v`: İşlem sırasında ayrıntılı çıktı verir.
- `-z`: Arşivi gzip ile sıkıştırır veya sıkıştırılmış bir arşivi çıkarır.

## Yaygın Örnekler
1. Yeni bir arşiv oluşturma:
   ```csh
   tar -cvf arşiv.tar dosya1 dosya2
   ```

2. Arşivi çıkarma:
   ```csh
   tar -xvf arşiv.tar
   ```

3. gzip ile sıkıştırılmış bir arşiv oluşturma:
   ```csh
   tar -czvf arşiv.tar.gz dosya1 dosya2
   ```

4. Sıkıştırılmış bir arşivi çıkarma:
   ```csh
   tar -xzvf arşiv.tar.gz
   ```

## İpuçları
- Arşiv dosyalarınızı düzenli tutmak için tarih ve saat ekleyerek adlandırmayı düşünebilirsiniz.
- `-v` seçeneğini kullanarak işleminiz sırasında hangi dosyaların işlendiğini görebilirsiniz.
- Büyük dosyalarla çalışırken `-z` seçeneği ile sıkıştırma yaparak disk alanından tasarruf edebilirsiniz.