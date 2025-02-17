# [Linux] Bash fsck uso: Verificar e corrigir sistemas de arquivos

## Overview
O comando `fsck` (File System Consistency Check) é utilizado para verificar a integridade de sistemas de arquivos em sistemas Unix e Linux. Ele identifica e corrige erros que podem ocorrer em sistemas de arquivos, garantindo que os dados sejam mantidos de forma segura e consistente.

## Usage
A sintaxe básica do comando `fsck` é a seguinte:

```bash
fsck [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `fsck`:

- `-a` ou `--auto`: Corrige automaticamente os erros encontrados sem solicitar confirmação.
- `-n` ou `--no`: Realiza a verificação sem fazer alterações, útil para visualizar problemas sem corrigi-los.
- `-f` ou `--force`: Força a verificação mesmo que o sistema de arquivos pareça estar limpo.
- `-t` ou `--test`: Realiza um teste sem corrigir os erros.
- `-y`: Assume "sim" para todas as perguntas, aplicando correções automaticamente.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `fsck`:

1. **Verificar um sistema de arquivos específico**:
   ```bash
   fsck /dev/sda1
   ```

2. **Forçar a verificação de um sistema de arquivos**:
   ```bash
   fsck -f /dev/sda1
   ```

3. **Verificar e corrigir automaticamente**:
   ```bash
   fsck -a /dev/sda1
   ```

4. **Verificação sem alterações**:
   ```bash
   fsck -n /dev/sda1
   ```

5. **Assumir "sim" para todas as correções**:
   ```bash
   fsck -y /dev/sda1
   ```

## Tips
- Sempre faça backup dos dados importantes antes de executar o `fsck`, especialmente se você estiver corrigindo erros.
- Execute o `fsck` em modo de usuário único ou quando o sistema de arquivos não estiver montado para evitar danos.
- Use a opção `-n` para verificar problemas sem fazer alterações, permitindo que você analise a situação antes de agir.