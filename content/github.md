# GitHub

Vamos utilizar o repositório gratuito GitHub para salvar nossos projetos.

## Criando sua conta

* Acesse https://github.com/ e crie sua conta.

![](000014.png)

* Guarde bem o e-mail, o nome de usuário e a senha.
* Efetue o login sempre que necessário.

## Criando um novo repositório

* Estando logado, acesse a opção `New Repository`.

![](000015.png)

* Preencha os campos a seguir:
  - `Repository name`: nome do seu projeto, deve ser único para cada usuário
  - `Description`: descrição do projeto, opcional
  - `Public/Private`: visibilidade do seu repositório
  - `Initialize this repository with a README`: marque essa opção para poder alterar o texto da página inicial
  - `Add .gitignore`: Selecione `VisualStudio` para projetos com C#

![](000016.png)

Seu repositório de projeto está criado.

![](000017.png)

## Preparando o ambiente local

* Verifique se o `git` está instalado:

```powershell
PS C:\Users\ermogenes> git --version
git version 2.22.0.windows.1
```

* Verifique se o seu usuário e e-mail estão configurados:

```powershell
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> git config user.name
Ermogenes Palacio
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> git config user.email
meu-email@meu-servidor.com
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> 
```

* Caso não esteja configurado, use os seguintes comandos para fazê-lo:

```powershell
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> git config --global user.name = "Ermogenes Palacio" 
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> git config --global user.email = "meu-email@meu-servidor.com"
```

## Abrindo o projeto localmente

* Na página inicial do seu projeto, obtenha o endereço do repositório:

![](000018.png)


* Acesse a pasta em que seu repositório será baixado (nela será criada uma nova pasta com o nome do repositório).

```powershell
PS C:\Users\ermogenes> cd desktop
PS C:\Users\ermogenes\desktop> cd aulas
PS C:\Users\ermogenes\desktop\aulas> dir
PS C:\Users\ermogenes\desktop\aulas> 
```

* Faça o download do repositório, utilizando o endereço obtido anteriormente:

```powershell
PS C:\Users\ermogenes\desktop\aulas> git clone https://github.com/ermogenes/primeiro-programa-em-cs.git
Cloning into 'primeiro-programa-em-cs'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.
PS C:\Users\ermogenes\desktop\aulas> 
```

* Verifique se os arquivos foram baixados.

```powershell
PS C:\Users\ermogenes\desktop\aulas> dir


    Diretório: C:\Users\ermogenes\desktop\aulas


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----       03/02/2020     16:14                primeiro-programa-em-cs


PS C:\Users\ermogenes\desktop\aulas> cd primeiro-programa-em-cs   
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> dir


    Diretório: C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----       03/02/2020     16:14           6352 .gitignore
-a----       03/02/2020     16:14             80 README.md


PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> 
```

* Estando na pasta raíz do repositório local, abra o projeto no Visual Studio Code:

```powershell
PS C:\Users\ermogenes\desktop\aulas\primeiro-programa-em-cs> code .
```

* Seu projeto estará aberto no VSCode.

![](000019.png)