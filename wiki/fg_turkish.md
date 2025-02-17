# [Linux] Bash fg Kullanımı: Arka planda çalışan bir işlemi ön plana çıkarma

## Genel Bakış
`fg` komutu, arka planda çalışan bir işlemi ön plana çıkarmak için kullanılır. Bu komut, kullanıcıların terminaldeki işlemler arasında geçiş yapmasına olanak tanır ve genellikle bir işlemi duraklatıp yeniden başlatmak için kullanılır.

## Kullanım
Temel sözdizimi şu şekildedir:

```bash
fg [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `job_spec`: Ön plana çıkarmak istediğiniz işlemin numarasını belirtir. Eğer birden fazla işlem varsa, hangi işlemi ön plana almak istediğinizi seçebilirsiniz.
- `%n`: İşlem numarasını belirtmek için kullanılır. Örneğin, `%1` ilk işlemi ifade eder.

## Yaygın Örnekler
1. **Arka planda çalışan ilk işlemi ön plana çıkarma:**
   ```bash
   fg %1
   ```

2. **Arka planda çalışan ikinci işlemi ön plana çıkarma:**
   ```bash
   fg %2
   ```

3. **Son duraklatılan işlemi ön plana çıkarma:**
   ```bash
   fg
   ```

## İpuçları
- `jobs` komutunu kullanarak arka planda çalışan işlemlerinizi görüntüleyebilirsiniz. Bu, hangi işlemi ön plana çıkarmak istediğinizi belirlemenize yardımcı olur.
- `fg` komutunu kullanmadan önce işlemin duraklatıldığından emin olun. Aksi takdirde, işlem çalışmaya devam edecektir.
- Bir işlemi duraklatmak için `Ctrl + Z` tuş kombinasyonunu kullanabilirsiniz. Bu, işlemi arka plana alır ve `fg` ile geri çağırmanızı sağlar.