# Gerenciadores de Pacotes:


### Sumário
- [apt / apt-get](#apt)
- [apt update](#apt-update)
- [apt upgrade](#apt-upgrade)
- [apt update && apt upgrade](#apt-update--apt-upgrade)
- [apt install](#apt-install)
- [apt remove](#apt-remove)
- [apt autoremove](#apt-autoremove)
- [apt search](#apt-search)
- [apt list](#apt-list)


---

#### apt / apt-get

Gerenciador de Pacotes padrão ALTO nível (Interface: Synaptic) para o S.O. Debian, Ubuntu, Linux Mint, Kali Linux, etc. Lançado em 1998.

---

#### apt update

Atualiza repositórios automaticamente. Antigamente era apt-get update.

Ex:
```bash
sudo apt update
```

---

#### apt upgrade

Atualiza softwares, bibliotecas do sistema. Antigamente era apt-get upgrade.

Ex:
```bash
sudo apt upgrade
```

---

#### apt update && apt upgrade

Junção dos dois comandos em apenas um.

Ex:
```bash
sudo apt update && sudo apt upgrade
```

---

#### apt install

Instala softwares, bibliotecas do sistema. Antigamente era apt-get install.

Ex:
```bash
sudo apt install nome_pacote
```

---

#### apt remove

Remove softwares, bibliotecas do sistema. Antigamente era apt-get remove.

Ex:
```bash
sudo apt remove nome_pacote
```

Remove todos os pacotes e seus arquivos de configuração:

Ex2:
```bash
sudo apt remove nome_pacote --purge
```

---

#### apt autoremove

Algumas dependências podem permanecer no seu sistema. Se você ficar incomodado com isso, poderá então remover os pacotes que não estão sendo mais utilizados pelo Apt. Antigamente era apt-get autoremove.

Ex:
```bash
sudo apt autoremove
```

---

#### apt search

Para procurar um pacote a ser instalado. Antigamente era apt-get search.

Ex:
```bash
sudo apt search termo_pesquisa
```

---

#### apt list

Lista todos os pacotes instalados com o Apt. 

Ex:
```bash
sudo apt list --installed
```

Mostra os pacotes com nome vlc instalados:
Ex:
```bash
sudo apt list --installed | grep vlc
```

---
