# [Linux] Bash screen Kullanımı: Terminal oturumlarını yönetmek

## Overview
`screen` komutu, birden fazla terminal oturumunu yönetmenizi sağlayan bir araçtır. Bu komut sayesinde, terminal oturumlarınızı arka planda çalıştırabilir, oturumlar arasında geçiş yapabilir ve bağlantınız kesilse bile işlemlerinizi sürdürebilirsiniz.

## Usage
Temel sözdizimi şu şekildedir:
```bash
screen [options] [arguments]
```

## Common Options
- `-S <session_name>`: Yeni bir oturum oluştururken özel bir isim vermek için kullanılır.
- `-d -r`: Ayrılmış bir oturumu yeniden bağlamak için kullanılır.
- `-list`: Mevcut oturumların listesini gösterir.
- `-X <command>`: Belirtilen oturuma bir komut gönderir.

## Common Examples
### Yeni bir oturum başlatma
```bash
screen -S mysession
```
Bu komut, "mysession" adında yeni bir oturum başlatır.

### Oturumu arka planda çalıştırma
Oturumdan çıkmak için `Ctrl + A` ardından `D` tuşlarına basabilirsiniz. Bu, oturumu arka plana alır.

### Ayrılmış oturumu yeniden bağlama
```bash
screen -d -r mysession
```
Bu komut, "mysession" adındaki ayrılmış oturuma yeniden bağlanmanızı sağlar.

### Mevcut oturumları listeleme
```bash
screen -list
```
Bu komut, aktif olan tüm screen oturumlarını listeler.

### Oturumdan çıkma
```bash
exit
```
Bu komut, mevcut screen oturumunu kapatır.

## Tips
- Oturumlarınızı düzenli tutmak için anlamlı isimler kullanın.
- Uzun süreli işlemler için screen kullanarak bağlantı kopmalarında işlerinizi kaybetmeyin.
- Oturumlar arasında geçiş yaparken `Ctrl + A` ardından `"` tuşlarına basarak açık oturumları görüntüleyebilirsiniz.