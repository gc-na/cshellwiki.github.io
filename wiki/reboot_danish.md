# [Linux] Bash reboot brug: Genstart systemet

## Oversigt
`reboot`-kommandoen bruges til at genstarte systemet. Den afslutter alle aktive processer og genstarter maskinen, hvilket kan være nyttigt, når systemet kræver en genstart for at anvende opdateringer eller ændringer.

## Brug
Den grundlæggende syntaks for `reboot`-kommandoen er som følger:

```bash
reboot [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Tvinger genstart uden at sende signaler til processerne.
- `-n`: Ignorerer synkronisering af filsystemet, hvilket kan være hurtigere, men risikabelt.
- `-w`: Skriver kun til logfilerne uden at udføre genstart.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `reboot`-kommandoen:

1. **Standard genstart**:
   ```bash
   reboot
   ```

2. **Tving genstart**:
   ```bash
   reboot -f
   ```

3. **Genstart uden synkronisering**:
   ```bash
   reboot -n
   ```

4. **Skrive til logfiler uden at genstarte**:
   ```bash
   reboot -w
   ```

## Tips
- Sørg for at gemme dit arbejde, inden du bruger `reboot`, da alle åbne programmer lukkes.
- Brug `-f` med forsigtighed, da det kan føre til datatab, hvis der er aktive processer.
- Overvej at bruge `shutdown`-kommandoen, hvis du ønsker at give brugerne tid til at gemme deres arbejde, før systemet genstartes.