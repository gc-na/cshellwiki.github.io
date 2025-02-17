# [Linux] Bash kubectl használat: A Kubernetes erőforrások kezelésére szolgáló parancs

## Áttekintés
A `kubectl` parancs a Kubernetes parancssori eszköze, amely lehetővé teszi a felhasználók számára, hogy interakcióba lépjenek a Kubernetes klaszterekkel. Ezzel a paranccsal különböző erőforrásokat hozhatunk létre, módosíthatunk és kezelhetünk.

## Használat
A `kubectl` parancs alapvető szintaxisa a következő:

```bash
kubectl [opciók] [érvek]
```

## Gyakori opciók
- `get`: Az erőforrások listázására szolgál.
- `describe`: Részletes információt ad egy adott erőforrásról.
- `create`: Új erőforrás létrehozására használható.
- `delete`: Meglévő erőforrások törlésére szolgál.
- `apply`: Erőforrások frissítésére vagy létrehozására YAML fájlok alapján.

## Gyakori példák
1. **Erőforrások listázása**:
   ```bash
   kubectl get pods
   ```

2. **Részletes információ egy podról**:
   ```bash
   kubectl describe pod <pod_neve>
   ```

3. **Új pod létrehozása**:
   ```bash
   kubectl create -f pod.yaml
   ```

4. **Pod törlése**:
   ```bash
   kubectl delete pod <pod_neve>
   ```

5. **Erőforrások frissítése**:
   ```bash
   kubectl apply -f deployment.yaml
   ```

## Tippek
- Mindig ellenőrizd a Kubernetes klasztered állapotát a `kubectl get nodes` paranccsal, hogy biztos legyél benne, hogy minden erőforrás megfelelően működik.
- Használj YAML fájlokat a `create` és `apply` parancsokkal, hogy könnyen verziózható és áttekinthető legyen az erőforrások konfigurációja.
- Használj aliasokat a gyakran használt parancsokhoz, hogy gyorsabban dolgozhass. Például:
  ```bash
  alias k=kubectl
  ```