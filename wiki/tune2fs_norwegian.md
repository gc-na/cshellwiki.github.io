# [Linux] Bash tune2fs bruksanvisning: Justering av ext2/ext3/ext4 filsystemparametere

## Oversikt
`tune2fs` er et verktøy som brukes til å justere og endre parametere for ext2, ext3 og ext4 filsystemer. Det gir brukeren muligheten til å optimalisere ytelsen og administrere filsysteminnstillinger uten å måtte montere filsystemet på nytt.

## Bruk
Grunnleggende syntaks for `tune2fs`-kommandoen er som følger:

```bash
tune2fs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c <maks antall monteringer>`: Sett maksimum antall monteringer før filsystemet blir merket for sjekk.
- `-i <intervall>`: Sett tidsintervall for sjekk av filsystemet (f.eks. hver 30. dag).
- `-m <prosent>`: Sett prosentandelen av diskplass som skal reserveres for rotbrukeren.
- `-O <funksjoner>`: Aktiver spesifikke filsystemfunksjoner.
- `-L <etikett>`: Sett en ny etikett for filsystemet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `tune2fs`:

### Endre maksimum antall monteringer
For å sette maksimum antall monteringer til 20 før sjekk:

```bash
sudo tune2fs -c 20 /dev/sdX1
```

### Endre sjekkintervall
For å sette sjekkintervall til 14 dager:

```bash
sudo tune2fs -i 14d /dev/sdX1
```

### Reserver diskplass for rotbrukeren
For å reservere 5% av diskplassen for rotbrukeren:

```bash
sudo tune2fs -m 5 /dev/sdX1
```

### Aktiver en filsystemfunksjon
For å aktivere journaling-funksjonen:

```bash
sudo tune2fs -O has_journal /dev/sdX1
```

### Sett en ny etikett
For å sette etiketten "MinDisk" på filsystemet:

```bash
sudo tune2fs -L MinDisk /dev/sdX1
```

## Tips
- Sørg for å ta en sikkerhetskopi av viktige data før du gjør endringer i filsysteminnstillingene.
- Kjør `tune2fs` med `-l` for å vise gjeldende innstillinger og parametere for filsystemet.
- Bruk `tune2fs` med forsiktighet, spesielt når du endrer kritiske innstillinger som sjekkintervall og monteringer.