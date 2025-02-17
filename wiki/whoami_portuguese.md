# [Linux] Bash whoami Uso: Exibir o nome do usuário atual

## Overview
O comando `whoami` é utilizado para exibir o nome do usuário que está atualmente logado no sistema. É uma ferramenta simples, mas muito útil para verificar a identidade do usuário em um ambiente de linha de comando.

## Usage
A sintaxe básica do comando `whoami` é a seguinte:

```bash
whoami [opções] [argumentos]
```

## Common Options
O comando `whoami` possui opções limitadas, mas aqui estão algumas que podem ser úteis:

- `--help`: Exibe uma mensagem de ajuda com informações sobre o comando.
- `--version`: Mostra a versão do comando `whoami`.

## Common Examples

### Exibir o nome do usuário atual
Para simplesmente exibir o nome do usuário que está logado, você pode usar:

```bash
whoami
```

### Exibir ajuda do comando
Se você precisar de ajuda sobre como usar o comando, pode executar:

```bash
whoami --help
```

### Verificar a versão do comando
Para saber qual versão do `whoami` você está utilizando, execute:

```bash
whoami --version
```

## Tips
- O comando `whoami` é especialmente útil em scripts para verificar a identidade do usuário que está executando o script.
- Combine `whoami` com outros comandos, como `echo`, para personalizar mensagens. Por exemplo:

```bash
echo "Você está logado como: $(whoami)"
```

- Lembre-se de que `whoami` sempre retornará o nome do usuário atual, independentemente de qual diretório você esteja navegando no sistema.