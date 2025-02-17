# [Linux] Bash fsck použití: Oprava souborových systémů

## Přehled
Příkaz `fsck` (file system check) slouží k procházení a opravě souborových systémů v Linuxu. Je určen k detekci a opravě chyb v souborových systémech, což může být užitečné po neplánovaném vypnutí systému nebo po poškození disku.

## Použití
Základní syntaxe příkazu `fsck` je následující:

```bash
fsck [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Automaticky opraví chyby bez interakce uživatele.
- `-n`: Provede kontrolu souborového systému, ale neprovádí žádné opravy.
- `-y`: Odpoví na všechny dotazy "ano", což znamená, že všechny nalezené chyby budou opraveny automaticky.
- `-t`: Umožňuje specifikovat typ souborového systému, například `ext4`, `vfat`, atd.

## Běžné příklady
1. Kontrola a oprava souborového systému na zařízení `/dev/sda1`:
   ```bash
   fsck /dev/sda1
   ```

2. Automatická oprava chyb bez interakce:
   ```bash
   fsck -a /dev/sda1
   ```

3. Kontrola souborového systému bez oprav:
   ```bash
   fsck -n /dev/sda1
   ```

4. Oprava všech chyb automaticky:
   ```bash
   fsck -y /dev/sda1
   ```

## Tipy
- Vždy zálohujte důležitá data před použitím příkazu `fsck`, protože opravy mohou vést k dalšímu poškození dat.
- Je dobré spustit `fsck` při bootování systému v režimu pro obnovu, aby se minimalizovalo riziko poškození souborového systému.
- Pokud je to možné, používejte `fsck` na odpojených souborových systémech, aby se předešlo konfliktům s běžícími procesy.