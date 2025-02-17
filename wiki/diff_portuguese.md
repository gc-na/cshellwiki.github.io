# [Linux] Bash diff uso: Compara arquivos e exibe diferenças

## Overview
O comando `diff` é utilizado para comparar o conteúdo de dois arquivos de texto e exibir as diferenças entre eles. É uma ferramenta valiosa para desenvolvedores e administradores de sistemas que precisam identificar alterações em arquivos de configuração, código-fonte ou qualquer outro tipo de documento.

## Usage
A sintaxe básica do comando `diff` é a seguinte:

```bash
diff [opções] [arquivo1] [arquivo2]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `diff`:

- `-u`: Exibe a saída em formato unificado, que é mais fácil de ler.
- `-c`: Mostra as diferenças em um formato de contexto.
- `-i`: Ignora diferenças entre maiúsculas e minúsculas.
- `-w`: Ignora espaços em branco ao comparar.
- `-r`: Compara diretórios recursivamente.

## Common Examples

### Exemplo 1: Comparar dois arquivos simples
```bash
diff arquivo1.txt arquivo2.txt
```

### Exemplo 2: Usar formato unificado
```bash
diff -u arquivo1.txt arquivo2.txt
```

### Exemplo 3: Ignorar diferenças de maiúsculas e minúsculas
```bash
diff -i arquivo1.txt arquivo2.txt
```

### Exemplo 4: Comparar diretórios
```bash
diff -r diretorio1/ diretorio2/
```

### Exemplo 5: Ignorar espaços em branco
```bash
diff -w arquivo1.txt arquivo2.txt
```

## Tips
- Sempre use a opção `-u` para uma visualização mais clara das diferenças, especialmente ao revisar alterações em código.
- Quando comparar diretórios, a opção `-r` é muito útil para identificar mudanças em arquivos aninhados.
- Combine opções para personalizar a saída de acordo com suas necessidades, como `diff -u -w arquivo1.txt arquivo2.txt` para ignorar espaços em branco e exibir em formato unificado.