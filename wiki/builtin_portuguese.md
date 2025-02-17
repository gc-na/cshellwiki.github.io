# [Linux] Bash builtin comando: Executa comandos internos do shell

## Overview
O comando `builtin` no Bash é utilizado para invocar comandos internos do shell, permitindo que você execute funções que são parte do próprio Bash, em vez de chamar executáveis externos. Isso é útil para garantir que você está utilizando a versão interna de um comando, especialmente quando há um executável externo com o mesmo nome.

## Usage
A sintaxe básica do comando `builtin` é a seguinte:

```bash
builtin [opções] [argumentos]
```

## Common Options
- `-p`: Utiliza a versão padrão do comando, ignorando quaisquer funções definidas pelo usuário.
- `-f`: Faz com que o comando seja executado sem verificar se ele é uma função.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `builtin`:

### Exemplo 1: Usando `builtin` para chamar `echo`
```bash
builtin echo "Este é um comando interno."
```

### Exemplo 2: Ignorando uma função com o mesmo nome
Suponha que você tenha uma função chamada `cd` definida no seu shell. Para garantir que você está chamando o comando interno `cd`, você pode usar:
```bash
builtin cd /home
```

### Exemplo 3: Usando `-p` para chamar `type`
```bash
builtin -p type ls
```

### Exemplo 4: Usando `-f` para forçar a execução de um comando
```bash
function ls {
  echo "Esta é uma função personalizada."
}
builtin ls
```

## Tips
- Sempre que houver um conflito entre um comando interno e um executável externo, considere usar `builtin` para garantir que você está chamando a versão interna.
- Utilize a opção `-p` quando você quiser evitar qualquer sobreposição de funções definidas pelo usuário.
- Lembre-se de que nem todos os comandos têm uma versão interna; verifique a documentação do Bash para mais detalhes.