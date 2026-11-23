# RSYNC


### Sumário
- [Definição](#definição)
- [Pacote de instalação](#site-oficial)
- [Opções](#opções)
- [Exemplos](#exemplos)


---

#### Definição

O **rsync** é um comando usado para efetuar cópias por meio da rede. Semelhante em utilização ao [scp](./scp.md), o rsync oferece algumas vantagens. Por exemplo, o rsync compara os dados na origem com os dados eventualmente presentes no destino e copia apenas os arquivos que tenham sido modificados. 

A _sintaxe_ básica para Rsync funciona assim:

rsync [modificadores opcionais] [SRC] [DEST]

Existem algumas maneiras diferentes de usar o Rsync Linux. Neste exemplo, [modificadores opcionais] indicam as ações a serem tomadas, [SRC] é o diretório de origem e [DEST] é o diretório ou a máquina de destino.



---

#### Pacote de instalação

Derivados do Debian:
```bash
apt install rsync
```

Derivados do Red Hat:
```bash
dnf install rsync
ou
yum install rsync
```

---

#### Opções


As opções podem ser vistas por meio do comando `rsync --help` ou `man rsync` sendo elas:

- 

---

#### Exemplos

---
