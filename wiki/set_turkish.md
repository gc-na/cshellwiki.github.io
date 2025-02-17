# [Linux] Bash set Kullanımı: Değişkenleri ve ortamı ayarlama

## Genel Bakış
`set` komutu, Bash kabuğunda değişkenleri ve ortamı ayarlamak için kullanılır. Bu komut, kabuk davranışını değiştirmek, değişkenleri tanımlamak veya mevcut ayarları görüntülemek için faydalıdır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```bash
set [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-e`: Komutlardan biri hata verirse, kabuğu durdurur.
- `-u`: Tanımsız değişkenlerin kullanılmasını engeller.
- `-x`: Her komut çalıştırılmadan önce ekrana yazdırılır.
- `-o`: Belirli bir seçenek ayarını değiştirmek için kullanılır (örneğin, `-o noclobber`).

## Yaygın Örnekler
1. **Hata durumunda kabuğu durdurma:**
   ```bash
   set -e
   ```
   Bu komut, bir hata oluşursa kabuğun çalışmasını durdurur.

2. **Tanımsız değişken hatası:**
   ```bash
   set -u
   echo $MY_VAR
   ```
   `MY_VAR` tanımlı değilse, bu komut hata verecektir.

3. **Komutları görüntüleme:**
   ```bash
   set -x
   ls
   ```
   `ls` komutu çalıştırılmadan önce, komutun kendisi ekrana yazdırılacaktır.

4. **Seçenek ayarlama:**
   ```bash
   set -o noclobber
   ```
   Bu seçenek, mevcut dosyaların üzerine yazılmasını engeller.

## İpuçları
- `set` komutunu, betiklerinizde hata ayıklama amacıyla kullanarak hangi komutların çalıştığını görebilirsiniz.
- Hata ayıklama sırasında `set -x` kullanmak, sorunları daha hızlı bulmanıza yardımcı olabilir.
- Betiklerinizi daha güvenilir hale getirmek için `set -e` ve `set -u` seçeneklerini birlikte kullanmayı düşünün.