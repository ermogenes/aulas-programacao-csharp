# Operações lógicas

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

## Operadores lógicos (booleanos)

Operador | Descrição
-- | -- 
`!` | Negação lógica (troca entre `true` e `false`)
`&&` | "E" lógico (`true` se ambos `true`, senão `false`)
`\|\|` | "OU" lógico (`false` se ambos `false`, senão `true`)
`^` | "OU EXCLUSIVO" lógico (`true` se somente um valor é `true`, senão `false`)

Tabela-verdade:

`x` | `y` | `!x` | `x && y` | `x \|\| y` | `x ^ y`
-- | -- | -- | -- | -- | --
`false` | `false` | `true` | `false` | `false` | `false`
`false` | `true` | `true` | `false` | `true` | `true`
`true` | `false` | `false` | `false` | `true` | `true`
`true` | `true` | `false` | `true` | `true` | `false`

