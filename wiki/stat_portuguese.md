# [Linux] Bash stat Uso: Exibir informações sobre arquivos e sistemas de arquivos

## Overview
O comando `stat` é utilizado para exibir informações detalhadas sobre arquivos e diretórios no sistema de arquivos. Ele fornece dados como o tamanho do arquivo, permissões, data de criação, modificação e acesso, entre outros.

## Usage
A sintaxe básica do comando `stat` é a seguinte:

```bash
stat [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `stat`:

- `-c` : Formato de saída personalizado.
- `--format` : Especifica um formato de saída, semelhante a `-c`.
- `-f` : Exibe informações sobre o sistema de arquivos em vez de um arquivo específico.
- `--help` : Mostra a ajuda do comando.
- `--version` : Exibe a versão do comando.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `stat`:

1. Exibir informações detalhadas sobre um arquivo específico:

   ```bash
   stat arquivo.txt
   ```

2. Usar um formato personalizado para exibir apenas o tamanho e a data de modificação:

   ```bash
   stat -c "Tamanho: %s bytes, Modificado em: %y" arquivo.txt
   ```

3. Exibir informações sobre um diretório:

   ```bash
   stat /caminho/para/diretorio/
   ```

4. Mostrar informações do sistema de arquivos onde um arquivo está localizado:

   ```bash
   stat -f arquivo.txt
   ```

## Tips
- Utilize a opção `-c` para personalizar a saída e obter apenas as informações que você precisa.
- Combine o comando `stat` com outros comandos, como `grep`, para filtrar informações específicas.
- Lembre-se de que o `stat` pode ser usado em qualquer tipo de arquivo, incluindo diretórios e links simbólicos.