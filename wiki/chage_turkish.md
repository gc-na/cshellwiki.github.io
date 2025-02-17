# [Linux] Bash chage Kullanımı: Kullanıcı parolası değiştirme sürelerini yönetme

## Overview
`chage` komutu, bir kullanıcının parolasının ne zaman değiştirilmesi gerektiğini ve parolanın geçerlilik süresini yönetmek için kullanılır. Bu komut, sistem yöneticilerine kullanıcıların parola güvenliğini artırma imkanı sunar.

## Usage
Temel sözdizimi aşağıdaki gibidir:
```bash
chage [options] [arguments]
```

## Common Options
- `-l, --list`: Kullanıcının parola değiştirme bilgilerini listele.
- `-m, --mindays MIN_DAYS`: Parolanın değiştirilmesi için minimum gün sayısını ayarla.
- `-M, --maxdays MAX_DAYS`: Parolanın maksimum geçerlilik süresini ayarla.
- `-I, --inactive INACTIVE`: Parola süresi dolduktan sonra hesabın ne kadar süreyle devre dışı kalacağını ayarla.
- `-E, --expiredate EXPIRE_DATE`: Kullanıcının hesabının sona ereceği tarihi ayarla.

## Common Examples
Aşağıda `chage` komutunun bazı pratik kullanım örnekleri bulunmaktadır:

### 1. Kullanıcı Bilgilerini Listeleme
Bir kullanıcının parola değiştirme bilgilerini listelemek için:
```bash
chage -l kullanıcı_adı
```

### 2. Minimum Gün Sayısını Ayarlama
Bir kullanıcının parolasını değiştirmeden önce beklemesi gereken minimum gün sayısını ayarlamak için:
```bash
chage -m 7 kullanıcı_adı
```

### 3. Maksimum Gün Sayısını Ayarlama
Bir kullanıcının parolasının geçerlilik süresini 90 gün olarak ayarlamak için:
```bash
chage -M 90 kullanıcı_adı
```

### 4. Hesap Süresini Devre Dışı Bırakma
Parola süresi dolduktan sonra hesabın 30 gün boyunca devre dışı kalmasını sağlamak için:
```bash
chage -I 30 kullanıcı_adı
```

### 5. Hesap Sona Erme Tarihini Ayarlama
Bir kullanıcının hesabının 2024-12-31 tarihinde sona ermesini sağlamak için:
```bash
chage -E 2024-12-31 kullanıcı_adı
```

## Tips
- Kullanıcıların parola sürelerini düzenli olarak kontrol edin ve güncelleyin.
- Parola güvenliğini artırmak için minimum ve maksimum gün sayıları ayarlarını dikkatli bir şekilde belirleyin.
- Kullanıcılarla iletişim kurarak, parola değişiklikleri hakkında bilgilendirme yapmayı unutmayın.