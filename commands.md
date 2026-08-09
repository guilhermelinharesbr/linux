# Comandos Linux:


### Sumário
- [adduser](#adduser)
- [arch](#arch)
- [arp](#arp)
- [bg](#bg)
- [bzip2](#bzip2)
- [bunzip2](#bunzip2)
- [cat](#cat)
- [cd](#cd)
- [chgrp](#chgrp)
- [chmod](#chmod)
- [chown](#chown)
- [chroot](#chroot)
- [clear](#clear)
- [cp](#cp)
- [curl](#curl)
- [date](#date)
- [df](#df)
- [du](#du)
- [echo](#echo)
- [env](#env)
- [ethtool](#ethtool)
- [exit](#exit)
- [export](#export)
- [faillog](#faillog)
- [fdisk](#fdisk)
- [fg](#fg)
- [fgrep](#fgrep)
- [file](#file)
- [find](#find)
- [free](#free)
- [fsck](#fsck)
- [grep](#grep)
- [gzip / gunzip](#gzip--gunzip)
- [halt](#halt)
- [head](#head)
- [history](#history)
- [hostname](#hostname)
- [id](#id)
- [ifconfig](#ifconfig)
- [inxi](#inxi)
- [ip](#ip)
- [jobs](#jobs)
- [kill](#kill)
- [killall](#killall)
- [last](#last)
- [less](#less)
- [locate](#locate)
- [ls](#ls)
- [lsblk](#lsblk)
- [lscpu](#lscpu)
- [man](#man)
- [mkdir](#mkdir)
- [more](#more)
- [mount](#mount)
- [ncdu](#ncdu)
- [netstat](#netstat)
- [nl](#nl)
- [nload](#nload)
- [nmap](#nmap)
- [nslookup](#nslookup)
- [ntpdate](#ntpdate)
- [ntsysv](#ntsysv)
- [od](#od)
- [passwd](#passwd)
- [paste](#paste)
- [ping](#ping)
- [pgrep](#pgrep)
- [poweroff](#poweroff)
- [ps](#ps)
- [rg](#rg)
- [rm](#rm)
- [runlevel](#runlevel)
- [scp](#scp)
- [sed](#sed)
- [shutdown](#shutdown)
- [sort](#sort)
- [split](#split)
- [ss](#ss)
- [ssh-keygen](#ssh-keygen)


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

#### cd

Altera o diretório de trabalho do shell.

**cd Downloads**  -> Entra no diretório Downloads.             

**cd ..**  -> Volta para o diretório anterior.

**cd "Arquivos Variados"** ou **cd 'Arquivos Variados'**  -> Acessa diretórios com nomes compostos.

**cd -**  -> Para voltar ao último diretório visitado antes do diretório atual.

**cd** ou **cd \~** ou **cd ~/**  -> Para ir para o seu diretório home.

**cd ../Documentos**  -> Para ir para um diretório do mesmo nível (diretório irmão) do diretório atual. No Linux Mint o Downloads e o Documentos são diretórios que estão no mesmo nível.   

---

#### chgrp

Altera o nome de grupo de arquivos.

**chgrp -Rc desenvolvimento teste** -> Altera o grupo do diretório _teste_ e de todos os arquivos e diretórios que estão hierarquicamente abaixo do diretório teste, pois foi usada a opção **-R**, que vem de recursive. Como a opção **-c** é usada, será mostrada a lista dos arquivos e diretórios que tiveram o nome do grupo alterado, a opção **-c** vem de _changes_.
A opção **-v** vem de _verbose_ -> Informa quais arquivos estão sendo processados (não necessariamente alterados).

---

#### chmod

Permite alterar manualmente as configurações de permissão de um arquivo.

**chmod -R 777 /home/pensador/Imagens** -> Faz com que todos os arquivos que estejam na pasta Imagens possam ser executados por qualquer usuário.

**chmod 777 arquivo** é o mesmo que **chmod ugo+rwx arquivo**. 

---

#### chown

Altera o dono do arquivo e pode também alterar o grupo a que este arquivo pertence.

**chown pensador arquivo.txt** -> Altera o dono do arquivo arquivo.txt para o usuário pensador.

**chown pensador. arquivo.txt** -> Altera o dono do arquivo _arquivo.txt_ para o usuário _pensador_ e o grupo do arquivo para o grupo do usuário.

**chown pensador:users arquivo.txt** -> Altera o dono do arquivo arquivo.txt para o usuário pensador e o grupo para users.

**chown .users arquivo.txt** -> Altera o grupo do arquivo para users e deixa inalterado o dono do arquivo. Dessa forma ele trabalha similar ao chgrp, mudando somente o grupo.

**chown -R pensador /home/pensador** -> Altera o dono de todos os arquivos e diretórios dentro de /home/pensador para o usuário pensador. A opção -R vem de recursive.
Um usuário comum somente pode passar a propriedade de arquivos e diretórios dos quais ele é dono. O usuário root pode alterar a propriedade de qualquer arquivo ou diretório.

Exemplo:
**ps aux | grep php**
apache    1232  0.1  2.6 533340 208332 ?       S    mai25   3:12 php-fpm: pool www
apache    1233  0.1  2.6 773088 205856 ?       Sl   mai25   3:57 php-fpm: pool www

Neste exemplo, o usuário que está executando o php-fpm é o apache.
Então, para dar permissão para o php gravar algo no diretório upload, não é necessário alterar a permissão, mas sim o dono do diretório:

**ls -l | grep upload**
drwxr-xr-x  2 root   root        4096 mai  25 22:33 upload

Altera-se então o dono do diretório upload para o usuário apache. Desta forma, o processo do php-fpm será capaz de gravar, ler e acessar o diretório upload:

**sudo chown apache upload**
**ls -l | grep upload**
drwxr-xr-x  2 apache   root        4096 mai  25 22:33 upload

---

#### chroot

Executa um comando ou um shell interativo de outro diretório e trata esse diretório como raiz. 

---

#### clear

Serve para limpar a tela do terminal. Também pode-se usar o atalho _CTRL + L_.

---

#### cp

Serve para copiar arquivos e diretórios. 

**cp -Rvi /home/user/imagem.jpg /home/user/Downloads**

**cp -i**  -> A opção **-i** serve para perguntar se deseja sobrescrever algum arquivo com mesmo nome no diretório de destino.

**cp -R** ou **cp -r** -> A opção serve para copiar os diretórios recursivamente.

**cp -v** -> A opção **-v** é modo verbose, serve para mostrar o que está sendo copiado.

---

#### curl

Client URL. O uso mais simples do curl é para mostrar o conteúdo de uma página. Para saber se máquina tem conexão com a internet.

Protocolos suportados: HTTP e HTTPS; FTP e FTPS; IMAP e IMAPS; POP3 e POP3S; SMB e SMBS; SFTP; SCP; TELNET; GOPHER; LDAP e LDAPS; SMTP e SMTPS.

Ex:  
**curl www.google.com.br**  
**curl google.com**  
**curl --connect-timeout 5 http://$IPADDRESS**  -> Imprime na tela o conteúdo do servidor, a opção de _conection-timeout_ serve para tentar somente até 5 segundos, depois disso ele não tenta novamente.

---

#### date

Mostra ou define a data e hora do sistema.

**date** ->   Mostra data e hora.  
**date -s "05 JUN 2020 15:17:00"** -> Configura data e hora. A opção **-s** vem de _set_. Só usar caso o comando _ntpdate_ não resolva. 

---

#### df

Mostra o quanto está sendo usado no disco.

**df -h** -> A opção -h vem de human readable.  
**df -Th** -> Para ver o tipo de sistema de arquivos, se é ext4, xfs, swap etc. A opção **-T** ou **--print-type** tem a mesma função.

---

#### du

DU vem de disk usage. 

__du -sh *__ -> Mostra o tamanho de arquivos e diretórios. Tem que estar dentro do diretório para usar esse comando.

**du -h | egrep -v "\./.+/" | sort -h** -> Mostra os maiores diretórios usando os comandos encadeados du, egrep e sort. Tem que estar dentro do diretório para usar esse comando.

**du -h --max-depth=1 /home** -> Mostra o tamanho das pastas do /home.

---

#### echo

Ex:  
**echo > nome_arquivo.log** -> Para zerar arquivos de logs, se um arquivo tiver 25GB ele ficará com 0KB.

---

#### env

É utilizado para executar um programa em um ambiente modificado, enviando para ele uma ou mais variáveis ambientais. 
Servindo para trocar o conteúdo de uma variável de uma forma temporária e mandar isso para um comando e dentro desse comando vai ter acesso a essa variável e dentro desse comando vai ter acesso a essa variável com o valor diferente. 

Exemplo de uso:  
**echo \$LIVRO** -> visto que a variável LIVRO ainda não foi definida.
**LIVRO="Certificação Linux"** -> Criada a variável LIVRO.
**echo \$LIVRO** -> visto que a variável LIVRO foi definida.
**vim lerlivro** -> Criando um script
#!/bin/bash
echo $LIVRO 
:wq -> Script de apenas 2 linhas criado
**chmod +x lerlivro** -> Fornecendo permissão de execução para o script.
**./lerlivro** -> Não "leu nada", ou seja não mostrou nada em tela, pois a variável LIVRO não foi exportada.
**export LIVRO** -> Exportada a variável LIVRO.
**./lerlivro** -> Mostrou em tela Certicação Linux.
**env LIVRO="TCC Trabalho de Conclusão de Curso" ./lerlivro** -> O env trocou o conteúdo da variável LIVRO e mandou esse conteúdo para o script lerlivro. Então o script mostrou em tela TCC  Trabalho de Conclusão de Curso.
**./lerlivro** -> Mostrou em tela novamente Certificação Linux. Confirmando que a variável só havia sido alterada de maneira temporária.

---

#### ethtool

Serve para ver informações detalhadas da interface de rede, como velocidade, duplex, link, auto-negociação, etc.

Ex:  
**ethtool eth0** -> mostra informações da interface eth0.

---

#### exit

Serve para sair da sessão.

---

#### export

Comando do shell que permite configurar e compartilhar variáveis de ambiente entre diversos programas e bibliotecas acessados a partir do mesmo terminal.

Ex:  
**export** -> mostra as variáveis de ambientes configuradas, inclusive senhas, caso tenham sido informadas. Exemplo de retorno declare -x MYSQL_ROOT_PASSWORD="q-+@l3O9uit)SV^{k37jdjdfsgn34kfgvdfklklj36"

---

#### faillog

Exibe o conteúdo do banco de dados de log de falhas (/var/log/faillog). Ele também pode definir os contadores de falhas e limites. Quando o faillog é executado sem argumentos, ele exibe apenas os registros de faillog dos usuários que tiveram uma falha de login.

Ex:  
**faillog -a** -> Mostra os registros de faillog para todos os usuários com um entrada no banco de dados faillog.

---

#### fdisk

É um programa baseado em diálogo para criação e manipulação de tabelas de partição. Ele compreende tabelas de partições GPT, MBR, Sun, SGI e BSD.

**sudo fdisk -l** -> Mostra as partições dos dispositivos conectados na máquina, seja HD interno/externo ou pendrive. Precisa permissão de super usuário para executar. 

---

#### fg

Move os jobs para o foreground. 

Exemplo de uso:  
**ping 8.8.8.8
CTRL+Z
fg**

Deixa o ping rodando em primeiro plano. Para cancelar basta usar o _CTRL+C_. 

Exemplo 2:  
**fg 2**  -> Para executar em foreground o comando que foi parado e recebeu o número de tarefa 2.

---

#### fgrep

É parecido com o _grep_, mas ele não suporta expressões regulares, procurando somente uma chave de busca ou um texto comum nos arquivos. Por este motivo, é mais rápido que o grep, mas menos versátil. 

Ele é o mesmo que a opção **-F** ou **--fixed-strings** do grep.

**fgrep clube hino_fortaleza.txt** -> Pesquisa a palavra clube dentro do arquivo hino_fortaleza.txt

---

#### file

Determina o tipo do arquivo.

**file livros_diversos.jpg** -> Resultado: livros_diversos.jpg: JPEG image data, baseline, precision 8, 640x480, components 3.

**file -i churrasqueira_01.jpg** -> A opção **-i** vem de m**I**me type. Resultado: churrasqueira_01.jpg: image/jpeg; charset=binary.

---

#### find

Pesquisa arquivos em uma hierarquia de diretórios.

**find / -iname “\*hba\*”** -> Pesquisa por qualquer arquivo no / do S.O. que tenha a palavra “hba” em qualquer parte do nome do arquivo. 

---

#### free

Mostra a quantidade de memória livre e em uso.

**free -h** -> Mostra a quantida de memória forma legível pelos humanos.

**free -m** -> Mostra a quantida de memória em megabytes.

---

#### fsck

Checa e repara o sistema de arquivos do Linux. [File System Check] 
Precisa ser executado como root. Não é interessante executar o fsck em uma partição montada, pois no processo de checagem/reparação podem acontecer erros.

**sudo fsck /dev/sdb1** -> Checa se o disco está com algum erro, ou bad block.

Opções úteis:
**-A**: Faz a checagem de todos os discos especificados no arquivo /etc/fstab.
**-p**: Repara automaticamente o sistema de arquivos.
**-y**: Executa o fsck de modo não interativo, ou seja ele coloca _yes_ para todas as perguntas.

---

#### grep

Mostra linhas que correspondem aos padrões. Ele filtra as linhas de um determinado arquivo procurando por uma expressão regular como padrão.

Utiliza o padrão de Expressões Regulares POSIX BRE. Assim, os meta-characters ? + { } | (  )  não tem significado especial. No padrão BRE(Basic Regular Expression) esses caracteres somente são interpretados com significado especial se precedidos com a contra-barra  \\?   \\+   \\{   \\}  \\|   \\(   \\). Já no ERE(Extended Regular Expression) os símbolos falados acima já são considerados meta-characters sem precisar colocar o \\.

**grep -i palavra** -> A opção **-i** ou **--ignore-case** serve para na pesquisa não ser case sensitive, tanto _grep -i id_ ou _grep -i Id_ retornarão o mesmo resultado. Se não usar o -i o grep só retornará como case sensitive.

**grep -c [palavra_buscada] [arquivo]** -> Resultado foi 6, ou seja encontrou 6 vezes a palavra dentro do arquivo.

**grep -h [palavra_buscada] [arquivo]** -> Mostra somente as linhas encontradas, sem a indicação do nome dos arquivos.

**grep -n [palavra_buscada] [arquivo]** -> Mostra, além do texto das linhas encontradas, o número das linhas dentro dos arquivos.

**grep -r [palavra_buscada] \*** -> Busca essa palavra em todos os arquivos do diretório atual, bem como subdiretórios. A opção **-r** vem de recursive.

---

#### gzip / gunzip

Comprimi ou expande arquivos.

**gzip** -> Serve para comprimir arquivos. Gera um arquivo com a seguinte nomenclatura: *nome_arquivo.gz*.

**gunzip** ou **gzip -d** -> Serve para descomprimir um arquivo.

**gzip -l** -> Lista informações do arquivo comprimido, como tamanho do arq. comprido e descomprimido, porcentagem da compressão, etc.

**gzip -r** -> Comprimi todos os arquivos dentro do diretório Recursivamente, mas não comprimi o diretório em si.

**gzip -rd** -> Descomprimi todos os arquivos dentro do diretório recursivamente, mas não descomprimi o diretório em si.

---

#### halt

Emitir o comando halt interromperá todas as funções da CPU no sistema. Na maioria dos sistemas, isso o levará ao modo de usuário único e desligará a máquina.

---

#### head

Mostra as primeiras 10 linhas do início de um arquivo como padrão. É o oposto do comando _tail_.

**head  nome_arquivo** -> Mostra as 10 primeiras linhas do arquivo.

**head -n7 nome_arquivo** -> Mostra as 7 primeiras linhas do arquivo. A opção **-n** ou **--lines**: Configura o número de linhas que o head irá mostrar. 

**head -n50 nome_arquivo** -> Mostra as 50 primeiras linhas do arquivo.

---

#### history

Mostra o histórico de comandos executados.

**history -d 990** -> Exclui a linha de número 990 do history. Útil para apagar um comando quando não desejar que ele fique no histórico.

Uma outra forma de deletar alguma linha do history é ir no arquivo **.bash_history** que fica no diretório home do usuário, Ex: /home/user ou /root, são arquivos diferentes para cada usuário. Após excluir o conteúdo via _vim_ ou _nano_ é necessário reiniciar o sistema.

---

#### hostname

Mostra o nome da máquina.

Também pode-se usar o _cat /etc/hostname_, que dá o mesmo resultado que somente hostname.

**hostname -I** -> Mostra todos os endereços de rede do host. 

---

#### id

Mostra os IDs e os grupos que determinado usuário faz parte.

**id guilherme.linhares**

---

#### ifconfig

Mostra o IP e o MAC. O mac fica em endereço de HW.

---

#### inxi

Script de informações do sistema de linha de comando para console e IRC (Internet Relay Chat).

**inxi -F** -> Mostra muitas informações do sistema e da máquina, como a versão da distro, hostname, kernel. 

---

#### ip

Mostra/manipula roteamento, dispositivos, roteamento de políticas e túneis.

**ip a** -> Mostra todos endereços de rede do host, muito similar ao comando ifconfig.

**ip a | grep inet** -> Mostra todos os IPs de maneira mais legível.

**ip neigh** -> é usado para listar, adicionar ou remover entradas na tabela de “neighbors”, ou tabela de associação entre endereços MAC e endereços IP. Eu vou evitar o termo “tabela ARP”, pois, como já foi dito, para endereços IPv6 o protocolo ARP não é usado. Aliás, o protocolo ARP irá morrer um dia junto com o IPv4.

---

#### jobs

Lista os processos que estão em execução em segundo plano. Se um número da tarefa é fornecido o comando retornará as informações pertinentes somente à tarefa em questão.

**jobs -l** ->   Lista o PID dos processos em segundo plano.

**jobs -r** ->   Lista somente os Jobs em execução (Running).

**jobs -s** ->  Lista somente os Jobs parados (Stopped).

Exemplo de uso:  
**watch ping 8.8.8.8
CTRL+Z
jobs -l
bg 1**  -> Para executar em background o comando que foi parado e recebeu o número de tarefa 1.

---

#### kill

**kill 2531** -> Mata um processo de maneira normal, no caso mata o processo de PID 2531.

**kill -9 2531** -> Mata o processo abruptamente.

---

#### killall

**killall htop** -> Mata processos pelo nome. Nesse exemplo mata todos os processos com o nome _htop_.

**killall -I htop** -> Mata todos os processos com o nome _htop_ ignorando se está escrito com letra maiúscula ou minúscula. A opção I vem de ignore case.

**killall -i htop** -> Mostra de maneira interativa todos os processos com o nome htop para você escolher quais matar. A opção **-i** vem de _interactive_.

---

#### last

Mostra os últimos logins (muito detalhado).

---

#### less

Permite fazer a paginação de arquivos ou da entrada padrão.
O less é uma versão melhorada do aplicativo _more_.

**ls | less** -> Faz com que a listagem dos arquivos do diretório corrente seja paginada pelo _less_.

**ls | less -N** -> A opção **-N** ou **--LINE-NUMBERS** numera as linhas do arquivo.

---

#### locate

Este comando utiliza um banco de dados de nomes de arquivos para pesquisar um determinado nome. Esta base de dados é criada/atualizada pelo administrador do sistema através do comando updatedb e é armazenada em _/var/lib/mlocate/mlocate.db_.  
É mais rápido que o _find_. Caso não encontre de primeira o arquivo procurado, deve-se rodar o _updatedb_ e depois o comando _locate_ novamente.

Ex:  
**locate nome_arquivo**

---

#### ls

Serve para listar o que tem dentro do diretório.  

Ex:  
**ls -a** ->     Serve para ver os arquivos ocultos da pasta.  
**ls -l** ->      Serve para listar em formato de linhas, mostra os atributos e as permissões do arquivos que estão em um determinado diretório.  
**ls -ld** ->     Serve para listar as permissões em um determinado diretório.  
**ls -lh** ->    Mostra tudo o que o _ls -l_ mostra, mas com informações mais amigáveis para humanos.
Obs: Se começar com _d_ é diretório, se começar com - é arquivo.
Obs2: O primeiro trio é o Owner/User, depois Group, depois Other.  
**ls -lhS** ->     Opção: _S_ maiúsculo ordena os arquivos do maior pro menor tamanho.  
**ls -lhSr** ->    Opção: _r_ inverte a listagem colocando por último os maiores arquivos.  
**ls | wc -l** ->  Mostra quantos arquivos tem dentro de uma pasta.  
**ll** ->             Um alias para _ls -alF_  
**ls -1 | wc -l**  -> Mostra o total de arquivos em um diretório.

---

#### lsblk

Lista informações sobre todos os dispositivos de bloco disponíveis ou especificados. Lê o sistema de arquivos sysfs e o udev db para coletar informações.
Exibe informações sobre as partições do HD e outros dispositivos de armazenamento como pen drives e CDs em formato de árvore.

**lsblk -S** -> Mostra apenas os dispositivos SCSI(Small Computer System Interface), como CD-ROM, etc. 

---

#### lscpu

Exibi informações sobre a arquitetura da CPU.

---

#### man

Mostra o manual do comando.  

Ex:  
**man nome_do_comando**

Ex2:  
**man ls**

---

#### mkdir

Cria diretórios.

Ex:  
**mkdir pasta1** -> Cria um único diretório.  
**mkdir pasta1 pasta2 pasta3** -> Cria três diretórios separados.  
**mkdir -p pasta1/subpasta2** -> Cria um diretório com um subdiretório nele. A opção **p** vem de _parents_.  
**mkdir -v pasta1 pasta2 pasta3** -> Cria três diretórios distintos, porém mostra eles sendo criados durante a execução do comando. A opção **v** vem de _verbose_.  
**mkdir "curso de terminal"** ou **mkdir 'curso de terminal'** -> Cria um diretório com nome composto.

---

#### more

Permite fazer a paginação de arquivos ou da entrada padrão.  
O more tem uma versão melhorada que é o _less_.

Ex:  
**ls | more** -> Faz com que a listagem dos arquivos do diretório corrente seja paginada pelo more.

---

#### mount

Monta um sistema de arquivos.  
**mount -a** ou **mount --all** -> Monta todos os sistemas de arquivos listados no _/etc/fstab_. Exceto aqueles assinalados com a opção _noauto_.

---

#### ncdu

NCDU(NCurses Disk Usage) é uma versão baseada em curses do conhecido comando _du_ e fornece uma maneira rápida de ver quais diretórios estão usando seu espaço em disco.

_Curses_ é uma biblioteca de controle de terminal para sistemas do tipo Unix, permitindo a construção de aplicativos de TUI(Text User Interface).

É muito simples de navegar por meio desse TUI, ou seja é uma ótima escolha para substituir o comando _du_.

---

#### netstat

O Comando netstat no Linux faz parte do antigo pacote legado Net-Tools e exibe as conexões de rede, tabela de rotas, estatísticas das interfaces etc. Ele foi elegantemente substituído pelo comando _ss_.

**sudo netstat -ltpn** -> Saída: netstat -ltpn         Opções: A opção **l** mostra somente os sockets listening, **t** mostra os sockets TCP, p mostra processos usando sockets, **n** não tenta resolver nomes de serviço e mostra valores de largura de banda exatos.

Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 0.0.0.0:15974           0.0.0.0:*               LISTEN      822/sshd: /usr/sbin
tcp        0      0 0.0.0.0:9102            0.0.0.0:*               LISTEN      2340/docker-proxy
tcp        0      0 0.0.0.0:80              0.0.0.0:*               LISTEN      2280/docker-proxy
tcp        0      0 0.0.0.0:443             0.0.0.0:*               LISTEN      2303/docker-proxy
tcp6       0      0 :::15974                :::\*                    LISTEN      822/sshd: /usr/sbin
tcp6       0      0 :::9102                 :::\*                    LISTEN      2346/docker-proxy
tcp6       0      0 :::80                   :::\*                    LISTEN      2288/docker-proxy
tcp6       0      0 :::443                  :::\*                    LISTEN      2310/docker-proxy

---

#### nl

É utilizado para numerar as linhas de um arquivo. O comando considera condições especiais para o cabeçalho e o rodapé do arquivo.

nl vem de _Number Lines_.

As opções frequentemente utilizadas são:
**-h** sub-opção: Utilizada para formatar o cabeçalho do texto. O padrão é não numerar o cabeçalho;

**-b** sub-opção: Utilizada para formatar o corpo do texto. O padrão é numerar somente as linhas não vazias;

**-f** sub-opção: Utilizada para formatar o rodapé do texto. O padrão é não numerar o rodapé.

As sub-opções são:

**A**: Numerar todas as linhas;
**t**: Numerar somente as preenchidas;
**n**: Não numerar as linhas.

Suponha que o _arquivo.txt_ tenha o seguinte conteúdo:
\\:\\:\\:
Relatório de Notas e Frequência dos alunos de Engenharia de Software
—————————————————————————————————
Nome Nota Freq. Resultado
—————————————————————————————————
\\:\\:
Carlos Torres 8,5 80% Aprovado
Maria de Lourdes 10,0 100% Aprovado
Mário Cabral 9,5 100% Aprovado
\\:
—————————————————————————————————
**nl arquivo.txt**

Resultado será:
Relatório de Notas e Frequência dos alunos de Engenharia de Software
—————————————————————————————————
Nome Nota Freq. Resultado
—————————————————————————————————
**1** Carlos Torres 8,5 80% Aprovado
**2** Maria de Lourdes 10,0 100% Aprovado
**3** Mário Cabral 9,5 100% Aprovado
—————————————————————————————————

---

#### nload

Mostra o atual uso de rede, tando Incoming(download), quanto Outgoing(upload).

---

#### nmap

Ferramenta de exploração de Rede e Rastreio de Segurança / Portas.

**nmap 8.8.8.8** -> Mostra as portas abertas do Google as portas 53(domain) e 443(https).

**nmap 10.0.0.8** -> Mostra as portas abertas de um sistema interno 80(http), 443(https), etc.

**nmap uol.com.br** -> Mostra as portas abertas da Uol as portas 80(http) e 443(https).

---

#### nslookup

Usado para consultar servidores de nomes de domínio da Internet para obter informações.

**nslookup google.com** -> Saída:  Server:127.0.0.53                                               Address:127.0.0.53#53                                              Non-authoritative answer:                  Name:google.com                                      Address: 142.250.218.238                                                            Name:google.com                                        Address: 2800:3f0:4001:825::200e

**nslookup 8.8.8.8** -> Saída:     8.8.8.8.in-addr.arpaname = dns.google.

**nslookup openvpn.orgao.gov.br** -> Saída:  Non-authoritative answer:                                                                      Name:openvpn.orgao.gov.br                                                                      Address: 179.104.42.200                                                                      Name:openvpn.orgao.gov.br                                                                      Address: 177.14.224.200

---

#### ntpdate

Configura a data/hora via o protocolo NTP(Network Time Protocol). 

**ntpdate 10.0.0.12** -> pega data e hora com base no servidor 12. 

**ntpdate a.ntp.br** -> pega data/hora com base no servidor público NTP.br(horário de Brasília), outros disponíveis: b.ntp.br e c.ntp.br.

---

#### ntsysv

Usado em _Red Hat_ e derivados. Oferece uma interface simples para ativar ou desativar serviços. Você pode usar o ntsysv para ligar ou desligar um serviço gerenciado pelo _xinetd_. 

---

#### od

O _od_ (Octal Dump) é utilizado para mostrar o conteúdo de um arquivo nos formatos hexadecimal, octal, ASCII e nome dos caracteres.

A opção frequentemente utilizada é:
**-t type**: Especifica o tipo de saída que o comando od deve gerar.

Os tipos possíveis são:
**a**: Nome do caractere;
**c**: ASCII;
**o**: Octal;
**x**: Hexadecimal.

Ex:  
**cat arquivo.txt**
Certificação Linux
**od –t x arquivo.txt**
0000000 74726543 63696669 6fe3e761 6e694c20
0000020 00007875
0000022

---

#### passwd

Para alterar a senha de um usuário.

**passwd** *nome_usuario*

---

#### paste

É utilizado para concatenar as linhas de diversos arquivos em colunas verticais.

As opções frequentemente utilizadas são:
**-d’s’** -> Separa as colunas com o símbolo **s** nas aspas simples. A opção **d** vem de delimiters.

**-s** -> Concatena todo o conteúdo de um arquivo com uma linha para cada arquivo. A opção **s** vem de serial.

Exemplo:  
Suponha que o arquivo1 tenha o seguinte conteúdo: 
lmmoraes
rrodrigues
aduarte

E o arquivo2 tenha o seguinte conteúdo:
provedor.com.br
provedor2.com.br
provedor3.com.br

Ao utilizarmos o comando paste, o resultado será o seguinte:
**paste –d'@' arquivo1 arquivo2**
lmmoraes@provedor.com.br
rrodrigues@provedor2.com.br
aduarte@provedor3.com.br

---

#### ping

Envia ICMP ECHO_REQUEST para hosts de rede.

Ex:  
**ping 8.8.8.8**

Para instalar -> _apt install iputils-ping_

---

#### pgrep

**pgrep vim** -> Mostra o PID do editor VIM caso ele esteja aberto.

---

#### poweroff

**poweroff** -> Envia um sinal ACPI(Advanced Configuration and Power Interface) com instruções para desligar o sistema.

**poweroff --reboot** -> Reinicia o sistema.

---

#### ps

Ps vem de Process Status.

**ps aux** -> Lista todos os processos rodando no sistema.

**ps aux | grep mysql** -> Mostra se existe algum serviço com o nome mysql rodando.

---

#### rg

O **ripgrep** (frequentemente abreviado como **rg**) é uma ferramenta de busca por linha de comando focada em texto. Em termos simples, ele serve para encontrar palavras ou padrões de texto dentro de arquivos, funcionando como um _substituto moderno_, ultraveloz e muito mais inteligente para o _clássico grep_.

Obs: Pacote ripgrep.

Ex:  
**rg "network" saida-ifdown** -> Pesquisa pelo termo network no arquivo saida-ifdown.

Ex2:  
**rg -i "network" saida-ifdown** -> Pesquisa pelo termo network no arquivo saida-ifdown, ignorando letras maiúsculas e minúsculas. A opção **-i** vem de _--ignore-case_.

Ex3:  
**rg -w "network" saida-ifdown** -> Pesquisa pelo termo network no arquivo saida-ifdown, busca apenas pela palavra exata, por exemplo "network-manager" seria ignorando. A opção **-w** vem de _--word-regexp_.

---

#### rm

Remove arquivos.

**rm -f Relatório\ Serviço\ de\ Suporte.pdf** -> A opção **-f** remove o arquivo sem perguntar, sem pedir confirmação. Quando o nome do arquivo tiver espaços em branco é necessário usar o contra barra **\\** e depois apertar espaço, para ir autocompletando o nome do arquivo.

**rm !(arq8.txt|arq9.txt)** -> Exclui todos os arquivos do diretório exceto os arquivos arq8.txt e arq9.txt.

---

#### runlevel

Mostra o nível de execução SysV anterior e atual.

**runlevel** -> Mostra o runlevel atual. 

---

#### scp

Comando para cópia segura de arquivos.

De um Servidor para uma Máquina Local:
**scp root@10.0.0.100:/tmp/file.sql /home/user/**  
Obs.: Antes do /home tem um espaço em branco.

**scp -P 14753 guilherme.linhares@10.0.0.100:/tmp/file.sql /home/user/**  
Obs.: Antes do /home tem um espaço em branco.

De um Servidor para um Servidor:
**scp file.sql.gz root@10.0.0.100:/tmp/**  
Obs.: Antes do root tem um espaço em branco.

De uma Máquina Local para um Servidor:
**scp -P14753 -r /home/user/print guilherme.linhares@10.0.0.100:/tmp**  
Obs.: **-r** → Parâmetro p/ cópia _recursiva_.

---

#### sed

É um editor poderoso de fluxo de textos, utilizado para filtrá-los e transformá-los. _Sed_ vem de **Stream editor** for filtering and transforming text.

**echo "Estou estudando o comando sed" | sed 's/estudando/devorando/'** -> A saída foi _“Estou devorando o comando sed”_, ou seja, ele substitui a palavra _estudando_ por _devorando_.

---

#### shutdown

**shutdown now** -> Desliga o sistema imediatamente da mesma forma que o _init 0_.

**shutdown -c** -> Cancela um desligamento agendado.

**shutdown -r now** -> Reinicia o sistema da mesma forma que o _init 6_.

**shutdown -r 11:35** -> Reinicia o sistema no horário especificado, no caso, 11:35am.

---

#### sort



---

#### split



---

#### ss



---

#### ssh-keygen



---
