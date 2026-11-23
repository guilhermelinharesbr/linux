# SCP


### Sumário
- [Definição](#definição)
- [Pacote de instalação](#site-oficial)
- [Opções](#opções)
- [Exemplos](#)


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

#### Exemplos

Ex1.0. **Enviando** um arquivo local para uma outra VM:
```bash
scp /caminho_arquivo/nome_arquivo usuario_da_vm_destino@ip_vm:/diretorio_destino
```

Ex1.1. Enviando um arquivo de nome metas.txt para a VM que possui o usuário de nome administrator, ip 192.168.1.105 e colocando na pasta /tmp:
```bash
scp /home/administrator/metas.txt root@192.168.1.105:/tmp
```

Ex2.0. **Recebendo/pegando** um arquivo de um servidor remoto:
```bash
scp usuario_da_vm_origem@ip_vm:/diretorio_origem/nome_arquivo /diretorio_destino 
```

Ex2.1. Recebendo/pegando o arquivo de nome arq2 utilizando o usuário root da VM de IP 192.168.1.105 e salvando na pasta /tmp:
```bash
scp root@192.168.1.105:/tmp/arq2 /tmp 
```

Ex2.2. Recebendo/pegando o arquivo de nome arq2 utilizando o usuário root da VM de IP 192.168.1.105, salvando na pasta /tmp e informando a porta do SSH, que no caso não é padrão 22:
```bash
scp -P12578 root@192.168.1.105:/tmp/arq2 /tmp 
```

---
