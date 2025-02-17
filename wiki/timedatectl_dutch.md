# [Linux] Bash timedatectl gebruik: Beheer tijd en datum instellingen

## Overzicht
De `timedatectl` opdracht is een hulpmiddel in Linux dat wordt gebruikt om de systeemdatum en -tijd te beheren. Het biedt een interface om de tijdzone in te stellen, de systeemklok te synchroniseren en de huidige tijd- en datuminstellingen te bekijken.

## Gebruik
De basis syntaxis van de `timedatectl` opdracht is:

```bash
timedatectl [opties] [argumenten]
```

## Veelvoorkomende opties
- `set-time`: Stel de systeemdatum en -tijd in.
- `set-timezone`: Wijzig de tijdzone van het systeem.
- `status`: Toon de huidige tijd- en datuminstellingen.
- `list-timezones`: Lijst alle beschikbare tijdzones.
- `set-ntp`: Schakel Network Time Protocol (NTP) in of uit.

## Veelvoorkomende voorbeelden
- **Bekijk de huidige tijd- en datuminstellingen:**
  ```bash
  timedatectl status
  ```

- **Stel de systeemdatum en -tijd in:**
  ```bash
  timedatectl set-time '2023-10-01 12:00:00'
  ```

- **Wijzig de tijdzone naar Amsterdam:**
  ```bash
  timedatectl set-timezone Europe/Amsterdam
  ```

- **Lijst alle beschikbare tijdzones:**
  ```bash
  timedatectl list-timezones
  ```

- **Schakel NTP in voor automatische tijdsynchronisatie:**
  ```bash
  timedatectl set-ntp true
  ```

## Tips
- Zorg ervoor dat je de juiste tijdzone selecteert om tijdsverwarring te voorkomen.
- Gebruik de `status` optie regelmatig om te controleren of je systeemklok correct is ingesteld.
- Overweeg om NTP in te schakelen voor automatische synchronisatie met internetservers, wat helpt om de tijd nauwkeurig te houden.