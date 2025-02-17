# [Linux] Bash shutdown brug: Luk systemet ned

## Overview
`shutdown`-kommandoen bruges til at lukke et Linux-system ned på en sikker måde. Den giver mulighed for at planlægge nedlukninger, genstart og sende meddelelser til brugere, der er logget ind på systemet.

## Usage
Den grundlæggende syntaks for `shutdown`-kommandoen er:

```bash
shutdown [options] [time] [message]
```

## Common Options
- `-h`: Luk systemet helt ned.
- `-r`: Genstart systemet.
- `-P`: Sluk for systemet (standard adfærd).
- `now`: Angiver, at nedlukningen skal ske med det samme.
- `+m`: Angiver, at nedlukningen skal ske efter m minutter.
- `hh:mm`: Angiver det præcise tidspunkt for nedlukningen i 24-timers format.

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `shutdown`-kommandoen:

1. Luk systemet ned med det samme:
    ```bash
    shutdown -h now
    ```

2. Genstart systemet om 5 minutter:
    ```bash
    shutdown -r +5
    ```

3. Luk systemet ned kl. 22:00:
    ```bash
    shutdown -h 22:00
    ```

4. Send en meddelelse til alle brugere før nedlukning:
    ```bash
    shutdown -h +1 "Systemet lukker ned om 1 minut."
    ```

5. Tving nedlukning uden at vente på aktive brugere:
    ```bash
    shutdown -h now -f
    ```

## Tips
- Sørg for at informere brugerne om en kommende nedlukning for at undgå tab af data.
- Brug `shutdown -c` for at annullere en planlagt nedlukning.
- Overvej at bruge `at`-kommandoen til at planlægge nedlukninger på bestemte tidspunkter, hvis det er nødvendigt.