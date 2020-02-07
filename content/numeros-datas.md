# Números e datas

## `System.Math`

Podemos efetuar diversas operações matemáticas utilizando os métodos da classe `Math`.

* `Sqrt` calcula a raíz quadrada do número.
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

## `System.DateTime` e `System.Timespan`

Trabalhar com datas e horas em C# é bastante facilitado pelo uso das classes `DateTime` e `Timespan`.

Veja o exemplo:

```cs
DateTime agora = DateTime.Now;
DateTime torresGemeas = new DateTime(2001, 9, 11, 8, 46, 0);
Console.WriteLine(agora);
Console.WriteLine(torresGemeas);
```

* `Datetime.Now` retorna a data e a hora do sistema.
* Utilizando o construtor podemos definir uma data específica, com ano, mês, dia, hora e segundos.

Também temos métodos auxiliares:

(_em breve_)


