# [Linux] Bash uživatelé příkaz: Zobrazit informace o uživatelích

## Přehled
Příkaz `users` v Bashu slouží k zobrazení seznamu aktuálně přihlášených uživatelů v systému. Tento příkaz je užitečný pro rychlé získání přehledu o tom, kdo je momentálně aktivní na systému.

## Použití
Základní syntaxe příkazu je následující:

```bash
users [options]
```

## Běžné možnosti
- `-n`: Zobrazí pouze unikátní uživatelská jména.
- `-u`: Zobrazí uživatelská jména spolu s jejich ID.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `users`:

1. Základní použití pro zobrazení přihlášených uživatelů:

    ```bash
    users
    ```

2. Zobrazení unikátních uživatelských jmen:

    ```bash
    users -n
    ```

3. Zobrazení uživatelských jmen s jejich ID:

    ```bash
    users -u
    ```

## Tipy
- Používejte příkaz `who` pro podrobnější informace o přihlášených uživatelích, jako je čas přihlášení a terminál.
- Pokud potřebujete sledovat aktivitu uživatelů v reálném čase, zkombinujte příkaz `users` s příkazem `watch`:

    ```bash
    watch users
    ``` 

Tento příkaz vám umožní pravidelně aktualizovat seznam přihlášených uživatelů.