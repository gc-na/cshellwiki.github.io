# [Linux] Bash sqlite3 Kullanımı: SQLite veritabanı ile etkileşim

## Overview
`sqlite3`, SQLite veritabanı yönetim sistemi ile etkileşim kurmak için kullanılan bir komut satırı aracıdır. Bu komut, veritabanı oluşturma, sorgulama yapma, veri ekleme ve güncelleme gibi işlemleri gerçekleştirmek için kullanılır.

## Usage
Temel kullanım biçimi aşağıdaki gibidir:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Yardım mesajını görüntüler.
- `-version`: SQLite sürümünü gösterir.
- `-init <file>`: Veritabanı açılmadan önce belirtilen dosyayı çalıştırır.
- `-batch`: Komut satırında etkileşim olmadan çalışır, çıktı dosyası oluşturur.

## Common Examples
Aşağıda `sqlite3` komutunun bazı yaygın kullanım örnekleri bulunmaktadır:

### 1. Yeni bir veritabanı oluşturma
```bash
sqlite3 mydatabase.db
```

### 2. Bir tablo oluşturma
```bash
sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT, age INTEGER);"
```

### 3. Veri ekleme
```bash
sqlite3 mydatabase.db "INSERT INTO users (name, age) VALUES ('Ali', 30);"
```

### 4. Veri sorgulama
```bash
sqlite3 mydatabase.db "SELECT * FROM users;"
```

### 5. Veritabanını bir dosyadan başlatma
```bash
sqlite3 mydatabase.db < script.sql
```

## Tips
- Veritabanı dosyanızın yedeğini almak için dosyayı kopyalayın.
- Sorgularınızı test etmek için `-batch` seçeneğini kullanarak etkileşim olmadan çalıştırabilirsiniz.
- Sık sık kullandığınız sorguları bir dosyada saklayarak `-init` seçeneği ile otomatik olarak çalıştırabilirsiniz.