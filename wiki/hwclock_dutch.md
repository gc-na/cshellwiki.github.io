# [Linux] Bash hwclock gebruik: Beheer de systeemklok

## Overzicht
De `hwclock`-opdracht wordt gebruikt om de hardwareklok van een computer te beheren. Deze klok, ook wel de Real Time Clock (RTC) genoemd, houdt de tijd bij, zelfs wanneer de computer is uitgeschakeld. Met `hwclock` kun je de tijd van de hardwareklok lezen, instellen of synchroniseren met de systeemklok.

## Gebruik
De basis syntaxis van de `hwclock`-opdracht is als volgt:

```bash
hwclock [opties] [argumenten]
```

## Veelvoorkomende opties
- `--show`: Toont de huidige tijd van de hardwareklok.
- `--set`: Stelt de hardwareklok in op de opgegeven tijd.
- `--systohc`: Synchroniseert de systeemklok met de hardwareklok.
- `--hctosys`: Synchroniseert de hardwareklok met de systeemklok.
- `--utc`: Geeft aan dat de hardwareklok in UTC-tijd is ingesteld.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `hwclock`:

1. **Toon de huidige tijd van de hardwareklok:**
   ```bash
   hwclock --show
   ```

2. **Stel de hardwareklok in op een specifieke tijd:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. **Synchroniseer de systeemklok met de hardwareklok:**
   ```bash
   hwclock --systohc
   ```

4. **Synchroniseer de hardwareklok met de systeemklok:**
   ```bash
   hwclock --hctosys
   ```

5. **Toon de tijd van de hardwareklok in UTC:**
   ```bash
   hwclock --show --utc
   ```

## Tips
- Zorg ervoor dat je de juiste tijdzone hebt ingesteld op je systeem voordat je de hardwareklok synchroniseert.
- Het is een goed idee om regelmatig de hardwareklok te controleren, vooral na een lange periode van uitschakeling van de computer.
- Gebruik `hwclock` met root-rechten voor het instellen of synchroniseren van de klok.