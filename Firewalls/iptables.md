# IPTABLES


### Sumário
- [Definição](#definição)
- [-V / --version](#-v----version)
- [-v / --verbose](#-v----verbose)
- [-L / --list](#-l----list)
- [-n / --numeric](#-n----numeric)
- [-A / --append | -p / --protocol | -j / --jump](#-a----append---p----protocol---j----jump)
- [-D / --delete](#-d----delete)
- [-d / --destination](#-d----destination)
- [-s / --source](#-s----source)
- [-F / --flush](#-f----flush)
- [-I / --insert](#-i----insert)
- [--dport](#--dport)
- [--sport](#)
- [iptables-save](#iptables-save)
- [iptables-restore](#iptables-restore)


---

#### Definição

O **iptables** é o programa padrão de firewall para sistemas Linux que controla o tráfego de rede ao permitir ou bloquear pacotes.

---

#### -V / --version

A opção **-V** ou **--version** serve para mostrar a versão do iptables.

Ex:
```bash
iptables -V
ou
iptables --version
``` 

---

#### -v / --verbose

A opção **-v** ou **--verbose** serve para mostrar mais detalhes.

Ex:
```bash
iptables -L -n -v
``` 

---

#### -L / --list

Lista todas as chains da tabela filter bem como suas regras.
Ao digitar iptables **-L** é o mesmo que digitar iptables **-L -t filter**, pois a tabela filter é a tabela default do comando iptables.

Ex:
```bash
iptables -L
ou
iptables -L -t filter
``` 

---

#### -n / --numeric

A opção **-n** ou **--numeric** serve para mostrar uma saída numérica, ou seja, sem traduzir os números em nomes. 

Ex:
```bash
iptables -L -n
ou
iptables -L --numeric
``` 

---

#### -A / --append | -p / --protocol | -j / --jump

Com base no exemplo abaixo serão explicadas as opções **-A**, **-p** e **-j**.

Ex:
```bash
iptables -t filter -A INPUT -p icmp -j DROP
``` 

Explicando o comando acima:
A opção **-A** ou **--append** serve adicionar uma regra em uma chain, no caso acima foi na chain **INPUT**, além disso ao usar a opção -A, a regra sempre é adicionada no final. Lembrando que o iptables trabalha na estrutura top/down.
A opção **-p** ou **--protocol** serve para indicar qual o protocolo.
A opção **-j** ou **--jump** serve para indicar a ação que será executada, no caso acima é de **DROP**, ou seja, bloquear.
Resumindo, foi adicionada uma regra na chain INPUT da tabela filter, bloqueando o protocolo **icmp**, não importando a origem e o destino.

---

#### -D / --delete

Com base no exemplo abaixo será explicada a opção **-D**.

Ex:
```bash
iptables -t filter -D INPUT -p icmp -j DROP
```

A opção **-D** ou **--delete** serve para deletar uma regra de uma chain.

---

#### -d / --destination

A opção **-d** ou **--destination** serve para definir um IP ou rede de destino.

Ex:
```bash
iptables -t filter -A INPUT -p icmp -d 192.168.1.112 -j DROP
```

---

#### -s / --source

A opção **-s** ou **--source** serve para definir um IP ou rede de origem.

Ex. Liberando o ping para a máquina de IP de origem 192.168.1.104:
```bash
iptables -t filter -A INPUT -p icmp -s 192.168.1.104 -j ACCEPT
```

---

#### -F / --flush

A opção **-F** ou **--flush** serve para deletar todas as regras de uma chain ou de todas as chains.

Ex. Apagando as regras de todas as chain:
```bash
iptables -F
``` 

Ex2. Apagando as regras da chain OUTPUT:
```bash
iptables -F OUTPUT
``` 

---

#### -I / --insert

A opção **-I** ou **--insert** serve para inserir uma regra em uma chain em uma determinada posição, a posição padrão é a 1, ou seja, se não colocar nada após o nome da chain a regra será colocada no topo da lista de regras da chain.

Ex:
```bash
iptables -t filter -I INPUT 1 -p icmp -s 192.168.1.104 -j ACCEPT 
ou
iptables -t filter -I INPUT -p icmp -s 192.168.1.200 -j ACCEPT
``` 

Ex2. Colocando o número 3, para que a regra seja criada na posição 3:
```bash
iptables -t filter -I INPUT 3 -p icmp -s 192.168.1.230 -j ACCEPT
``` 

---

#### --dport

Com base no exemplo abaixo será explicada a opção **--dport**.

Ex. Criando uma regra para barrar a porta de destino[destination port(dport)] 1234:
```bash
iptables -A FORWARD -p tcp --dport 1234 -j DROP
``` 

---

#### iptables-save

Salva as regras do iptables, geralmente se redireciona a sáida para um arquivo.

Ex. Salvando a saída do comando em um arquivo:
```bash
iptables-save > /etc/iptables.rules
``` 

---

#### iptables-restore

Restaura as regras do iptables, geralmente pegando de um arquivo.

Ex. Restaurando as regras:
```bash
iptables-restore < /etc/iptables.rules
``` 

---
