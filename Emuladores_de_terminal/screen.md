# Screen


### Sumário
- [Definição](#definição)
- [Site oficial](#site-oficial)
- [Pacote de instalação](#pacote-de-instalação)
- [Comandos com CTRL + A](#comandos-com-ctrl--a)
- [CTRL + A + :caption always %w](#ctrl--a--caption-always-w)
- [CTRL + A + c](#ctrl--a--c)
- [CTRL + A + d](#ctrl--a--d)
- [CTRL + A + k](#ctrl--a--k)
- [CTRL + A + p](#ctrl--a--p)
- [CTRL + A + n](#ctrl--a--n)

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

### Comandos com CTRL + A

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
