# [Linux] Bash sysctl brug: Justering af kernelparametre

## Oversigt
`sysctl` er et værktøj i Unix-lignende operativsystemer, der bruges til at ændre og vise kernelparametre i realtid. Det giver brugerne mulighed for at justere systemets opførsel uden at skulle genstarte maskinen.

## Brug
Den grundlæggende syntaks for `sysctl`-kommandoen er som følger:

```bash
sysctl [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`: Viser alle kernelparametre og deres nuværende værdier.
- `-w`: Sætter en kernelparameter til en ny værdi.
- `-n`: Viser kun værdien af den angivne parameter uden at vise navnet.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `sysctl`:

1. **Vis alle kernelparametre:**
   ```bash
   sysctl -a
   ```

2. **Ændre en kernelparameter:**
   For eksempel, for at ændre `vm.swappiness` til 10:
   ```bash
   sysctl -w vm.swappiness=10
   ```

3. **Vis værdien af en specifik parameter:**
   For at se værdien af `net.ipv4.ip_forward`:
   ```bash
   sysctl -n net.ipv4.ip_forward
   ```

4. **Gem ændringer permanent:**
   For at sikre, at ændringerne overlever en genstart, kan du tilføje dem til `/etc/sysctl.conf`. For eksempel:
   ```bash
   echo "vm.swappiness=10" >> /etc/sysctl.conf
   ```

5. **Anvend ændringer fra konfigurationsfilen:**
   Efter at have redigeret `/etc/sysctl.conf`, kan du anvende ændringerne med:
   ```bash
   sysctl -p
   ```

## Tips
- Vær forsigtig, når du ændrer kernelparametre, da forkert konfiguration kan påvirke systemets stabilitet.
- Brug `sysctl -a` til at få et overblik over alle tilgængelige parametre og deres nuværende indstillinger.
- Overvej at tage en sikkerhedskopi af din nuværende konfiguration, før du foretager ændringer.