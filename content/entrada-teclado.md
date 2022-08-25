# Entrada de dados via teclado

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/C2CaB2-kEQo)

## Aguardar o usuário pressionar qualquer tecla

`Console.ReadKey`

```cs
Console.ReadKey();
```

Para não exibir a tecla pressionada:

```cs
Console.ReadKey(true);
```

Para guardar informações sobre a tecla pressionada:

```cs
ConsoleKeyInfo teclaPressionada = Console.ReadKey(true);
```

- `teclaPressionada.Keychar` armazena o caractere visível da tecla pressionada (ex.: `g` ao pressionar `ALT+G`, `<vazio>` ao pressionar `F12`);
- `teclaPressionada.Key` armazena um código representando a tecla exata que foi pressionada (ex.: `ConsoleKey.Enter` para `ENTER`, `ConsoleKey.UpArrow` caso `Seta para Cima`), [segundo esta tabela](https://docs.microsoft.com/pt-br/dotnet/api/system.consolekey?view=net-6.0).
- `teclaPressionada.Modifiers` permite verificar se as teclas `ALT`, `SHIFT` e `CTRL` estavam pressionadas em conjunto com `teclaPressionada.Key`.

```cs
Console.Write("Pressione uma tecla...");
var tecla = Console.ReadKey(true);

Console.Write("\nFoi pressionado ");

bool pressionadoAlt = (tecla.Modifiers & ConsoleModifiers.Alt) != 0;
bool pressionadoShift = (tecla.Modifiers & ConsoleModifiers.Shift) != 0;
bool pressionadoControl = (tecla.Modifiers & ConsoleModifiers.Control) != 0;

if (pressionadoAlt) Console.Write("ALT+");
if (pressionadoShift) Console.Write("SHIFT+");
if (pressionadoControl) Console.Write("CTRL+");
Console.WriteLine(tecla.Key);
```

## Aguardar o usuário digitar uma sequência de teclas finalizadas por `ENTER`

`Console.ReadLine`

```cs
Console.ReadLine();
```

## Guardar o conteúdo digitado em uma variável

```cs
string textoDigitado = Console.ReadLine()!;
```

## Exibir o conteúdo da variável

```cs
Console.Write("Digite seu nome: ");
string textoDigitado = Console.ReadLine()!;
Console.Write("Olá, ");
Console.Write(textoDigitado);
Console.WriteLine("!");
Console.WriteLine("Pressione uma tecla para continuar...");
Console.ReadKey();
```

Resultado

```powershell
PS C:\Users\ermogenes\Desktop\code\ExemploConsole> dotnet run
Digite seu nome: Ermogenes
Olá, Ermogenes!
Pressione uma tecla para continuar...
PS C:\Users\ermogenes\Desktop\code\ExemploConsole>
```

## Limpar o _buffer_ de teclado

```cs
while (Console.KeyAvailable) Console.ReadKey(true);
```
