# Variáveis, constantes e tipos de dados

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/CY6DI7dN29g)

Podemos armazenar dados na memória principal (RAM) do computador para serem tratados pelo nosso programa. Precisaremos disso para tratar entrada de dados externas ao programa, e para implementar as lógicas que resolverão os problemas que nos são apresentados.

Armazenamos valores na memória utilizando duas estruturas:

- **Variáveis**, caso os valores possam ser alterados durante a execução do programa.
- **Constantes**, caso os valores permaneçam os mesmo durante toda a vida do programa.

## Tipos de dados

Toda variável pode armazenar um **tipo** específico de informação. Esse tipo dirá quais valores são permitidos na variável (textos, números, datas, etc.).

Os tipos que permitem armazenar textos são:

| Tipo     | Classe          | Descrição                                                          |
| -------- | --------------- | ------------------------------------------------------------------ |
| `char`   | `System.Char`   | Um único caractere em codificação UTF-16, armazenado em 16 bits.   |
| `string` | `System.String` | Uma cadeia (sequência) de caracteres, cada um deles do tipo `char` |

Mais detalhes [aqui](https://docs.microsoft.com/pt-br/dotnet/api/system.string?view=netcore-3.1#definition).

Os tipos numéricos que mais utilizaremos neste curso:

| Tipo      | Classe           | Descrição                                                                                                                                                                                |
| --------- | ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `byte`    | `System.Byte`    | Número inteiro sem sinal, entre 0 e 255, armazenado em 8 bits                                                                                                                            |
| `short`   | `System.Int16`   | Número inteiro com sinal, entre -32.768 e 32.767, armazenado em 16 bits                                                                                                                  |
| `int`     | `System.Int32`   | Número inteiro com sinal, entre -2.147.483.648 e 2.147.483.647, armazenado em 32 bits                                                                                                    |
| `long`    | `System.Int64`   | Número inteiro com sinal, entre -9.223.372.036.854.775.808 e 9.223.372.036.854.775.807, armazenado em 64 bits                                                                            |
| `float`  | `System.Single`  | Número real (com casas decimais) em ponto flutuante, entre -3,4 × 10<sup>38</sup> e +3,4 × 10<sup>38</sup>, com precisão de 6 a 9 dígitos, armazenado em 4 bytes.                         |
| `double`  | `System.Double`  | Número real (com casas decimais) em ponto flutuante, entre -1,7 × 10<sup>308</sup> e +1,7 × 10<sup>308</sup>, com precisão de 15 a 17 dígitos, armazenado em 8 bytes.                         |
| `decimal` | `System.Decimal` | Número real (com casas decimais) em ponto flutuante de alta precisão, entre ±1,0 x 10<sup>-28</sup> e ±7,9228 x 10<sup>28</sup>, com precisão de 28 a 29 dígitos, armazenado em 16 bytes |

Mais detalhes sobre os tipos numéricos [aqui](https://docs.microsoft.com/pt-br/dotnet/standard/numerics) e [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/builtin-types/integral-numeric-types).

Utilizaremos também um tipo lógico:

| Tipo   | Classe           | Descrição                                                                             |
| ------ | ---------------- | ------------------------------------------------------------------------------------- |
| `bool` | `System.Boolean` | Armazena valores lógicos VERDADEIRO (`true`) e FALSO (`false`), armazenado em 32 bits |

Mais detalhes [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/builtin-types/bool).

## Declarando variáveis

Uma variável deve ser declarada indicando seu tipo, seu nome e, opcionalmente, um valor inicial.

Exemplos:

Uma variável inteira chamada `idade` com o valor inicial `17`:

```cs
int idade = 17;
```

Uma variável decimal chamada `salario` sem valor inicial:

```cs
decimal salario;
```

Uma variável _string_ chamada `nome` com o valor inicial `Maria Aparecida dos Santos`;

```cs
string nome = "Maria Aparecida dos Santos";
```

Uma variável _booleana_ chamada `possuiCnh` com o valor inicial `true`:

```cs
bool possuiCnh = true;
```

## Utilizando variáveis

Podemos gravar um valor em uma variável assim:

```cs
string mensagem;

mensagem = "Pressione uma tecla para continuar...";
```

Esse processo é chamado de _atribuição_.

Podemos utilizar essa variável em outra parte do programa:

```cs
Console.WriteLine(mensagem); // Exibe o valor armazenado
```

## Gravando entrada via teclado em variáveis

Podemos utiliza a atribuição para ler o valor digitado pelo usuário em uma variável _string_:

```cs
string valorDigitado = Console.ReadLine()!;
```

Porém, para receber valores numéricos, precisamos utilizar um método de conversão (`Parse`) da classe adequada:

```cs
int idadeDigitada = Int32.Parse(valorDigitado);
```

ou então, utilizar a classe `System.Convert`:

```cs
int idadeDigitada = Convert.ToInt32(valorDigitado);
```

ou ainda, utilizando `TryParse`, que permite avaliar se a conversão ocorreu com sucesso:

```cs
int idadeDigitada;
bool convertidoComSucesso = Int32.TryParse(valorDigitado, out idadeDigitada);
```

## Conversão explícita (_typecast_)

Podemos forçar a leitura de um valor de um tipo como se fosse de outro. Muitas vezes esse processo pode substituir uma conversão, porém é recomendado somente quando não há possibilidade de erro de conversão.

```cs
int x = 1, y = 2;
double quociente;
quociente = x / y;                 // resulta em 0
quociente = (double)x / (double)y; // resulta em 0.5

double a = 2.6, b = 2;
double quocienteInteiro;
quocienteInteiro = a / b;         // resulta em 1.3
quocienteInteiro = (int)(a / b);  // resulta em 1

int codigoAscii = (int)'A';       // resulta em 65
char caractere  = (char)66;       // resulta em 'B'
```

## Constantes

São criadas e acessadas da mesma maneira que as variáveis utilizando a palavra-chave `const`, porém só podem ter seu valor atribuído na declaração. Depois disso são imutáveis.

```cs
const double NumeroPiAproximado = 3.1416;
```

## Convenção de nomenclatura

Variáveis devem ser nomeadas utilizando caracteres alfanuméricos ou `_`, desde que não iniciando em numeral.

Há uma [lista de palavras-chave que são reservadas](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/) pela linguagem. Caso seja necessário criar uma variável com o mesmo nome de uma palavra-chave reservada, inicie o nome com `@` (por exemplo, `int @base = 2; @base++;`).

Utilizaremos `camelCase` para variáveis e `PascalCase` para constantes.

Mais detalhes [aqui](https://pt.wikipedia.org/wiki/CamelCase) e [aqui](https://medium.com/better-programming/string-case-styles-camel-pascal-snake-and-kebab-case-981407998841).
