# [Linux] Bash case uso: Avaliação de padrões de string

## Overview
O comando `case` no Bash é utilizado para realizar a correspondência de padrões em strings. Ele permite que você verifique uma variável contra uma série de padrões e execute comandos diferentes com base na correspondência encontrada. É uma alternativa ao comando `if` quando você precisa testar uma variável contra múltiplos valores.

## Usage
A sintaxe básica do comando `case` é a seguinte:

```bash
case [variável] in
    [padrão1])
        [comando1]
        ;;
    [padrão2])
        [comando2]
        ;;
    *)
        [comando_default]
        ;;
esac
```

## Common Options
O comando `case` não possui muitas opções, mas é importante entender a estrutura básica:
- `*)`: Este é o padrão padrão que será executado se nenhum dos outros padrões corresponder.
- `;;`: Indica o final de um bloco de comandos para um padrão específico.

## Common Examples

### Exemplo 1: Verificando o dia da semana
```bash
dia="segunda"

case $dia in
    "segunda")
        echo "Hoje é segunda-feira."
        ;;
    "terça")
        echo "Hoje é terça-feira."
        ;;
    "quarta")
        echo "Hoje é quarta-feira."
        ;;
    *)
        echo "Não é um dia da semana válido."
        ;;
esac
```

### Exemplo 2: Atribuindo uma ação com base em uma extensão de arquivo
```bash
arquivo="documento.txt"

case $arquivo in
    *.txt)
        echo "É um arquivo de texto."
        ;;
    *.jpg | *.png)
        echo "É uma imagem."
        ;;
    *)
        echo "Tipo de arquivo desconhecido."
        ;;
esac
```

### Exemplo 3: Menu simples
```bash
opcao="2"

case $opcao in
    1)
        echo "Você escolheu a opção 1."
        ;;
    2)
        echo "Você escolheu a opção 2."
        ;;
    3)
        echo "Você escolheu a opção 3."
        ;;
    *)
        echo "Opção inválida."
        ;;
esac
```

## Tips
- Utilize `case` quando você tiver múltiplas condições para testar, pois isso torna o código mais limpo e legível.
- Lembre-se de usar `;;` após cada bloco de comandos para evitar que o Bash continue executando os próximos blocos.
- Os padrões podem incluir caracteres curinga, como `*` e `?`, o que permite uma correspondência mais flexível.