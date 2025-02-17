# [Linux] Bash uniq használata: Ismétlődő sorok eltávolítása

## Áttekintés
A `uniq` parancs a fájlokban vagy a standard bemeneten található ismétlődő sorok eltávolítására szolgál. A parancs csak az egymás után következő azonos sorokat képes kezelni, ezért gyakran a `sort` parancsot használják előtte a hatékonyabb működés érdekében.

## Használat
A `uniq` parancs alapvető szintaxisa a következő:

```bash
uniq [opciók] [argumentumok]
```

## Gyakori opciók
- `-c`: Számolja az ismétlődő sorokat és megjeleníti a számukat.
- `-d`: Csak az ismétlődő sorokat jeleníti meg.
- `-u`: Csak az egyedi sorokat jeleníti meg.
- `-i`: Figyelmen kívül hagyja a kis- és nagybetűk közötti különbséget.

## Gyakori példák

1. **Alapvető használat**: Ismétlődő sorok eltávolítása egy fájlból.
   ```bash
   uniq fajl.txt
   ```

2. **Sorok számolása**: Az ismétlődő sorok számának megjelenítése.
   ```bash
   uniq -c fajl.txt
   ```

3. **Csak az ismétlődő sorok megjelenítése**:
   ```bash
   uniq -d fajl.txt
   ```

4. **Csak az egyedi sorok megjelenítése**:
   ```bash
   uniq -u fajl.txt
   ```

5. **Kis- és nagybetűk figyelmen kívül hagyása**:
   ```bash
   uniq -i fajl.txt
   ```

## Tippek
- Használja a `sort` parancsot a `uniq` előtt, hogy biztosítsa az azonos sorok egymás melletti elhelyezkedését:
  ```bash
  sort fajl.txt | uniq
  ```
- Ha nagy fájlokkal dolgozik, érdemes a `-u` vagy `-d` opciókat használni, hogy gyorsan azonosíthassa az egyedi vagy ismétlődő sorokat.
- A `uniq` parancs kimenete átirányítható egy új fájlba, ha az eredményt meg szeretné őrizni:
  ```bash
  uniq fajl.txt > egyedi_sorok.txt
  ```