# Listas

[📽 Veja esta vídeo-aula no Youtube](https://youtu.be/qd18FR7a3s4)

Programa da [vídeo-aula](https://youtu.be/qd18FR7a3s4):

`Program.cs`:
```cs
using System;
using System.Collections.Generic;
using System.Linq;

namespace AulaListas
{
    class Program
    {
        static void Main(string[] args)
        {
            // Listas: coleções fortemente tipadas
            // Declaração e inicialização
            List<int> numeros;
            numeros = new List<int>();

            // Adicionando itens
            numeros.Add(42);
            numeros.Add(-35);
            numeros.Add(42);
            numeros.Add(0);

            // Quantidade de itens
            Console.WriteLine($"Quantidade = {numeros.Count}");
            numeros.Add(-295);
            Console.WriteLine($"Quantidade = {numeros.Count}");

            // Recuperando elemento pela posição
            Console.WriteLine($"Elemento da posição 3: {numeros.ElementAt(3)}");
            Console.WriteLine($"Elemento da posição 1: {numeros.ElementAt(1)}");

            // Encontrando um elemento pelo conteúdo
            Console.WriteLine($"Posição de -295: {numeros.IndexOf(-295)}");
            Console.WriteLine($"Posição de 651591: {numeros.IndexOf(651591)}");

            // Removendo itens: pela posição e pelo conteúdo
            Console.WriteLine($"Elemento da posição 3: {numeros.ElementAt(3)}");
            numeros.RemoveAt(3);
            Console.WriteLine($"Elemento da posição 3: {numeros.ElementAt(3)}");
            numeros.Remove(42);

            // Iterando com foreach
            Console.WriteLine("Lista:");

            foreach (int numero in numeros)
            {
                Console.Write($"{numero} ");
            }

            // Limpando a lista
            numeros.Clear();
            Console.WriteLine($"\nItens após limpeza = {numeros.Count}");

            // Sintaxe resumida
            List<int> n2 = new List<int> {1, 34, 95, 280, -167};

            // Listas de strings
            List<string> nomesMasculinos = new List<string>
            {
                "João",
                "Mario",
                "José"
            };

            List<string> nomesFemininos = new List<string>();
            nomesFemininos.Add("Joana");
            nomesFemininos.Add("Maria");
            nomesFemininos.Add("Josefa");

            List<string> nomes = new List<string>();

            // Adicionando uma lista em outra
            nomes.AddRange(nomesFemininos);
            nomes.AddRange(nomesMasculinos);

            foreach(string nome in nomes)
            {
                Console.WriteLine($"Nome = {nome}");
            }

            // Listas de objetos
            List<Pessoa> amigos = new List<Pessoa>
            {
                new Pessoa() { Nome = "Neri", Idade = 25 },
                new Pessoa() { Nome = "Ermogenes", Idade = 17 }
            };

            Pessoa p3 = new Pessoa();
            p3.Nome = "Ronaldo";
            p3.Idade = 30;

            amigos.Add(p3);

            foreach(Pessoa p in amigos)
            {
                Console.WriteLine($"amigo = {p.Nome} ({p.Idade})");
            }

            // Linq: min, max, average, sum
            Console.WriteLine($"menor número = {n2.Min()}");
            Console.WriteLine($"maior número = {n2.Max()}");
            Console.WriteLine($"média dos números = {n2.Average()}");
            Console.WriteLine($"soma dos números = {n2.Sum()}");

            // Linq: filtrando com expressões lambda, e ordenando
            List<string> nomesComJ = nomes
                .Where(n => n.ToUpper().StartsWith("J"))
                .OrderBy(n => n)
                .ToList();
            
            foreach(string nome in nomesComJ)
            {
                Console.WriteLine($"nome com J = {nome}");
            }

            List<Pessoa> amigosVelhos = amigos
                .Where(amigo => amigo.Idade >= 18)
                .OrderByDescending(amigo => amigo.Idade)
                .ToList();

            foreach(Pessoa amigoVelho in amigosVelhos)
            {
                Console.WriteLine($"amigo velho = {amigoVelho.Nome} ({amigoVelho.Idade})");
            }

            // Outras coleções: Filas
            Queue<string> filaPao = new Queue<string>();
            filaPao.Enqueue("Anastacia");
            filaPao.Enqueue("Deodato");
            filaPao.Enqueue("Madalena");

            Console.WriteLine($"tamanho da fila do pão = {filaPao.Count}");

            string proximo = filaPao.Dequeue();
            Console.WriteLine($"Atendendo {proximo}");
            Console.WriteLine($"tamanho da fila do pão = {filaPao.Count}");

            // Outras coleções: Pilhas
            Stack<string> caminhaoMudanca = new Stack<string>();
            caminhaoMudanca.Push("Roupeiro");
            caminhaoMudanca.Push("Sofá");
            caminhaoMudanca.Push("Plantas");

            Console.WriteLine($"Tamanho do caminhão de mudança = {caminhaoMudanca.Count}");

            Console.WriteLine($"Retirado {caminhaoMudanca.Pop()}");
            Console.WriteLine($"Retirado {caminhaoMudanca.Pop()}");
        }
    }
}
```

Pessoa.cs
```cs
namespace AulaListas
{
    class Pessoa
    {
        public string Nome { get; set; }
        public int Idade { get; set; }
    }
}
```

**Saída**:
```
Quantidade = 4
Quantidade = 5
Elemento da posição 3: 0
Elemento da posição 1: -35
Posição de -295: 4
Posição de 651591: -1
Elemento da posição 3: 0
Elemento da posição 3: -295
Lista:
-35 42 -295
Itens após limpeza = 0
Nome = Joana
Nome = Maria
Nome = Josefa
Nome = João
Nome = Mario
Nome = José
amigo = Neri (25)
amigo = Ermogenes (17)
amigo = Ronaldo (30)
menor número = -167
maior número = 280
média dos números = 48,6
soma dos números = 243
nome com J = Joana
nome com J = João
nome com J = José
nome com J = Josefa
amigo velho = Ronaldo (30)
amigo velho = Neri (25)
tamanho da fila do pão = 3
Atendendo Anastacia
tamanho da fila do pão = 2
Tamanho do caminhão de mudança = 3
Retirado Plantas
Retirado Sofá
```

## Material oficial

Faça também o [tutorial interativo oficial](https://learn.microsoft.com/pt-br/dotnet/csharp/tour-of-csharp/tutorials/list-collection).
