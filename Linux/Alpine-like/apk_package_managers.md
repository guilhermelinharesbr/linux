# APK - Gerenciadores de Pacotes:


### Sumário
- [Descrição](#descrição)
- [Fonte de Pesquisa](#fonte-de-pesquisa)
- [Instalação e remoção do pacote](#instalação-e-remoção-do-pacote)
    - [apk add](#apk-add)
    - [apk del](#apk-del)
- [Manutenção do Sistema](#manutenção-do-sistema)
    - [apk update](#apk-update)
    - [apk upgrade](#apk-upgrade)
    - [apk update && apk upgrade](#apk-update--apk-upgrade)
- [Consultando informações do pacote](#)
    - [apk search](#apk-search)
    - [apk info](#apk-info)
- [Variados](#)
    - [apk stats](#apk-stats)

---

#### Descrição

O **apk** (Alpine Package Keeper) é o gerenciador de pacotes oficial do Alpine Linux. Ele foi escrito do zero em C para ser extremamente rápido, leve e eficiente no consumo de memória e espaço em disco, características essenciais para imagens de containers e ambientes minimalistas.

---

#### Fonte de Pesquisa

[Wiki Alpine Linux](https://wiki.alpinelinux.org/wiki/Alpine_Package_Keeper)

---

### Instalação e remoção do pacote

---

#### apk add

Instala softwares, bibliotecas do sistema.

Ex:
```bash
apk add nome_pacote
```

---

#### apk del

Remove softwares, bibliotecas do sistema.

Ex:
```bash
apk del nome_pacote
```

---

### Manutenção do Sistema

---

#### apk update

Para atualizar os índices do repositório.

Ex:
```bash
apk update
```

---

#### apk upgrade

Instala as atualizações disponíveis nos repositórios.

Ex:
```bash
apk upgrade
```

---

#### apk update && apk upgrade

Junção dos dois comandos em apenas um.

Ex:
```bash
sudo apk update && sudo apk upgrade
```

---

### Consultando informações do pacote

---

#### apk search

Para procurar um pacote a ser instalado. 

Ex:
```bash
apk search termo_pesquisa
```

---

#### apk info

Fornece informações detalhadas sobre pacotes ou repositórios.

Ex:
```bash
apk info nome_pacote
```

---

### Variados

---

#### apk stats

Exibe estatísticas sobre repositórios e instalações, como pacotes instalados e disponíveis para instalação, total de arquivos e diretórios, etc.


Ex:
```bash
apk stats
```

---
