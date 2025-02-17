# [Linux] Bash expr használata: Kifejezések kiértékelése

## Áttekintés
Az `expr` parancs egy egyszerű eszköz a kifejezések kiértékelésére a Bash környezetben. Lehetővé teszi matematikai műveletek, logikai összehasonlítások és karakterláncok manipulálását.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
expr [opciók] [argumentumok]
```

## Gyakori opciók
- `+` : Összeadás.
- `-` : Kivonás.
- `*` : Szorzás (használj `\*`-t a shellben).
- `/` : Osztás.
- `%` : Maradékos osztás.
- `=` : Egyenlőség vizsgálata.
- `!=` : Különbség vizsgálata.
- `>` : Nagyobb mint vizsgálata.
- `<` : Kisebb mint vizsgálata.

## Gyakori példák

### 1. Egyszerű matematikai művelet
Összeadás végrehajtása:
```bash
expr 5 + 3
```
Kimenet: `8`

### 2. Kivonás
Kivonás végrehajtása:
```bash
expr 10 - 4
```
Kimenet: `6`

### 3. Szorzás
Szorzás végrehajtása:
```bash
expr 7 \* 6
```
Kimenet: `42`

### 4. Osztás
Osztás végrehajtása:
```bash
expr 20 / 4
```
Kimenet: `5`

### 5. Karakterlánc hossza
Karakterlánc hosszának meghatározása:
```bash
expr length "Hello, World!"
```
Kimenet: `13`

### 6. Összehasonlítás
Egyenlőség vizsgálata:
```bash
expr 5 = 5
```
Kimenet: `1` (igaz)

## Tippek
- Használj zárójeleket a bonyolultabb kifejezésekhez, hogy elkerüld a nem kívánt eredményeket.
- Az `expr` parancs kimenete nem tartalmaz szóközöket, így ha a kimenetet változóba szeretnéd menteni, érdemes a kimenetet idézőjelek közé tenni.
- A `expr` parancs helyett érdemes lehet a Bash beépített aritmetikai kifejezéseit (`$(( ))`) használni, mivel azok gyorsabbak és egyszerűbbek.