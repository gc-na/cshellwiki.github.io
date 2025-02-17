# [Linux] Bash tune2fs brug: Justering af ext2/ext3/ext4 filsystemer

## Oversigt
`tune2fs` er et værktøj, der bruges til at justere og ændre indstillingerne for ext2, ext3 og ext4 filsystemer. Det giver brugerne mulighed for at ændre filsystemets metadata og konfigurationer, såsom mount-indstillinger og reserved space.

## Brug
Den grundlæggende syntaks for `tune2fs` er som følger:

```bash
tune2fs [muligheder] [argumenter]
```

## Almindelige muligheder
- `-o` : Angiv mount-indstillinger for filsystemet.
- `-m` : Angiv procentdelen af plads, der skal reserveres til root-brugeren.
- `-c` : Angiv det maksimale antal mounts før en kontrol.
- `-i` : Angiv intervallet mellem kontroller i dage.
- `-L` : Ændre filsystemets label.
- `-U` : Ændre UUID for filsystemet.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `tune2fs`:

1. **Ændre mount-indstillinger:**
   ```bash
   tune2fs -o journal_data /dev/sda1
   ```

2. **Reservere plads til root-brugeren:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

3. **Sætte kontrol efter et bestemt antal mounts:**
   ```bash
   tune2fs -c 30 /dev/sda1
   ```

4. **Ændre filsystemets label:**
   ```bash
   tune2fs -L MyLabel /dev/sda1
   ```

5. **Ændre UUID for filsystemet:**
   ```bash
   tune2fs -U random /dev/sda1
   ```

## Tips
- Sørg for at have sikkerhedskopieret data, før du ændrer indstillingerne for et filsystem.
- Kør `tune2fs` med root-rettigheder for at sikre, at du har de nødvendige tilladelser.
- Brug `tune2fs -l /dev/sda1` for at se de nuværende indstillinger og metadata for filsystemet, før du foretager ændringer.