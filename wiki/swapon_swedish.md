# [Linux] Bash swapon användning: Aktivera swap-partitioner

## Översikt
Kommandot `swapon` används för att aktivera swap-partitioner eller swap-filer i Linux. Swap-minne används när det fysiska RAM-minnet är fullt, vilket gör att systemet kan hantera mer data än vad som ryms i det fysiska minnet.

## Användning
Den grundläggande syntaxen för kommandot `swapon` är:

```bash
swapon [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Aktiverar alla swap-enheter som anges i `/etc/fstab`.
- `-s`: Visar en sammanställning av aktiva swap-enheter.
- `--show`: Visar information om aktiva swap-enheter i ett mer detaljerat format.

## Vanliga exempel
Aktivera en specifik swap-partition:

```bash
sudo swapon /dev/sda2
```

Aktivera alla swap-enheter som anges i `/etc/fstab`:

```bash
sudo swapon -a
```

Visa en sammanställning av aktiva swap-enheter:

```bash
swapon -s
```

Visa detaljerad information om aktiva swap-enheter:

```bash
swapon --show
```

## Tips
- Kontrollera alltid att swap-enheter är korrekt konfigurerade i `/etc/fstab` för att säkerställa att de aktiveras vid systemstart.
- Använd `free -h` för att snabbt se hur mycket swap-minne som används och tillgängligt.
- Om du har flera swap-enheter, kan du prioritera dem genom att ange en prioritet i `/etc/fstab`.