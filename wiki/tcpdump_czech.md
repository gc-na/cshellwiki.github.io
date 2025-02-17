# [Linux] Bash tcpdump použití: Sledování síťového provozu

## Přehled
Příkaz `tcpdump` slouží k zachycování a analýze síťového provozu. Umožňuje uživatelům sledovat data přenášená přes síťové rozhraní a poskytuje cenné informace pro diagnostiku a monitorování síťových aktivit.

## Použití
Základní syntaxe příkazu `tcpdump` je následující:

```bash
tcpdump [možnosti] [argumenty]
```

## Běžné možnosti
- `-i <rozhraní>`: Určuje síťové rozhraní, které má být sledováno (např. `eth0`).
- `-n`: Zabraňuje převodu adres IP na názvy hostitelů.
- `-v`: Zvyšuje úroveň podrobností výstupu.
- `-c <počet>`: Ukončuje zachytávání po zadaném počtu paketů.
- `-w <soubor>`: Ukládá zachycené pakety do souboru pro pozdější analýzu.
- `-r <soubor>`: Čte pakety ze souboru místo ze síťového rozhraní.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `tcpdump`:

1. **Zachytávání paketů na specifickém rozhraní:**
   ```bash
   tcpdump -i eth0
   ```

2. **Zachytávání paketů bez převodu adres:**
   ```bash
   tcpdump -i eth0 -n
   ```

3. **Zachytávání prvních 10 paketů:**
   ```bash
   tcpdump -i eth0 -c 10
   ```

4. **Ukládání zachycených paketů do souboru:**
   ```bash
   tcpdump -i eth0 -w zachytane_pakety.pcap
   ```

5. **Čtení paketů ze souboru:**
   ```bash
   tcpdump -r zachytane_pakety.pcap
   ```

## Tipy
- Používejte možnost `-n`, pokud nechcete, aby se příkaz pokoušel převádět IP adresy na názvy hostitelů, což může urychlit proces.
- Při analýze velkého množství dat je užitečné ukládat pakety do souboru a později je analyzovat pomocí specializovaných nástrojů jako Wireshark.
- Vždy se ujistěte, že máte potřebná oprávnění pro sledování síťového provozu, protože některé operace mohou vyžadovat administrátorská práva.