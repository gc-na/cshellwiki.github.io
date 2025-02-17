# [Linux] Bash grep Uso: Pesquisa de texto em arquivos

## Overview
O comando `grep` é uma ferramenta poderosa utilizada para buscar padrões de texto em arquivos. Ele permite que os usuários filtrem e localizem informações específicas, tornando-se essencial para a análise de dados e a manipulação de texto em sistemas Unix e Linux.

## Usage
A sintaxe básica do comando `grep` é a seguinte:

```bash
grep [opções] [padrão] [arquivo]
```

## Common Options
Aqui estão algumas opções comuns do `grep`:

- `-i`: Ignora a diferenciação entre maiúsculas e minúsculas.
- `-r`: Realiza a busca recursivamente em diretórios.
- `-v`: Inverte a busca, mostrando linhas que não correspondem ao padrão.
- `-n`: Exibe o número da linha onde o padrão foi encontrado.
- `-l`: Lista apenas os nomes dos arquivos que contêm o padrão.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `grep`:

1. **Buscar uma palavra em um arquivo:**
   ```bash
   grep "palavra" arquivo.txt
   ```

2. **Buscar ignorando maiúsculas e minúsculas:**
   ```bash
   grep -i "palavra" arquivo.txt
   ```

3. **Buscar recursivamente em um diretório:**
   ```bash
   grep -r "palavra" /caminho/do/diretorio
   ```

4. **Exibir números das linhas onde o padrão foi encontrado:**
   ```bash
   grep -n "palavra" arquivo.txt
   ```

5. **Listar arquivos que contêm uma palavra específica:**
   ```bash
   grep -l "palavra" *.txt
   ```

## Tips
- Utilize o `grep` em combinação com outros comandos, como `ls` ou `cat`, para filtrar resultados de maneira mais eficiente.
- Para padrões mais complexos, considere usar expressões regulares com o `grep` para uma busca mais precisa.
- Salve os resultados da busca em um arquivo usando a redireção, por exemplo: `grep "palavra" arquivo.txt > resultados.txt`.