# [Linux] Bash timedatectl användning: Hantera systemtid och datum

## Översikt
`timedatectl` är ett kommando som används för att visa och ändra systemets tid och datum, samt för att konfigurera tidszoner. Det är en del av systemd och ger användare möjlighet att hantera tid och datum på ett enkelt sätt.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
timedatectl [alternativ] [argument]
```

## Vanliga alternativ
- `status`: Visar aktuell tid, datum och tidszon.
- `set-time [TIME]`: Sätter systemets tid till den angivna tiden.
- `set-timezone [ZONE]`: Ändrar systemets tidszon.
- `set-ntp [boolean]`: Aktiverar eller inaktiverar NTP (Network Time Protocol) synkronisering.
- `list-timezones`: Visar en lista över tillgängliga tidszoner.

## Vanliga exempel
För att visa systemets aktuella tid och datum:

```bash
timedatectl status
```

För att sätta systemets tid till 15:30 den 1 januari 2023:

```bash
timedatectl set-time '2023-01-01 15:30:00'
```

För att ändra systemets tidszon till Stockholm:

```bash
timedatectl set-timezone Europe/Stockholm
```

För att aktivera NTP-synkronisering:

```bash
timedatectl set-ntp true
```

För att lista alla tillgängliga tidszoner:

```bash
timedatectl list-timezones
```

## Tips
- Kontrollera alltid att NTP är aktiverat för att säkerställa att systemtiden hålls korrekt.
- Använd `list-timezones` för att hitta rätt tidszon innan du gör ändringar.
- Var försiktig när du sätter tiden manuellt, eftersom det kan påverka schemalagda uppgifter och loggar.