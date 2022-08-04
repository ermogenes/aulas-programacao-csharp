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

## Tocar um sinal sonoro

`Console.Beep`

```cs
Console.Beep();
```

Para alterar a frequência e o tempo do sinal sonoro, passamos dois argumento à `Beep`. No exemplo, tocamos a nota _dó_ por 200 milésimos de segundo:

```cs
Console.Beep(1320, 200);
```

Algumas notas:

| Nota | Frequência |
| ---- | ---------- |
| Dó   | 1320       |
| Ré   | 1485       |
| Mi   | 1650       |
| Fá   | 1759       |
| Sol  | 1980       |
| Lá   | 2200       |
| Si   | 2475       |

Saiba mais [aqui](http://www.das.inpe.br/~alex/FisicadaMusica/fismus_escalas.htm), [aqui](https://docs.microsoft.com/pt-br/dotnet/api/system.console.beep?view=net-6.0), [aqui](https://pages.mtu.edu/~suits/notefreqs.html) e [aqui](https://www.codeproject.com/Tips/438519/Console-BEEP-Methods-Notation-and-Generation).

## Fazer uma pausa na execução do programa

`Thread.Sleep`

É necessário passar a duração da pausa em milésimos de segundo (use 1000 para 1 segundo).

```cs
Thread.Sleep(1000);
```

## Mudar a cor da letra

`Console.ForegroundColor`

Cores disponíveis no enumerador `System.ConsoleColor`:

| Constante     | Valor | Cor                                               |
| ------------- | ----- | ------------------------------------------------- |
| `Black`       | 0     | A cor preta.                                      |
| `Blue`        | 9     | A cor azul.                                       |
| `Cyan`        | 11    | A cor ciano (verde-azul).                         |
| `DarkBlue`    | 1     | A cor azul-escuro.                                |
| `DarkCyan`    | 3     | A cor ciano-escuro (azul escuro-verde).           |
| `DarkGray`    | 8     | A cor cinza-escuro.                               |
| `DarkGreen`   | 2     | A cor verde-escuro.                               |
| `DarkMagenta` | 5     | A cor magenta-escuro (arroxeado-escuro-vermelho). |
| `DarkRed`     | 4     | A cor vermelho-escuro.                            |
| `DarkYellow`  | 6     | A cor amarelo-escuro (ocre).                      |
| `Gray`        | 7     | A cor cinza.                                      |
| `Green`       | 10    | A cor verde.                                      |
| `Magenta`     | 13    | A cor magenta (arroxeado-vermelho).               |
| `Red`         | 12    | A cor vermelha.                                   |
| `White`       | 15    | A cor branca.                                     |
| `Yellow`      | 14    | A cor amarela.                                    |

Usando o enumerador:

```cs
Console.ForegroundColor = ConsoleColor.Red;
```

Usando o código numérico:

```cs
Console.ForegroundColor = (ConsoleColor)12;
```

## Mudar a cor do fundo

`Console.BackgroundColor`

Cores disponíveis no enumerador `System.ConsoleColor`:

Usando o enumerador:

```cs
Console.BackgroundColor = ConsoleColor.Blue;
```

Usando o código numérico:

```cs
Console.BackgroundColor = (ConsoleColor)9;
```

## Voltar para a cor padrão

`Console.ResetColor`

```cs
Console.ResetColor();
```
