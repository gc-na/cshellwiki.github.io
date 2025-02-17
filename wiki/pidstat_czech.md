# [Linux] Bash pidstat použití: Sledování statistiky procesů

## Přehled
Příkaz `pidstat` slouží k monitorování výkonu procesů v systému. Umožňuje uživatelům sledovat různé statistiky, jako je využití CPU, paměti a další parametry pro jednotlivé procesy.

## Použití
Základní syntaxe příkazu je následující:

```bash
pidstat [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí hlavičku s informacemi o sloupcích.
- `-r`: Zobrazí využití paměti procesy.
- `-u`: Zobrazí využití CPU procesy.
- `-p <pid>`: Sleduje konkrétní proces podle jeho PID.
- `-t`: Zobrazí statistiky pro všechny vlákna procesu.

## Běžné příklady
1. **Zobrazení využití CPU pro všechny procesy:**

```bash
pidstat -u
```

2. **Zobrazení využití paměti pro všechny procesy:**

```bash
pidstat -r
```

3. **Sledování konkrétního procesu podle PID:**

```bash
pidstat -p 1234
```

4. **Zobrazení statistik pro všechny vlákna procesu:**

```bash
pidstat -t -p 1234
```

5. **Zobrazení statistiky každé 2 sekundy:**

```bash
pidstat 2
```

## Tipy
- Používejte `-h`, abyste získali přehledné hlavičky sloupců, což usnadní čtení výstupu.
- Kombinujte možnosti, například `pidstat -u -r`, pro získání komplexního pohledu na výkon procesů.
- Sledujte procesy v reálném čase pomocí příkazu `pidstat` s intervalem, abyste mohli rychle reagovat na problémy s výkonem.