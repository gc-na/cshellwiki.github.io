# [Linux] Bash docker-compose použití: Správa více kontejnerů Docker

## Přehled
Příkaz `docker-compose` slouží k definování a správě více kontejnerů Docker jako jedné aplikace. Umožňuje uživatelům snadno spouštět, zastavovat a spravovat skupiny kontejnerů pomocí jednoduchého konfiguračního souboru.

## Použití
Základní syntaxe příkazu je následující:

```bash
docker-compose [options] [arguments]
```

## Běžné možnosti
- `up`: Spustí kontejnery definované v souboru `docker-compose.yml`.
- `down`: Zastaví a odstraní kontejnery, sítě a objemy vytvořené příkazem `up`.
- `build`: Sestaví nebo znovu sestaví služby definované v `docker-compose.yml`.
- `logs`: Zobrazí výstup protokolů pro kontejnery.
- `exec`: Spustí příkaz v běžícím kontejneru.

## Běžné příklady
1. **Spuštění kontejnerů**:
   ```bash
   docker-compose up
   ```

2. **Spuštění kontejnerů na pozadí**:
   ```bash
   docker-compose up -d
   ```

3. **Zastavení a odstranění kontejnerů**:
   ```bash
   docker-compose down
   ```

4. **Sestavení kontejnerů**:
   ```bash
   docker-compose build
   ```

5. **Zobrazení protokolů**:
   ```bash
   docker-compose logs
   ```

6. **Spuštění příkazu v kontejneru**:
   ```bash
   docker-compose exec <service_name> <command>
   ```

## Tipy
- Vždy používejte soubor `docker-compose.yml` pro definici vašich služeb, aby bylo možné snadno spravovat konfiguraci.
- Používejte příznak `-d`, pokud chcete spustit kontejnery na pozadí a uvolnit terminál.
- Pravidelně kontrolujte protokoly pomocí `docker-compose logs`, abyste sledovali stav aplikace a odhalili případné problémy.
- Při úpravách konfiguračního souboru nezapomeňte znovu sestavit kontejnery pomocí `docker-compose up --build`.