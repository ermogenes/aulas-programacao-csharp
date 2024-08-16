# Usando o Visual Studio Code

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/mOtSc3SbavY)

## Tela inicial

![](000003.png)

## Como abrir uma pasta

**Método 1**: Pelo explorador

![](000005.png)

**Método 2**: Pelo menu 'Abrir'

![](000006.png)

**Método 3**: Pelo menu de contexto do Windows

![](000007.png)

**Método 4**: Pelo terminal do Windows

![](000008.png)

**Método 5**: Pelo terminal do VsCode

```powershell
code .
```

Para forçar a abrir na mesma janela

```powershell
code -r .
```

Para forçar a abrir em uma nova janela

```powershell
code -n .
```

## Como utilizar o terminal integrado

![](000009.png)

![](000010.png)

## Como navegar entre arquivos na pasta aberta

Através da aba `Explorer`

![](000011.png)

## Como instalar extensões

Através da aba `Extensions`

![](000004.png)

Algumas extensões notáveis:

- Pacote de Idioma Português Brasileiro - `ms-ceintl.vscode-language-pack-pt-br`
- C# Dev Kit - `ms-dotnettools.csdevkit` - kit de extensões oficiais da Microsoft para C#
    - C# - `ms-dotnettools.csharp` - extensão oficial da Microsoft para C#
    - .NET Install Tool - `ms-dotnettools.vscode-dotnet-runtime` - extensão para gerenciamento das SDK's
- Dracula Official - `dracula-theme.theme-dracula` - Tema Dracula [https://draculatheme.com/](https://draculatheme.com/)
- Material Icon Theme - `pkief.material-icon-theme` - Pacote de ícones para diferentes tipos de arquivos
- Power Mode - `hoovercj.vscode-power-mode` - Efeitos ao digitar

## Configurando o C# Dev Kit

O VS Code estará no modo restrito. Para resolver:

1. Clique em _Manage_

![](000101.png)

2. Clique em _Trust_

![](000102.png)

_Com isso, você diz ao VSCode que esta pasta é segura para seus artefatos_

3. As extensões serão automaticamente atualizadas (_Installing_)

![](000103.png)

4. Clique em _Reload Required_

![](000104.png)

5. Aguarde alguns instantes e a instalação será concluída

![](000105.png)

6. Em algumas situações, clique em _Restart Extensions_

![](000108.png)

### Caso o _Manage_ esteja indisponível

Através da Aba `Extensions`

1. Digite `dev c#`
1. Clique no cadeado que aparece em `C# Dev Kit`
1. CLique em _Trust_

![](000106.png)

## Desabilite o _Auto Save_

Menu _File_ --> Desmarque _Auto Save_

![](000107.png)

## Como mudar a língua do VsCode para português (pt-br)

Dentro do VsCode, pressione `CTRL+SHIFT+P` (ou `F1`), digite `Configure Display Language` e confirme.

![](000034.png)

Caso não apareça `pt-br` na lista, escolha `Install Additional Languages...`:

![](000036.png)

Selecione a língua desejada e clique em `Install`.

![](000037.png)

Surgirá uma notificação avisando que o VsCode será reiniciado. Confirme.

![](000038.png)
