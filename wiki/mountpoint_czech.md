# [Linux] Bash mountpoint použití: Zjistit, zda je cesta montovací bod

## Overview
Příkaz `mountpoint` slouží k určení, zda je zadaná cesta montovacím bodem. To znamená, že můžete snadno zjistit, zda je adresář připojen k nějakému souborovému systému.

## Usage
Základní syntaxe příkazu je následující:

```bash
mountpoint [options] [arguments]
```

## Common Options
- `-q`: Tichý režim. Neprovádí žádný výstup, pouze vrací stav.
- `-d`: Zobrazí podrobnosti o montovacím bodu, pokud je nalezen.

## Common Examples

### Základní použití
Zjistit, zda je `/mnt/data` montovací bod:

```bash
mountpoint /mnt/data
```

### Tichý režim
Zkontrolovat, zda je `/media/usb` montovací bod bez výstupu:

```bash
mountpoint -q /media/usb
```

### Zobrazení podrobností
Získat podrobnosti o montovacím bodu `/mnt/backup`:

```bash
mountpoint -d /mnt/backup
```

## Tips
- Používejte tichý režim `-q`, pokud potřebujete pouze zjistit stav bez zbytečného výstupu.
- Před použitím příkazu se ujistěte, že cesta, kterou kontrolujete, existuje, abyste se vyhnuli chybovým hlášením.
- `mountpoint` je užitečný při skriptování, kde potřebujete ověřit, zda je určité zařízení připojeno před provedením dalších operací.