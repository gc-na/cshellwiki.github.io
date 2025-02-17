# [Linux] Bash exit Kullanımı: Komut dosyasını sonlandırma

## Genel Bakış
`exit` komutu, bir Bash betiğini veya terminal oturumunu sonlandırmak için kullanılır. Bu komut, çıkış kodu belirterek, programın başarıyla mı yoksa hata ile mi sona erdiğini belirtmeye olanak tanır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
exit [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `n`: Çıkış kodunu belirtir. Varsayılan olarak 0 (başarı) olarak kabul edilir. Örneğin, `exit 1` komutu hata durumunu belirtir.
- `-n`: Çıkış kodunu belirtmeden çıkış yapar.

## Yaygın Örnekler
1. Basit bir çıkış:
   ```bash
   exit
   ```

2. Belirli bir çıkış kodu ile çıkış:
   ```bash
   exit 0
   ```

3. Hata durumu ile çıkış:
   ```bash
   exit 1
   ```

4. Bir betik içinde çıkış kodu kullanımı:
   ```bash
   #!/bin/bash
   if [ -f "dosya.txt" ]; then
       echo "Dosya mevcut."
       exit 0
   else
       echo "Dosya bulunamadı."
       exit 1
   fi
   ```

## İpuçları
- Çıkış kodlarını kullanarak, betiklerinizin hata ayıklamasını kolaylaştırabilirsiniz.
- `exit` komutunu, betiklerinizin belirli koşullara göre sonlanmasını sağlamak için kullanın.
- Terminal oturumlarınızı kapatırken `exit` komutunu kullanarak, açık olan tüm işlemleri düzgün bir şekilde sonlandırabilirsiniz.