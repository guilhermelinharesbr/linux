# Tmux


### Sumário
- [Definição](#definição)
- [Site oficial](#site-oficial)
- [Pacote de instalação](#pacote-de-instalação)

---

#### Definição

O **tmux** é um multiplexador de terminal de código aberto para sistemas operacionais do tipo Unix. Ele permite que várias sessões de terminal sejam acessadas simultaneamente em uma única janela. É útil para executar mais de um programa de linha de comando em simultâneo.

Obs: Se uma sessão do Tmux for criada no _usuário root_ e outra pessoa rodar `tmux ls` com _outro usuário_ a sessão criada no usuário root não será listada.

---

#### Site Oficial

- [Tmux](https://tmux.app/)

---

#### Pacote de instalação

Derivados do Debian:
```bash
apt install tmux
```

Derivados do Red Hat:
```bash
dnf install tmux
ou
yum install tmux
```

---
