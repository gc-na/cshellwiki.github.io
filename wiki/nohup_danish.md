# [Linux] Bash nohup brug: Kør kommandoer uden at blive påvirket af logud

## Oversigt
`nohup` (no hang up) er et Bash-kommando, der gør det muligt at køre en proces, selvom brugeren logger ud af systemet. Det er nyttigt til langvarige opgaver, der skal fortsætte med at køre, selv når terminalen lukkes.

## Brug
Den grundlæggende syntaks for `nohup`-kommandoen er:

```bash
nohup [options] [arguments]
```

## Almindelige muligheder
- `&`: Kører kommandoen i baggrunden.
- `-h`: Viser hjælp og information om brugen af `nohup`.
- `output_file`: Angiver en fil, hvor output fra kommandoen skal gemmes (standard er `nohup.out`).

## Almindelige eksempler
Her er nogle praktiske eksempler på brug af `nohup`:

1. Kør en script-fil i baggrunden:
   ```bash
   nohup ./mit_script.sh &
   ```

2. Kør en langvarig kommando og gem output i en specifik fil:
   ```bash
   nohup long_running_command > output.txt &
   ```

3. Kør en Python-server, der fortsætter med at køre efter logud:
   ```bash
   nohup python3 -m http.server 8000 &
   ```

## Tips
- Brug `&` for at sikre, at kommandoen kører i baggrunden, så du kan fortsætte med at bruge terminalen.
- Tjek `nohup.out`-filen for output, hvis du ikke angiver en specifik output-fil.
- Overvej at bruge `screen` eller `tmux` til mere avanceret session management, hvis du har brug for at interagere med processen senere.