# [Linux] Bash hostname brug: Viser eller ændrer værtsnavnet

## Oversigt
`hostname`-kommandoen bruges til at vise eller ændre værtsnavnet på en computer. Værtsnavnet er det navn, som en computer identificeres med på et netværk, og det kan være nyttigt til både netværksadministration og fejlfinding.

## Brug
Den grundlæggende syntaks for `hostname`-kommandoen er:

```bash
hostname [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`, `--alias`: Viser værtsaliaset.
- `-d`, `--domain`: Viser domænenavnet.
- `-f`, `--fqdn`: Viser det fuldt kvalificerede domænenavn (FQDN).
- `-i`, `--ip-address`: Viser IP-adressen for værtsnavnet.
- `-s`, `--short`: Viser det korte værtsnavn.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `hostname`-kommandoen:

1. **Vis det nuværende værtsnavn**:
   ```bash
   hostname
   ```

2. **Vis det fuldt kvalificerede domænenavn**:
   ```bash
   hostname -f
   ```

3. **Vis IP-adressen for værtsnavnet**:
   ```bash
   hostname -i
   ```

4. **Ændre værtsnavnet midlertidigt**:
   ```bash
   sudo hostname ny-værtsnavn
   ```

5. **Vis domænenavnet**:
   ```bash
   hostname -d
   ```

## Tips
- For at gøre ændringerne permanente, skal du redigere `/etc/hostname` og `/etc/hosts` filer.
- Brug `hostnamectl`-kommandoen på systemer med systemd for mere avanceret håndtering af værtsnavne.
- Kontroller altid, at det nye værtsnavn ikke allerede er i brug på netværket for at undgå konflikter.