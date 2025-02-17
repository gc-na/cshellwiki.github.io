# [Linux] Bash popd brug: Gå tilbage til den tidligere mappe

## Oversigt
`popd`-kommandoen bruges til at skifte tilbage til den tidligere mappe, der er gemt i stakken af mapper. Det er en nyttig funktion i forbindelse med `pushd`, som tilføjer en mappe til stakken. Ved at bruge `popd` kan du nemt navigere tilbage til en tidligere placering uden at skulle indtaste hele stien.

## Brug
Den grundlæggende syntaks for `popd`-kommandoen er som følger:

```bash
popd [options] [arguments]
```

## Almindelige muligheder
- `-n`: Udfør ikke ændringen af den nuværende mappe, men vis den næste mappe i stakken.
- `+n`: Gå til den n-te mappe i stakken, hvor `n` er et helt tal, der angiver positionen i stakken.
- `-n`: Gå til den n-te mappe fra slutningen af stakken.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `popd`:

1. **Skift tilbage til den tidligere mappe:**
   ```bash
   pushd /home/user/documents
   pushd /home/user/downloads
   popd
   ```
   Dette vil tage dig tilbage til `/home/user/documents`.

2. **Vis den næste mappe i stakken uden at skifte:**
   ```bash
   pushd /var/log
   pushd /etc
   popd -n
   ```
   Her vil `popd -n` vise den næste mappe i stakken, men skifter ikke til den.

3. **Gå til en specifik mappe i stakken:**
   ```bash
   pushd /usr/local
   pushd /usr/bin
   popd +1
   ```
   Dette vil tage dig til `/usr/local`, som er den næstsidste mappe i stakken.

## Tips
- Brug `pushd` og `popd` sammen for effektiv navigation mellem mapper.
- Tjek stakken af mapper med `dirs` for at se, hvilke mapper der er gemt.
- Vær opmærksom på, at `popd` fjerner den øverste mappe fra stakken, så sørg for at du ikke mister vigtige stier.