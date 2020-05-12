# Números

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/2WdAlMvExE8)

Programa da [vídeo-aula](https://youtu.be/2WdAlMvExE8):

```cs
using System;

namespace AulaNumeros
{
    class Program
    {
        static void Main(string[] args)
        {
            // Operações com inteiros
            Console.WriteLine("--- Operações com inteiros");
            int intX = 2;
            int intY = 5;
            int intSoma = intX + intY;           // 7
            int intSubtracao = intX - intY;      // -3
            int intMultiplicacao = intX * intY;  // 10
            int intDivisao = intX / intY;        // 0 e não 0,4
            Console.WriteLine($"{intX} + {intY} = {intSoma}");
            Console.WriteLine($"{intX} - {intY} = {intSubtracao}");
            Console.WriteLine($"{intX} * {intY} = {intMultiplicacao}");
            Console.WriteLine($"{intX} / {intY} = {intDivisao}");

            // Literais em ponto flutuante
            Console.WriteLine("--- Literais em ponto flutuante");
            double a = 1;
            double b = +1;
            double c = -1;
            double d = 0.1;
            double e = .1;
            double f = 1.0;
            double g = 1e0;   // 1 * 10^0
            double h = 1d;
            Console.WriteLine($"a = {a}");
            Console.WriteLine($"b = {b}");
            Console.WriteLine($"c = {c}");
            Console.WriteLine($"d = {d}");
            Console.WriteLine($"e = {e}");
            Console.WriteLine($"f = {f}");
            Console.WriteLine($"g = {g}");
            Console.WriteLine($"h = {h}");

            // Operações com ponto flutuante: double
            Console.WriteLine("--- Operações com ponto flutuante: double");
            double doubleX = 2;
            double doubleY = 5;
            double doubleSoma = doubleX + doubleY;
            double doubleSubtracao = doubleX - doubleY;
            double doubleMultiplicacao = doubleX * doubleY;
            double doubleDivisao = doubleX / doubleY;
            Console.WriteLine($"{doubleX} + {doubleY} = {doubleSoma}");
            Console.WriteLine($"{doubleX} - {doubleY} = {doubleSubtracao}");
            Console.WriteLine($"{doubleX} * {doubleY} = {doubleMultiplicacao}");
            Console.WriteLine($"{doubleX} / {doubleY} = {doubleDivisao}");

            // Operações com ponto flutuante: decimal
            Console.WriteLine("--- Operações com ponto flutuante: decimal");
            decimal decimalX = 2;
            decimal decimalY = 5;
            decimal decimalSoma = decimalX + decimalY;
            decimal decimalSubtracao = decimalX - decimalY;
            decimal decimalMultiplicacao = decimalX * decimalY;
            decimal decimalDivisao = decimalX / decimalY;
            Console.WriteLine($"{decimalX} + {decimalY} = {decimalSoma}");
            Console.WriteLine($"{decimalX} - {decimalY} = {decimalSubtracao}");
            Console.WriteLine($"{decimalX} * {decimalY} = {decimalMultiplicacao}");
            Console.WriteLine($"{decimalX} / {decimalY} = {decimalDivisao}");

            // Formatação de números em ponto flutuante
            Console.WriteLine("-- Formatação de números em ponto flutuante");
            Console.WriteLine($"Double = {doubleDivisao} | Decimal = {decimalDivisao} -- sem formatação");
            Console.WriteLine($"Double = {doubleDivisao:N} | Decimal = {decimalDivisao:N} -- formato Número");
            Console.WriteLine($"Double = {doubleDivisao:C} | Decimal = {decimalDivisao:C} -- formato Moeda");
            Console.WriteLine($"Double = {doubleDivisao:C3} | Decimal = {decimalDivisao:C3} -- formato Moeda, 3 casas");
            Console.WriteLine($"Double = {doubleDivisao:N4} | Decimal = {decimalDivisao:N4} -- Número, 4 casas");
            Console.WriteLine($"Double = {doubleDivisao:N30} | Decimal = {decimalDivisao:N30} -- Número, 30 casas");

            // Conversões double/decimal
            Console.WriteLine("--- Conversões double/decimal");
            double doubleConversao = doubleX + Convert.ToDouble(decimalX);
            decimal decimalConversao = Convert.ToDecimal(doubleX) + decimalX;
            Console.WriteLine($"Double = {doubleConversao} | Decimal = {decimalConversao}");
            
            // Conversões com string
            Console.WriteLine("--- Conversões com string");
            double doubleString = Convert.ToDouble("5,3");
            decimal decimalString = Convert.ToDecimal("5,3");
            string stringDouble = doubleDivisao.ToString("N4");
            string stringDecimal = decimalDivisao.ToString("N4");
            Console.WriteLine($"Double = {doubleString:N4} | Decimal {decimalString:N4}");
            Console.WriteLine($"Double = {stringDouble} | Decimal {stringDecimal}");

            // Entrada via teclado
            Console.WriteLine("--- Entrada via teclado");
            Console.Write("Digite um número...: ");
            string stringDigitada = Console.ReadLine();
            double doubleDigitado = Convert.ToDouble(stringDigitada);
            decimal decimalDigitado = Convert.ToDecimal(stringDigitada);
            Console.WriteLine($"String = {stringDigitada} | Double = {doubleDigitado} | Decimal = {decimalDigitado}");
        }
    }
}
```

**Saída**:

```
C:\Users\ermogenes\Documents\DevCs\AulaNumeros>dotnet run
--- Operações com inteiros
2 + 5 = 7
2 - 5 = -3
2 * 5 = 10
2 / 5 = 0
--- Literais em ponto flutuante
a = 1
b = 1
c = -1
d = 0,1
e = 0,1
f = 1
g = 1
h = 1
--- Operações com ponto flutuante: double
2 + 5 = 7
2 - 5 = -3
2 * 5 = 10
2 / 5 = 0,4
--- Operações com ponto flutuante: decimal
2 + 5 = 7
2 - 5 = -3
2 * 5 = 10
2 / 5 = 0,4
-- Formatação de números em ponto flutuante
Double = 0,4 | Decimal = 0,4 -- sem formatação
Double = 0,40 | Decimal = 0,40 -- formato Número
Double = R$0,40 | Decimal = R$0,40 -- formato Moeda
Double = R$0,400 | Decimal = R$0,400 -- formato Moeda, 3 casas
Double = 0,4000 | Decimal = 0,4000 -- Número, 4 casas
Double = 0,400000000000000022204460492503 | Decimal = 0,400000000000000000000000000000 -- Número, 30 casas
--- Conversões double/decimal
Double = 4 | Decimal = 4
--- Conversões com string
Double = 5,3000 | Decimal 5,3000
Double = 0,4000 | Decimal 0,4000
--- Entrada via teclado
Digite um número...: 2,5
String = 2,5 | Double = 2,5 | Decimal = 2,5
```
