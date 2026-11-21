# Tmux


### Sumário
- [Definição](#definição)
- [Site oficial](#site-oficial)
- [Pacote de instalação](#pacote-de-instalação)
- [COMANDOS COM CTRL + B](#comandos-com-ctrl--b)
    - [CTRL + B + símbolo (+) mais](#ctrl--b--símbolo--mais)
    - [CTRL + B + símbolo (-) menos](#ctrl--b--símbolo---menos)
    - [CTRL + B + símbolo (&) E comercial](#ctrl--b--símbolo--e-comercial)
    - [CTRL + B + símbolo (,) vírgula](#ctrl--b--símbolo--vírgula)
    - [CTRL + B + símbolo (%) porcentagem](#ctrl--b--símbolo--porcentagem)
    - [CTRL + B + símbolo (") aspas duplas](#ctrl--b--símbolo--aspas-duplas)
    - [CTRL + B + símbolo (→ ou ← ou ↑ ou ↓) setas](#ctrl--b--símbolo--ou--ou--ou--setas)
    - [CTRL + B + c](#ctrl--b--c)
    - [CTRL + B + d](#ctrl--b--d)
    - [CTRL + B + p](#ctrl--b--p)
    - [CTRL + B + n](#ctrl--b--n)
    



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


### COMANDOS COM CTRL + B

Existem diversos subcomandos do tmux que precisam ser precedidos por CTRL + B.
Estes subcomandos serão mostrados mais abaixo neste artigo.

---

#### CTRL + B + símbolo (+) mais

O **CTRL + B** habilita a parte de configuração do tmux, digitar **+** servirá para _aumentar o tamanho da fonte_ do terminal, é preciso nesse caso manter o Ctrl+b pressionado para só depois teclar no **+**.

---

#### CTRL + B + símbolo (-) menos

O **CTRL + B** habilita a parte de configuração do tmux, digitar **-** servirá para _reduzir o tamanho da fonte_ do terminal, é preciso nesse caso manter o Ctrl+b pressionado para só depois teclar  no **-**.

---

#### CTRL + B + símbolo (&) E comercial

O **CTRL + B** habilita a parte de configuração do tmux, digitar **&** servirá para matar a janela atual, estando dentro da janela. Ele pergunta se deseja mesmo matar a janela.

---

#### CTRL + B + símbolo (,) vírgula

O **CTRL + B** habilita a parte de configuração do tmux, digitar **,** abre uma opção para renomear uma janela, para confirmar teclar enter.

---

#### CTRL + B + símbolo (%) porcentagem

O **CTRL + B** habilita a parte de configuração do tmux, digitar **%** divide(**split**) a tela criando uma nova janela dentro da mesma seção na **vertical**.

---

#### CTRL + B + símbolo (") aspas duplas

O **CTRL + B** habilita a parte de configuração do tmux, digitar **"**  divide(**split**) a tela criando uma nova janela dentro da mesma seção na **horizontal**.

---

#### CTRL + B + símbolo (→ ou ← ou ↑ ou ↓) setas

O **CTRL + B** habilita a parte de configuração do tmux, digitar **→** ou **←** ou **↑** ou **↓** para navegar entre as janelas que foram divididas no split.

---

#### CTRL + B + c

O **CTRL + B** habilita a parte de configuração do tmux, digitar **c** para criar uma nova janela dentro do tmux. O c vem de **c**reate.

---

#### CTRL + B + d

O **CTRL + B** habilita a parte de configuração do tmux, digitar **d** para sair do terminal. O d vem de **d**etached.

---

#### CTRL + B + p

O **CTRL + B** habilita a parte de configuração do tmux, digitar **p** para navegar entre as janelas criadas, p de **p**review.

---

#### CTRL + B + n

O **CTRL + B** habilita a parte de configuração do tmux, digitar **n** para  navegar entre as janelas criadas, n de **n**ext.

---
