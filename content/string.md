# Trabalhando com strings

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/bAfoJV-jc74)

## O básico

Uma _string_ é uma cadeia (sequência, arranjo) de [caracteres individuais](#tipo-char). Por exemplo, a string `Etec` é formada pelos caracteres `E`, `t`, `e` e `c`. No .NET, por padrão, é utilizada a codificação UTF-16.

Para definir uma string em C# utilizamos as aspas duplas (`"`).

Você já conheceu as strings quando estudou o comando `Console.WriteLine`:

```cs
Console.WriteLine("Etec Adolpho Berezin");
```

Nesse exemplo, a string é definida em `"Etec Adolpho Berezin"` e passada como argumento para o método `Console.WriteLine`.

Podemos armazenar uma string em memória utilizando variáveis do tipo `string`:

```cs
string nome = "Ermogenes";
string sobrenome = "Palacio";
```

## Concatenação

Digamos que agora queremos uma variável contendo o nome completo. Precisamos instruir o computador a _juntar_ os conteúdos das variáveis. Esse processo pode ser feito de várias maneiras. Vejamos:

- Concatenação via operador `+`

```cs
string nomeCompleto = nome + " " + sobrenome;
```

- Concatenação via método `Concat`

```cs
string nomeCompleto = String.Concat(nome, " ", sobrenome);
```

- Formatação de composição

```cs
string nomeCompleto = String.Format("{0} {1}", nome, sobrenome);
```

- Interpolação

```cs
string nomeCompleto = $"{nome} {sobrenome}";
```

- Objeto auxiliar (_Buffer_)

```cs
using System.Text;

// ...

StringBuilder nomeCompletoBuffer = new();

nomeCompletoBuffer.Append(nome);
nomeCompletoBuffer.AppendFormat(" {0}", sobrenome);

string nomeCompleto = nomeCompletoBuffer.ToString();
```

## Interpolação e formatação de composição

Podemos alinhar as strings ao interpolar, bem como indicar algumas formatações simples nos valores (chamadas de [formatação de composição](https://docs.microsoft.com/pt-br/dotnet/standard/base-types/composite-formatting)).

Sintaxe:

```
{expressão,alinhamento:formatação}
```

Alinhamentos:

| Entrada | `alinhamento` | Saída        | Explicação                                                    |
| ------- | ------------- | ------------ | ------------------------------------------------------------- |
| `abc`   | `10`          | `•••••••abc` | A saída terá 10 caracteres, com a entrada alinhada à direita  |
| `abc`   | `-10`         | `abc•••••••` | A saída terá 10 caracteres, com a entrada alinhada à esquerda |

Caso o valor seja maior do que o tamanho especificado, o alinhamento é ignorado.

Formatações:

| Entrada  | `formatação` | Saída         | Explicação                                                                          |
| -------- | ------------ | ------------- | ----------------------------------------------------------------------------------- |
| `2124.5` | `C`          | `R$ 2.124,50` | Formatação de moeda, na cultura atual do sistema operacional                        |
| `2124.5` | `N4`         | `2.124,5000`  | Saída numérica formatada como número da cultura atual, com 4 casas decimais         |
| `0,3982` | `P1`         | `39,8 %`      | Saída numérica multiplicada por 100, com uma casa decimal, seguida do caractere `%` |

## Conversão para string

Todos os objetos de C# possuem um método para conversão do seu valor em string, chamado `.ToString()`. Caso não haja uma representação humanamente legível adequada, será retornado o tipo do objeto.

Cada tipo pode disponibilizar parametrizações para personalizar a saída. Muitos deles (mas nem todos) aceitam a formatação de composição.

```cs
192.ToString("N4") // Retorna 192,0000
```

Também é possível a conversão de inteiros para string usando a classe `Convert`, onde pode ser definida a base numérica a ser utilizada:

```cs
Convert.ToString(192, 2)  // "11000000", que é a representação de 192 em binário
Convert.ToString(192, 8)  // "300", que é a representação de 192 em octal
Convert.ToString(192, 16) // "c0", que é a representação de 192 em hexadecimal
```

## Opções úteis em `System.String`

- Resultam em uma string

  - `Insert` insere uma cadeia de caracteres na string atual.
  - `PadLeft` insere uma ou mais ocorrências de um caractere especificado no início de uma string.
  - `PadRight` insere uma ou mais ocorrências de um caractere especificado no final de uma string.
  - `Remove` exclui uma subcadeia de caracteres da string.
  - `Replace` substitui uma subcadeia de caracteres por outra subcadeia de caracteres na string.
  - `Substring` obtém partes de uma string de acordo com sua posição
    - `Substring(x, y)` retorna os `y` próximos caracteres na string iniciando na posição `x`
    - `Substring(z)` retorna todos os caracteres da string a partir da posição `z` até o final
  - `ToLower` converte todos os caracteres em uma string em minúsculas.
  - `ToUpper` converte todos os caracteres em uma string em letras maiúsculas.
  - `Trim` remove todas as ocorrências de um caractere do início e do fim de uma string.
  - `TrimEnd` remove todas as ocorrências de um caractere do final de uma string.
  - `TrimStart` remove todas as ocorrências de um caractere do início de uma string.

Exemplo de `ToUpper` e `ToLower`

```cs
Console.WriteLine($"{nome.ToUpper()} {sobrenome.ToLower()}")
```

Resultado:

```
ERMOGENES palacio
```

Outros exemplos:

```cs
"abcdef".Insert(3, " :) ")   // "abc :) def"
"123".PadLeft(10, '.')       // ".......123"
"123".PadRight(10, '.')      // "123......."
"abcdefghij".Remove(5)       // "abcde"
"abcdefghij".Remove(5, 2)    // "abcdehij"
"bala".Replace("a", "o")     // "bolo"
"abcdefghij".Substring(0, 5) // "abcde"
"abcdefghij".Substring(5)    // "fghij"
"AbCdeF".ToLower()           // "abcdef"
"AbCdeF".ToUpper()           // "ABCDEF"
"   123   ".Trim()           // "123"
"   123   ".TrimEnd()        // "   123"
"   123   ".TrimStart()      // "123   "
```

- Resultam em um número

  - `Length` retorna o número de caracteres contidos na string
  - `IndexOf` retorna o índice da primeira ocorrência de uma string em outra
  - `LastIndexOf` retorna o índice da última ocorrência de uma string em outra

```cs
"veneno".Length             // 6
"veneno".IndexOf("en")      // 1
"veneno".LastIndexOf("en")  // 3
"veneno".IndexOf("xyz")     // -1 (não encontrado)
```

- Resultam em um booleano

  - `Equals` compara a igualdade de duas strings
  - `Contains` busca se uma string existe dentro de outra
  - `EndsWith` retorna se uma string termina em outra
  - `StartsWith` retorna se uma string começa em outra

```cs
"abc".Equals("abc") // True
"abc".Equals("ABC") // False
"abc".Equals("xyz") // False
"etec adolpho berezin".Contains("mongaguá") // False
"etec adolpho berezin".EndsWith("adolpho")  // False
"etec adolpho berezin".StartsWith("etec")   // True
```

- Resultam em um arranjo

  - `Split` separa a string em elementos de um arranjo de string, a cada ocorrência de outra string
  - `ToCharArray` cria um arranjo de `char` com os caracteres da string

```cs
"Amanhã será um novo dia".Split(" ") // new string[] { "Amanhã", "será", "um", "novo", "dia" }
"Etec".ToCharArray()                 // new char[] { 'E', 't', 'e', 'c' }
```

- Opções estáticas

  - `String.Concat` concatena várias strings em uma única string nova
  - `String.Format` concatena várias strings em uma única string nova usando formatação de composição
  - `String.Empty` retorna a string vazia `""`
  - `String.IsNullOrEmpty` retorna um booleano indicando se a string é nula (`null`) ou vazia (`""`)
  - `String.Join` concatena strings contidas em uma lista, separados por uma string indicada
  - `Convert.ToString` converte um conteúdo em string
    - `Convert.ToString(numero, base)` converte um número em uma string representando o número em outra base
  - `<valor>.ToString` converte valor qualquer em sua representação em string

```cs
String.Concat("Etec", "Adolpho", "Berezin")                        // "EtecAdolphoBerezin"
String.Format("{0} {1} {2}", "Etec", "Adolpho", "Berezin")         // "Etec Adolpho Berezin"
String.Empty                                                       // ""
String.IsNullOrEmpty("teste")                                      // False
String.IsNullOrEmpty("")                                           // True
String.IsNullOrEmpty(String.Empty)                                 // True
String.IsNullOrEmpty(null)                                         // True
String.Join("... ", new string[] { "Etec", "Adolpho", "Berezin" }) // "Etec... Adolpho... Berezin"
Convert.ToString(true)                                             // "True"
Convert.ToString(192)                                              // "192"
Convert.ToString(192, 2)                                           // "11000000" -> 192 em base 2 (binário)
Convert.ToString(192, 8)                                           // "300" -> 192 em base 8 (octal)
Convert.ToString(192, 16)                                          // "c0" -> 192 em base 16 (hexadecimal)
1500.ToString()                                                    // "1500"
```

As strings podem ser acessadas como um arranjo de `char`, usando o operador `[índice]`. O índice indica a posição desejada, iniciando em zero.

```cs
"mongaguá"[0] // 'm'
"mongaguá"[3] // 'g'
"mongaguá"[7] // 'á'
"mongaguá"[8] // erro!
```

## Sequências de escape

Digamos que você queira exibir a seguinte citação no console:

```
"Lágrimas não são argumentos."
Machado de Assis
```

Mas como podemos exibir o caracteres `"` (aspas duplas)?

Percebam que teremos um erro se utilizarmos diretamente:

```cs
Console.WriteLine(""Lágrimas não são argumentos."");
Console.WriteLine("Machado de Assis");
```

Isso acontece porque as aspas tem função especial em strings: ser o delimitador.

Para representar em uma string caracteres especiais temos que usar uma sequência equivalente, chamada de escape.

Para armazenar aspas duplas em uma string delimitada por aspas duplas, podemos usar a sequência de escape `\"`.

```cs
Console.WriteLine("\"Lágrimas não são argumentos.\"");
```

Perceba que as aspas delimitadoras continuam normalmente.

Algumas sequências de escape importantes:

| Caracter          | Sequência de escape | Um exemplo (string)                         |
| ----------------- | ------------------- | ------------------------------------------- |
| `"`               | `\"`                | `"Ganhar na mega-sena é \"fácil\" demais."` |
| `'`               | `\'`                | `"Eu \'prefiro\' aspas simples."`           |
| (quebra de linha) | `\n`                | `"Oi!\nTchau!"`                             |
| (tabulação)       | `\t`                | `"Olá!\tTudo bem?\nSim!\tE você?"`          |

O C# ignorará todas as sequências de escape se a string for criada com o identificador textual `@`:

```cs
Console.WriteLine(@"Meus projetos estão salvos em c:\Users\ermogenes\Documents\novosProjetos");
```

Exibirá:

```
Meus projetos estão salvos em c:\Users\ermogenes\Documents\novosProjetos
```

## Emojis

As strings C# podem armazenar emojis (_na maioria dos casos_) sem maiores problemas.

```cs
string mensagem = "Não faça barulho nas aulas! 🤫";
```

Infelizmente não conseguimos exibir os emojis em aplicações do tipo `console` (mas nada nos impede de exibir em uma página web ou app _mobile_).

Listas de emojis:

- [Emojipedia](https://emojipedia.org/)
- [Lista oficial](http://www.unicode.org/emoji/charts/full-emoji-list.html)

Você pode copiar o emoji e colar no VsCode.

## Tipo `char`

Representa um caractere Unicode UTF-16. É o componente formador de uma string.

Podemos criar um `char` de diversas maneiras:

```cs
char letraJotaMinuscula = 'j'; // = [j], usando um literal entre aspas simples
char cuboDeGelo = '🧊'; // = [🧊], usando um emoji literal entre aspas simples
char espacoEmBranco = (char)32; // = [ ], usando o número inteiro equivalente
char betaGrego = '\u03B2'; // = [β], usando o código UTF-16
char aguaChines = '\x6C34'; // = [水], usando o valor hexadecimal
```

Strings podem ser convertidos em arranjos de `char` (usando `.ToCharArray()`) e vice-versa (usando `String.Join`).
