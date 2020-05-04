# Saída em console

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/zRzLq1zzb5M)

Comandos disponíveis na classe `System.Console`.

## Exibir um texto, sem quebrar linha

`Console.Write`

```cs
Console.Write("Primeiro texto");
Console.Write("Segundo texto");
```

Resultado:

```
Primeiro textoSegundo texto
```

## Exibir um texto, com quebra de linha no final

`Console.WriteLine`

```cs
Console.Write("Primeiro texto");
Console.WriteLine("Segundo texto");
Console.Write("Terceiro texto");
```

Resultado:

```
Primeiro textoSegundo texto
Terceiro Texto
```

## Limpar todos os textos da tela

`Console.Clear`

```cs
Console.Clear();
```

##  Tocar um sinal sonoro

`Console.Beep`

```cs
Console.Beep();
```

## Mudar a cor da letra

`Console.ForegroundColor`

Cores disponíveis no enumerador `System.ConsoleColor`:

Constante | Valor | Cor
--  | -- | --
`Black` | 0 | A cor preta.
`Blue` | 9 | A cor azul.
`Cyan` | 11 | A cor ciano (verde-azul).
`DarkBlue` | 1 | A cor azul-escuro.
`DarkCyan` | 3 | A cor ciano-escuro (azul escuro-verde).
`DarkGray` | 8 | A cor cinza-escuro.
`DarkGreen` | 2 | A cor verde-escuro.
`DarkMagenta` | 5 | A cor magenta-escuro (arroxeado-escuro-vermelho).
`DarkRed` | 4 | A cor vermelho-escuro.
`DarkYellow` | 6 | A cor amarelo-escuro (ocre).
`Gray` | 7 | A cor cinza.
`Green` | 10 | A cor verde.
`Magenta` | 13 | A cor magenta (arroxeado-vermelho).
`Red` | 12 | A cor vermelha.
`White` | 15 | A cor branca.
`Yellow` | 14 | A cor amarela.

```cs
Console.ForegroundColor = ConsoleColor.Red;
```

## Mudar a cor do fundo

`Console.BackgroundColor`

Cores disponíveis no enumerador `System.ConsoleColor`:

```cs
Console.BackgroundColor = ConsoleColor.Blue;
```

## Voltar para a cor padrão

`Console.ResetColor`

```cs
Console.ResetColor();
```
