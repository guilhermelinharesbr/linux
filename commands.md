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
- [date]()


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