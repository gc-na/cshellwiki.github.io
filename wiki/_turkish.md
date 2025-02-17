# [Linux] Bash @ Kullanımı: Komutları çalıştırma

## Genel Bakış
`@` komutu, Bash ortamında bir komutun arka planda çalıştırılmasını sağlar. Bu, komutların terminalde görünmeden veya kullanıcıdan herhangi bir girdi almadan çalıştırılmasına olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
@ [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-n`: Komutun çalıştırılmadan önce yalnızca sözdizimini kontrol etmesini sağlar.
- `-v`: Komutları çalıştırmadan önce terminalde gösterir.
- `-e`: Belirtilen komutları çalıştırır.

## Yaygın Örnekler
Aşağıda, `@` komutunun bazı pratik örnekleri bulunmaktadır:

1. Basit bir komutun arka planda çalıştırılması:
   ```bash
   @ echo "Merhaba Dünya"
   ```

2. Bir dosyanın içeriğini arka planda görüntülemek:
   ```bash
   @ cat dosya.txt
   ```

3. Bir betiği arka planda çalıştırmak:
   ```bash
   @ ./script.sh
   ```

4. Birden fazla komutu arka planda çalıştırmak:
   ```bash
   @ echo "İlk Komut" && echo "İkinci Komut"
   ```

## İpuçları
- Arka planda çalıştırılan komutların çıktısını görmek için `-v` seçeneğini kullanabilirsiniz.
- Komutların düzgün çalıştığından emin olmak için `-n` seçeneği ile sözdizimi kontrolü yapmayı unutmayın.
- Uzun süreli çalışan komutlar için, çıktıları bir dosyaya yönlendirmek iyi bir uygulamadır. Örneğin:
  ```bash
  @ uzun_komut > cikti.txt 2>&1
  ```