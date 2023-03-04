# Cola (Cheatsheet) do processo para criação de repo com programa C#

## Criar o repositório remoto

- Criar um repositório em https://github.com/, na opção _new repository_.
- Colocar o nome e a descrição.
- Deixar público.
- Adicionar o README.
- Adicionar o `.gitignore` do tipo _VisualStudio_.
- Não adicionar uma licença.

Copiar o URL de clonagem na opção _Code_ > _Clone (HTTPS)_.

## Clonar o repositório no computador local

- Abra o terminal (Prompt de Comando).
- Acesse a pasta onde você guardará seus arquivos (ex. pasta _Documents_). Use os comandos `cd` e `dir` para navegar.
- Faça a clonagem do repositório usando a URL copiada:
```
git clone URL-COPIADA
```
- Será criada uma pasta com o nome do seu repositório. Verifique usando `dir`.
- Acesse a pasta usando `cd`.
- Verifique se você está na pasta certa usando `git status`. Se aparecer `not a git repository` você não está na pasta certa.
- Abra seu projeto no VsCode usando `code .`.

## Configurar o git

- Caso outro aluno tenha feito antes no mesmo computador, digite o comando a seguir para deslogar:
```
cmdkey /delete LegacyGeneric:target=git:https://github.com
```

- Altere seu nome e email.
```
git config --global user.name "Meu Nome" 
git config --global user.email "meu-email@meu-servidor.com"
```

## Escreva seu programa

- No VsCode, com o repositório aberto, abra um terminal usando _Terminal_ > _New Terminal_.
- Crie um projeto C# em branco usando `dotnet new console`.
- Faça o programa desejado e salve usando CTRL+S.
- Execute e teste usando `dotnet run`.

## Guardando a versão localmente

Use `git status` a qualquer momento para entender a situação atual.

- Adicione todas as alterações à versão a ser guardada usando `git add .`.
- Efetive as alterações usando `git commit -m "xxx"`. Troque `xxx` por uma mensagem explicando o que foi alterado nesta versão.

Você pode repetir esse processo quantas vezes quiser.

## Enviando as alterações para o repositório remoto

- Envie todas as versões locais para a nuvem usando `git push`.
- Clique em _Sign in with your browser_ na janela do GitHub que aparecer.

![](lousa_20230303_215634_github.jpg)