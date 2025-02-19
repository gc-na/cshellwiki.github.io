# [Linux] C Shell (csh) umask gebruik: Beheer van bestandspermissies

## Overzicht
De `umask`-opdracht in C Shell (csh) wordt gebruikt om de standaard bestandspermissies in te stellen voor nieuwe bestanden en directories. Het bepaalt welke rechten niet worden toegewezen aan nieuwe bestanden die door een gebruiker worden gemaakt.

## Gebruik
De basis syntaxis van de `umask`-opdracht is als volgt:

```csh
umask [opties] [argumenten]
```

## Veelvoorkomende opties
- `-S`: Toont de huidige umask in symbolische notatie.
- `-p`: Toont de huidige umask zonder deze te wijzigen.

## Veelvoorkomende voorbeelden

1. **Huidige umask weergeven:**

```csh
umask
```

2. **Huidige umask in symbolische notatie weergeven:**

```csh
umask -S
```

3. **Umask instellen op 022:**

```csh
umask 022
```

4. **Umask instellen op 007:**

```csh
umask 007
```

5. **Umask instellen op 077 voor maximale beveiliging:**

```csh
umask 077
```

## Tips
- Stel de umask in op een waarde die past bij de beveiligingsbehoeften van je project.
- Controleer regelmatig je umask-instellingen om ervoor te zorgen dat ze overeenkomen met je huidige vereisten.
- Gebruik de `-S` optie om de umask in een begrijpelijke vorm te bekijken, vooral als je met meerdere gebruikers werkt.