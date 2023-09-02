# Operações

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/rLvBeB8Qsmc)

Podemos efetuar processamentos sobre expressões utilizando operadores. 

Por exemplo: gostaríamos de solicitar ao computador que execute um cálculo.

```cs
int resultado = 375 * 472;
Console.WriteLine(resultado);
```

O computador calculará a expressão `375 * 472` e armazenará na variável `resultado` (valor `177000`), que será então exibida no console.

Podemos utilizar outras variáveis na expressão:

```cs
decimal precoUnitario = 25.30;
int quantidade = 12;
decimal valorDesconto = 50.00;
decimal valorTotal = (precoUnitario * quantidade) - valorDesconto;
```

## Operadores aritméticos

Operador | Descrição | Exemplo | Resultado
-- | -- | -- | --
`+` | Soma | `1 + 3` | `4`
`-` | Subtração | `2 - 5` | `-3`
`*` | Multiplicação | `3 * 4` | `12`
`/` | Divisão | `7 / 2` | `3`
`%` | Resto da divisão | `7 % 2` | `1`

Os operadores `/` e `%` utilizam divisão inteira ou real conforme os valores de entrada.

## `System.Math`

Podemos efetuar diversas operações matemáticas utilizando os métodos da classe `Math`.

* `Sqrt` calcula a [raiz quadrada](https://www.youtube.com/watch?v=AHQxP2G0QTQ) do número.
* `Pow` retorna um número elevado à uma potência especificada.
* `Sin`, `Cos` e `Tan` calculam seno, cosseno e tangente de um número.
* `Log` retorna o logaritmo de um número em uma determinada base.
* `Max` e `Min` retornam o maior (ou o menor) número entre dois números informados.
* `Round` arredonda um número decimal para o inteiro mais próximo, ou para a quantidade de casas decimais informadas.
* `Abs` retorna o valor absoluto de um número (i.e. "retira" o sinal).
* `Sign` avalia o sinal de um número retornando `-1` se negativo, `0` se zero e `1` se positivo.

Use `Math.PI` para obter o valor da constante π (pi).

Exemplos:

```cs
Console.WriteLine(Math.Sqrt(2));           // 1,4142135623730951
Console.WriteLine(Math.Pow(2, 3));         // 8
Console.WriteLine(Math.PI);                // 3,141592653589793
Console.WriteLine(Math.Sin(0));            // 0
Console.WriteLine(Math.Cos(0));            // 1
Console.WriteLine(Math.Tan(0));            // 0
Console.WriteLine(Math.Log(2, 10));        // 0,30102999566398114
Console.WriteLine(Math.Max(2, 7));         // 7
Console.WriteLine(Math.Min(2, 7));         // 2
Console.WriteLine(Math.Round(2.45667));    // 2
Console.WriteLine(Math.Round(2.45667, 3)); // 2,457
Console.WriteLine(Math.Abs(-35));          // 35
Console.WriteLine(Math.Abs(35));           // 35
Console.WriteLine(Math.Sign(-17));         // -1
Console.WriteLine(Math.Sign(0));           // 0
Console.WriteLine(Math.Sign(17));          // 1
```

Programa da [vídeo-aula](https://youtu.be/2WdAlMvExE8):

```cs
using System;

namespace AulaOperacoes
{
    class Program
    {
        static void Main(string[] args)
        {
            // Operadores aritméticos
            Console.WriteLine("--- Operadores aritméticos");
            double x = 5;
            double y = -3;
            double soma = x + y;
            double diferenca = x - y;
            double produto = x * y;
            double quociente = x / y;
            Console.WriteLine($"{x} + {y} = {soma}");
            Console.WriteLine($"{x} - {y} = {diferenca}");
            Console.WriteLine($"{x} * {y} = {produto}");
            Console.WriteLine($"{x} / {y} = {quociente}");

            // Precedência
            Console.WriteLine("--- Precedência");
            double n1 = 2, n2 = 3, n3 = 1;
            double r1 = n1 * n2 + n3;
            double r2 = n1 * (n2 + n3);
            double r3 = (n1 * n2) + n3;
            double r4 = ((n1 * n2) + n3) / n1;
            Console.WriteLine($"{n1} * {n2} + {n3} = {r1}");
            Console.WriteLine($"{n1} * ({n2} + {n3}) = {r2}");
            Console.WriteLine($"({n1} * {n2}) + {n3} = {r3}");
            Console.WriteLine($"(({n1} * {n2}) + {n3}) / {n1} = {r4}");

            // Divisão inteira
            Console.WriteLine("--- Divisão inteira");
            int a = 7;
            int b = 2;
            int quocienteInteiro = a / b;
            int restoInteiro = a % b;       // % = módulo ou resto
            Console.WriteLine($"{a} / {b} = {quocienteInteiro}");
            Console.WriteLine($"{a} % {b} = {restoInteiro}");

            // Funções matemáticas
            double doisAoCubo = Math.Pow(2, 3);   // 2³ = 8 ==> 2 * 2 * 2
            double raizQuadradaDeDois = Math.Sqrt(2); // Square Root, √2 = 1.41...
            Console.WriteLine($"2³ = {doisAoCubo}");
            Console.WriteLine($"√2 = {raizQuadradaDeDois}");

            // Funções trigonométricas
            Console.WriteLine("--- Funções trigonométricas");
            double pi = Math.PI;                           // 3,14...
            double seno30 = Math.Sin(30 * pi / 180);       // 1/2
            double cosseno60 = Math.Cos(60 * pi / 180);    // 1/2
            double tangente45 = Math.Tan(45 * pi / 180);    // 1
            Console.WriteLine($"π = {pi}");
            Console.WriteLine($"seno de 30° = {seno30}");
            Console.WriteLine($"cosseno de 60° = {cosseno60}");
            Console.WriteLine($"tangente de 45° = {tangente45}");

            // Arredondamento
            Console.WriteLine("--- Arredondamento");
            double piArredondado6 = Math.Round(pi, 6);
            double piArredondado2 = Math.Round(pi, 2);
            double piArredondado0 = Math.Round(pi, 0);
            Console.WriteLine($"π com 6 casas = {piArredondado6:N10}");
            Console.WriteLine($"π com 2 casas = {piArredondado2:N10}");
            Console.WriteLine($"π com 0 casas = {piArredondado0:N10}");
        }
    }
}
```

**Saída**:

```
C:\Users\ermogenes\Documents\DevCs\AulaOperacoes>dotnet run
--- Operadores aritméticos
5 + -3 = 2
5 - -3 = 8
5 * -3 = -15
5 / -3 = -1,6666666666666667
--- Precedência
2 * 3 + 1 = 7
2 * (3 + 1) = 8
(2 * 3) + 1 = 7
((2 * 3) + 1) / 2 = 3,5
--- Divisão inteira
7 / 2 = 3
7 % 2 = 1
2³ = 8
V2 = 1,4142135623730951
--- Funções trigonométricas
p = 3,141592653589793
seno de 30° = 0,49999999999999994
cosseno de 60° = 0,5000000000000001
tangente de 45° = 0,9999999999999999
--- Arredondamento
p com 6 casas = 3,1415930000
p com 2 casas = 3,1400000000
p com 0 casas = 3,0000000000
```

## Operadores unários

Operador | Descrição
-- | --
`+` | Sinal "positivo"
`-` | Sinal "negativo"
`++` | Incremento
`--` | Decremento

* Utilize os sinais para criar números positivos ou negativos (ex. `-5` para o número _cinco negativo_) ou para retornar o oposto de um número (se `v1` vale `-2`, `-v1` vale `2`).
* Os operadores de incremento e decremento somam/diminuem em uma unidade o valor da expressão (`++5` vale `6`). Se usados depois da expressão, incrementam somente após a utilização do seu valor (veja exemplos [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/operators/arithmetic-operators#increment-operator-)).

Mais detalhes sobre os (muitos) outros operadores da linguagem C# [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/operators/).
