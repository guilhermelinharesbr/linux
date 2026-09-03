# RPM - Gerenciadores de Pacotes:


### Sumário
- [rpm](#rpm)
- [rpm -Uvh](#rpm--uvh)
- [rpm -ivh](#rpm--ivh)
- [rpm -e](#rpm--e)
- [rpm -q](#rpm--q)

---

#### RPM

Gerenciador de Pacotes padrão BAIXO nível para o S.O. Fedora , CentOS. Lançado em 1997.

---

#### rpm -Uvh

Atualizar pacotes. Se o \<pacote\> que você estiver atualizando estiver numa versão mais antiga que a já instalada, uma mensagem de alerta irá surgir e a atualização não continuará. Para forçar a atualização mesmo assim, use este mesmo comando com o parâmetro --force: rpm -Uvh --force nome_pacote.

Ex:
```bash
rpm -Uvh nome_pacote
``` 

---

#### rpm -ivh

Instalar pacotes. **i**= install, **v**= verbose, **h**= hashing(porcentagem para terminar de instalar).

Ex:
```bash
rpm -ivh nome_pacote
``` 

---

#### rpm -e

Desinstalar pacotes. **e**= erase.

Ex:
```bash
rpm -e nome_pacote
``` 

---

#### rpm -q

Para verificar se um pacote específico está instalado. **q**= query.

Ex:
```bash
rpm -q nome_pacote
``` 

Para verificar todos os pacotes instalados no sistema:

Ex2:
```bash
rpm -qa nome_pacote
``` 

Para exibir informações do pacote, tais como release, tamanho, etc:

Ex3:
```bash
rpm -qi nome_pacote
``` 

---
