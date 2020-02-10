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

## `System.DateTime`

Trabalhar com datas e horas em C# é bastante facilitado pelo uso das classes `DateTime`.

Veja o exemplo:

```cs
DateTime agora = DateTime.Now;
DateTime torresGemeas = new DateTime(2001, 9, 11, 8, 46, 0);
Console.WriteLine(agora);
Console.WriteLine(torresGemeas);
```

* `DateTime.Now` retorna a data e a hora do sistema.
* Utilizando o construtor podemos definir uma data específica, com ano, mês, dia, hora e segundos.

Podemos obter algumas informações interessantes:

* `Now` retorna a data e a hora atual. `Today`, somente a data.
* Use `Year`, `Month`, `Day`, `Hour`, `Minute`, `Second` e `Millisecond` para recuperar as partes componentes da data/hora.
* `Date` e `TimeOfDay` retornam somente a data ou a hora.
* Use `DayOfWeek` para saber qual o dia da semana, e `DayOfYear` para saber quantos dias a data está distante do início do ano.

```cs
DateTime agora = DateTime.Now;
Console.WriteLine(agora);
Console.WriteLine(DateTime.Today);
Console.WriteLine(agora.Day);
Console.WriteLine(agora.Month);
Console.WriteLine(agora.Year);
Console.WriteLine(agora.Hour);
Console.WriteLine(agora.Minute);
Console.WriteLine(agora.Second);
Console.WriteLine(agora.Millisecond);		
Console.WriteLine(agora.Date);
Console.WriteLine(agora.TimeOfDay);
Console.WriteLine(agora.DayOfWeek);
Console.WriteLine(agora.DayOfYear);
```

Também temos métodos auxiliares:

* Para saber quantos dias tem um mês, usamos `DaysInMonth`.
* Para saber se um ano é bissexto, `IsLeapYear`.
* Para saber se a data/hora está no período de horário de verão, `IsDaylightSavingTime`.

```cs
DateTime agora = DateTime.Now;
Console.WriteLine(agora.IsDaylightSavingTime());
Console.WriteLine(DateTime.IsLeapYear(2020));
Console.WriteLine(DateTime.DaysInMonth(2020, 2));
```

Para formatos de exibição padronizados, use `ToShortDateString` e `ToLongDateString`.

```cs
DateTime agora = DateTime.Now;
Console.WriteLine(agora.ToShortDateString());
Console.WriteLine(agora.ToLongDateString());
```

* Podemos alterar uma data somando valores individuais com `AddYear`, `AddMonth`, `AddDay`, `AddHour`, `AddMinute`, `AddSecond` e `AddMillisecond`.
* Podemos comparar duas datas com `Compare`: `-1` se a primeira é anterior, `0` se são iguais e `1` se a segunda é anterior.

```cs
DateTime agora = DateTime.Now;
DateTime amanha = DateTime.Today.AddDays(1);
Console.WriteLine(agora);
Console.WriteLine(amanha);
Console.WriteLine(DateTime.Compare(agora, amanha));
Console.WriteLine(DateTime.Compare(amanha, agora));
```

Operadores de comparação podem ser usados entre dois `DateTime`: `==`, `!=`, `<`, `>`, `<=` e `>=`.

```cs
DateTime agora = DateTime.Now;
DateTime amanha = DateTime.Today.AddDays(1);
Console.WriteLine(agora == amanha);
Console.WriteLine(amanha >= agora);
```

## `System.TimeSpan`

Para representar intervalos de tempo, utilizamos `TimeSpan`.

```cs
DateTime agora = DateTime.Now;
DateTime amanha = DateTime.Today.AddDays(1);
TimeSpan intervalo = amanha - agora;
TimeSpan tresHorasEQuinze = new TimeSpan(3, 15, 0);
Console.WriteLine(agora);
Console.WriteLine(amanha);
Console.WriteLine(intervalo);
Console.WriteLine(tresHorasEQuinze);
Console.WriteLine(agora + tresHorasEQuinze);
```
