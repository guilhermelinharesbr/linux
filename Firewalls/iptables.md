# IPTABLES


### Sumário
- [Definição](#definição)
- [-V / --version](#-v----version)
- [-v / --verbose](#-v----verbose)
- [-L / --list](#-l----list)
- [-n / --numeric](#-n----numeric)
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
