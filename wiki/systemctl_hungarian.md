# [Linux] Bash systemctl használata: Szolgáltatások kezelése

## Áttekintés
A `systemctl` parancs a systemd rendszerkezelő eszköze, amely lehetővé teszi a rendszer szolgáltatásainak és egységeinek kezelését. Ezzel a paranccsal indíthatjuk, leállíthatjuk, újraindíthatjuk vagy ellenőrizhetjük a szolgáltatásokat.

## Használat
A `systemctl` parancs alapvető szintaxisa a következő:

```bash
systemctl [opciók] [argumentumok]
```

## Gyakori opciók
- `start`: Szolgáltatás indítása.
- `stop`: Szolgáltatás leállítása.
- `restart`: Szolgáltatás újraindítása.
- `status`: Szolgáltatás állapotának megjelenítése.
- `enable`: Szolgáltatás engedélyezése a rendszerindításkor.
- `disable`: Szolgáltatás letiltása a rendszerindításkor.

## Gyakori példák
- Szolgáltatás indítása:
  ```bash
  systemctl start nginx
  ```

- Szolgáltatás leállítása:
  ```bash
  systemctl stop nginx
  ```

- Szolgáltatás újraindítása:
  ```bash
  systemctl restart nginx
  ```

- Szolgáltatás állapotának ellenőrzése:
  ```bash
  systemctl status nginx
  ```

- Szolgáltatás engedélyezése a rendszerindításkor:
  ```bash
  systemctl enable nginx
  ```

- Szolgáltatás letiltása a rendszerindításkor:
  ```bash
  systemctl disable nginx
  ```

## Tippek
- Mindig ellenőrizd a szolgáltatás állapotát a `status` opcióval, mielőtt bármilyen módosítást végeznél.
- Használj `--now` opciót az `enable` vagy `disable` parancsokkal, hogy azonnal alkalmazd a változtatásokat.
- A `list-units` opcióval megtekintheted az összes aktív szolgáltatást és egységet:
  ```bash
  systemctl list-units --type=service
  ```