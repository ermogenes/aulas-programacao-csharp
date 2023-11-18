# Publicação

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/k_pH9sWxyTc)

Para publicar a versão atual do projeto use:

```
dotnet publish -c Release
```

Será criada uma pasta em `bin\Release\netcoreapp3.1\publish` com o conteúdo a ser distribuído.

Para executar, acessa essa pasta e digite:

```
dotnet NomeDoProjeto.dll
```

No Windows você pode digitar somente `NomeDoProjeto`, ou dar duplo clique arquivo `.exe`.

Essa versão será portátil, ou seja, poderá ser executada em qualquer sistema operacional que suporte .NET, como Windows, Linux, MacOS, etc. desde que instalado o .NET Core Runtime.

# Distribuição

Uma maneira de distribuir seu projeto é criando um site para que se possa fazer o download. Podemos fazer isso utilizando o GitHub Pages.

* Crie um `.zip` com o conteúdo da pasta `publish`.
* Salve esse arquivo em uma pasta `dist`, na raiz do seu projeto.
* Escreva um arquivo README bacana, incluindo link de download (apontando para o `.zip` em `dist`).
* Publique como um site usando o GitHub Pages.

## GitHub Pages

Entre em _Settings_:

![](publish000066.png)

Ative o GitHub Pages para a _branch_ `Master`:

![](publish000067.png)

Será exibido um link para seu site. Guarde esse link.

![](publish000077.png)

Escolha um tema:

![](publish000068.png)

Salve.

![](publish000069.png)

Será feito um _commit_ que alterará sua página inicial. Pode ignorar. Volte à página inicial.

![](publish000070.png)

Edite a descrição para incluir o link:

![](publish000071.png)

![](publish000072.png)

Ficará assim:

![](publish000073.png)

**Altere o arquivo `README.md` livremente. Ele será convertido para HTML e será sua _home-page_**

Você pode divulgar somente o link do seu site, sem que a pessoa precise conhecer o GitHub.

## Integração Contínua

Você também pode usar uma ação de integração contínua do GitHub para publicação automática.

Exemplo:

Crie um arquivo em `.github\workflows\dotnet.yml` com o seguinte conteúdo:

```yaml
name: .NET

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

permissions: write-all

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - name: Get files
      uses: actions/checkout@v3

    - name: Setup .NET
      uses: actions/setup-dotnet@v3
      with:
        dotnet-version: 6.0.x

    - name: Restore
      run: dotnet restore

    - name: Build
      run: dotnet build --no-restore -o /home/runner/work/output
      
    - name: Zip
      run: cd /home/runner/work/output/ && zip ${{ github.event.repository.name }}.zip *.dll

    - name: Release
      uses: "marvinpinto/action-automatic-releases@latest"
      with:
        repo_token: "${{ secrets.GITHUB_TOKEN }}"
        automatic_release_tag: "latest"
        prerelease: false
        files: |
          /home/runner/work/output/*.zip
```

A cada commit, um arquivo `.zip` será disponibilizado na seção _Releases_ do seu repositório.

## Projeto criado na vídeo-aula

https://ermogenes.github.io/ObrigadoDevCSharp/
