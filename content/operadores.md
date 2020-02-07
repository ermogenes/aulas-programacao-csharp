# Operadores

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
`%` | Resto da divisão | `7 / 2` | `1`

Os operadores `/` e `%` utilizam divisão inteira ou real conforme os valores de entrada.

## Operadores unários

Operador | Descrição
-- | --
`+` | Sinal "positivo"
`-` | Sinal "negativo"
`++` | Incremento
`--` | Decremento

* Utilize os sinais para criar números positivos ou negativos (ex. `-5` para o número _cinco negativo_) ou para retornar o oposto de um número (se `v1` vale `-2`, `-v1` vale `2`).
* Os operadores de incremento e decremento somam/diminuem em uma unidade o valor da expressão (`++5` vale `6`). Se usados depois da expressão, incrementam somente após a utilização do seu valor (veja exemplos [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/operators/arithmetic-operators#increment-operator-)).

## Operadores lógicos (booleanos)

Operador | Descrição
-- | -- 
`!` | Negação lógica (troca entre `true` e `false`)
`&&` | "E" lógico (`true` se ambos `true`, senão `false`)
`||` | "OU" lógico (`false` se ambos `false`, senão `true`)
`^` | "OU EXCLUSIVO" lógico (`true` se somente um valor é `true`, senão `false`)

Tabela-verdade:

`x` | `y` | `!x` | `x && y` | `x \|\| y` | `x ^ y`
-- | -- | -- | -- | -- | --
`false` | `false` | `true` | `false` | `false` | `false`
`false` | `true` | `true` | `false` | `true` | `true`
`true` | `false` | `false` | `false` | `true` | `true`
`true` | `true` | `false` | `true` | `true` | `false`

## Operadores de comparação

Comparam dois valores e retornam um resultado booleano.

Operador | Descrição | Exemplo
-- | -- | -- 
`==` | Igual a | `7.2 == -3` retorna `false`
`!=` | Diferente de | `7.2 != -3` retorna `true`
`<` | Menor que | `7.2 < -3` retorna `false`
`>` | Maior que | `7.2 > -3` retorna `true`
`<=` | Menor ou igual a | `5 <= 5` retorna `true`
`>=` | Maior ou igual a | `4 >= 5` retorna `false`

Mais detalhes sobre os (muitos) outros operadores da linguagem C# [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/operators/).