# [Linux] Bash hostnamectl Kullanımı: Sistem adını yönetme aracı

## Overview
`hostnamectl` komutu, Linux sistemlerinde sistem adını, ağ alan adını ve diğer ilgili bilgileri yönetmek için kullanılan bir araçtır. Bu komut, sistemin adını değiştirmek ve mevcut bilgileri görüntülemek için kullanılır.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
hostnamectl [options] [arguments]
```

## Common Options
- `set-hostname`: Sistemin adını değiştirmek için kullanılır.
- `set-icon-name`: Sistem simgesi adını ayarlamak için kullanılır.
- `set-chassis`: Sistem kasasını tanımlamak için kullanılır.
- `status`: Mevcut sistem bilgilerini görüntülemek için kullanılır.
- `help`: Komut hakkında yardım almak için kullanılır.

## Common Examples
Aşağıda `hostnamectl` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Sistemin adını değiştirme
```bash
sudo hostnamectl set-hostname yeni-sistem-adi
```

### 2. Mevcut sistem bilgilerini görüntüleme
```bash
hostnamectl status
```

### 3. Sistem simgesi adını ayarlama
```bash
sudo hostnamectl set-icon-name bilgisayar
```

### 4. Sistem kasasını tanımlama
```bash
sudo hostnamectl set-chassis sunucu
```

## Tips
- Değişikliklerin etkili olabilmesi için bazı durumlarda sistemi yeniden başlatmanız gerekebilir.
- `hostnamectl` komutunu kullanmadan önce, mevcut sistem adınızı kontrol etmek için `hostname` komutunu kullanabilirsiniz.
- Komutları çalıştırırken `sudo` kullanmayı unutmayın; aksi takdirde gerekli izinler olmayabilir.