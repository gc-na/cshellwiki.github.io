# [Linux] Bash uptime brug: Viser systemets driftstid

## Oversigt
`uptime`-kommandoen bruges til at vise, hvor længe systemet har været kørende, samt hvor mange brugere der er logget ind og systemets belastning i de seneste 1, 5 og 15 minutter. Dette kan være nyttigt til at overvåge systemets ydeevne og stabilitet.

## Brug
Den grundlæggende syntaks for `uptime`-kommandoen er:

```bash
uptime [options]
```

## Almindelige muligheder
- `-p` : Viser driftstiden i et mere læsbart format.
- `-s` : Viser tidspunktet for systemets seneste opstart.

## Almindelige eksempler

1. **Vis driftstid og systembelastning:**
   ```bash
   uptime
   ```
   Dette viser systemets driftstid, antallet af brugere og belastningen.

2. **Vis driftstid i et læsbart format:**
   ```bash
   uptime -p
   ```
   Dette viser driftstiden i et mere forståeligt format, f.eks. "oppe i 5 timer".

3. **Vis tidspunkt for seneste opstart:**
   ```bash
   uptime -s
   ```
   Dette viser det nøjagtige tidspunkt, hvor systemet sidst blev startet.

## Tips
- Brug `uptime` regelmæssigt for at overvåge systemets sundhed og ydeevne.
- Kombiner `uptime` med andre systemovervågningsværktøjer for en mere omfattende analyse.
- Tjek belastningen i forhold til antallet af brugere for at vurdere, om systemet er overbelastet.