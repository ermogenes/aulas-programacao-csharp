# Datas

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/KT5B9WSjehc)

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

## `System.DateOnly` e `System.TimeOnly`

O .NET 6 introduziu tipos que tratam separadamente data (como em aniversários) e hora (como em alarmes diários).

---

[Programa da vídeo-aula](https://youtu.be/KT5B9WSjehc)

```cs
using System;

namespace AulaDatas
{
    class Program
    {
        static void Main(string[] args)
        {
            // Obtendo a data do sistema
            Console.WriteLine("--- Obtendo a data do sistema");
            DateTime horaSistema = DateTime.Now;
            Console.WriteLine($"Hora do sistema: {horaSistema}");

            // Inicializando uma data específica
            Console.WriteLine("--- Inicializando uma data específica");
            DateTime decolagemApollo11 = new DateTime(1969, 07, 16, 13, 32, 00);
            string stringData = "20/07/1969 20:17:17";
            DateTime primeiroPousoLunar = Convert.ToDateTime(stringData);
            Console.WriteLine($"Decolagem Apollo 11..: {decolagemApollo11}");
            Console.WriteLine($"Pouso na Lua.........: {primeiroPousoLunar}");

            // Exibindo data/hora, curta e longa
            Console.WriteLine("--- Exibindo data/hora, curta e longa");
            string dataCurta = horaSistema.ToShortDateString();
            string dataLonga = horaSistema.ToLongDateString();
            string horaCurta = horaSistema.ToShortTimeString();
            string horaLonga = horaSistema.ToLongTimeString();
            Console.WriteLine($"Data curta: {dataCurta}");
            Console.WriteLine($"Data longa: {dataLonga}");
            Console.WriteLine($"Hora curta: {horaCurta}");
            Console.WriteLine($"Hora longa: {horaLonga}");

            // Obtendo partes de uma data
            Console.WriteLine("--- Obtendo partes de uma data");
            int ano = horaSistema.Year;
            DateTime dataSemHora = horaSistema.Date;
            int diaDaSemanaNumero = Convert.ToInt32(horaSistema.DayOfWeek);
            string diaDaSemanaTexto = horaSistema.ToString("dddd");
            Console.WriteLine($"Ano: {ano}");
            Console.WriteLine($"Data sem a hora: {dataSemHora}");
            Console.WriteLine($"Dia da semana: {diaDaSemanaNumero} => {diaDaSemanaTexto}");

            // Alterando uma data
            Console.WriteLine("--- Alterando uma data");
            DateTime vencimento = horaSistema.AddMonths(1).AddDays(1).Date;
            DateTime duasHorasAtras = horaSistema.AddHours(-2);
            Console.WriteLine($"Vencimento: {vencimento}");
            Console.WriteLine($"Duas horás atrás: {duasHorasAtras}");

            // Intervalos de tempo fixos
            Console.WriteLine("--- Intervalos de tempo fixos");
            TimeSpan tresHorasEQuinze = new TimeSpan(3, 15, 0);
            DateTime daquiHaPouco = horaSistema + tresHorasEQuinze;
            Console.WriteLine($"Daqui há pouco: {daquiHaPouco}");

            // Calculando o intervalo entre duas datas
            Console.WriteLine("--- Calculando o intervalo entre duas datas");
            TimeSpan intervaloDesdeMeiaNoite = horaSistema.TimeOfDay;
            int horasDecorridas = intervaloDesdeMeiaNoite.Hours;
            TimeSpan tempoViagemLua = primeiroPousoLunar - decolagemApollo11;
            int diasViagemLua = tempoViagemLua.Days;
            Console.WriteLine($"Horas desde 0h: {horasDecorridas} horas");
            Console.WriteLine($"A primeira viagem à lua levou {diasViagemLua} dias");
        }
    }
}
```

**Saída**:

```
C:\Users\ermogenes\Documents\DevCs\AulaDatas>dotnet run
--- Obtendo a data do sistema
Hora do sistema: 12/05/2020 19:30:33      
--- Inicializando uma data específica     
Decolagem Apollo 11..: 16/07/1969 13:32:00
Pouso na Lua.........: 20/07/1969 20:17:17
--- Exibindo data/hora, curta e longa     
Data curta: 12/05/2020
Data longa: terça-feira, 12 de maio de 2020
Hora curta: 19:30
Hora longa: 19:30:33
--- Obtendo partes de uma data
Ano: 2020
Data sem a hora: 12/05/2020 00:00:00
Dia da semana: 2 => terça-feira
--- Alterando uma data
Vencimento: 13/06/2020 00:00:00
Duas horás atrás: 12/05/2020 17:30:33
--- Intervalos de tempo fixos
Daqui há pouco: 12/05/2020 22:45:33
--- Calculando o intervalo entre duas datas
Horas desde 0h: 19 horas
A primeira viagem à lua levou 4 dias
```
