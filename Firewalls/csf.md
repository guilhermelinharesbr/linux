# CSF firewall


### Sumário
- [Definição](#definição)
- [Arquivos e Diretórios](#arquivos-e-diretórios)
- [-h / --help](#-h----help)
- [-v / --version](#-v----version)
- [-l / --status](#-l----status)
- [-l6 / --status6](#-l6----status6)

---

#### Definição

O **CSF** (ConfigServer Security & Firewall) é um firewall de nível de servidor bastante popular em sistemas Linux, especialmente em servidores web com cPanel, DirectAdmin e outros painéis. Ele é conhecido por ser fácil de administrar e por adicionar camadas extras de segurança que vão além do firewall tradicional.

O CSF é um _wrapper_ (camada de gerenciamento) para o _iptables_ ou _nftables_, adicionando:
- Controle intuitivo via arquivos de configuração;
- Ferramentas automáticas de segurança;
- Detecção de intrusão;
- Limitação de conexões;
- Integração com painéis administrativos.


Internamente, ele usa iptables (ou nftables em versões recentes), mas entrega um gerenciamento muito mais amigável.

---

#### Arquivos e Diretórios

- **/etc/csf/** -> Principal diretório de configuração.
- /etc/csf/**csf.conf** -> Principal arquivo de configuração.
- /etc/csf/**csf.allow** -> Lista os IPs permitidos.
- /etc/csf/csf.deny
/* Lista os IPs bloqueados. */
- /var/log/lfd.log
/* Log do LFD(Login Failure Daemon). */
- /usr/sbin/csf
/* Binário principal. */



---

#### -h / --help

Mostra o meu de ajuda do comando csf.

Ex:
```bash
csf -h
ou
csf --help
``` 

---

#### -v / --version

Mostra a versão do firewall csf.

Ex:
```bash
csf -v
ou
csf --version
``` 

---

#### -l / --status

Mostra a configuração das tabelas IPv4 do iptables.

Ex:
```bash
csf -l
ou
csf --status
``` 

---

#### -l6 / --status6

Mostra a configuração das tabelas IPv6 do iptables.

Ex:
```bash
csf -l6
ou
csf --status6
``` 

---
