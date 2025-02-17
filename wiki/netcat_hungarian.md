# [Linux] Bash netcat használata: Hálózati kapcsolatok létrehozása és tesztelése

## Áttekintés
A netcat (vagy nc) egy rendkívül sokoldalú parancs, amely lehetővé teszi a hálózati kapcsolatok létrehozását, tesztelését és hibakeresését. Használható TCP vagy UDP protokollon keresztül történő adatátvitelre, és gyakran alkalmazzák portok ellenőrzésére, fájlok átvitelére vagy egyszerű chat alkalmazások létrehozására.

## Használat
A netcat parancs alapvető szintaxisa a következő:

```bash
netcat [opciók] [argumentumok]
```

## Gyakori opciók
- `-l`: Hallgató üzemmód, amely lehetővé teszi a netcat számára, hogy várakozzon bejövő kapcsolatokra.
- `-p`: A port megadása, amelyen a netcat hallgat.
- `-u`: UDP protokoll használata a TCP helyett.
- `-v`: Verbose (részletes) mód, amely több információt ad a kapcsolatról.
- `-w`: Várakozási idő másodpercekben, amely a kapcsolat megszakítása előtt érvényes.

## Gyakori példák

### 1. Hálózati kapcsolat létrehozása
Egy egyszerű TCP kapcsolat létrehozása egy adott IP-címmel és porttal:

```bash
netcat 192.168.1.1 80
```

### 2. Hallgató üzemmód
A netcat hallgató üzemmódban egy adott porton:

```bash
netcat -l -p 1234
```

### 3. Fájl átvitele
Fájl átvitele a netcat segítségével:

**Küldő gépen:**

```bash
netcat -l -p 1234 < file.txt
```

**Fogadó gépen:**

```bash
netcat 192.168.1.2 1234 > received_file.txt
```

### 4. Chat alkalmazás létrehozása
Két gép közötti egyszerű chat létrehozása:

**Gép 1:**

```bash
netcat -l -p 1234
```

**Gép 2:**

```bash
netcat 192.168.1.1 1234
```

## Tippek
- Mindig ellenőrizd, hogy a tűzfal beállításai engedélyezik-e a kívánt portok használatát.
- Használj `-v` opciót a részletes információk megjelenítéséhez a kapcsolatról.
- A netcat használata során ügyelj arra, hogy a titkosítatlan adatátvitel biztonsági kockázatokat rejthet.