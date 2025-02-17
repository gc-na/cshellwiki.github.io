# [Linux] Bash groupmod Kullanımı: Grupları değiştirme

## Overview
`groupmod` komutu, mevcut bir kullanıcı grubunun özelliklerini değiştirmek için kullanılır. Bu komut, grup adını veya grup kimliğini (GID) güncelleyerek sistem yöneticilerine esneklik sağlar.

## Usage
Temel sözdizimi aşağıdaki gibidir:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name NEW_NAME`: Grubun yeni adını belirtir.
- `-g, --gid GID`: Grubun yeni grup kimliğini (GID) ayarlar.
- `-o, --non-unique`: GID'nin benzersiz olmamasını sağlar; başka bir grup ile aynı GID kullanılabilir.

## Common Examples
Aşağıda `groupmod` komutunun bazı pratik örnekleri bulunmaktadır:

1. **Grup adını değiştirme**:
   ```bash
   groupmod -n yeni_grup_adi eski_grup_adi
   ```

2. **Grup kimliğini değiştirme**:
   ```bash
   groupmod -g 1001 grup_adi
   ```

3. **Grup adını ve GID'yi aynı anda değiştirme**:
   ```bash
   groupmod -n yeni_grup_adi -g 1002 eski_grup_adi
   ```

## Tips
- Grup adını değiştirirken, yeni adın sistemdeki diğer gruplarla çakışmadığından emin olun.
- GID değişikliği yapmadan önce, bu GID'yi kullanan kullanıcıların etkilenip etkilenmeyeceğini kontrol edin.
- Değişikliklerin etkili olması için, ilgili kullanıcıların oturumlarını kapatıp açmaları gerekebilir.