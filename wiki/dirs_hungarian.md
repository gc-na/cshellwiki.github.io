# [Linux] Bash dirs használata: A könyvtárak listázása

## Áttekintés
A `dirs` parancs a Bash shell-ben a könyvtárak listázására szolgál, amelyeket a jelenlegi munkamenet során használtunk. Ez a parancs megjeleníti a könyvtárak stack-jét, lehetővé téve a felhasználók számára, hogy könnyen navigáljanak a korábban meglátogatott helyek között.

## Használat
A `dirs` parancs alapvető szintaxisa a következő:

```bash
dirs [opciók] [argumentumok]
```

## Gyakori opciók
- `-p`: A könyvtárak listáját egy sorba rendezve, a könyvtárak teljes útvonalával jeleníti meg.
- `-l`: A könyvtárak listáját hosszú formátumban jeleníti meg, beleértve a könyvtárak teljes elérési útját.

## Gyakori példák
1. **Alapértelmezett használat**:
   A `dirs` parancs egyszerű használata a jelenlegi könyvtárak listázására.
   ```bash
   dirs
   ```

2. **Teljes útvonal megjelenítése**:
   A `-p` opcióval a könyvtárak teljes útvonalát láthatjuk.
   ```bash
   dirs -p
   ```

3. **Hosszú formátumú lista**:
   A `-l` opció használatával a könyvtárak hosszú formátumban jelennek meg.
   ```bash
   dirs -l
   ```

4. **Könyvtárak visszaállítása**:
   A `pushd` és `popd` parancsokkal együtt használva a `dirs` segít a könyvtárak közötti navigálásban.
   ```bash
   pushd /home/user/documents
   pushd /var/log
   dirs
   popd
   dirs
   ```

## Tippek
- Használja a `dirs` parancsot a `pushd` és `popd` parancsokkal együtt a könyvtárak gyors váltásához.
- A `dirs -p` opció különösen hasznos, ha több könyvtárat használ, és szeretné látni az összes elérési utat.
- Ne feledje, hogy a `dirs` parancs csak a Bash shell környezetében érhető el, így más shell-ekben nem működik.