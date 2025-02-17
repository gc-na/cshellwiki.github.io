# [Linux] Bash systemctl brug: Administrer systemtjenester

## Oversigt
`systemctl` er et kommandolinjeværktøj, der bruges til at kontrollere systemtjenester og enheder i systemd, som er init-systemet for mange Linux-distributioner. Det giver brugerne mulighed for at starte, stoppe, genstarte og overvåge tjenester.

## Brug
Den grundlæggende syntaks for `systemctl`-kommandoen er:

```bash
systemctl [muligheder] [argumenter]
```

## Almindelige muligheder
- `start`: Starter en tjeneste.
- `stop`: Stopper en tjeneste.
- `restart`: Genstarter en tjeneste.
- `status`: Viser status for en tjeneste.
- `enable`: Aktiverer en tjeneste til at starte automatisk ved opstart.
- `disable`: Deaktiverer en tjeneste fra at starte automatisk.
- `list-units`: Viser en liste over aktive enheder.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `systemctl`:

1. **Starte en tjeneste:**
   ```bash
   sudo systemctl start apache2
   ```

2. **Stoppe en tjeneste:**
   ```bash
   sudo systemctl stop apache2
   ```

3. **Genstarte en tjeneste:**
   ```bash
   sudo systemctl restart apache2
   ```

4. **Tjekke status for en tjeneste:**
   ```bash
   systemctl status apache2
   ```

5. **Aktivere en tjeneste ved opstart:**
   ```bash
   sudo systemctl enable apache2
   ```

6. **Deaktivere en tjeneste ved opstart:**
   ```bash
   sudo systemctl disable apache2
   ```

7. **Liste aktive enheder:**
   ```bash
   systemctl list-units --type=service
   ```

## Tips
- Brug `sudo` for at udføre kommandoer, der kræver administrative rettigheder.
- Tjek status for en tjeneste, hvis du oplever problemer, for at få indsigt i eventuelle fejl.
- Brug `systemctl list-units --failed` for hurtigt at finde enheder, der ikke fungerer korrekt.
- Vær opmærksom på, at ændringer i tjenesteindstillinger kræver genstart af tjenesten for at træde i kraft.