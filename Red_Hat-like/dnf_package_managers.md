# DNF - Gerenciadores de Pacotes:


### Sumário
- [dnf](#dnf)
- [dnf update](#dnf-update)
- [dnf install](#dnf-install)
- [dnf remove](#dnf-remove)
- [dnf autoremove](#dnf-autoremove)
- [dnf search]()


---

#### dnf

Gerenciador de Pacotes padrão ALTO nível para o S.O. Fedora 22(2015) em diante, CentOS 8(2019) em diante. Evolução/fork do YUM. É um comando para gerenciar arquivos .RPM. Lançado em 2013.

---

#### dnf update

Atualiza repositórios automaticamente.

Ex:
```bash
sudo dnf update
``` 

---

#### dnf install

Instala softwares, bibliotecas do sistema.

Ex:
```bash
sudo dnf install nome_pacote
``` 

Instalação de pacotes a partir de uma URL:

Ex2:
```bash
sudo dnf install $url
``` 

---

#### dnf remove

Remove softwares, bibliotecas do sistema.

Ex:
```bash
sudo dnf remove nome_pacote
``` 

---

#### dnf autoremove

Algumas dependências podem permanecer no seu sistema. Se você ficar incomodado com isso, poderá então remover os pacotes que não estão sendo mais utilizados pelo DNF.

Ex:
```bash
sudo dnf autoremove
``` 

---
