# Screen


### Sumário
- [Definição](#definição)
- [Site oficial](#site-oficial)
- [Pacote de instalação](#pacote-de-instalação)
- [COMANDOS COM CTRL + A](#comandos-com-ctrl--a)
- [CTRL + A + :caption always %w](#ctrl--a--caption-always-w)
- [CTRL + A + c](#ctrl--a--c)
- [CTRL + A + d](#ctrl--a--d)
- [CTRL + A + k](#ctrl--a--k)
- [CTRL + A + p](#ctrl--a--p)
- [CTRL + A + n](#ctrl--a--n)
- [CTRL + A + Nº](#ctrl--a--nº)
- [OPÇÕES DO COMANDO SCREEN](#opções-do-comando-screen)
- [-ls / -list](#-ls---list)
- [-r](#-r)
- [-S](#-s)
- [-x](#-x)

---

#### Definição

O **screen** é um software que permite trabalharmos com vários terminais ao mesmo tempo, traz aos administradores e usuários o poder de abrir várias instâncias de terminais separados dentro de um único gerenciador de janela de terminal. 

Um item muito interessante é que o Screen permite anexar e desanexar sessões de terminais. 

É _indicado_ para rodar comandos em servidores compartilhados, pois pode compartilhar a sessão com outros usuários, bem como rodar comandos em Background, ao invés do _Foreground_ usado pelos terminais padrões dos servidores Linux.  Ex: Dumps e Restores de bancos de dados.

---

#### Site Oficial

- [GNU Screen](https://www.gnu.org/software/screen/)

---

#### Pacote de instalação

Derivados do Debian:
```bash
apt install screen
```

Derivados do Red Hat:
```bash
dnf install screen
ou
yum install screen
```

---

### COMANDOS COM CTRL + A

Existem diversos subcomandos do screen precisão ser precedidos por CTRL + A.
Estes subcomandos serão mostrados mais abaixo neste artigo.

---

#### CTRL + A + :caption always %w


O **CTRL + A** habilita a parte de configuração do screen, digitar **:caption always %w**, depois **Enter**, faz com que a tela passe a ter uma tarja branca na parte de baixo, facilanto identifcar que está dentro de uma screen.

---

#### CTRL + A + c

O **CTRL + A** habilita a parte de configuração do screen, digitar **c** que vem de **create**, cria uma nova aba de terminal.

---

#### CTRL + A + d

O **CTRL + A** habilita a parte de configuração do screen, digitar **d** que vem de **detached**, na prática ele sai do terminar sem matar a sessão.

---

#### CTRL + A + k

O **CTRL + A** habilita a parte de configuração do screen, digitar **k** que vem de **kill**, mata a sessão atual.
Muito usado para cancelar um comando que tenha loop e que tenha sido executado dentro da screen.

---

#### CTRL + A + p

O **CTRL + A** habilita a parte de configuração do screen, digitar **p** que vem de **previous**, vai para a aba anterior do terminal.

---

#### CTRL + A + n

O **CTRL + A** habilita a parte de configuração do screen, digitar **n** que vem de **next**, vai para a próxima aba do terminal.

---

#### CTRL + A + Nº

O **CTRL + A** habilita a parte de configuração do screen, digitar **3** vai pra _quarta_ aba, pois as abas são numeradas a partir do **0**.


---

### OPÇÕES DO COMANDO SCREEN

Existem diversas opções do screen, onde elas serão mostradas mais abaixo neste artigo.

---

#### -ls / -list

O **screen -ls** lista os terminais screen atachados ou desatachados.

```bash
screen -ls
ou
screen -list
```

---

#### -r

O **screen -r** lista os terminais Attached. Se tiver apenas um, ele já entra na sessão. O **r** vem de **reattach**.

```bash
screen -r
ou
screen -r 727447.ping_externo
```

---

#### -S

O **screen -S** coloca um nome em uma nova screen. O **S** vem de **sockname**.

```bash
screen -S imapsync
screen -S backup
```

---

#### -x

O **screen -x** é usado para _Multi-display_ entra em uma screen que já esteja _Attached_ em outra máquina, _sem derrubar a sessão_ da outra pessoa. 

```bash
screen -x 8059.imapsync
screen -x 8098.backup
```

---
