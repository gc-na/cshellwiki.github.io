# [Linux] Bash sysctl gebruik: Beheer van kernelparameters

## Overzicht
De `sysctl` opdracht wordt gebruikt om kernelparameters in een Linux-systeem te beheren en te configureren. Hiermee kunnen gebruikers de runtime-instellingen van de Linux-kernel aanpassen zonder dat een herstart nodig is.

## Gebruik
De basis syntaxis van de `sysctl` opdracht is als volgt:

```bash
sysctl [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Toont alle kernelparameters en hun huidige waarden.
- `-w`: Wijzigt de waarde van een kernelparameter.
- `-p`: Laadt instellingen van een configuratiebestand, meestal `/etc/sysctl.conf`.

## Veelvoorkomende Voorbeelden

1. **Toon alle kernelparameters**:
   ```bash
   sysctl -a
   ```

2. **Wijzig een kernelparameter**:
   Stel de waarde van `vm.swappiness` in op 10:
   ```bash
   sysctl -w vm.swappiness=10
   ```

3. **Laad instellingen uit het configuratiebestand**:
   ```bash
   sysctl -p
   ```

4. **Controleer de waarde van een specifieke parameter**:
   Om de huidige waarde van `net.ipv4.ip_forward` te bekijken:
   ```bash
   sysctl net.ipv4.ip_forward
   ```

## Tips
- Zorg ervoor dat je de juiste permissies hebt (meestal root) om kernelparameters te wijzigen.
- Maak een back-up van je configuratiebestand voordat je wijzigingen aanbrengt.
- Gebruik `sysctl -a | grep <parameter>` om snel een specifieke parameter te vinden in de lijst van alle parameters.