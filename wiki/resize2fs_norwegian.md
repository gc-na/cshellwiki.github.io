# [Linux] Bash resize2fs Bruk: Endre størrelsen på filsystemet

## Oversikt
`resize2fs` er et verktøy som brukes til å endre størrelsen på ext2, ext3 og ext4 filsystemer. Dette verktøyet kan både øke og redusere størrelsen på et filsystem, avhengig av behovene dine.

## Bruk
Grunnleggende syntaks for `resize2fs` er:

```bash
resize2fs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`: Tvinger endring av størrelse, selv om filsystemet er skadet.
- `-p`: Viser fremdriften mens operasjonen pågår.
- `-s`: Reduserer størrelsen på filsystemet til den angitte størrelsen.
- `-M`: Reduserer filsystemet til minimum størrelse.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `resize2fs`:

### Eksempel 1: Øke størrelsen på filsystemet
For å øke størrelsen på et filsystem som er montert på `/dev/sda1`, kan du bruke følgende kommando:

```bash
resize2fs /dev/sda1
```

### Eksempel 2: Redusere størrelsen på filsystemet
For å redusere størrelsen på et filsystem til 20 GB, kan du bruke:

```bash
resize2fs -s 20G /dev/sda1
```

### Eksempel 3: Vise fremdrift under endring
For å vise fremdriften mens du endrer størrelsen på filsystemet, kan du bruke:

```bash
resize2fs -p /dev/sda1
```

## Tips
- Sørg for å ta en sikkerhetskopi av dataene dine før du endrer størrelsen på filsystemet, da det alltid er en risiko for datatap.
- Det er best å utføre `resize2fs` når filsystemet er avmontert for å unngå potensielle problemer.
- Kontroller alltid filsystemet med `fsck` før og etter du endrer størrelsen, for å sikre at det ikke er noen feil.