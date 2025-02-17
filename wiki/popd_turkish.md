# [Linux] Bash popd Kullanımı: Dizin yığınından dizin çıkarma

## Genel Bakış
`popd` komutu, dizin yığınından (directory stack) en üstteki dizini çıkararak kullanıcıyı bir önceki dizine geri döndürür. Bu, `pushd` komutuyla eklenmiş dizinler arasında kolayca geçiş yapmayı sağlar.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```bash
popd [options]
```

## Yaygın Seçenekler
- `-n`: Dizin yığınını değiştirmeden dizinleri gösterir.
- `+n`: Yığın içindeki belirli bir dizine geri döner (n, dizin yığındaki dizinlerin sırasını belirtir).

## Yaygın Örnekler
1. En üstteki dizini çıkar ve bir önceki dizine geri dön:
   ```bash
   popd
   ```

2. Dizin yığınındaki ikinci dizine geri dön:
   ```bash
   popd +1
   ```

3. Dizin yığınını değiştirmeden mevcut dizinleri görüntüle:
   ```bash
   popd -n
   ```

## İpuçları
- `pushd` ve `popd` komutlarını birlikte kullanarak dizinler arasında hızlıca geçiş yapabilirsiniz.
- Dizin yığınını kontrol etmek için `dirs` komutunu kullanabilirsiniz; bu, mevcut dizin yığınını gösterir.
- Dizin yığınındaki dizinlerin sırasını takip etmek, `popd` komutunu daha etkili kullanmanıza yardımcı olur.