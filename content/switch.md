# Decisão múltipla com `switch`

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/t0DyqALDYgQ)

Testa uma expressão, comparando sequencialmente com diversas outras. Permite que se disponha múltiplos caminhos de execução, de acordo com o valor da primeira expressão.

Exemplo:

```
Menu de opções
--------------

N. Novo arquivo
A. Abrir arquivo
H. Ajuda
X. Sair

Digite a sua opção: _
```

Nesse caso, gostaríamos de avaliar o resultado da digitação entre 4 valores disjuntos (`"N"`, `"A"`, `"H"` e `"X"`).

## Comando `switch`

Implementa a decisão múltipla em C#.

```cs
switch (expressaoTeste)
{
    case expressaoCaso1:
        comandosCaso1Verdadeiro
        ...
        break;
    case expressaoCaso2:
        comandosCaso2Verdadeiro
        ...
        ...
        break;
    ...
    default:
        comandosTodosCasosFalsos
}
```

- `switch`: comando de decisão múltipla
- `expressaoTeste`: expressão a ser avaliada pelos testes
- `case`: um teste de igualdade em relação a `expressaoTeste`
- `expressaoCaso1` e `expressaoCaso2`: valores inteiros a serem testados contra `expressaoTeste`
- `comandosCaso1Verdadeiro` e `comandosCaso2Verdadeiro`: listas de comandos a serem executados caso seus testes avaliem como verdadeiro
- `break`: indica não deve mais executar comandos do bloco `switch`
- `default` (opcional): caso padrão, se nenhum dos casos anteriores for verdadeiro
- `comandosTodosCasosFalsos` (opcional): comandos a serem executados no caso padrão

Exemplo:

```c
string opcaoUsuario = "";

Console.WriteLine("Menu de opções");
Console.WriteLine("--------------");
Console.WriteLine("N. Novo arquivo");
Console.WriteLine("A. Abrir arquivo");
Console.WriteLine("H. Ajuda");
Console.WriteLine("X. Sair");

Console.WriteLine("\nDigite a sua opção: ");
opcaoUsuario = Console.ReadLine()!;

Console.WriteLine($"\nOPÇÃO SELECIONADA: {opcaoUsuario}\n");

switch (opcaoUsuario.ToUpper())
{
case "N":
    Console.WriteLine("Um arquivo novo será criado.");
    break;
case "A":
    Console.WriteLine("Um arquivo existente poderá ser aberto.");
    break;
case "H":
    Console.WriteLine("Uma tela de ajuda será exibida.");
    break;
case "X":
    Console.WriteLine("Obrigado por utilizar nosso software!");
    break;
default:
    Console.WriteLine("Opção inválida!");
    Environment.Exit(1); // Código de erro
    break;
}
Environment.Exit(0); // Código de sucesso
```

[Lista completa de códigos de erro do Windows](https://docs.microsoft.com/pt-br/windows/win32/debug/system-error-codes)

## Expressão `switch`

Assim como para decisão simples temos o operador `?:`, também temos o operador `switch` para decisão múltipla _inline_.

Exemplo:

```cs
int opcao = 1;

string mensagem = opcao switch
{
    0 => "Solteiro(a)",
    1 => "Casado(a)",
    2 => "Divorciado(a)",
    3 => "Viúvo(a)",
    _ => "Outro"
};

Console.WriteLine(mensagem); // Casado(a)
```

Exemplo 2:

```cs
using System.Security.Cryptography;

int naipeSorteado = RandomNumberGenerator.GetInt32(1, 5);

string naipe = naipeSorteado switch
{
    1 => "Paus",
    2 => "Copas",
    3 => "Espadas",
    4 => "Ouros"
};

Console.WriteLine(naipe);
```
