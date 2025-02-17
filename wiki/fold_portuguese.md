# [Linux] Bash fold Uso: Quebra de linhas em texto

## Overview
O comando `fold` é utilizado para formatar texto, quebrando linhas longas em várias linhas mais curtas. Isso é especialmente útil para garantir que o texto se ajuste em telas ou impressoras que têm largura limitada.

## Usage
A sintaxe básica do comando `fold` é a seguinte:

```bash
fold [opções] [argumentos]
```

## Common Options
- `-w, --width=N`: Define a largura máxima das linhas. O valor padrão é 80 caracteres.
- `-s, --break-at-space`: Quebra a linha no espaço mais próximo, em vez de cortar palavras.
- `-b, --bytes`: Conta a largura em bytes, em vez de caracteres.

## Common Examples

1. **Quebrar linhas em um arquivo de texto**:
   Para quebrar linhas de um arquivo chamado `texto.txt` com largura de 50 caracteres:
   ```bash
   fold -w 50 texto.txt
   ```

2. **Quebrar linhas e salvar em um novo arquivo**:
   Para quebrar linhas de `texto.txt` e salvar o resultado em `texto_formatado.txt`:
   ```bash
   fold -w 50 texto.txt > texto_formatado.txt
   ```

3. **Quebrar linhas sem cortar palavras**:
   Para quebrar linhas em `texto.txt` em 60 caracteres, respeitando os espaços:
   ```bash
   fold -s -w 60 texto.txt
   ```

4. **Contar largura em bytes**:
   Para quebrar linhas em `texto.txt` considerando a largura em bytes:
   ```bash
   fold -b -w 50 texto.txt
   ```

## Tips
- Sempre verifique a largura do terminal ou da impressora antes de definir a largura com `-w`.
- Use a opção `-s` para evitar que palavras sejam cortadas, o que melhora a legibilidade do texto.
- Combine `fold` com outros comandos, como `cat` ou `grep`, para processar texto de maneira mais eficiente.