# SCP


### Sumário
- [Definição](#definição)
- [Pacote de instalação](#site-oficial)
- [Opções](#)


---

#### Definição

O **scp** (**s**ecure **c**o**p**y) faz parte do pacote _openssh-client_.
O comando scp no Linux faz a cópia de arquivos de/para computadores remotos utilizando o protocolo SSH, de forma segura. 

O scp pode ser utilizado para enviar ou receber arquivos, dependendo se a origem ou o destino é um caminho de cópia remoto.

Um caminho remoto tem a seguinte sintaxe: usuário@endereço:/diretório.


---

#### Pacote de instalação

Derivados do Debian:
```bash
apt install openssh-client
```

Derivados do Red Hat:
```bash
dnf install openssh-clients
ou
yum install openssh-clients
```

Obs: Existe a diferença no nome dos pacotes, sendo no derivado do Debian no singular e no derivado do Red Hat no plural.

---
