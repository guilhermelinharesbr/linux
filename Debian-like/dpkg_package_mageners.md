# DPKG - Gerenciadores de Pacotes:


### Sumário
- [dpkg](#dpkg)
- [dpkg -i](#dpkg--i)
- [dpkg -r](#dpkg--r)
- [dpkg -l](#dpkg--l)
- [dpkg -s](#dpkg--s)
- [dpkg -L](#dpkg--l-1)
- [dpkg -c](#dpkg--c)
- [dpkg --unpack](#dpkg---unpack)
- [dpkg --configure](#dpkg---configure)
- []()

---

#### dpkg

Gerenciador de Pacotes padrão BAIXO nível para o S.O. Debian, Ubuntu, Linux Mint, Kali Linux, etc. É um comando para gerenciar arquivos .DEB. Lançado em 1993.

---

#### dpkg -i

Instalar/atualizar programas ou pacotes.

Ex:
```bash
dpkg -i nome_pacote.deb
```

---

#### dpkg -r

Remover programas ou pacotes. Este comando remove o pacote inteiro, exceto os arquivos de configuração.

Ex:
```bash
dpkg -r nome_pacote.deb
```

---

#### dpkg -l

Listar pacotes atualmente instalados. 

Ex:
```bash
dpkg -l
```

Ex2:
```bash
dpkg -l | grep vlc
```

---

#### dpkg -s

Verifica se um pacote específico está instalado.

Ex:
```bash
dpkg -s nome_pacote.deb
```

---

#### dpkg -L

Verifica o local onde o pacote está instalado.

Ex:
```bash
dpkg -L nome_pacote.deb
```

---

#### dpkg -c

Listar o conteúdo de um pacote.

Ex:
```bash
dpkg -c nome_pacote.deb
ou
dpkg --contents nome_pacote.deb
```

---

#### dpkg --unpack

Descompactar um pacote .DEB.

Ex:
```bash
dpkg --unpack nome_pacote.deb
```

---

#### dpkg --configure

Depois de fazer alterações nos arquivos, use este comando para configurá-lo e reempacotá-lo em um arquivo .DEB para instalação.

Ex:
```bash
dpkg --configure nome_pacote.deb
```

---
