# CSF firewall


### Sumário
- [Definição](#definição)
- [-h / --help](#)



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

#### -h / --help

Mostra o meu de ajuda do comando csf.

Ex:
```bash
csf -h
ou
ou csf --help
``` 

---


