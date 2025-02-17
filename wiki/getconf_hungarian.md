# [Linux] Bash getconf használata: Rendszerinformációk lekérdezése

## Áttekintés
A `getconf` parancs lehetővé teszi a rendszerkonfigurációs paraméterek lekérdezését. Ezzel a paranccsal információkat kaphatunk a rendszer teljesítményéről és beállításairól, mint például a maximális fájlméret vagy a memória korlátai.

## Használat
A `getconf` parancs alapvető szintaxisa a következő:

```bash
getconf [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a`: Minden elérhető konfigurációs paraméter megjelenítése.
- `PARAMÉTER_NÉV`: A lekérdezni kívánt konkrét paraméter neve, például `PAGE_SIZE` vagy `ARG_MAX`.

## Gyakori Példák
1. A maximális fájlméret lekérdezése:
   ```bash
   getconf _PC_MAX_INPUT
   ```

2. A rendszer által támogatott maximális argumentumok számának megjelenítése:
   ```bash
   getconf ARG_MAX
   ```

3. Az oldalméret lekérdezése:
   ```bash
   getconf PAGE_SIZE
   ```

4. Az összes elérhető konfigurációs paraméter megjelenítése:
   ```bash
   getconf -a
   ```

## Tippek
- Használja az `-a` opciót, ha szeretné látni az összes elérhető paramétert, hogy felfedezze a rendszer beállításait.
- Ellenőrizze a dokumentációt a specifikus paraméterek részleteiért, mivel a különböző rendszerek eltérő paramétereket támogathatnak.
- A `getconf` parancsot scripteléshez is használhatja, hogy dinamikusan lekérdezze a rendszerbeállításokat.