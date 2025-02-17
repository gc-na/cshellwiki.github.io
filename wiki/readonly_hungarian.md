# [Linux] Bash readonly használata: Változók írásvédetté tétele

## Áttekintés
A `readonly` parancs a Bash környezetben lehetővé teszi, hogy egy változót írásvédetté tegyünk. Ez azt jelenti, hogy a változó értékét a későbbiekben nem lehet módosítani, ami hasznos lehet a programok stabilitásának megőrzésében.

## Használat
A `readonly` parancs alapvető szintaxisa a következő:

```bash
readonly [változó_név[=érték]]
```

## Gyakori Opciók
- **-p**: Kiírja az összes írásvédett változót és azok értékeit.

## Gyakori Példák

### 1. Változó írásvédetté tétele
```bash
readonly MY_VAR="Hello, World!"
```
Ez a parancs létrehoz egy `MY_VAR` nevű változót, amelynek értéke "Hello, World!", és írásvédetté teszi.

### 2. Írásvédett változó megkísérlése módosítani
```bash
MY_VAR="New Value"  # Ez hibaüzenetet fog eredményezni
```
Próbálkozás a `MY_VAR` módosítására hibaüzenetet eredményez, mivel a változó írásvédett.

### 3. Írásvédett változók listázása
```bash
readonly -p
```
Ez a parancs kiírja az összes írásvédett változót és azok értékeit a terminálra.

## Tippek
- Használj `readonly`-t a fontos változók védelme érdekében, hogy elkerüld a véletlen módosítást.
- Ellenőrizd a változók állapotát a `readonly -p` paranccsal, hogy lásd, mely változók írásvédettek.
- Ne felejtsd el, hogy a `readonly` parancs csak a Bash környezetben működik, más shell-ek esetén eltérő lehet a viselkedés.