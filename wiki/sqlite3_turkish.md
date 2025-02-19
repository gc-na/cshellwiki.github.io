# [Linux] C Shell (csh) sqlite3 Kullanımı: Veritabanı yönetimi için bir araç

## Genel Bakış
`sqlite3` komutu, SQLite veritabanı dosyaları ile etkileşimde bulunmak için kullanılan bir komuttur. Bu komut, veritabanı oluşturma, sorgulama yapma, güncelleme ve silme işlemleri gibi birçok işlevi yerine getirir.

## Kullanım
Temel sözdizimi şu şekildedir:
```bash
sqlite3 [seçenekler] [argümanlar]
```

## Yaygın Seçenekler
- `-help`: Yardım bilgilerini görüntüler.
- `-version`: SQLite sürümünü gösterir.
- `-init <dosya>`: Başlangıçta çalıştırılacak SQL komutlarını içeren bir dosya belirtir.
- `-batch`: Komut dosyası modunda çalışır, etkileşimli girişi devre dışı bırakır.

## Yaygın Örnekler
Aşağıda `sqlite3` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Yeni bir veritabanı oluşturma
```bash
sqlite3 yeni_veritabani.db
```

### 2. Var olan bir veritabanında tablo oluşturma
```bash
sqlite3 varolan_veritabani.db "CREATE TABLE kullanicilar (id INTEGER PRIMARY KEY, isim TEXT);"
```

### 3. Tabloya veri ekleme
```bash
sqlite3 varolan_veritabani.db "INSERT INTO kullanicilar (isim) VALUES ('Ahmet');"
```

### 4. Verileri sorgulama
```bash
sqlite3 varolan_veritabani.db "SELECT * FROM kullanicilar;"
```

### 5. Veritabanını bir dosyadan başlatma
```bash
sqlite3 -init başlangıç.sql varolan_veritabani.db
```

## İpuçları
- Veritabanı dosyalarınızı düzenli tutun ve yedeklemelerini alın.
- SQL komutlarını bir dosyaya yazarak `sqlite3` ile bu dosyayı çalıştırmak, karmaşık sorguları daha kolay yönetmenizi sağlar.
- `-batch` seçeneğini kullanarak etkileşimli moddan çıkabilir ve komut dosyalarıyla çalışmayı kolaylaştırabilirsiniz.