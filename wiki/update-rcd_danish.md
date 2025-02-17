# [Linux] Bash update-rc.d brug: Administrer systemtjenester

## Oversigt
`update-rc.d` er et Bash-kommando, der bruges til at tilføje, fjerne eller ændre opstartsindstillinger for systemtjenester i Debian-baserede Linux-distributioner. Det hjælper med at konfigurere, hvordan og hvornår tjenester skal startes eller stoppes ved systemopstart.

## Brug
Den grundlæggende syntaks for `update-rc.d` er som følger:

```bash
update-rc.d [options] [arguments]
```

## Almindelige muligheder
- `defaults`: Tilføjer standard opstart og stop niveauer for tjenesten.
- `remove`: Fjerner tjenesten fra opstartssekvenserne.
- `enable`: Aktiverer tjenesten til at starte ved opstart.
- `disable`: Deaktiverer tjenesten fra at starte ved opstart.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `update-rc.d`:

1. **Tilføj en tjeneste med standardindstillinger:**
   ```bash
   sudo update-rc.d myservice defaults
   ```

2. **Fjern en tjeneste fra opstartssekvenserne:**
   ```bash
   sudo update-rc.d myservice remove
   ```

3. **Aktiver en tjeneste til opstart:**
   ```bash
   sudo update-rc.d myservice enable
   ```

4. **Deaktiver en tjeneste fra opstart:**
   ```bash
   sudo update-rc.d myservice disable
   ```

## Tips
- Sørg for at have de nødvendige rettigheder (typisk root) for at kunne ændre opstartsindstillinger.
- Kontroller altid, at tjenesten er korrekt konfigureret, før du tilføjer den til opstart.
- Brug `update-rc.d` i kombination med scripts i `/etc/init.d/` for at sikre, at dine tjenester fungerer korrekt ved opstart.