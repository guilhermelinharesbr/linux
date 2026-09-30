# IPTABLES


### Sumário
- [Definição](#definição)
- [-V / --version](#-v----version)
- [-v / --verbose](#-v----verbose)
- [-L / --list](#-l----list)
- [-n / --numeric](#-n----numeric)
- [-A / --append](#)
- [-F / --flush](#-f----flush)
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

#### -A / --append



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
