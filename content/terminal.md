# Interface de linha de comando

## Terminal básico no Windows

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/3H7huG1cEQ4)

## Referência rápida de comandos de terminal

### Windows (`cmd` e `Powershell`) / Linux (`bash` ou qualquer outro)

Comando | Descrição
-- | --
`dir` (Windows) ou `ls` (Linux) | Lista o conteúdo da pasta atual (arquivos e pastas).
`cd <pasta>` | Acessa a pasta informada.
`cls` (Windows) ou `clear` (Linux) | Limpa o conteúdo da tela, facilitando a leitura.

Há vasto material sobre o assunto na Internet. você pode começar por [aqui](https://www.lucascaton.com.br/2018/01/07/comandos-para-o-terminal-windows-macos-e-linux/) e [aqui](https://linux.ime.usp.br/~lucasmmg/livecd/documentacao/documentos/terminal/Terminal_basico.html).

Veja também o [material do Prof Neri sobre o assunto](https://github.com/diegoneri/aulas-gso-1).

### `code`

Comando | Descrição
-- | --
`code` | Abre o VsCode.
`code --version` | Mostra a versão instalada do VsCode.
`code --help` | Mostra a tela de ajuda.
`code .` | Abre a pasta atual.
`code -n .` | Abre a pasta atual em uma nova janela.
`code -r .` | Abre a pasta atual na janela atual.

Referência: [https://code.visualstudio.com/docs/editor/command-line](https://code.visualstudio.com/docs/editor/command-line)

### `dotnet`

Comando | Descrição
-- | --
`dotnet --help` | Mostra a tela de ajuda.
`dotnet --version` | Mostra a versão instalada do .NET.
`dotnet new console` | Cria uma nova aplicação de console na pasta atual.
`dotnet new console -o NomeProjeto` | Cria uma nova aplicação de console em uma pasta dentro da pasta atual, com o nome indicado.
`dotnet new -l` | Lista os templates de projeto existentes.
`dotnet build` | Compila o projeto da pasta atual.
`dotnet run` | Compila e executa o projeto da pasta atual.
`dotnet list reference` | Lista os projetos aos quais o projeto atual faz referência.
`dotnet list package` | Lista os pacotes aos quais o projeto atual faz referência.
`dotnet restore` | Baixa os pacotes aos quais o projeto atual faz referência e ainda não existam localmente, bem como suas dependências.
`dotnet add package <pacote>` | Adiciona um pacote no projeto atual.
`dotnet remove package <pacote>` | Remove um pacote do projeto atual.


Referência: [https://docs.microsoft.com/pt-br/dotnet/core/tools](https://docs.microsoft.com/pt-br/dotnet/core/tools)

Principais templates de aplicação:

Template | Descrição
-- | --
`console` | Aplicações de linha de comando em console (CLI).
`classlib` | Biblioteca de classes.
`web` | Sites para a web simples.
`mvc` | Sites utilizando o padrão de desenvolvimento MVC.
`webapp` | Sites utilizando o padrão de desenvolvimento MVC, com páginas Razor.
`webapi` | Serviços web.
`winforms` | Aplicações Desktop nativas do Windows.
`wpf` | Aplicações Desktop portáveis.

Alguns pacotes notáveis:

Pacote | Descrição
-- | --
[Humanizer](https://www.nuget.org/packages/Humanizer/) | Permite gerar descrições textuais legíveis por humanos para diversos objetos.
[Figgle](https://www.nuget.org/packages/Figgle/) | Cria ASCII-Art a partir de strings.
[Noda Time](https://www.nuget.org/packages/NodaTime/) | Biblioteca avançada para manipulação de Datas e Horas no .NET.


### `git`

Comando | Descrição
-- | --
`git --help` | Mostra a tela de ajuda.
`git --version` | Mostra a versão instalada do git.
`git init` | Cria um repositório local na pasta atual.
`git clone <endereço>` | Cria um repositório local a partir de um repositório remoto.
`git add <arquivo>` | Adiciona um arquivo na lista de alterações executadas.
`git add .` | Adiciona todos os arquivos alterados na lista de alterações executadas.
`git add -i` | Adiciona arquivos interativamente na lista de alterações executadas.
`git commit -m "comentários das alterações"` | Efetiva as alterações no branch atual do repositório local.
`git push` | Envia as alterações do branch atual para o repositório remoto atual.
`git push origin master` | Envia as alterações do branch local `master` para o repositório remoto `origin`.
`git push <nome_repositorio> <nome_branch>` | Envia as alterações do branch indicado para o repositório remoto indicado.
`git remote` | Lista os repositórios remotos.
`git remote add <nome_repositorio> <endereço>` | Adiciona um repositório remoto.
`git branch` | Lista os branchs locais.
`git checkout -b <nome_branch>` | Cria um novo branch baseado no branch atual e o torna ativo.
`git checkout <nome_branch>` | Ativa um branch local existente.
`git branch -d <nome_branch>` | Remove um branch local.
`git push <nome_remote> --delete <nome_branch>` | Remove um branch remoto.
`git pull` | Atualizar o repositório local com a versão mais recente do repositório remoto.
`git merge <nome_branch>` | Mescla alterações do branch indicado no branch atual.
`git diff <nome_branch_origem> <nome_branch_destino>` | Mostra as diferenças entre dois branches.
`git log` | Mostra o histórico de alterações.
`git log --oneline` | Mostra o histórico de alterações de forma resumida, uma alteração por linha.
`git tag <descricao> <10_primeiros_caracteres_id_commit>` | Cria uma versão nomeada do código a partir de um commit existente.
`git tag <descricao> -m "comentários"` | Cria uma versão nomeada do código no commit atual, com comentários.
`git checkout -- <arquivo>` | Desfaz as alterações locais desde o último commit.
`git push origin --tags` | Envia as tags criadas para o repositório remoto.
`git clean -ndx` | Lista todos os arquivos e diretórios que não fazem parte do versionamento.
`git clean -fdx` | Exclui todos os arquivos e diretórios que não fazem parte do versionamento.
`git stash` | Adiciona as alterações na área de _stash_.
`git stash list` | Lista áreas de _stash_.
`git stash pop` | Recupera as alterações da área de _stash_.

Desfazer todas as alterações locais, voltando à situação do repositório remoto:
```
git fetch origin
git reset --hard origin/master
```

## Ajustando a aparência do seu terminal

Você pode [deixar seu terminal mais elegante](https://gist.github.com/ermogenes/106c79087327feda8227b79a7c284512) usando o Oh My Posh.
