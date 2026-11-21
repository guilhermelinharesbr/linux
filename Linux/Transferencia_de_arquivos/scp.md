# SCP


### Sumário
- [Definição](#definição)
- [Pacote de instalação](#site-oficial)
- [Opções](#opções)


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

#### Opções


As opções podem ser vistas por meio do comando `scp --help` ou `man scp` sendo elas:

- **-C** -> Comprime(**C**ompression enable) os arquivos durante a transferência;
- **-p** -> preserva(**p**reserves) as permissões dos arquivos e datas de acesso e modificação;
- **-P** -> definir a porta(**P**ort) do SSH;
- **-r** -> Copia recursivamente(**r**ecursively) subdiretórios e arquivos.

---
