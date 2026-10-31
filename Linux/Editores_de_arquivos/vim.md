# VIM


### Sumário
- [Definição](#definição)
- [Site oficial](#site-oficial)
- [Pacote de instalação](#pacote-de-instalação)
- [ATALHOS](#atalhos)
- [Comandos de PESQUISA](#comandos-de-pesquisa)
- [/](#---barra)
- [?](#---interrogação)
- [\\](#---barra-invertida)
- [n](#n)
- [N](#n-maiúsculo)
- [Comandos para INSERÇÃO](#comandos-para-inserção)
- [i](#i)
- [o](#o)
- [O](#o-maiúsculo)
- [a](#a)
- [A](#a-maiúsculo)
- [Esc](#esc)
- [Comandos para EDIÇÃO DE TEXTO](#comandos-para-edição-de-texto)
- [c](#c)

---

#### Definição

O programa **vi** foi criado por Bill Joy em 1976 para o BSD. O nome é uma forma abreviada para visual, um comando do editor de texto **ex** que o faz oferecer recursos parecidos com os do **vi**.
Em 1991, foi lançado o editor **Vim**, uma derivação melhorada do **vi** (o nome **Vim** é abreviação para Vi IMproved). Ele está presente em quase todas as distribuições Linux, oferecendo mais recursos.

O **vi** é o principal editor em modo texto do Linux.

O **vi** ao ser executado procura por um arquivo de configuração  chamado “**.vimrc**” no diretório **HOME** dos usuários. Nem sempre este arquivo existe, mas pode ser criado pelo usuário para fazer algumas coisas bacanas com o **vi**, que serão mostradas neste artigo.

---

#### Site Oficial

- [vim.org](https://www.vim.org/)

---

#### Pacote de instalação

Derivados do Debian:
```bash
apt install vim
```

Derivados do Red Hat:
```bash
dnf install vim
ou
yum install vim
```

---

### ATALHOS

O **vim** possui diversos atalhos para facilitar a sua atulização.

---

### Comandos de PESQUISA

---

#### / -> barra

O **/** é usado para realizar uma pesquisa. Pesquisa do **começo** do arquivo para o final.

---

#### ? -> interrogação

O **?** é usado para realizar uma pesquisa. Pesquisa do **final** do arquivo para o começo.

---

#### \ -> barra invertida

O **\\** é usado para escapar um caractere especial. 

Ex:  
``/03\/May\/2022\:16`` para pesquisar uma data no caso **03/May/2022:16**. 

Usa padrão _ERE_(Extended Regular Expression). A presença da contrabarra significa que o caractere posterior deve ser interpretado como literal. Isso significa que não são usadas barras invertidas para identificar metacaracteres.

---

#### n 

Para encontrar as próximas ocorrências(next). Do **início** do arquivo para o final se for usado em conjunto com o / e do fim do arquivo para o início se for usado em conjunto com o ? .

---

#### N maiúsculo

Para encontrar as ocorrências anteriores. Do **final** do arquivo para o início se for usado em conjunto com o / e do início do arquivo para o fim se for usado em conjunto com o ? .

---

### Comandos para INSERÇÃO

---

#### i

Entra no modo de Inserção. _Insere_ texto **antes** do cursor.

---

#### o

Entra no modo de Inserção. Insere texto em uma nova linha em branco, no caso na linha **abaixo** de onde o cursor está.

---

#### O maiúsculo

Entra no modo de Inserção. Insere texto em uma nova linha em branco, no caso na linha **acima** de onde o cursor está. 

---

#### a

Entra no modo de Inserção. Insere texto **depois(after) do cursor**.  

---

#### A maiúsculo

Entra no modo de Inserção. Insere texto no **final da linha** em que o cursor está.

---

#### Esc

Para sair do modo de inserção.    

---

### Comandos para EDIÇÃO DE TEXTO

---

#### c

Recorta(cut) o texto marcado. 

---