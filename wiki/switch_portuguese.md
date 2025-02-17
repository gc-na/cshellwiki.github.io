# [Linux] Bash switch uso: Alternar entre opções de execução

## Overview
O comando `switch` no Bash é utilizado para executar diferentes blocos de código com base no valor de uma variável. Ele permite que você escolha entre várias alternativas de forma clara e organizada, facilitando a execução de diferentes comandos dependendo da condição especificada.

## Usage
A sintaxe básica do comando `switch` é a seguinte:

```bash
switch [variável] {
    case [valor1]:
        [comandos]
        break
    case [valor2]:
        [comandos]
        break
    default:
        [comandos]
}
```

## Common Options
Embora o `switch` em si não tenha muitas opções como outros comandos, é importante entender os elementos que compõem sua estrutura:

- `case`: Define uma condição a ser verificada.
- `break`: Encerra a execução do bloco atual e sai do `switch`.
- `default`: Executa comandos se nenhuma das condições anteriores for atendida.

## Common Examples

### Exemplo 1: Usando switch para verificar um dia da semana
```bash
dia="segunda"

switch $dia {
    case "segunda":
        echo "Hoje é segunda-feira."
        break
    case "terça":
        echo "Hoje é terça-feira."
        break
    default:
        echo "Hoje não é um dia da semana conhecido."
}
```

### Exemplo 2: Verificando o nível de acesso
```bash
nivel="admin"

switch $nivel {
    case "admin":
        echo "Você tem acesso total."
        break
    case "usuario":
        echo "Você tem acesso limitado."
        break
    default:
        echo "Acesso negado."
}
```

### Exemplo 3: Selecionando uma fruta
```bash
fruta="maçã"

switch $fruta {
    case "maçã":
        echo "Você escolheu uma maçã."
        break
    case "banana":
        echo "Você escolheu uma banana."
        break
    default:
        echo "Fruta não reconhecida."
}
```

## Tips
- Sempre inclua um `default` para tratar casos não previstos, garantindo que seu script não falhe silenciosamente.
- Utilize `break` após cada `case` para evitar a execução de blocos subsequentes desnecessariamente.
- Teste seu `switch` com diferentes valores para garantir que todas as condições estão sendo tratadas corretamente.