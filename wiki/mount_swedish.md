# [Linux] Bash mount användning: Montera filsystem

## Översikt
Kommandot `mount` används för att montera filsystem i Linux och Unix-liknande operativsystem. Det gör det möjligt att ansluta en lagringsenhet, som en hårddisk eller USB-enhet, till en specifik punkt i filsystemet så att användare kan komma åt dess innehåll.

## Användning
Den grundläggande syntaxen för kommandot `mount` är:

```bash
mount [alternativ] [enhet] [monteringspunkt]
```

## Vanliga alternativ
- `-t` : Anger typ av filsystem (t.ex. ext4, ntfs).
- `-o` : Anger monteringsalternativ, som `ro` (read-only) eller `rw` (read-write).
- `-a` : Monterar alla filsystem som anges i `/etc/fstab`.
- `-v` : Visar detaljerad information om monteringsprocessen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mount`:

1. Montera en USB-enhet:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Montera en NTFS-partition med read-only alternativ:
   ```bash
   mount -t ntfs -o ro /dev/sdc1 /mnt/ntfs
   ```

3. Montera alla filsystem i `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Montera en nätverksresurs (NFS):
   ```bash
   mount -t nfs server:/path/to/share /mnt/nfs
   ```

## Tips
- Kontrollera alltid att du har rätt behörigheter för att montera en enhet.
- Använd `umount` för att avmontera en enhet innan du kopplar bort den för att undvika datakorruption.
- Kontrollera monteringspunkten med `df -h` för att se vilka enheter som är monterade och deras utrymmesanvändning.