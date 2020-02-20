# Trabalhando com strings

## O básico

Uma _string_ é uma cadeia (sequência) de caracteres individuais. Por exemplo, a string `Etec` é formada pelos caracteres `E`, `t`, `e` e `c`. No .NET, por padrão, é utilizada a codificação UTF-16.

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

* Concatenação via operador `+`

```cs
string nomeCompleto = nome + " " + sobrenome;
```

* Concatenação via método `Concat`

```cs
string nomeCompleto = String.Concat(nome, " ", sobrenome);
```

* Formatação de composição

```cs
string nomeCompleto = String.Format("{0} {1}", nome, sobrenome);
```

* Interpolação

```cs
string nomeCompleto = $"{nome} {sobrenome}";
```

## Métodos úteis em `System.String`

* Alguns métodos que resultam em uma string

  * `Insert` insere uma cadeia de caracteres na string atual.
  * `PadLeft` insere uma ou mais ocorrências de um caractere especificado no início de uma string.
  * `PadRight` insere uma ou mais ocorrências de um caractere especificado no final de uma string.
  * `Remove` exclui uma subcadeia de caracteres da string.
  * `Replace` substitui uma subcadeia de caracteres por outra subcadeia de caracteres na string.
  * `ToLower` converte todos os caracteres em uma string em minúsculas.
  * `ToUpper` converte todos os caracteres em uma string em letras maiúsculas.
  * `Trim` remove todas as ocorrências de um caractere do início e do fim de uma string.
  * `TrimEnd` remove todas as ocorrências de um caractere do final de uma string.
  * `TrimStart` remove todas as ocorrências de um caractere do início de uma string.

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
"abcdef".Insert(3, " :) ")  // "abc :) def"
"123".PadLeft(10, '.')      // ".......123"
"123".PadRight(10, '.')     // "123......."
"abcdefghij".Remove(5)      // "abcde"
"abcdefghij".Remove(5, 2)   // "abcdehij"
"bala".Replace("a", "o")    // "bolo"
"AbCdeF".ToLower()          // "abcdef"
"AbCdeF".ToUpper()          // "ABCDEF"
"   123   ".Trim()          // "123"
"   123   ".TrimEnd()       // "   123"
"   123   ".TrimStart()     // "123   "
```

* Alguns métodos que resultam em um número

  * `IndexOf` retorna o índice da primeira ocorrência de uma string em outra
  * `LastIndexOf` retorna o índice da última ocorrência de uma string em outra

```cs
"veneno".IndexOf("en")      // 1
"veneno".LastIndexOf("en")  // 3
"veneno".IndexOf("xyz")     // -1 (não encontrado)
```

* Alguns métodos que resultam em um booleano

  * `Equals` compara a igualdade de duas strings
  * `Contains` busca se uma string existe dentro de outra
  * `EndsWith` retorna se uma string termina em outra
  * `StartsWith` retorna se uma string começa em outra

```cs
"abc".Equals("abc") // True
"abc".Equals("ABC") // False
"abc".Equals("xyz") // False
"etec adolpho berezin".Contains("mongaguá") // False
"etec adolpho berezin".EndsWith("adolpho")  // False
"etec adolpho berezin".StartsWith("etec")   // True
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

Caracter | Sequência de escape | Um exemplo (string)
-- | -- | --
" | \\" | "Ganhar na mega-sena é \\"fácil\\" demais."
' | \\' | "Eu \\'prefiro\\' aspas simples."
(quebra de linha) | \\n | "Oi!\nTchau!"
(tabulação) | \\t | "Olá!\tTudo bem?\nSim!\tE você?"

O C# ignorará todas as sequências de escape se a string for criada com o identificador textual `@`:

```cs
Console.WriteLine(@"Meus projetos estão salvos em c:\Users\ermogenes\Documents\novosProjetos");
```

Exibirá:

```
Meus projetos estão salvos em c:\Users\ermogenes\Documents\novosProjetos
```