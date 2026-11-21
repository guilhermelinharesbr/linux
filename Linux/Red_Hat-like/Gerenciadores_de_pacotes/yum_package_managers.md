# YUM - Gerenciadores de Pacotes:


### Sumário
- [yum](#yum)
- [yum update](#yum-update)
- [yum install](#yum-install)
- [yum remove](#yum-remove)
- [yum search](#yum-search)

---

#### yum

Gerenciador de Pacotes padrão ALTO nível para o S.O. Fedora 21(2014) pra trás, CentOS 7(2014) pra trás. É um comando para gerenciar arquivos .RPM. Lançado em 2003.

---

#### yum update

Atualiza repositórios automaticamente.

Ex:
```bash
sudo yum update
``` 

---

#### yum install

Instala softwares, bibliotecas do sistema.

Ex:
```bash
sudo yum install nome_pacote
``` 

Instalação de pacotes a partir de uma URL:
```bash
sudo yum install $url
``` 

---

#### yum remove

Remove softwares, bibliotecas do sistema.

Ex:
```bash
sudo yum remove nome_pacote
``` 

Obs: O YUM **não inclui** um comando _autoremove_ para encontrar e remover dependências não utilizadas.

---

#### yum search

Para procurar um pacote a ser instalado.

Ex:
```bash
sudo yum search nome_pacote
``` 

---
