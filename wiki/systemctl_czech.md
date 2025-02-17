# [Linux] Bash systemctl použití: Správa systémových služeb

## Přehled
Příkaz `systemctl` slouží k řízení a správě systémových služeb a jednotek v systému Linux, který používá systemd jako init systém. Umožňuje uživatelům spouštět, zastavovat, restartovat a spravovat služby a další systémové jednotky.

## Použití
Základní syntaxe příkazu `systemctl` je následující:

```bash
systemctl [možnosti] [argumenty]
```

## Běžné možnosti
- `start`: Spustí službu.
- `stop`: Zastaví službu.
- `restart`: Restartuje službu.
- `status`: Zobrazí stav služby.
- `enable`: Povolení služby při startu systému.
- `disable`: Zakáže službu při startu systému.
- `list-units`: Zobrazí seznam všech jednotek.

## Běžné příklady
1. **Spuštění služby**
   ```bash
   systemctl start název_služby
   ```

2. **Zastavení služby**
   ```bash
   systemctl stop název_služby
   ```

3. **Restartování služby**
   ```bash
   systemctl restart název_služby
   ```

4. **Zobrazení stavu služby**
   ```bash
   systemctl status název_služby
   ```

5. **Povolení služby při startu**
   ```bash
   systemctl enable název_služby
   ```

6. **Zakázání služby při startu**
   ```bash
   systemctl disable název_služby
   ```

7. **Zobrazení seznamu jednotek**
   ```bash
   systemctl list-units
   ```

## Tipy
- Při práci s `systemctl` je dobré mít administrátorská práva, proto často používejte `sudo`.
- Pro sledování logů služeb použijte příkaz `journalctl -u název_služby`.
- Před provedením změn v konfiguraci služby je doporučeno zkontrolovat její aktuální stav pomocí `systemctl status`.