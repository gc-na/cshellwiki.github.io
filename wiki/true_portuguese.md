# [Linux] Bash true uso equivalente: Comando que sempre retorna verdadeiro

## Overview
O comando `true` é um utilitário simples que sempre retorna um código de saída 0, indicando sucesso. Ele é frequentemente utilizado em scripts e pipelines para garantir que uma condição seja verdadeira, permitindo que outras operações sejam executadas sem interrupção.

## Usage
A sintaxe básica do comando `true` é a seguinte:

```bash
true [opções]
```

## Common Options
O comando `true` não possui opções ou argumentos significativos. Ele é utilizado sem qualquer modificação. 

## Common Examples

### Exemplo 1: Uso básico
Executar o comando `true` por si só:

```bash
true
```

### Exemplo 2: Usando com um comando condicional
Você pode usar `true` em uma estrutura condicional:

```bash
if true; then
    echo "Esta condição é sempre verdadeira."
fi
```

### Exemplo 3: Em um loop
Usar `true` para criar um loop infinito:

```bash
while true; do
    echo "Este loop nunca termina."
    sleep 1
done
```

### Exemplo 4: Combinando com outros comandos
Usar `true` para ignorar erros em um pipeline:

```bash
command1 || true
```

## Tips
- O comando `true` é útil para testar scripts e estruturas de controle sem causar falhas.
- Em scripts complexos, use `true` para garantir que um bloco de código seja sempre executado, independentemente de erros anteriores.
- Combine `true` com `&&` para criar sequências de comandos onde o próximo comando deve ser executado independentemente do resultado do anterior.