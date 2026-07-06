# Comandos Linux:


##### Sumário
- [bg](#bg)


---


##### bg

Move os jobs para o background. Exemplo de uso:

Ex:  
**ping 8.8.8.8**
**CTRL+Z**
_**bg**_

Deixa o _ping_ rodando em segundo plano. Para cancelar não adianta usar o _CTRL+C_, para cancelar quando ele estiver em segundo plano é preciso acessar outro terminal rodar _ps aux | grep ping_, depois _kill [id do processo do ping]_.  

Ex2:  
**bg 2**  -> Para executar em background o comando que foi parado e recebeu o número de tarefa 2.

---
