# Primeiros passos para usar o GIT e o GITHUB como um Profissional!


Este guião é dividido em 2 partes, primeira parte mais inicial, com um trabalho mais simples e o 2º com um nível de dificuldade levemente mais avançado. Para treinares e perceberes as artimanhas do Git!    
# 1ª Parte 

## Instala e configura o GIT 

1. Instalar GIT:

    - **Windows**: [Git para Windows](https://git-scm.com/install/windows)

    - **Debian/Ubuntu**: `sudo apt install git`

    - **macOS**: `brew install git`


Para verificares que o git foi instalado, abre powershell(windows) terminal(linux), e corre o comando: `git -v`

Resultado esperado: `git version 2.52.0.1`

2.  Cria uma conta no GITHUB

> [!IMPORTANT]
> Caso não ainda não tenhas uma conta -> https://github.com

>[!TIP]
> Quando já tiveres uma conta entra na tua conta github!

<div id="refazer"></div>

3. Configura o GIT com o teu nome e email!
    
    No terminal:
    ```bash
    git config --user.name "O teu nome"
    git config --user.email "oTeuEmail@exemplo.com"
    ```

4. Configurar o tipo de autenticação SSH (recomendado):  

    ```bash
    ssh-keygen -t ed25519 -C "teuemail@exemplo.com"
    eval "$(ssh-agent -s)"
    ssh-add ~/.ssh/id_ed25519
    cat ~/.ssh/id_ed25519.pub
    ```

    No GITHUB, vai a **Settings → SSH and GPG keys → New SSH key**

    Verifica se tudo correu bem com: 
    
    ```bash
     ssh -T git@github.com 
     ```
## Vamos começar a trabalhar com GIT!

### 1. Cria o teu Repositório local

```bash
    mkdir git_workshop
    cd git_workshop
    git init
```

### 2. Cria e faz alterações
```bash
    echo "# Bem-vindo ao meu Repositório!" > README.md
    git add README.md
    git commit -m "O meu primeiro commit!" 
```

Verifica que agora o ficheiro faz parte do histórico:
```bash
    git log --oneline
```

Fizeste o teu primeiro commit!! 

## 2. Cria o teu Repositório remoto no GitHub! 

1. Vai a [github.com/new](https://github.com/new);
2. Dá o mesmo nome do diretório que deste neste caso **git_workshop**;
3. Não adiciones README nem .gitignore, já os criaste localmente;
4. Clica em **Create repository**;
5. Copia o link **SSH** exemplo:

    ```bash
     git@github:o-teu-utilizador/git_workshop.git
    ```

## 3. Liga o teu Repositório Local ao Remoto(GitHub) via SSH 

```bash
git remote add origin git@github.com:teu-utilizador/git_workshop.git
git branch -M main
git push -u origin main
```

---

## 4. Usar Branches

```bash 
git checkout -b new_feature/nome
echo "## Olá eu sou o/a <o_teu_nome>!👋" >> README.md 
git add README.md
git commit -m "Adição do meu nome."
git push -u origin new_feature/nome  

git log --graph --oneline --decorate --all
```
---

## 5. Faz Merge no GitHub

1. No GitHub, vai à secção Pull Request, clica em **Merge pull request**  → **Confirm merge**.
2. Volta ao terminal:
    
    ```bash 
        git checkout main
        git pull
        git log --graph --oneline --decorate --all 
    ```


<br><br><br><br>


# 2ª Parte 

Agora que já criaste o teu próprio Repositório local, e conseguiste ligar esse repositório local ao remoto no GitHub. 

Vamos agora em vez de criar, vamos colaborar! 

## Requesitos: 

1. Ter uma conta no GitHub
2. Ter o GIT no teu computador configurado com nome de utilizador, email, chave ssh etc. 

### Caso não o tenhas feito:  <a href="#refazer"> aqui</a>

## 1. Acede a:

[github.com/matleitner/GIT_workshop](https://github.com/matleitner/GIT_workshop)

Existe um botão que diz **Fork**!

Depois podes clicar **Create Fork**

> [!NOTE] 
> Quando fazemos um fork basicamente estamos a "copiar" o repositório de outra pessoa neste caso GIT_workshop, para o nosso GitHub quase como se fosse nosso mas não oficialmente.


## 2. Vamos colocar o Fork que fizemos num repositório local 
1. Ainda no GitHub clica no botão verde **Code**, e clica em **SSH** e copia será algo do género:
    
    `git@github.com:<o-teu-user>/GIT_workshop.git`
    
2. Escolhe um lugar para guardar o trabalho que vais fazer, por exemplo nos Documents ou no Desktop;

3. No gestor de ficheiros do teu computador, escolhe o diretório (pasta) onde queres que o repositório vá e depois clica no botão direito e clica **Abrir no Terminal**;

3. No terminal cola à frente de `git clone` o que copiaste anteriormente:
    ```bash
    git clone git@github.com:<o-teu-user>/GIT_workshop.git
    ```

## 3. Adiciona o teu contributo ao repositório original

Agora cabe te a ti, usar a tua criatividade e adicionar um ficheiro com o teu contributo! 

> [!WARNING]
> Mas não abusem por favor ^_^

Cria um ficheiro, de texto com o teu nome por exemplo! Com o que quiseres lá dentro.

Não te esqueças, adicionar esse ficheiro ao diretório GIT_workshop para que possas utilizar o GIT.

Achas que consegues adicionar o teu novo ficheiro ao GITHUB?

 <a href="#ajuda">Vou precisar da ajuda dos universitários! </a>


## 4. Pull Request 

Agora que adicionaste o ficheiro ao repositório no **teu** GitHub, precisas de mandar as alterações para o repositório "original" que fizeste o **Fork**.

Para isso no GitHub no repositório GIT_workshop, vais ao canto superior esquerdo tens um botão **Pull Requests** clica nele! Depois **New pull request**. 

Agora se tudo correr bem encontras a verde uma mensagem **Able to merge.** e um botão **Create pull request** clica nele. Se quiseres na descrição, descreve o teu contributo! 


Mais uma vez clica **Create pull request** 
    
## Boa, conseguiste! 

Agora basta esperares que o responsável do repositório (eu) aceite o teu contributo, mais tarde volta a visitar o repositório que certamente terás a tua contribuição presente!!



(P.S. claro que depois quando acabares podes eliminar o **repositório** do teu PC)



# Ajuda

Não te esqueças dos 
<a href="#requesitos">requesitos</a>
no teu terminal deves ter algo como:

```bash 
.../GIT_workshop>git clone git@github.com/o-teu-user/GIT_workshop.git

# Aqui criaste e fizeste as tuas alterações no <nome_do_teu_ficheiro>

.../GIT_workshop>git add <nome_do_teu_ficheiro>

.../GIT_workshop>git commit -m "Mensagem do commit que queiras colocar"

.../GIT_workshop>git push -u origin main
```


