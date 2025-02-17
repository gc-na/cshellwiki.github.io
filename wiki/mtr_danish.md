# [Linux] Bash mtr brug: Netværksfejlfinding

## Oversigt
mtr (My Traceroute) er et værktøj, der kombinerer funktionerne fra traceroute og ping. Det bruges til at diagnosticere netværksproblemer ved at vise ruten og den tid, det tager at nå hver hop i netværket.

## Brug
Den grundlæggende syntaks for mtr-kommandoen er:

```bash
mtr [muligheder] [mål]
```

## Almindelige muligheder
- `-r`: Kør i rapporttilstand og vis resultaterne, når de er færdige.
- `-c [antal]`: Angiv antallet af pakker, der skal sendes.
- `-i [sekunder]`: Angiv intervallet mellem hver pakke.
- `-p`: Kør mtr i en permanent tilstand, der opdaterer resultaterne løbende.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger mtr:

1. **Grundlæggende brug**:
   For at se ruten til en given adresse, f.eks. google.com:
   ```bash
   mtr google.com
   ```

2. **Rapporttilstand**:
   For at køre mtr i rapporttilstand og vise resultaterne, når de er færdige:
   ```bash
   mtr -r google.com
   ```

3. **Angiv antal pakker**:
   For at sende 10 pakker til en destination:
   ```bash
   mtr -c 10 google.com
   ```

4. **Ændre intervallet mellem pakker**:
   For at sende pakker hvert 2. sekund:
   ```bash
   mtr -i 2 google.com
   ```

## Tips
- Brug `-r` muligheden, når du ønsker en hurtig oversigt over forbindelsen uden at se opdateringer i realtid.
- Kombiner `-c` og `-i` for at tilpasse din test, så den passer til dine behov.
- Hvis du oplever langsomme forbindelser, kan du bruge mtr til at identificere, hvilket hop der forårsager problemet.