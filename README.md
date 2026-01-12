
# Aspetos interessantes falar

## Breve intodução teórica do GIT, explicar o que consiste 

(...) É um software de controlo de versões, basicamente serve para registar o progresso do desenvolvimento de trabalhos, com a possibilidade de criar um histórico de alterações feitas no trabalho.
(...)

# Explicar também a estrutura de forma esquematizada de como o git funciona 
<img src="img.png">
(Não vou usar esta imagem é só para ter aqui)

<br>

# Explicar comandos básicos de GIT sem utilizar github 

```

GLUA@leitner:/my_repo$ git init 

GLUA@leitner:/my_repo$ git add .

GLUA@leitner:/my_repo$ git commit -m "Isto é um commit ^-^"

GLUA@leitner:/my_repo$ git log 

GLUA@leitner:/my_repo$ git diff <commit_hash1> <commit_hash2> (o quê que o commit 1 tem que o 2 não tem) 

GLUA@leitner:/my_repo$ git restore .  

```


## Focar na parte do GIT em si, controlo de versões, ou seja capacidade de adicionar "checkpoints", de trabalho, ir voltar, usar hashs do commit para ir e voltar 

`git diff --name-only <hash1> <hash2>`


# Criação de um repo no github e ligar o diretório local ao repositório no github

```
GLUA@leitner:/my_repo$ git remote add origin 
GLUA@leitner:/my_repo$ git remote -v
```

# Ou criar um repo e clonar Local

- Criação de um repo
- Adicionar, commits, etc 
- Simulação de trabalho em conjunto 

# Simular erros por exemplo: 

## Evitar auto MERGE COMMITS

### Situação: na origin main está ahead só que na minha branch ainda não fiz `git pull` ou (preferivel `git fetch origin` -> `git merge main`).   
### Se eu tiver na branch leitner, e tiver feito um commit, e após isso fiz `git merge main`, apareceu para resolver o problema um **MERGE COMMITS** e o git resolve automaticamente, mas isso resulta de um historico de commits feio
> Merge branch 'main' into leitner
### e para evitar isso, boa prática fazer `git fetch origin` -> `git rebase`


## `git restore` 
 
## Situação: Estava a trabalhar no meu projeto com o meu colega e por acaso acabo de reparar, que andei para lá a inventar e tornei o trabalho mais confuso do que o que estava, entre essas alterações não consigo voltar a trás, ou pior, estava a eliminar ficheiros auxiliares e sem querer apaguei um ficheiro importante. Com `git restore <nome do ficheiro>` é possível voltar a trás! Ao que estava no último commit


## `git rebase`

# Sobre o README 
## Falar sobre README em repositórios

### Tópicos importantes:

- Descrição do projeto
- Dependências
- Como utilizar

 


## Falar sobre README do perfil, dar exemplo ou fazer

Como o ficheiro tipo markdown é altamente personalizável, existem enúmeras formas de o personalizar, por isso podemos dar as bases e ferramentas e possibilidades mais "simples".  

### Tópicos importantes:

- Breve descrição
- Vida profissional 
- Skills
- Contactos
- Projetos relevantes (?) 

<br><br>

# Por exemplo: 
<br>

# Hi there, my name is Martim Leitner, I'm studying Computer Engineer at Aveiro's University.

<div align="center">

## Currently I'm working at GLUA in some projects! :D <br> WOW this is one of them!!!!  

<div align="left">


## - 🔭 I’m currently working on **GLUA**

## - 💬 Ask me about **git**

## - 📫 How to reach me **leitnermartim@ua.pt**
<br><br>
<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->


# 📊 Stats:

</div>

![](https://github-readme-stats.vercel.app/api/top-langs/?username=matleitner&theme=blue_navy&hide_border=true&include_all_commits=false&count_private=false&layout=compact)
<!--![](https://github-readme-stats.vercel.app/api?username=matleitner&theme=blue_navy&hide_border=true&include_all_commits=false&count_private=false)<br/>
-->
![](https://nirzak-streak-stats.vercel.app/?user=matleitner&theme=blue_navy&hide_border=true)<br/>

###

<div align="left">


# 💻 Tech Skills:
</div>
<!---
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Assembly](https://img.shields.io/badge/assembly%20script-%23000000.svg?style=for-the-badge&logo=assemblyscript&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
-->

<div align="center">
  <img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/programming%20languages/c.svg" height="60" alt="C logo" />
  <img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/programming%20languages/python.svg" height="60" alt="python logo" />
  <img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/programming%20languages/c%2B%2B.svg" height="60" alt="C++" />
  <img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/programming%20languages/java.svg" height="60" alt="java" />
  <img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/programming%20languages/javascript.svg" height="60" alt="js" />
  <img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/social%20icons/html5.svg" alt="Html" height="50" width="50" />
<img src="https://raw.githubusercontent.com/bablubambal/All_logo_and_pictures/1ac69ce5fbc389725f16f989fa53c62d6e1b4883/social%20icons/css3.svg" alt="CSS" height="50" width="50" />
    <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a>
</div>




# 🌐 Contacts:
  [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/_leitner) [![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:leitnermartim@ua.pt)


<div align="left"></div>
</div>

<!--Herr Leitner-->

