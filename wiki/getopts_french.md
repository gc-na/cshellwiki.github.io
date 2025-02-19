# [Linux] C Shell (csh) getopts : [traitement des options de ligne de commande]

## Overview
La commande `getopts` est utilisée dans les scripts C Shell pour analyser les options de ligne de commande. Elle permet de gérer les arguments passés au script, facilitant ainsi la création de programmes interactifs et flexibles.

## Usage
La syntaxe de base de la commande `getopts` est la suivante :

```csh
getopts optstring variable
```

- `optstring` : une chaîne de caractères qui définit les options valides.
- `variable` : le nom de la variable qui recevra l'option actuelle.

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `getopts` :

- `:` : Indique que l'option nécessite un argument.
- `?` : Indique une option invalide, ce qui permet de gérer les erreurs.

## Common Examples

### Exemple 1 : Options simples
```csh
#!/bin/csh
set optstring = "ab:c"
while (getopts "$optstring" option)
    switch ($option)
        case "a":
            echo "Option A sélectionnée"
            breaksw
        case "b":
            echo "Option B avec argument : $OPTARG"
            breaksw
        case "c":
            echo "Option C sélectionnée"
            breaksw
        case "?":
            echo "Option invalide : $OPTARG"
            breaksw
    endsw
end
```

### Exemple 2 : Utilisation d'arguments
```csh
#!/bin/csh
set optstring = "f:vh"
while (getopts "$optstring" option)
    switch ($option)
        case "f":
            echo "Fichier spécifié : $OPTARG"
            breaksw
        case "v":
            echo "Mode verbeux activé"
            breaksw
        case "h":
            echo "Affichage de l'aide"
            breaksw
        case "?":
            echo "Option invalide : $OPTARG"
            breaksw
    endsw
end
```

### Exemple 3 : Gestion d'options multiples
```csh
#!/bin/csh
set optstring = "x:y:z"
while (getopts "$optstring" option)
    switch ($option)
        case "x":
            echo "Option X avec argument : $OPTARG"
            breaksw
        case "y":
            echo "Option Y avec argument : $OPTARG"
            breaksw
        case "z":
            echo "Option Z sélectionnée"
            breaksw
        case "?":
            echo "Option invalide : $OPTARG"
            breaksw
    endsw
end
```

## Tips
- Toujours définir un `optstring` clair pour éviter la confusion lors de l'analyse des options.
- Utilisez `:` pour indiquer les options qui nécessitent un argument afin de gérer les erreurs correctement.
- Pensez à inclure une option d'aide pour améliorer l'expérience utilisateur de votre script.