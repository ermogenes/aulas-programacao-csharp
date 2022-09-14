# Classes

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/r6EllahDrEQ)

Classes são estruturas de dados que agregam estado (dados) e comportamento (funcionalidades). Criando classes podemos criar programas que imitam a lógica de coisas do mundo real, permitindo que se transporte o conhecimento adquirido do problema de negócio diretamente para o código na linguagem de programação.

## Objetos

Uma _classe_ é um molde, uma planta, um esquema de abstração de uma ideia, implementada em linguagem de programação. Cada ocorrência, chamada _instância_, possui existência real na memória, no formato definido pela classe, e representa um _objeto_ real no nosso problema.

Por exemplo, a classe `Cachorro` define (usando C#) como um cachorro deve ser e se comportar (em nosso programa). Os objetos `c1` (personagem _Pluto_), `c2` (_Snoopy_) e `c3` (_Scooby-Doo_) seguem as regras da classe `Cachorro` e representam cada um, um cachorro específico.

## Estado

Em uma classe, o estado é mantido através de **atributos**, que são dados associados a uma instância. Cada objeto possui sua própria cópia dos dados.

No exemplo anterior, todo `Cachorro` possui um nome, uma raça e uma cor: Pluto é um _bloodhound_ amarelo, Snoopy é um _beagle_ branco e Scooby-Doo é um _dogue alemão_ marrom.

<img height=250 src="https://upload.wikimedia.org/wikipedia/pt/4/4c/Pluto_%28Disney%29.jpg" alt="Pluto: Todos os direitos da imagem para Disney" /><img height=250 src="https://upload.wikimedia.org/wikipedia/pt/5/53/Snoopy_Peanuts.png" alt="Snoopy: Todos os direitos da imagem para Charles M. Schulz" /><img height=250 src="https://upload.wikimedia.org/wikipedia/pt/b/b2/Scooby.jpg" alt="Scooby-Doo: Todos os direitos da imagem para Hanna-Barbera" />

<!-- ![Todos os direitos da imagem para Disney](https://upload.wikimedia.org/wikipedia/pt/4/4c/Pluto_%28Disney%29.jpg)
![Todos os direitos da imagem para Charles M. Schulz](https://upload.wikimedia.org/wikipedia/pt/5/53/Snoopy_Peanuts.png)
![Todos os direitos da imagem para Hanna-Barbera](https://upload.wikimedia.org/wikipedia/pt/b/b2/Scooby.jpg) -->

## Comportamento

Indica quais ações uma classe pode realizar ou quais mensagens um objeto daquela classe pode receber.

No exemplo anterior, todo `Cachorro` pode latir ou rosnar.

## Abstração

Conseguimos, então, escrever em C# um código que representa essas ideias.

Começamos definido a classe `Cachorro`:

```cs
public class Cachorro
{
    public string nome;
    public string raca;
    public string cor;

    public void Latir()
    {
        Console.WriteLine($"[{this.nome}] BARF! Barf! BARF!!!");
    }

    public void Rosnar()
    {
        Console.WriteLine($"[{this.nome}] GrrRRRRRrrrr!");
    }
}
```

Essa classe possui 5 membros:

* os atributos `Nome`, `Raca` e `Cor`;
* os métodos `Latir` e `Rosnar`.

Agora podemos criar instâncias de `Cachorro`:

```cs
Cachorro c1;
c1 = new Cachorro();
c1.nome = "Pluto";
c1.raca = "bloodhound";
c1.cor = "amarelo";
```

Podemos criar os demais objetos de outras maneiras igualmente válidas:

```cs
Cachorro c2 = new Cachorro();
c2.nome = "Snoopy";
c1.raca = "beagle";
c2.cor = "branco";
```

```cs
Cachorro c3 = new Cachorro {
    nome = "Scooby-Doo",
    raca = "dogue alemão",
    cor = "marrom"
};
```

Agora, por exemplo, se quisermos que o Pluto rosne e depois os demais latam:

```cs
c1.Rosnar();
c2.Latir();
c3.Latir();
```

Saída:

```
[Pluto] GrrRRRRRrrrr!
[Snoopy] BARF! Barf! BARF!!!
[Scooby-Doo] BARF! Barf! BARF!!!
```

## Acessando membros da instância com `this`

Usamos a palavra chave `this` para referenciar o objeto atual. Perceba como os métodos `Latir` e `Rosnar` conseguem obter corretamente o `nome` de cada instância usando `this`.

## Modificadores de acesso

* `public` indica que o membro está exposto, e acessível fora da classe;
* `private` indica que o membro está encapsulado, e acessível somente de dentro da classe;
* `protected`indica que o membro é acessível soemnte dentro de sua classe ou de classes derivadas.

Há outros modificadores, para saber mais consulte a [documentação](https://docs.microsoft.com/pt-br/dotnet/csharp/language-reference/keywords/access-modifiers).

## Construtores

Executado quando se instancia um objeto através da palavra `new`.

Podemos adicionar código a ser executado na criação de cada objeto utilizando um construtor. Ao definir, é só utilizar o mesmo nome da classe:

```cs
    public Cachorro()
    {
        // código a ser executado ao criar uma instância
    }
```

Podemos definir parâmetros obrigatórios ao se criar um objeto. No exemplo abaixo, só vamos permitir criar um novo `Cachorro` se a raça for informada:

```cs
    public Cachorro(string raca)
    {
        this.raca = raca;
    }
```

Perceba que já utilizamos o valor recebido para gravá-lo no atributo `raca`. Para instanciar:

```cs
Cachorro c4 = new Cachorro("vira-latas");
c4.nome = "Muttley";
c4.cor = "amarelo";
```

```cs
Cachorro c5 = new Cachorro("schnauzer") {
    nome = "Bidu",
    cor = "azul"
};
```

Ao se definir um construtor, impedimos o acesso à instanciação normal. No exemplo acima, não poderíamos mais chamar `new` sem indicar a raça. Podemos criar vários construtores para resolver esse problema, desde que cada um tenha uma assinatura diferente.

## Propriedades

Permitem que se encapsule um atributo mantendo-o privado, e ainda assim o exponha somente para leitura ou somente para gravação, ou ambos. Ainda podemos adicionar lógica a ser executada quando da leitura e/ou da gravação.

## Estático e não estático

Utilizando a palavra `static`, fazemos com que um membro seja acessível diretamente pela classe, sem necessitar de um objeto.

Exemplos, na classe `Cachorro`:

```cs
// ...
    private static string _nomePopular = "Cão doméstico";
    private static string _nomeCientifico = "Canis lupus familiaris";
// ...
    static string Especie()
    {
        return $"{_nomePopular} ({_nomeCientifico})";
    }
```

Não precisamos de um objeto `Cachorro` para obter a identificação da espécie, pois os membros estão ligado à classe, e não às suas instâncias.

---

Programa da [vídeo-aula](https://youtu.be/r6EllahDrEQ):

Arquivo `Cliente.cs`:

```cs
namespace MeuBanco
{
    class Cliente
    {
        public string Nome { get; set; }
        public string Sobrenome { get; set; }

        public Cliente(string nome, string sobrenome)
        {
            this.Nome = nome;
            this.Sobrenome = sobrenome;
        }
        public string NomeCompleto()
        {
            return $"{this.Nome} {this.Sobrenome}";
        }
    }
}
```

Arquivo `Conta.cs`:

```cs
using System;

namespace MeuBanco
{
    class Conta
    {
        private decimal _saldo;
        public Cliente Titular { get; private set; }
        public decimal Saldo
        {
            get
            {
                return this._saldo;
            }
            private set
            {
                if (value < 0)
                {
                    throw new ArgumentException("Saldo inválido.");
                }
                this._saldo = value;
            }
        }

        public Conta(Cliente titular, decimal saldo)
        {
            this.Titular = titular;
            this.Saldo = saldo;
        }

        public void Depositar(decimal valorADepositar)
        {
            if (valorADepositar <= 0)
            {
                throw new ArgumentException("Depósitos devem ser positivos.");
            }
            this.Saldo += valorADepositar;
        }

        public bool Sacar(decimal valorASacar)
        {
            if (valorASacar <= 0)
            {
                throw new ArgumentException("Saques devem ser positivos.");
            }

            bool possuiSaldo = (this.Saldo >= valorASacar);
            if (possuiSaldo)
            {
                this.Saldo -= valorASacar;
            }
            return possuiSaldo;
        }
    }
}
```

Arquivo `Program.cs`:

```cs
using System;
using MeuBanco;

namespace AulaClasses
{
    class Program
    {
        static void Main(string[] args)
        {
            Cliente t1 = new Cliente("Ermogenes", "Palacio");

            Conta c1;
            c1 = new Conta(t1, 100);

            c1.Depositar(10);
            c1.Depositar(500);

            Conta c2 = new Conta(new Cliente("Diego", "Neri"), 200);

            c2.Depositar(95);

            if (!c1.Sacar(20))
            {
                Console.WriteLine("20: Saldo insuficiente.");
            }

            Console.WriteLine($"{c1.Titular.NomeCompleto()} tem {c1.Saldo:C2} e {c2.Titular.NomeCompleto()} tem {c2.Saldo:c2}.");
        }
    }
}
```

**Saída**:

```
Ermogenes Palacio tem R$590,00 e Diego Neri tem R$295,00.
```
