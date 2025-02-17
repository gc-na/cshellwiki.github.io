# [Linux] Bash echo uso: Exibir mensagens no terminal

## Overview
O comando `echo` é utilizado para exibir mensagens ou variáveis no terminal. É uma ferramenta simples, mas muito útil para mostrar informações ao usuário ou para depuração de scripts.

## Usage
A sintaxe básica do comando `echo` é a seguinte:

```bash
echo [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `echo`:

- `-n`: Não imprime a nova linha no final da saída.
- `-e`: Habilita a interpretação de caracteres especiais como `\n` (nova linha) e `\t` (tabulação).
- `-E`: Desabilita a interpretação de caracteres especiais (comportamento padrão).

## Common Examples

### Exibir uma mensagem simples
```bash
echo "Olá, mundo!"
```

### Exibir uma mensagem sem nova linha
```bash
echo -n "Esta mensagem não termina com nova linha."
```

### Usar caracteres especiais
```bash
echo -e "Linha 1\nLinha 2\tCom tabulação"
```

### Exibir o valor de uma variável
```bash
nome="João"
echo "Meu nome é $nome."
```

### Exibir múltiplas mensagens
```bash
echo "Mensagem 1" "Mensagem 2" "Mensagem 3"
```

## Tips
- Use `echo -n` quando quiser que a saída continue na mesma linha, especialmente útil em prompts interativos.
- Lembre-se de usar aspas ao redor de mensagens que contêm espaços para garantir que sejam tratadas como um único argumento.
- Para evitar problemas com caracteres especiais, considere usar `echo -e` quando necessário, mas esteja ciente de que isso pode não ser suportado em todas as versões do `echo`.