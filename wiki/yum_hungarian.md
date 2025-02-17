# [Linux] Bash yum használata: Csomagok kezelése

## Áttekintés
A `yum` (Yellowdog Updater, Modified) egy csomagkezelő eszköz, amelyet a Red Hat-alapú Linux disztribúciók, például a CentOS és a Fedora használnak. Segítségével könnyedén telepíthetünk, frissíthetünk és eltávolíthatunk szoftvercsomagokat.

## Használat
A `yum` parancs alapvető szintaxisa a következő:

```bash
yum [opciók] [argumentumok]
```

## Gyakori opciók
- `install`: Csomag telepítése.
- `remove`: Csomag eltávolítása.
- `update`: Csomag frissítése a legújabb verzióra.
- `search`: Csomagok keresése név vagy leírás alapján.
- `info`: Információk megjelenítése egy adott csomagról.

## Gyakori példák
1. Csomag telepítése:
   ```bash
   yum install httpd
   ```

2. Csomag eltávolítása:
   ```bash
   yum remove httpd
   ```

3. Csomag frissítése:
   ```bash
   yum update httpd
   ```

4. Csomagok keresése:
   ```bash
   yum search nginx
   ```

5. Csomag információk megjelenítése:
   ```bash
   yum info httpd
   ```

## Tippek
- Mindig érdemes frissíteni a csomaglistát a `yum update` parancs futtatásával, mielőtt új csomagokat telepítenénk.
- Használj `yum clean all` parancsot a gyorsítótár törlésére, ha helyet szeretnél felszabadítani.
- A `yum` parancsot rendszergazdai jogosultságokkal kell futtatni, ezért használj `sudo`-t, ha szükséges.