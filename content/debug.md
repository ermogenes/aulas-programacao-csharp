# Depuração (_debug_)

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/QEb9G3Hrajk)

Permite que se acompanhe a execução do programa passo-a-passo, visualizando os valores de suas variáveis e avaliando expressões.

É utilizado principalmente para investigação e correção de _bugs_.

## Configuração do VsCode

As opções do depurador ficam na aba `Run`:

![](debug000036.png)

O método `Launch` deve estar selecionado.

![](debug000062.png)

O console interno do depurador não é compatível com entrada via teclado. Devemos configurar o depurador para utilizar o terminal integrado do VsCode. Para isso, abra o arquivo de configuração `launch.json` clicando no ícone indicado:

![](debug000048.png)

Altere a opção `console` de `internalConsole` para `integratedTerminal`.

Antes:

![](debug000046.png)

Depois:

![](debug000047.png)

Suas configurações ficam salvas em `.vscode/launch.json`.

![](debug000045.png)

## Pontos de parada (_breakpoints_)

Você deve incluir pelo menos um ponto de parada para o depurador. Sem eles, seu programa executará até o final sem que você possa interagir.

Podemos adicionar _breakpoints_ clicando ao lado dos números de linha.

![](debug000038.png)

No exemplo, o depurador parará nas linhas 41, 44 e 46.

A janela `Breakpoints` permite que você veja os pontos de parada configurados:

![](debug000039.png)

Na maioria dos casos simples você pode colocar um _breakpoint_ na primeira linha do método `Main`, permitindo que você acompanhe toda a execução do programa.

![](debug000040.png)

## Iniciando a depuração

Para executar o programa em modo de depuração clique no ícone de execução:

![](debug000037.png)

A barra de status ficará vermelha:

![](debug000042.png)

Surgirá um menu de depuração no canto superior direito:

![](debug000043.png)

A janela `Variables` mostrará todas as variáveis acessíveis no ponto atual de execução, com seus valores:

![](debug000044.png)

O depurador executará até encontrar o primeiro _breakpoint_.

![](debug000041.png)

Agora você pode controlar a sequência dos próximos comandos.

## Executando trechos de código

Para ir até o próximo _breakpoint_ utilize a opção `Continue` ou pressione <kbd>F5</kbd>:

![](debug000050.png)

Para executar uma linha por vez, utilize a opção `Step Over` ou pressione <kbd>F10</kbd>:

![](debug000049.png)

As demais opções são:
* `Step Into` (<kbd>F11</kbd>): Como `Step Over`, mas entra na subrotina a ser executada.
* `Step Out` (<kbd>Shift+F11</kbd>): Como `Step Over`, mas sai da subrotina atual.
* `Restart` (<kbd>Ctrl+Shift+F5</kbd>): Reinicia a depuração.
* `Stop` (<kbd>Shift+F5</kbd>): Termina a depuração.

## Inspecionando o programa

Você pode analisar os valores atuais das variáveis de diversas maneiras.

**`Variables`**

A lista de variáveis disponíveis está em `Variables`. Você pode inclusive alterá-los diretamente utilizando a opção `Set Value`.

![](debug000059.png)

**Cursor sobre a variável, no código**

Ao passar o cursor sobre uma variável, você verá o seu valor atual.

![](debug000051.png)

**`Watches`**

A janela `Watches` permite que você crie expressões a serem avaliadas automaticamente pelo depurador.

Você pode colocar uma variável ou uma expressão contida no seu código selecionando-a e clicando na opção `Add to watch`:

![](debug000060.png)

Você também pode observar o valor de uma expressão que não existe no seu código, criando-a diretamente na janela `Watches`:

![](debug000053.png)

![](debug000054.png)

Use e abuse da depuração. Ela é a melhor amiga do programador.