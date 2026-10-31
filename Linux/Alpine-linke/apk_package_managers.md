# APK - Gerenciadores de Pacotes:


### Sumário
- [apk](#apk)
- [apk update](#apk-update)
- [apk update && apk upgrade](#apk-update--apk-upgrade)
- [apk add](#apk-add)
- [apk del](#apk-del)
- [apk search](#apk-search)

---

#### apk

O APK (Alpine Package Keeper) é o gerenciador de pacotes oficial do Alpine Linux. Ele foi escrito do zero em C para ser extremamente rápido, leve e eficiente no consumo de memória e espaço em disco, características essenciais para imagens de containers e ambientes minimalistas.

---

#### apk update

Para atualizar sua lista de pacotes.

Ex:
```bash
apk update
```

---

#### apk update && apk upgrade

Junção dos dois comandos em apenas um.

Ex:
```bash
sudo apk update && sudo apk upgrade
```

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

#### apk search

Para procurar um pacote a ser instalado. 

Ex:
```bash
apk search termo_pesquisa
```

---
