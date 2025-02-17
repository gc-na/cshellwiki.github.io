# [Linux] Bash sysctl användning: Hantera kärnparametrar

## Översikt
`sysctl` är ett verktyg i Linux som används för att läsa och ändra kärnparametrar i realtid. Det gör det möjligt för användare att justera systeminställningar utan att behöva starta om systemet.

## Användning
Den grundläggande syntaxen för `sysctl` är:

```bash
sysctl [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visa alla kärnparametrar.
- `-w`: Skriv (ändra) en kärnparameter.
- `-n`: Visa värdet av en kärnparameter utan att skriva ut namnet.
- `-p`: Ladda kärnparametrar från en specifik fil.

## Vanliga exempel
Här är några praktiska exempel på hur `sysctl` kan användas:

1. Visa alla kärnparametrar:
   ```bash
   sysctl -a
   ```

2. Visa värdet av en specifik kärnparameter, till exempel `vm.swappiness`:
   ```bash
   sysctl -n vm.swappiness
   ```

3. Ändra värdet av `vm.swappiness` till 10:
   ```bash
   sysctl -w vm.swappiness=10
   ```

4. Ladda kärnparametrar från en fil, till exempel `/etc/sysctl.conf`:
   ```bash
   sysctl -p
   ```

## Tips
- Kontrollera alltid aktuella värden innan du gör ändringar för att förstå hur de påverkar systemet.
- Använd `sysctl -a` för att få en översikt över alla tillgängliga parametrar och deras nuvarande värden.
- För att göra ändringar permanenta, lägg till dem i `/etc/sysctl.conf` så att de laddas vid systemstart.