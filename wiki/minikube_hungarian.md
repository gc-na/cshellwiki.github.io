# [Linux] Bash minikube használata: Helyi Kubernetes klaszter indítása és kezelése

## Áttekintés
A minikube egy parancssori eszköz, amely lehetővé teszi a felhasználók számára, hogy helyi Kubernetes klasztert indítsanak és kezeljenek. Ideális fejlesztési és tesztelési környezetekhez, mivel egyszerűsíti a Kubernetes telepítését és használatát.

## Használat
A minikube parancs alapvető szintaxisa a következő:

```bash
minikube [opciók] [argumentumok]
```

## Gyakori opciók
- `start`: Indítja a minikube klasztert.
- `stop`: Leállítja a futó minikube klasztert.
- `status`: Megjeleníti a klaszter állapotát.
- `delete`: Törli a minikube klasztert.
- `kubectl`: A Kubernetes parancssori eszköz, amely a minikube klaszthoz kapcsolódik.

## Gyakori példák
1. **Klaszter indítása:**
   ```bash
   minikube start
   ```

2. **Klaszter állapotának ellenőrzése:**
   ```bash
   minikube status
   ```

3. **Klaszter leállítása:**
   ```bash
   minikube stop
   ```

4. **Klaszter törlése:**
   ```bash
   minikube delete
   ```

5. **Kubernetes parancsok futtatása a minikube klaszterben:**
   ```bash
   kubectl get pods --all-namespaces
   ```

## Tippek
- Mindig ellenőrizd a minikube állapotát a `minikube status` paranccsal, mielőtt új parancsokat futtatnál.
- Használj `minikube addons` parancsot a különböző kiegészítők telepítéséhez és kezeléséhez.
- A minikube erőforrásait a `--cpus` és `--memory` opciókkal testre szabhatod a `minikube start` parancs során, hogy optimalizáld a teljesítményt a fejlesztési környezetedhez.