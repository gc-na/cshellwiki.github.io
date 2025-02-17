# [Linux] Bash timedatectl brug: Administrer systemets dato og tid

## Oversigt
`timedatectl` er et værktøj, der bruges til at administrere systemets dato og tid, samt til at konfigurere tidszoner og synkronisering med tidsservere.

## Brug
Den grundlæggende syntaks for `timedatectl` er som følger:

```bash
timedatectl [muligheder] [argumenter]
```

## Almindelige muligheder
- `set-time <tid>`: Sætter systemets tid.
- `set-timezone <zone>`: Ændrer systemets tidszone.
- `status`: Viser den nuværende dato, tid og tidszone.
- `list-timezones`: Viser en liste over tilgængelige tidszoner.
- `set-ntp <boolean>`: Aktiverer eller deaktiverer NTP (Network Time Protocol) synkronisering.

## Almindelige eksempler
- For at vise den nuværende dato og tid:
  ```bash
  timedatectl status
  ```

- For at ændre systemets tid til 15:30:
  ```bash
  timedatectl set-time '15:30:00'
  ```

- For at ændre tidszonen til København:
  ```bash
  timedatectl set-timezone Europe/Copenhagen
  ```

- For at aktivere NTP synkronisering:
  ```bash
  timedatectl set-ntp true
  ```

- For at liste alle tilgængelige tidszoner:
  ```bash
  timedatectl list-timezones
  ```

## Tips
- Sørg for at have de nødvendige rettigheder (typisk root) for at ændre systemets tid og tidszone.
- Brug `timedatectl list-timezones` for at finde den korrekte tidszone, før du ændrer den.
- Det er en god idé at aktivere NTP for at sikre, at systemets tid altid er præcis.