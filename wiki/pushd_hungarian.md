# [Linux] Bash pushd használata: Könyvtárak gyors váltása

## Áttekintés
A `pushd` parancs lehetővé teszi a könyvtárak közötti gyors váltást a parancssorban, miközben a korábbi könyvtárakat egy verembe helyezi. Ez megkönnyíti a navigációt és a könyvtárak közötti visszatérést.

## Használat
A `pushd` parancs alapvető szintaxisa a következő:

```bash
pushd [opciók] [érvek]
```

## Gyakori opciók
- `+n`: Az n-edik könyvtárra vált a veremben.
- `-n`: A verem legutolsó könyvtárát távolítja el, és visszatér a következőre.

## Gyakori példák
1. **Könyvtár váltás**:
   A következő parancs a `Documents` könyvtárra vált:
   ```bash
   pushd ~/Documents
   ```

2. **Több könyvtár váltása**:
   Egyszerre több könyvtárra is válthatsz:
   ```bash
   pushd ~/Documents ~/Downloads
   ```

3. **Visszatérés a korábbi könyvtárra**:
   A `pushd` parancs használatával bármikor visszatérhetsz a legutolsó könyvtárra:
   ```bash
   pushd -
   ```

4. **Könyvtár eltávolítása a veremből**:
   A legutolsó könyvtár eltávolítása a veremből:
   ```bash
   pushd -n
   ```

## Tippek
- Használj `dirs` parancsot a verem tartalmának megjelenítésére, hogy lásd, mely könyvtárak vannak a veremben.
- A `popd` parancs segítségével visszatérhetsz a legutolsó könyvtárhoz, amelyet a `pushd`-del adtál hozzá.
- A `pushd` és `popd` kombinálásával hatékonyan kezelheted a könyvtárak közötti navigációt, különösen, ha több könyvtárral dolgozol egyszerre.