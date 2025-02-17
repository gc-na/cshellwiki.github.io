# [Linux] Bash fsck Kullanımı: Dosya sistemini kontrol etme

## Genel Bakış
`fsck` (file system check), Linux ve Unix benzeri işletim sistemlerinde dosya sistemlerini kontrol etmek ve onarmak için kullanılan bir komuttur. Dosya sistemindeki hataları tespit eder ve mümkünse düzeltir. Bu komut, sistemin güvenilirliğini artırmak ve veri kaybını önlemek için düzenli olarak kullanılmalıdır.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
fsck [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Hataları otomatik olarak düzeltir.
- `-n`: Hataları düzeltmeden sadece kontrol eder (okuma modu).
- `-y`: Tüm hataları otomatik olarak onaylar ve düzeltir.
- `-t`: Hangi dosya sisteminin kontrol edileceğini belirtir.

## Yaygın Örnekler
1. **Bir dosya sistemini kontrol etme**:
   ```bash
   fsck /dev/sda1
   ```
   Bu komut, `/dev/sda1` dosya sistemini kontrol eder.

2. **Otomatik düzeltme ile kontrol etme**:
   ```bash
   fsck -a /dev/sda1
   ```
   Bu komut, `/dev/sda1` dosya sistemindeki hataları otomatik olarak düzeltir.

3. **Sadece kontrol etme (okuma modu)**:
   ```bash
   fsck -n /dev/sda1
   ```
   Bu komut, hataları düzeltmeden sadece kontrol eder.

4. **Tüm hataları onaylayarak düzeltme**:
   ```bash
   fsck -y /dev/sda1
   ```
   Bu komut, `/dev/sda1` dosya sistemindeki tüm hataları otomatik olarak onaylayarak düzeltir.

## İpuçları
- `fsck` komutunu çalıştırmadan önce dosya sisteminin montajının kaldırıldığından emin olun. Montajda olan bir dosya sistemi üzerinde `fsck` çalıştırmak veri kaybına yol açabilir.
- Düzenli aralıklarla dosya sisteminizi kontrol etmek, sistem güvenilirliğini artırır.
- Eğer bir dosya sistemi hatalıysa, `fsck` komutunu çalıştırmadan önce önemli verilerinizi yedeklemeyi unutmayın.