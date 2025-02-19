# [Linux] C Shell (csh) stty Kullanımı: Terminal ayarlarını değiştirme

## Genel Bakış
`stty` komutu, terminal ayarlarını değiştirmek için kullanılan bir komuttur. Bu komut, terminalin giriş ve çıkış özelliklerini yapılandırarak kullanıcı deneyimini iyileştirir.

## Kullanım
Temel sözdizimi aşağıdaki gibidir:
```csh
stty [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-a`: Tüm terminal ayarlarını gösterir.
- `-g`: Terminal ayarlarını bir dize olarak gösterir.
- `erase`: Silme karakterini ayarlar.
- `kill`: Satır silme karakterini ayarlar.
- `intr`: Kesme karakterini ayarlar.

## Yaygın Örnekler
Aşağıda `stty` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Tüm terminal ayarlarını görüntüleme
```csh
stty -a
```

### 2. Silme karakterini ayarlama
```csh
stty erase ^H
```

### 3. Kesme karakterini ayarlama
```csh
stty intr ^C
```

### 4. Terminal ayarlarını dize olarak gösterme
```csh
stty -g
```

## İpuçları
- Terminal ayarlarını değiştirmeden önce mevcut ayarları kaydetmek iyi bir uygulamadır.
- `stty` komutunu kullanırken dikkatli olun; yanlış ayarlar terminalin çalışmasını etkileyebilir.
- Ayarları kalıcı hale getirmek için, `stty` komutunu başlangıç dosyalarınıza eklemeyi düşünün.