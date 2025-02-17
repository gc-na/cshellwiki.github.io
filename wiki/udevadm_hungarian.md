# [Linux] Bash udevadm használat: Eszközök és események kezelése

## Áttekintés
A `udevadm` parancs a Linux rendszerek eszközkezelésének egyik alapvető eszköze. Segítségével a felhasználók és rendszergazdák információkat kaphatnak az eszközökről, valamint kezelhetik az udev eseményeket és szabályokat.

## Használat
A `udevadm` parancs alapvető szintaxisa a következő:

```bash
udevadm [opciók] [argumentumok]
```

## Gyakori opciók
- `info`: Információt ad meg egy adott eszközről.
- `trigger`: Eseményeket generál a meglévő eszközök számára.
- `settle`: Várakozik, amíg az összes eszköz esemény feldolgozásra kerül.
- `control`: Az udev daemon működését befolyásolja (pl. indítás, leállítás).

## Gyakori példák
1. **Eszköz információ lekérése**:
   ```bash
   udevadm info --query=all --name=/dev/sda
   ```

2. **Események generálása**:
   ```bash
   udevadm trigger
   ```

3. **Eszközök állapotának rendezése**:
   ```bash
   udevadm settle
   ```

4. **Udev daemon vezérlése**:
   ```bash
   udevadm control --reload-rules
   ```

## Tippek
- Mindig ellenőrizd az eszköz nevét, mielőtt információt kérnél le róla, hogy elkerüld a hibákat.
- Használj `--verbose` opciót a parancsok részletesebb kimenetéhez, hogy jobban megértsd a folyamatokat.
- Rendszeresen frissítsd az udev szabályokat, különösen új eszközök csatlakoztatásakor.