# Entrada de dados via teclado

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/C2CaB2-kEQo)

## Aguardar o usuário pressionar qualquer tecla

`Console.ReadKey`

```cs
Console.ReadKey();
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
