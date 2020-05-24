# Decisão simples com `if`

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/0HPxji8lL_M)

Permite que um comando seja ou não seja executado, de acordo com uma condição.

Por exemplo, queremos implementar o seguinte algoritmo:

```
- Receba a nota da prova 1.
- Receba a nota da prova 2.
- Calcule a média das notas das duas provas.
- Se a média for abaixo de 5, então informe que o aluno foi reprovado.
- Senão, informe que o aluno foi aprovado.
```

Conseguimos resolver alguns pontos facilmente. Os comandos de entrada, por exemplo, podem ser implementados assim:

```cs
decimal p1, p2, media;

Console.Write("Nota da P1: ");
p1 = Convert.ToDecimal(Console.ReadLine());

Console.Write("Nota da P2: ");
p2 = Convert.ToDecimal(Console.ReadLine());
```
Em seguida, podemos calcular a média.

```cs
media = (p1 + p2) / 2;
```

Podemos até exibir a média (apesar do algoritmo não exigir tal passo, fazemos por facilidade ao usuário).

```cs
Console.WriteLine($"Média: {media}");
```

Agora, para exibir a mensagem final, temos duas alternativas:

```cs
Console.WriteLine("Aprovado");
```
e

```cs
 Console.WriteLine("Reprovado");
```

Precisamos de uma maneria de escolher somente um dos comandos, de acordo com a nota.

## Comando `if`

Executa comandos condicionalmente, baseado no resultado de uma expressão.

```cs
if (teste)
    comando_entao
else
    comando_senao
```

O comando representado por `comando_entao` só será executado se a expressão representada por `teste` resultar em um resultado verdadeiro (qualquer valor diferente de zero).

O comando representado por `comando_senao` só será executado se a expressão representada por `teste` resultar em um resultado falso (somente o valor zero).

Os comandos `comando_entao` e `comando_senao` são mutuamente exclusivos: se um for executado, o outro não será.

No exemplo do cálculo da média, poderíamos utilizar:

```cs
if (media >= 5)
    Console.WriteLine("Aprovado");
else
    Console.WriteLine("Reprovado");
```
### Construções possíveis

Nas imagens abaixo, `comando___` representa um comando qualquer, `Alternativa` e `alternativa___` representam uma expressão lógica.

#### `if` com `else`

Neste caso, necessitamos de dois comandos diferentes, um em caso verdadeiro e outro em caso falso.

<img src="if-else.svg" width="500">

```cs
comandoAntes;
if (Alternativa)
    comandoVerdadeiro;
else
    comandoFalso;
comandoDepois;
```

Exemplo:

Exibir se uma pessoa é menor ou maior de idade.

```cs
int idade = 74;
if (idade < 18)
    Console.WriteLine("Menor de Idade");
else
    Console.WriteLine("Maior de Idade");
```

É uma boa prática utilizar blocos sempre, mesmo que tenhamos somente um comando.

```cs
int idade = 74;
if (idade < 18)
{
    Console.WriteLine("Menor de Idade");
}
else
{
    Console.WriteLine("Maior de Idade");
}
```

#### `if` sem `else`

Neste caso, necessitamos de um comando a mais no caso verdadeiro, mas nada a fazer caso falso.

<img src="if-sem-else.svg" width="500">

```cs
comandoAntes;
if (Alternativa)
    comandoVerdadeiro;
comandoDepois;
```

Exemplo:

Exibir uma mensagem específica somente se a pessoa tiver 15 anos.

```cs
int idade = 12;
if (idade == 15)
{
    Console.WriteLine("Parabéns, debutante!");
}
```

#### `if` com `else`, utilizando blocos

Neste caso, necessitamos de mais de um comando diferente para cada um dos casos.

<img src="if-else-bloco.svg" width="500">

```cs
comandoAntes;
if (Alternativa)
{
    comandoVerdadeiro;
    comandoVerdadeiro2;
}
else
{
    comandoFalso;
    comandoFalso2;
}
comandoDepois;
```

Exemplo:

Menores de idade não recebem benefício. Maiores de idade recebem R$ 100,00 por filho.

```cs
const decimal SALARIO_BASE = 998;
const decimal BENEFICIO_POR_FILHO = 100;

decimal salario;
int idade = 42, numFilhos = 2;

if (idade < 18)
{
    salario = SALARIO_BASE;
}
else
{
    decimal beneficio = numFilhos * BENEFICIO_POR_FILHO;
    salario = SALARIO_BASE + beneficio;
}

Console.WriteLine(salario);
```

#### `if` sem `else`, utilizando blocos

<img src="if-sem-else-bloco.svg" width="500">

```cs
comandoAntes;
if (Alternativa)
{
    comandoVerdadeiro;
    comandoVerdadeiro2;
}
comandoDepois;
```

#### `else if`

Esta construção permite testar condições altamente relacionadas, uma das formas de se fazer desvio múltiplo.

<img src="if-else-if.svg">

```cs
comandoAntes;
if (alternativa1)
{
    comando1;
}
else if (alternativa2)
{
    comando2;
}
else if (alternativa3)
{
    comando3;
}
else
{
    comandoElse;
}
comandoDepois;
```

Exemplo:

Exibir se a pessoa é criança, adolescente, adulto ou idoso.

```cs
int idade = 35;
if (idade <= 12)
{
    Console.WriteLine("Criança");
}
else if (idade <= 17)
{
    Console.WriteLine("Adolescente");
}
else if (idade < 65)
{
    Console.WriteLine("Adulto");
}
else
{
    Console.WriteLine("Idoso");
}
```

#### `if`'s aninhados

Podemos criar qualquer tipo de lógica, imaginando que cada comando pode ser também outro `if`.

<img src="if-aninhado.svg" width="500">

```cs
comandoAntes;
if (alternativa1)
{
    comando1;
    if (alternativa2)
    {
        comando3;
    }
    else
    {
        comando4;
    }
    comando5;
}
else
{
    comando2;
}
comandoDepois;
```

Exemplo:

Em um jogo de _adivinha_, o usuário diz um número de 1 a 100. Se ele adivinhar, ganha o jogo. Se ele errar, dê uma pista (é maior ou é menor). Caso esteja fora da faixa, exiba uma mensagem de orientação.

```cs
int numeroMagico = 73;

int numeroDigitado;

Console.Write("Digite um número: ");
numeroDigitado = Convert.ToInt32(Console.ReadLine());

if (numeroDigitado < 1 || numeroDigitado > 100)
{
    Console.WriteLine("Número inválido. Digite um número entre 1 e 100.");
}
else
{
    if (numeroDigitado == numeroMagico)
    {
        Console.WriteLine("Você acertou!");
    }
    else
    {
        if (numeroDigitado < numeroMagico)
        {
            Console.WriteLine($"O número que você digitou é menor. Digite um número maior que {numeroDigitado}.");
        }
        else
        {
            Console.WriteLine($"O número que você digitou é maior. Digite um número menor que {numeroDigitado}.");
        }
    }
}
```

[Programa da vídeo-aula](https://youtu.be/0HPxji8lL_Ms)

```cs
using System;

namespace AulaDecisaoSimples
{
    class Program
    {
        static void Main(string[] args)
        {
            decimal valorTotal = 1000.00m;
            int quantidadeParcelas;
            string quantidadeDigitada;
            bool numeroValido;

            Console.WriteLine("-- Simulador de Financiamento --\n");

            Console.Write("Financiamento de R$1.000,00 em quantas vezes? ");

            quantidadeDigitada = Console.ReadLine();

            numeroValido = Int32.TryParse(quantidadeDigitada, out quantidadeParcelas);

            if (!numeroValido)
            {
                Console.WriteLine("Quantidade de parcelas inválida. Por favor digite um número.");
            }
            else if (quantidadeParcelas <= 0 || quantidadeParcelas > 10)
            {
                Console.WriteLine($"Não é possível parcelar em {quantidadeParcelas} vez(es).");
            }
            else
            {
                decimal valorParcela = valorTotal / quantidadeParcelas;
                Console.WriteLine($"Você pagará {quantidadeParcelas} parcela(s) fixa(s) de {valorParcela:C}.");                
            }

            Console.WriteLine("\nObrigado por utilizar nosso programa!");
        }
    }
}
```