# [Linux] Bash fc Bruk: Rediger og kjør tidligere kommandoer

## Oversikt
`fc`-kommandoen i Bash brukes til å redigere og kjøre tidligere kommandoer fra kommandolinjen. Den gir brukeren muligheten til å hente opp kommandohistorikken, redigere den i en tekstredigerer, og deretter kjøre den redigerte kommandoen.

## Bruk
Den grunnleggende syntaksen for `fc`-kommandoen er:

```bash
fc [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l`: List opp kommandoene i historikken.
- `-s`: Kjør den angitte kommandoen uten å åpne en redigerer.
- `-n`: Vis ikke linjenumre når du lister opp kommandoene.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `fc`:

### Liste opp de siste 10 kommandoene
```bash
fc -l -10
```

### Redigere den siste kommandoen
```bash
fc
```
Dette åpner den siste kommandoen i standard tekstredigerer.

### Kjør en spesifikk kommando fra historikken
```bash
fc -s 123
```
Her vil `123` være linjenummeret til kommandoen du ønsker å kjøre.

### Liste opp de siste 5 kommandoene uten linjenumre
```bash
fc -ln -5
```

## Tips
- Bruk `fc` for raskt å rette opp feil i nylig kjørte kommandoer uten å måtte skrive dem på nytt.
- Du kan spesifisere et intervall av kommandoer ved å bruke `fc start..end` for å redigere flere kommandoer på en gang.
- Husk å sette opp din foretrukne tekstredigerer i Bash ved å bruke `export EDITOR=nano` (eller annen redigerer) for å tilpasse redigeringsopplevelsen.