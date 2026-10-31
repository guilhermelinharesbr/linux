# Guia para Administração de Sistemas Linux

Repositório dedicado à documentação de comandos, boas práticas de infraestrutura, gerenciamento de pacotes e configurações de segurança no ambiente Linux.

## Objetivo

Servir como base de conhecimento centralizada e guia de referência rápida para administração de sistemas GNU/Linux, cobrindo distribuições baseadas em Debian e Red Hat, manipulação de terminal, automação e segurança de rede.

---

## Estrutura do Repositório

O conteúdo está organizado por categorias de comandos e famílias de distribuições:

```text
.
├── Debian-like/               # Gerenciamento em distros Debian/Ubuntu
│   ├── apt_package_managers.md
│   └── snap_package_managers.md
├── Red_Hat-like/              # Gerenciamento em distros RHEL/CentOS/Rocky/Fedora
│   ├── yum_package_managers.md
│   └── dnf_package_managers.md
├── Firewalls/                 # Regras de filtro de pacotes e segurança de rede
│   └── iptables.md
├── commands.md                # Comandos gerais do Shell e manipulação de arquivos
├── package_managers.md        # Visão geral e comparação de gerenciadores
├── shortcuts_to_the_terminal.md # Atalhos de produtividade para Bash/Zsh
└── README.md
```

---

## Conteúdo Coberto

### 1. Manipulação do Terminal & Shell
* Comandos essenciais de navegação, busca, permissões e redirecionamento de E/S.
* Atalhos práticos do terminal para ganho de produtividade no dia a dia.

### 2. Gerenciamento de Pacotes
* **Debian-like:** Uso avançado de `apt`, `dpkg` e pacotes universais via `snap`.
* **Red Hat-like:** Operações com `yum`, `dnf` e gerenciamento de repositórios `.rpm`.

### 3. Segurança & Redes
* Regras e tabelas de roteamento/filtragem utilizando `iptables`.
* Diagnósticos de rede e checagem de portas ativas.

---

### Autor

**Guilherme Linhares**  
*SysAdmin / Infraestrutura de T.I.*  
