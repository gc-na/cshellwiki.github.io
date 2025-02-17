# [Linux] Bash komutu cp: [dosya kopyalama]

## Genel Bakış
`cp` komutu, bir veya daha fazla dosyayı veya dizini başka bir konuma kopyalamak için kullanılır. Bu komut, dosyaların yedeğini almak veya dosyaları farklı dizinlere taşımak için oldukça faydalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:
```
cp [seçenekler] [kaynak] [hedef]
```

## Yaygın Seçenekler
- `-r`: Dizinleri ve içindeki dosyaları kopyalamak için kullanılır (rekürsif).
- `-i`: Hedefteki dosya zaten varsa, üzerine yazmadan önce onay ister.
- `-u`: Sadece kaynak dosya hedef dosyadan daha yeni ise kopyalar.
- `-v`: Kopyalama işlemi sırasında hangi dosyaların kopyalandığını gösterir.

## Yaygın Örnekler
1. Basit bir dosya kopyalama:
   ```bash
   cp dosya.txt yedek_dosya.txt
   ```

2. Bir dizini ve içindeki tüm dosyaları kopyalama:
   ```bash
   cp -r kaynak_dizin/ hedef_dizin/
   ```

3. Kopyalama işlemi sırasında onay istemek:
   ```bash
   cp -i dosya.txt yedek_dosya.txt
   ```

4. Sadece daha yeni dosyaların kopyalanması:
   ```bash
   cp -u dosya.txt yedek_dosya.txt
   ```

5. Kopyalama işlemi sırasında bilgi gösterimi:
   ```bash
   cp -v dosya.txt yedek_dosya.txt
   ```

## İpuçları
- Kopyalama işlemi yapmadan önce hedef dizinin var olduğundan emin olun; aksi takdirde hata alırsınız.
- `-i` seçeneğini kullanarak yanlışlıkla üzerine yazma riskini azaltabilirsiniz.
- Büyük dosyalarla çalışırken, kopyalama işleminin ne kadar sürdüğünü görmek için `-v` seçeneğini kullanmak faydalı olabilir.