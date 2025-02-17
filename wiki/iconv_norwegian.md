# [Linux] Bash iconv bruk: Konverterer tekstfilers tegnsett

## Oversikt
`iconv` er et kommandolinjeverktøy som brukes til å konvertere tekstfiler fra ett tegnsett til et annet. Dette er spesielt nyttig når man arbeider med filer som inneholder tekst på forskjellige språk eller når man må tilpasse filer til spesifikke systemkrav.

## Bruk
Grunnleggende syntaks for `iconv`-kommandoen er som følger:

```bash
iconv [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f, --from-code=KODE`: Angir tegnsettet som filen er kodet i.
- `-t, --to-code=KODE`: Angir tegnsettet som filen skal konverteres til.
- `-o, --output=FIL`: Angir utdatafilen. Hvis ikke spesifisert, vil utdataene bli skrevet til standard utgang.
- `-c`: Ignorerer ugyldige tegn i inndata.

## Vanlige eksempler

### Konvertere fra ISO-8859-1 til UTF-8
```bash
iconv -f ISO-8859-1 -t UTF-8 input.txt -o output.txt
```

### Konvertere fra UTF-16 til UTF-8
```bash
iconv -f UTF-16 -t UTF-8 input.txt -o output.txt
```

### Ignorere ugyldige tegn
```bash
iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
```

### Konvertere flere filer
```bash
for file in *.txt; do
    iconv -f ISO-8859-1 -t UTF-8 "$file" -o "converted_$file"
done
```

## Tips
- Sørg for å vite hvilket tegnsett filene dine er kodet i før du konverterer, for å unngå datatap.
- Test alltid konverteringen med en liten fil før du bruker det på større filer.
- Bruk `-o` alternativet for å spesifisere en utdatafil, slik at du ikke overskriver originalfilen ved et uhell.