# Variáveis, constantes e tipos de dados

<a href="https://youtu.be/CY6DI7dN29g"><img src="https://img.youtube.com/vi/CY6DI7dN29g/maxresdefault.jpg" width=320 alt="Dev C#" /></a>

Podemos armazenar dados na memória principal (RAM) do computador para serem tratados pelo nosso programa. Precisaremos disso para tratar entrada de dados externas ao programa, e para implementar as lógicas que resolverão os problemas que nos são apresentados.

Armazenamos valores na memória utilizando duas estruturas:

* **Variáveis**, caso os valores possam ser alterados durante a execução do programa.
* **Constantes**, caso os valores permaneçam os mesmo durante toda a vida do programa.

## Tipos de dados

Toda variável pode armazenar um **tipo** específico de informação. Esse tipo dirá quais valores são permitidos na variável (textos, números, datas, etc.).

Os tipos que permitem armazenar textos são:

Tipo | Classe | Descrição
-- | -- | --
`char` | `System.Char` | Um único caractere em codificação UTF-16, armazenado em 16 bits.
`string` | `System.String` | Uma cadeia (sequência) de caracteres, cada um deles do tipo `char`

Mais detalhes [aqui](https://docs.microsoft.com/pt-br/dotnet/api/system.string?view=netcore-3.1#definition).

Os tipos numéricos que mais utilizaremos neste curso:

Tipo | Classe | Descrição
-- | -- | --
`int` | `System.Int32` | Número inteiro com sinal, entre -2.147.483.648 a 2.147.483.647, armazenado em 32 bits 
`decimal` | `System.Decimal` | Número real (com casas decimais) em ponto flutuante de alta precisão, entre ±1,0 x 10<sup>-28</sup> e ±7,9228 x 10<sup>28</sup>, com precisão de 28 a 29 dígitos, armazenado em 16 bytes

Mais detalhes sobre os tipos numéricos [aqui](https://docs.microsoft.com/pt-br/dotnet/standard/numerics) e [aqui](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/builtin-types/integral-numeric-types).

Utilizaremos também um tipo lógico:

Tipo | Classe | Descrição
-- | -- | --
`bool` | `System.Boolean` | Armazena valores lógicos VERDADEIRO (`true`) e FALSO (`false`), armazenado em 32 bits

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
string valorDigitado = Console.ReadLine();
```

Porém, para receber valores numéricos, precisamos utilizar um método de conversão (`Parse`) da classe adequada:

```cs
int idadeDigitada = Int32.Parse(valorDigitado);
```

ou então, utilizar a classe `System.Convert`:

```cs
int idadeDigitada = Convert.ToInt32(valorDigitado);
```

## Constantes

São criadas e acessadas da mesma maneira que as variáveis utilizando a palavra-chave `const`, porém só podem ter seu valor atribuído na declaração. Depois disso são imutáveis.

```cs
const decimal NumeroPiAproximado = 3.1416;
```

## Convenção de nomenclatura

Utilizaremos `camelCase` para variáveis e `PascalCase` para constantes.

Mais detalhes [aqui](https://pt.wikipedia.org/wiki/CamelCase) e [aqui](https://medium.com/better-programming/string-case-styles-camel-pascal-snake-and-kebab-case-981407998841).
