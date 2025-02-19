# [Linux] C Shell (csh) chage Kullanımı: Kullanıcı parolası değişikliklerini yönetme

## Genel Bakış
`chage` komutu, bir kullanıcının parolasının ne zaman değiştirileceğini ve parolanın geçerlilik süresini yönetmek için kullanılır. Bu komut, sistem yöneticilerinin kullanıcıların parola politikalarını belirlemesine olanak tanır.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:

```shell
chage [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-l`: Kullanıcının mevcut parola bilgilerini listelemek için kullanılır.
- `-m`: Parola değişikliği için minimum gün sayısını ayarlar.
- `-M`: Parolanın maksimum geçerlilik süresini gün cinsinden ayarlar.
- `-I`: Parola geçerliliği sona ermeden önceki gün sayısını ayarlar.
- `-E`: Kullanıcının hesabının sona ereceği tarihi ayarlar.

## Yaygın Örnekler
Aşağıda `chage` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Kullanıcının parola bilgilerini listeleme
```shell
chage -l kullanıcı_adı
```

### 2. Parola değişikliği için minimum gün sayısını ayarlama
```shell
chage -m 7 kullanıcı_adı
```

### 3. Parolanın maksimum geçerlilik süresini ayarlama
```shell
chage -M 30 kullanıcı_adı
```

### 4. Parola geçerliliği sona ermeden önceki gün sayısını ayarlama
```shell
chage -I 14 kullanıcı_adı
```

### 5. Kullanıcının hesabının sona ereceği tarihi ayarlama
```shell
chage -E 2024-12-31 kullanıcı_adı
```

## İpuçları
- Kullanıcıların parola değişikliklerini düzenli olarak yapmalarını sağlamak için maksimum geçerlilik süresi ayarlayın.
- Parola bilgilerini kontrol etmek için `-l` seçeneğini kullanarak kullanıcıların mevcut durumunu gözden geçirin.
- Güvenlik politikalarınıza uygun olarak minimum ve maksimum gün sayısını belirleyin.