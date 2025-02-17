# [Linux] Bash hostname Kullanımı: Bilgisayar adını görüntüleme ve ayarlama

## Overview
`hostname` komutu, bir bilgisayarın ağ üzerindeki adını görüntülemek veya değiştirmek için kullanılır. Bu komut, sistem yöneticileri ve kullanıcılar için ağ ayarlarını yönetmede önemli bir araçtır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn`: Tam nitelikli alan adı (FQDN) olarak bilgisayar adını gösterir.
- `-i`, `--ip-address`: Bilgisayarın IP adresini görüntüler.
- `-s`, `--short`: Kısa bilgisayar adını gösterir.
- `-V`, `--version`: Komutun sürümünü gösterir.

## Common Examples
Aşağıda `hostname` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

1. **Bilgisayar adını görüntüleme:**
   ```bash
   hostname
   ```

2. **Tam nitelikli alan adı görüntüleme:**
   ```bash
   hostname -f
   ```

3. **Bilgisayarın IP adresini görüntüleme:**
   ```bash
   hostname -i
   ```

4. **Kısa bilgisayar adını görüntüleme:**
   ```bash
   hostname -s
   ```

5. **Bilgisayar adını değiştirme:**
   ```bash
   sudo hostname yeni_ad
   ```

## Tips
- Bilgisayar adını değiştirdikten sonra, değişikliğin etkili olması için sistemi yeniden başlatmanız gerekebilir.
- Ağ ayarlarınızı yönetirken, bilgisayar adının diğer cihazlarla çakışmadığından emin olun.
- `hostname` komutunu kullanmadan önce, gerekli izinlere sahip olduğunuzdan emin olun; bazı işlemler için yönetici yetkileri gerekebilir.