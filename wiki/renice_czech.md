# [Linux] Bash renice použití: Změna priority běžících procesů

## Přehled
Příkaz `renice` slouží k úpravě priority běžících procesů v systému. Pomocí tohoto příkazu můžete zvýšit nebo snížit prioritu procesů, což ovlivňuje, jak moc CPU času dostanou v porovnání s ostatními procesy.

## Použití
Základní syntaxe příkazu `renice` je následující:

```bash
renice [možnosti] [priorita] [PID]
```

## Běžné možnosti
- `-n`, `--priority`: Určuje novou prioritu procesu. Může být kladná (nízká priorita) nebo záporná (vysoká priorita).
- `-p`, `--pid`: Určuje PID (identifikační číslo procesu), jehož prioritu chcete změnit.
- `-g`, `--pgroup`: Změní prioritu celé skupiny procesů podle jejich skupinového ID.
- `-u`, `--user`: Změní prioritu všech procesů běžící pod daným uživatelským jménem.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `renice`:

1. **Zvýšení priority procesu**:
   Pokud chcete zvýšit prioritu procesu s PID 1234 na -5, použijte:
   ```bash
   renice -n -5 -p 1234
   ```

2. **Snížení priority procesu**:
   Pro snížení priority procesu s PID 5678 na 10, použijte:
   ```bash
   renice -n 10 -p 5678
   ```

3. **Změna priority všech procesů uživatele**:
   Pokud chcete změnit prioritu všech procesů běžících pod uživatelským jménem "uživatel" na 5, použijte:
   ```bash
   renice -n 5 -u uživatel
   ```

4. **Změna priority skupiny procesů**:
   Pro změnu priority všech procesů ve skupině s GID 1000 na 0, použijte:
   ```bash
   renice -n 0 -g 1000
   ```

## Tipy
- Při změně priority buďte opatrní, protože příliš vysoká priorita může způsobit, že jiné procesy budou mít nedostatek CPU času.
- Mějte na paměti, že pro snížení priority procesů s nižšími oprávněními budete potřebovat administrátorská práva.
- Používejte `renice` s rozmyslem, zejména na serverech, kde může ovlivnit výkon aplikací.