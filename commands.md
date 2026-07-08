# Comandos Linux:


### Sumário
- [adduser](#adduser)
- [arch](#arch)
- [bg](#bg)


---

#### adduser

O _adduser_ é um script perl que usa useradd binary no backend. Tem um Wizard mais amigável que o _userddd_.

Ex:  
```bash
adduser nome_usuario
```

---

#### arch

Diz se o sistema é 64 ou 32 bits.

---

#### bg

Move os jobs para o background. Exemplo de uso:

Ex: 
```bash
ping 8.8.8.8
CTRL+Z
bg
```

Deixa o _ping_ rodando em segundo plano. Para cancelar não adianta usar o _CTRL+C_, para cancelar quando ele estiver em segundo plano é preciso acessar outro terminal rodar _ps aux | grep ping_, depois _kill [id do processo do ping]_.  

Ex2:  
`bg 2`  -> Para executar em background o comando que foi parado e recebeu o número de tarefa 2.

---
