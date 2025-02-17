# [Linux] Bash usermod uso: Modificar contas de usuário

## Overview
O comando `usermod` é utilizado para modificar as contas de usuário no sistema Linux. Ele permite que administradores alterem atributos de usuários, como nome, grupo, diretório home, entre outros.

## Usage
A sintaxe básica do comando `usermod` é a seguinte:

```bash
usermod [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `usermod`:

- `-aG`: Adiciona o usuário a um ou mais grupos sem removê-lo de outros grupos.
- `-d`: Altera o diretório home do usuário.
- `-l`: Muda o nome de login do usuário.
- `-g`: Define o grupo primário do usuário.
- `-s`: Altera o shell padrão do usuário.

## Common Examples

### Adicionar um usuário a um grupo
Para adicionar o usuário `joao` ao grupo `developers`, use:

```bash
usermod -aG developers joao
```

### Alterar o diretório home do usuário
Para mudar o diretório home do usuário `maria` para `/home/maria_nova`, execute:

```bash
usermod -d /home/maria_nova maria
```

### Mudar o nome de login do usuário
Para alterar o nome de login do usuário `carlos` para `carl`, utilize:

```bash
usermod -l carl carlos
```

### Alterar o grupo primário do usuário
Para definir o grupo primário do usuário `ana` como `admin`, faça:

```bash
usermod -g admin ana
```

### Alterar o shell padrão do usuário
Para mudar o shell padrão do usuário `pedro` para `/bin/zsh`, use:

```bash
usermod -s /bin/zsh pedro
```

## Tips
- Sempre faça um backup das configurações de usuários antes de fazer alterações significativas.
- Use `usermod` com cautela, pois mudanças incorretas podem afetar o acesso do usuário ao sistema.
- Verifique as permissões e grupos do usuário após fazer alterações para garantir que tudo esteja configurado corretamente.