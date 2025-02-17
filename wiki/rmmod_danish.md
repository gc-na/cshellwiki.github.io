# [Linux] Bash rmmod brug: Fjerner moduler fra Linux-kernen

## Oversigt
`rmmod` er et Bash-kommando, der bruges til at fjerne (eller afmontere) moduler fra Linux-kernen. Dette kan være nyttigt, når du ønsker at frigøre ressourcer eller opdatere en modul uden at genstarte systemet.

## Brug
Den grundlæggende syntaks for `rmmod`-kommandoen er som følger:

```bash
rmmod [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Tvinger fjernelse af modulet, selvom det er i brug.
- `--wait`: Venter på, at alle referencer til modulet er frigivet, før det fjernes.
- `-n`: Angiver ikke at opdatere modulkataloget.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `rmmod` kan bruges:

1. **Fjern et modul**
   ```bash
   rmmod my_module
   ```

2. **Tving fjernelse af et modul**
   ```bash
   rmmod -f my_module
   ```

3. **Vent på frigivelse af referencer**
   ```bash
   rmmod --wait my_module
   ```

4. **Fjern flere moduler på én gang**
   ```bash
   rmmod module1 module2 module3
   ```

## Tips
- Sørg for at kontrollere, om modulet er i brug, før du forsøger at fjerne det, da det kan forårsage systemproblemer.
- Brug `lsmod`-kommandoen til at se en liste over indlæste moduler, før du fjerner et modul.
- Vær forsigtig med at bruge `-f`-muligheden, da det kan føre til ustabilitet, hvis modulet stadig er aktivt.