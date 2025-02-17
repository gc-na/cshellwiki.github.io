# [Linux] Bash pwd Uso equivalente: [exibir o diretório atual]

## Overview
O comando `pwd` (print working directory) é utilizado para exibir o caminho completo do diretório atual em que o usuário se encontra no sistema de arquivos. É uma ferramenta simples, mas essencial para navegação e gerenciamento de arquivos no terminal.

## Usage
A sintaxe básica do comando `pwd` é a seguinte:

```bash
pwd [opções]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `pwd`:

- `-L`: Exibe o caminho lógico do diretório atual, que pode incluir links simbólicos.
- `-P`: Exibe o caminho físico do diretório atual, resolvendo todos os links simbólicos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `pwd`:

1. **Exibir o diretório atual:**
   ```bash
   pwd
   ```

2. **Exibir o caminho lógico do diretório atual:**
   ```bash
   pwd -L
   ```

3. **Exibir o caminho físico do diretório atual:**
   ```bash
   pwd -P
   ```

## Tips
- Utilize `pwd` frequentemente para verificar sua localização no sistema de arquivos, especialmente ao navegar entre vários diretórios.
- Combine o uso do `pwd` com outros comandos, como `cd`, para garantir que você está no diretório correto antes de executar operações de arquivo.
- Lembre-se de que o `pwd` é uma ferramenta útil para scripts, pois pode ajudar a capturar o diretório atual para uso posterior.