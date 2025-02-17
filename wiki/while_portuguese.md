# [Linux] Bash while uso: Executa um comando repetidamente enquanto uma condição for verdadeira

## Overview
O comando `while` no Bash é utilizado para executar um bloco de comandos repetidamente enquanto uma condição especificada for verdadeira. É uma estrutura de controle de fluxo que permite a automação de tarefas que precisam ser repetidas até que uma determinada condição não seja mais atendida.

## Usage
A sintaxe básica do comando `while` é a seguinte:

```bash
while [ condição ]; do
    # comandos a serem executados
done
```

## Common Options
O comando `while` não possui opções específicas, mas a condição pode ser uma expressão que utilize operadores de comparação e lógicos. Aqui estão algumas formas comuns de condições:

- `true`: sempre retorna verdadeiro, resultando em um loop infinito.
- `false`: sempre retorna falso, não executando o bloco de comandos.
- `test -e arquivo`: verifica se um arquivo existe.
- `test -n string`: verifica se uma string não está vazia.

## Common Examples

### Exemplo 1: Loop infinito
```bash
while true; do
    echo "Este loop nunca termina."
done
```

### Exemplo 2: Contar até 5
```bash
contador=1
while [ $contador -le 5 ]; do
    echo "Contador: $contador"
    contador=$((contador + 1))
done
```

### Exemplo 3: Ler linhas de um arquivo
```bash
while IFS= read -r linha; do
    echo "Linha: $linha"
done < arquivo.txt
```

### Exemplo 4: Esperar até que um arquivo exista
```bash
while [ ! -e "arquivo.txt" ]; do
    echo "Aguardando a criação de arquivo.txt..."
    sleep 2
done
echo "arquivo.txt foi criado!"
```

## Tips
- Sempre tenha cuidado com loops infinitos. Certifique-se de que a condição eventualmente se tornará falsa.
- Utilize o comando `sleep` dentro de loops para evitar sobrecarga no sistema, especialmente em loops que verificam condições repetidamente.
- Teste suas condições antes de implementá-las em scripts para evitar comportamentos inesperados.