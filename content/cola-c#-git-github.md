# Cola (Cheatsheet) do processo para criação de repo com programa C#

## Criar o repositório remoto

- Acessar https://github.com/ e fazer o login (_Sign In_).
- Criar um repositório usando a opção _new repository_.
- Colocar o nome (obrigatório) e a descrição (opcional).
- Deixar público.
- Adicionar o README.
- Adicionar o `.gitignore` do tipo _VisualStudio_.
- Não adicionar uma licença.

Copiar o URL de clonagem na opção _Code_ > _Clone (HTTPS)_.

_Obs.: Mantenha a janela do github aberta para facilitar o processo de envio das alterações locais para o github (último passo desta cola)._

## Clonar o repositório no computador local

- Abra o VsCode.
- Vá em _File_ > _ Open Folder_.
- Acesse a pasta onde você guardará seus arquivos (ex. pasta _Documentos_). Acesse a sua pasta de trabalho (ex. `Aula PC1`). Se não existir, crie-a antes de acessar.
- Abra o terminal integrado usando _Terminal_ > _New Terminal_ (ou <kbd>Ctrl</kbd>+<kbd>'</kbd>).
- Faça a clonagem do repositório usando a URL copiada:
```
git clone URL-COPIADA
```
- Será criada uma pasta com o nome do seu repositório.
- Abra a pasta criada, usando _File_ > _ Open Folder_ (_Arquivo_ > _Abrir Pasta..._).
- Verifique se você está na pasta certa usando `git status`. Se aparecer `not a git repository` você não está na pasta certa, portanto repita o item anterior.

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

- Configure o acesso à rede via _proxy_ (**somente se estiver presencialmente na Etec Adolpho Berezin**):
```
git config --global http.proxy http://etecadolphoberezin@17.1.0.1:3128
```

## Escreva seu programa

- No VsCode, com o repositório aberto, abra um terminal usando _Terminal_ > _New Terminal_.
- Crie um projeto C# em branco usando `dotnet new console`.
- Faça o programa desejado e salve usando <kbd>Ctrl</kbd>+<kbd>S</kbd>.
- Execute e teste usando `dotnet run`.

## Guardando a versão localmente

Use `git status` a qualquer momento para entender a situação atual.

- Adicione todas as alterações à versão a ser guardada usando `git add .`.
- Efetive as alterações usando `git commit -m "xxx"`. Troque `xxx` por uma mensagem explicando o que foi alterado nesta versão.

Você pode repetir esse processo quantas vezes quiser.

## Enviando as alterações para o repositório remoto

- Envie todas as versões locais para a nuvem usando `git push`.
- Clique em _Sign in with your browser_ na janela do GitHub que aparecer (é um botão azul).

![](lousa_20230303_215634_github.jpg)
