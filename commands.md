# Comandos Linux:


### Sumário
- [adduser](#adduser)
- [arch](#arch)
- [arp](#arp)
- [bg](#bg)
- [bzip2](#bzip2)
- [bunzip2](#bunzip2)
- [cat](#cat)


---

#### adduser

O _adduser_ é um script perl que usa useradd binary no backend. Tem um Wizard mais amigável que o _userddd_.

Ex:  
**adduser** _nome_usuario_


---

#### arch

Diz se o sistema é 64 ou 32 bits.

---

#### arp

Manipula ou exibe os vizinhos de rede IPv4 do em cache do kernel. Ele pode adicionar entradas à tabela, excluir uma ou exibir a conteúdo atual.

**arp -n** -> mostra endereços numéricos, ao invés de tentar determinar os nomes simbólicos da máquina, porta e usuário. Mostra MAC e IP.

---

#### bg

Move os jobs para o background. Exemplo de uso:

Ex: 
**ping 8.8.8.8
CTRL+Z
bg**

Deixa o _ping_ rodando em segundo plano. Para cancelar não adianta usar o _CTRL+C_, para cancelar quando ele estiver em segundo plano é preciso acessar outro terminal rodar _ps aux | grep ping_, depois _kill [id do processo do ping]_.  

Ex2:  
**bg 2**  -> Para executar em background o comando que foi parado e recebeu o número de tarefa 2.

---

#### bzip2

Serve para comprimir e descomprimir arquivos.

Ex:  
**bzip2** _nome_arquivo_ -> Comprime o arquivo, gerando com a seguinte nomenclatura: _nome_arquivo.bz2_.

Ex2:  
**bzip2 -d** _arquivo.bz2_ -> O **-d** é de decompress. Serve para descomprimir um arquivo.

---

#### bunzip2

Serve para descomprimir um arquivo.

Ex:  
**bunzip2** arquivo.bz2 

---

#### cat

Concatena arquivos e imprimi na saída padrão.

Ex:  
**cat /etc/*-release**  -> Mostra qual a versão S.O. está instalada.  
**cat /etc/shells**  -> Mostra quais shells estão instalados na máquina.  
**cat /var/log/syslog | grep bat**  -> Mostra as linhas de Log do syslog onde tenham a palavra bat nelas. Esse bat faz referência ao antiga interface do Bacula.

---
