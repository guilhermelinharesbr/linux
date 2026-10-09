# Screen


### Sumário
- [Definição](#definição)
- [Site oficial](#site-oficial)
- [Pacote de instalação](#pacote-de-instalação)
- [Comandos com CTRL + A](#)


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
