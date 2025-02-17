# [Linux] Bash rehash použití: Obnovení seznamu příkazů

## Přehled
Příkaz `rehash` v Bash slouží k obnovení seznamu příkazů, které jsou uloženy v paměti. Když přidáte nové spustitelné soubory do adresáře, který je zahrnut v proměnné prostředí `PATH`, Bash nemusí automaticky rozpoznat tyto nové příkazy. Příkaz `rehash` aktualizuje tento seznam, což umožňuje okamžité použití nových příkazů.

## Použití
Základní syntaxe příkazu `rehash` je následující:

```bash
rehash [options] [arguments]
```

## Běžné možnosti
Příkaz `rehash` obvykle nemá žádné specifické možnosti, ale je důležité si uvědomit, že se používá bez dalších argumentů.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `rehash`:

1. **Obnovení seznamu příkazů po přidání nového spustitelného souboru:**

   Pokud jste přidali nový skript do adresáře `/usr/local/bin`, můžete použít:

   ```bash
   rehash
   ```

2. **Použití nového příkazu bez restartování shellu:**

   Po přidání nového příkazu do vašeho `PATH`, stačí spustit:

   ```bash
   rehash
   novy_prikaz
   ```

3. **Obnovení v interaktivním shellu:**

   Pokud pracujete v interaktivním shellu a chcete okamžitě použít nový příkaz:

   ```bash
   rehash
   ```

## Tipy
- **Pravidelně používejte `rehash`:** Pokud často přidáváte nové skripty nebo programy, je dobré pravidelně používat `rehash`, abyste zajistili, že máte aktuální seznam příkazů.
- **Zkontrolujte proměnnou `PATH`:** Ujistěte se, že adresáře, které obsahují vaše spustitelné soubory, jsou zahrnuty v proměnné `PATH`.
- **Používejte v interaktivních shellech:** Příkaz `rehash` je užitečný zejména v interaktivních shellech, kde potřebujete rychle reagovat na změny v dostupných příkazech.