# [Linux] Bash helm használata: Helm csomagkezelés Kuberneteshez

## Áttekintés
A `helm` egy csomagkezelő eszköz a Kubernetes számára, amely lehetővé teszi a Kubernetes alkalmazások egyszerű telepítését, frissítését és kezelését. A Helm segítségével könnyedén kezelhetjük a Kubernetes "chart"-okat, amelyek a telepítési konfigurációkat tartalmazzák.

## Használat
A `helm` parancs alapvető szintaxisa a következő:

```bash
helm [opciók] [argumentumok]
```

## Gyakori opciók
- `install`: Új chart telepítése.
- `upgrade`: Meglévő chart frissítése.
- `uninstall`: Chart eltávolítása.
- `list`: Telepített chartok listázása.
- `repo`: Helm repository-k kezelése.

## Gyakori példák
1. **Chart telepítése:**
   ```bash
   helm install my-release my-chart
   ```
   Ezzel a paranccsal telepítjük a `my-chart` chartot `my-release` néven.

2. **Chart frissítése:**
   ```bash
   helm upgrade my-release my-chart
   ```
   Ezzel a paranccsal frissítjük a már telepített `my-release` chartot.

3. **Chart eltávolítása:**
   ```bash
   helm uninstall my-release
   ```
   Ezzel a paranccsal eltávolítjuk a `my-release` chartot a Kubernetes klaszterből.

4. **Telepített chartok listázása:**
   ```bash
   helm list
   ```
   Ezzel a paranccsal megtekinthetjük az összes telepített chartot.

5. **Helm repository hozzáadása:**
   ```bash
   helm repo add my-repo https://example.com/charts
   ```
   Ezzel a paranccsal hozzáadunk egy új Helm repository-t.

## Tippek
- Mindig ellenőrizd a chart verzióját a telepítés előtt, hogy biztos legyél benne, hogy a legfrissebb verziót használod.
- Használj `--dry-run` opciót a telepítési parancsok előtt, hogy előre láthasd, mi fog történni.
- Rendszeresen frissítsd a Helm repository-dat a `helm repo update` paranccsal, hogy a legújabb chartokat használd.