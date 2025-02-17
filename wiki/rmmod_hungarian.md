# [Linux] Bash rmmod használata: Modul eltávolítása a Linux kernelből

## Áttekintés
A `rmmod` parancs a Linux kernel modulok eltávolítására szolgál. Ezzel a paranccsal a betöltött modulokat lehet eltávolítani a rendszerből, ami hasznos lehet a rendszer karbantartása és a modulok frissítése során.

## Használat
A `rmmod` parancs alapvető szintaxisa a következő:

```bash
rmmod [opciók] [argumentumok]
```

## Gyakori Opciók
- `-f`: Kényszerített eltávolítás, ha a modul használatban van.
- `-n`: Ne írja ki a modul nevét a naplóba.
- `--help`: Megjeleníti a parancs használati útmutatóját.

## Gyakori Példák
1. **Egyszerű modul eltávolítása:**
   ```bash
   rmmod modul_neve
   ```

2. **Kényszerített eltávolítás:**
   ```bash
   rmmod -f modul_neve
   ```

3. **Modul eltávolítása naplózás nélkül:**
   ```bash
   rmmod -n modul_neve
   ```

4. **Több modul eltávolítása egyszerre:**
   ```bash
   rmmod modul1 modul2 modul3
   ```

## Tippek
- Mindig ellenőrizd, hogy a modul nem használatban van-e, mielőtt eltávolítanád, hogy elkerüld a rendszer instabilitását.
- Használj `lsmod` parancsot a betöltött modulok listázásához, mielőtt eltávolítanád őket.
- A kényszerített eltávolítás (`-f` opció) használata előtt győződj meg róla, hogy tudod, mit csinálsz, mivel ez problémákat okozhat a rendszer működésében.