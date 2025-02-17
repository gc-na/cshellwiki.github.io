# [Linux] Bash chkconfig brug: Administrer systemtjenester

## Oversigt
`chkconfig` er et kommandolinjeværktøj, der bruges til at administrere systemtjenester på Linux-systemer. Det gør det muligt at aktivere eller deaktivere tjenester ved opstart og kontrollere deres status.

## Brug
Den grundlæggende syntaks for `chkconfig`-kommandoen er som følger:

```bash
chkconfig [options] [arguments]
```

## Almindelige muligheder
- `--list`: Viser en liste over alle tjenester og deres aktiveringsstatus.
- `--add`: Tilføjer en tjeneste til systemet.
- `--del`: Fjerner en tjeneste fra systemet.
- `--level`: Angiver niveauet (runlevel), hvor tjenesten skal aktiveres eller deaktiveres.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `chkconfig`:

1. **Liste alle tjenester**:
   ```bash
   chkconfig --list
   ```

2. **Aktivere en tjeneste ved opstart**:
   ```bash
   chkconfig httpd on
   ```

3. **Deaktivere en tjeneste ved opstart**:
   ```bash
   chkconfig httpd off
   ```

4. **Fjerne en tjeneste**:
   ```bash
   chkconfig --del httpd
   ```

5. **Tilføje en tjeneste**:
   ```bash
   chkconfig --add myservice
   ```

## Tips
- Sørg for at køre `chkconfig` med root-rettigheder for at kunne ændre tjenesternes status.
- Brug `chkconfig --list` regelmæssigt for at holde styr på, hvilke tjenester der er aktiveret ved opstart.
- Vær opmærksom på, at ændringer foretaget med `chkconfig` kun gælder for de angivne runlevels.