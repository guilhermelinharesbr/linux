# IPTABLES


### Sumário
- [Definição](#definição)
- [-V](#-v)
- [-L](#-l)
- [-n](#-n)
- [iptables-save](#iptable-save)
- [iptables-restore](#)


---

#### Definição

O **iptables** é o programa padrão de firewall para sistemas Linux que controla o tráfego de rede ao permitir ou bloquear pacotes.

---

#### -V

A opção **-V** ou **--version** serve para mostrar a versão do iptables.

Ex:
```bash
iptables -V
ou
iptables --version
``` 

---

#### -L

Lista todas as chains da tabela filter bem como suas regras.
Ao digitar iptables **-L** é o mesmo que digitar iptables **-L -t filter**, pois a tabela filter é a tabela default do comando iptables.

Ex:
```bash
iptables -L
ou
iptables -L -t filter
``` 

---

#### -n

A opção **-n** ou **--numeric** serve para mostrar uma saída numérica, ou seja, sem traduzir os números em nomes. 

Ex:
```bash
iptables -L -n
ou
iptables -L --numeric
``` 

---

#### iptable-save

Salva as regras do iptables, geralmente se redireciona a sáida para um arquivo.

Ex. Salvando a saída do comando em um arquivo:
```bash
iptables-save > /etc/iptables.rules
``` 

---

