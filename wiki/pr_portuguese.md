# [Linux] Bash pr: Formatar e imprimir arquivos de texto

## Overview
O comando `pr` é utilizado para formatar arquivos de texto para impressão. Ele organiza o conteúdo em colunas e adiciona cabeçalhos e numeração de páginas, facilitando a leitura e a apresentação do texto impresso.

## Usage
A sintaxe básica do comando `pr` é a seguinte:

```bash
pr [opções] [arquivos]
```

## Common Options
Aqui estão algumas opções comuns do comando `pr`:

- `-h`: Define um cabeçalho personalizado para a saída.
- `-l número`: Define o número de linhas por página.
- `-w número`: Define a largura da página em caracteres.
- `-t`: Remove a numeração de páginas e cabeçalhos.

## Common Examples

### Exemplo 1: Formatar um arquivo de texto
Para formatar um arquivo chamado `documento.txt` com a configuração padrão, você pode usar:

```bash
pr documento.txt
```

### Exemplo 2: Definir um cabeçalho personalizado
Para adicionar um cabeçalho personalizado ao arquivo:

```bash
pr -h "Meu Cabeçalho" documento.txt
```

### Exemplo 3: Alterar o número de linhas por página
Para definir que cada página deve ter 30 linhas:

```bash
pr -l 30 documento.txt
```

### Exemplo 4: Remover cabeçalhos e numeração de páginas
Para formatar o arquivo sem cabeçalhos e numeração:

```bash
pr -t documento.txt
```

## Tips
- Utilize a opção `-w` para ajustar a largura da página se estiver imprimindo em papel de tamanho específico.
- Combine o `pr` com outros comandos, como `less`, para visualizar a saída formatada diretamente no terminal.
- Experimente com diferentes opções para encontrar a melhor formatação para suas necessidades específicas.