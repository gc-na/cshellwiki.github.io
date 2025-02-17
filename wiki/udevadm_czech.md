# [Linux] Bash udevadm použití: Správa zařízení v systému

## Přehled
Příkaz `udevadm` slouží k interakci s udev, což je systém pro správu zařízení v Linuxu. Umožňuje uživatelům spravovat a monitorovat zařízení připojená k systému, jako jsou USB disky, síťové karty a další hardware.

## Použití
Základní syntaxe příkazu `udevadm` je následující:

```bash
udevadm [možnosti] [argumenty]
```

## Běžné možnosti
- `info`: Zobrazí informace o zařízení.
- `trigger`: Spustí události pro zařízení.
- `settle`: Čeká, dokud se všechny události zařízení nevyřeší.
- `control`: Ovládá udev daemon (např. start, stop).
- `monitor`: Sleduje události zařízení v reálném čase.

## Běžné příklady
### Získání informací o zařízení
Chcete-li získat informace o konkrétním zařízení, použijte:

```bash
udevadm info --query=all --name=/dev/sda
```

### Spuštění událostí pro zařízení
Pokud potřebujete spustit události pro všechna zařízení, použijte:

```bash
udevadm trigger
```

### Čekání na vyřešení událostí
Pokud chcete čekat, dokud se všechny události nevyřeší, použijte:

```bash
udevadm settle
```

### Monitorování událostí zařízení
Pro sledování událostí zařízení v reálném čase můžete použít:

```bash
udevadm monitor
```

## Tipy
- Při používání `udevadm` je dobré mít na paměti, že některé akce mohou vyžadovat administrátorská práva, takže je vhodné používat `sudo`, pokud narazíte na problémy s oprávněními.
- Pravidelně monitorujte události zařízení, zejména při připojování nového hardwaru, abyste zajistili, že systém správně reaguje na změny.
- Používejte `udevadm info` k diagnostice problémů s detekcí zařízení, což může pomoci při řešení problémů s hardwarem.