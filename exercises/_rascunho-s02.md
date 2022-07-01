- [Saída em console](#Exercícios-Saída-em-console) x 9
- [Entrada de dados e Strings](#Exercícios-Entrada-de-dados-e-Strings) x 1
- [Números e Operadores](#Exercícios-Números-e-Operadores) x 3
- [Decisão e operações lógicas](#Exercícios-Decisão-e-operações-lógicas) x 9
- [Sub-rotinas](#Exercícios-Sub-rotinas) x 0
- [Laços](#Exercícios-Laços) x 5
- [Arranjos](#Exercícios-Arranjos) x 2
- [Classes](#Exercícios-Classes) x 0
- [Listas](#Exercícios-Listas) x 1

# Exercícios: Saída em console

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[Continue](#Exercício-Continue) | _em breve_ | 
[DezSegundos](#Exercício-DezSegundos) | _em breve_ | 
[Haikai](#Exercício-Haikai) | _em breve_ | 
[FrutasPreferidas](#Exercício-FrutasPreferidas) | _em breve_ | 
[Piada](#Exercício-Piada) | _em breve_ | 
[Adivinha](#Exercício-Adivinha) | _em breve_ | 
[TimeDoCoracao](#Exercício-TimeDoCoracao) | _em breve_ | 
[PoemaConcreto](#Exercício-PoemaConcreto) | _em breve_ | 
[BebaCocaCola](#Exercício-BebaCocaCola) | _em breve_ | 

---
## Exercício `Continue`

Faça um programa que exiba a seguinte mensagem:

```
Pressione uma tecla para continuar...
```

Após o usuário pressionar uma tecla, agradeça ao usuário e finalize o programa.

---
## Exercício `DezSegundos`

Faça um programa que exiba uma contagem de 0 a 10 na mesma linha, aguardando um segundo entre cada número.

Exemplo:
```
Contando até dez: 0
```

(um segundo depois)

```
Contando até dez: 0 1
```

(um segundo depois)

```
Contando até dez: 0 1 2
```

... e assim sucessivamente.

************************************** adicionar Thread.Sleep em console

---
## Exercício `FrutasPreferidas`

Faça um programa que exiba as suas 5 frutas preferidas.

Exemplo:
```
--- Minhas frutas preferidas ---

1. Pitaia
2. Mirtilo
3. Atemoia
4. Ingá
5. Araçá
```

---
## Exercício `Piada`

Faça um programa que exiba uma piada.

Exemplo:
```
O professor:
– Quem se acha burro fique em pé.
Joãozinho se levanta:
– Você se acha burro, Joãozinho?
– Não, mas fiquei com dó de ver o senhor em pé sozinho.
```

---
## Exercício `Adivinha`

Faça um programa que exiba um adivinha, no formato "_o que é, o que é?_". Faça uma pausa de 5 segundos para que usuário possa pensar na resposta.

Exemplo:
```
O que é, o que é... 
... que o nadador faz para bater o recorde?

Nada.
```

************************************** adicionar Thread.Sleep em console

---
## Exercício `PoemaConcreto`

Faça um programa que exiba o seguinte poema concreto:

![](exemplo-PoemaConcreto.jpg)

Saiba mais [aqui](https://www.todamateria.com.br/poesia-concreta/) e [aqui](https://mundoeducacao.uol.com.br/literatura/poesia-concreta.htm).

---
## Exercício `BebaCocaCola`

Faça um programa que exiba o poema concreto _Beba Coca-Cola_, de Décio Pignatari.

![](exemplo-BebaCocaCola.webp)

---
## Exercício `TimeDoCoracao`

Faça um programa que exiba o nome do seu time do coração (ou um time qualquer, não importa o esporte). Utilize as cores do time.

Exemplos:

![](exemplo-TimeDoCoracao.png)

# Exercícios: Entrada de dados e Strings

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[PrimeroCaractere](#Exercício-PrimeroCaractere) | _em breve_ | 

---
## Exercício `PrimeroCaractere`

Faça um programa que exiba o primeiro caractere digitado, ignorando espaços em branco.

Digitação | Resultado esperado
--- | ---
`abc` | `a`
`!235` | `!`
`···xyz·····` | `x`

************* Adicionar Substring em https://github.com/ermogenes/aulas-programacao-csharp/blob/master/content/string.md

# Exercícios: Números e Operadores

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[TempoDownload](#Exercício-TempoDownload) | _em breve_ | 
[Troco](#Exercício-Troco) | _em breve_ | 
[IndependenciaFinanceira](#Exercício-IndependenciaFinanceira) | _em breve_ | 

---
## Exercício `TempoDownload`

Calcule o tempo estimado para _download_ de um arquivo. Para isso, receba o tamanho do arquivo em _megabytes_ (MB) e a velocidade da conexão em _megabits_ por segundo (Mbps). Exiba o tempo em minutos.

Lembre-se que 1 byte = 8 bits (e 1MB = 8Mb).

Exemplo:
```
--- Tempo de Download ---

Tamanho do arquivo em MB........: 105
Velocidade da conexão em Mbps...: 4

Tempo estimado de download: 3,5 minutos
```

---
## Exercício `Troco`

Solicite que o usuário digite o valor da compra e o valor pago. Exiba o valor do troco.

---
## Exercício `IndependenciaFinanceira`

Faça um programa que calcule quanto dinheiro é necessário possuir em um investimento para conseguir sua independência financeira com dividendos (ou seja, os dividendos deverão pagar todos os seus custos). Receba os gastos mensais e o rendimento dos dividendos (_dividend yield_). O valor necessário investido para receber X reais de dividendo todo mês com Y% de _dividend yield_ é `X / (Y / 100)`.

Valores para teste:
Para receber mensalmente | com _dividend yield_ de | é necessário investir 
--- | --- | ---
R$ 1.000,00 | 1,0% | R$ 100.000,00
R$ 1.000,00 | 0,5% | R$ 200.000,00
R$ 3.500,00 | 1,0% | R$ 350.000,00
R$ 3.500,00 | 0,5% | R$ 700.000,00
R$ 5.000,00 | 1,0% | R$ 500.000,00
R$ 5.000,00 | 0,5% | R$ 1.000.000,00

Exemplo:
```
--- Vivendo de dividendos ---

Gastos mensais (em R$)....: 3500
Rendimentos mensais (%)...: 0,5

Para receber R$3500,00 por mês com rendimentos de 0,5% você precisa ter investido R$700000,00.
```

# Exercícios: Decisão e operações lógicas

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[InteiroOuDecimal](#Exercício-InteiroOuDecimal) | _em breve_ | 
[PescaAmadora](#Exercício-PescaAmadora) | _em breve_ | 
[CasaDeTintas](#Exercício-CasaDeTintas) | _em breve_ | 
[MaiorDeTres](#Exercício-MaiorDeTres) | _em breve_ | 
[Multiplo](#Exercício-Multiplo) | _em breve_ | 
[Bissexto](#Exercício-Bissexto) | _em breve_ | 
[FluxogramaEngenharia](#Exercício-FluxogramaEngenharia) | _em breve_ | 
[Estacionamento](#Exercício-Estacionamento) | _em breve_ | 
[CaixaEletronico](#Exercício-CaixaEletronico) | _em breve_ | 

---
## Exercício `InteiroOuDecimal`

Solicite que o usuário digite o valor real. Exiba se ele é um número inteiro ou decimal.

Exemplos:
```
--- Inteiro ou Decimal? ---

Digite um número: 4,0

4,0 é um número inteiro.
```

```
--- Inteiro ou Decimal? ---

Digite um número: 4,5

4,5 é um número decimal.
```

---
## Exercício `PescaAmadora`

Um pescador amador solicita um software avaliação da legalidade de sua pesca. Faça um programa que receba um peso em kg e o local da pesca (`C` ou `M`) e exiba, conforme o caso:

 - `Pescaria dentro dos limites legais.`, ou
 - `Pescaria excede os limites legais em XXX kg. Sujeito a multa de R$ YYY.`

Limites de peso para pesca amadora:
Local | Limites
--- | ---
Águas continentais e estuarinas | 10kg
Águas marinhas | 15kg

Multa prevista em caso de excesso de peso: R$1000,00, com acréscimo de R$20,00 por quilo excedido.

Exemplos:
```
--- Pesca Amadora ---

Peso (em kg)...: 50
Águas [c]ontinentais ou [m]arinhas? m

Pescaria excede os limites legais em 35kg.
Sujeito a multa de R$700,00.
```

```
--- Pesca Amadora ---

Peso (em kg)...: 5
Águas [c]ontinentais ou [m]arinhas? c

Pescaria dentro dos limites legais.
```

---
## Exercício `CasaDeTintas`

Faça uma calculadora para uma casa de tintas. O usuário fornecerá a área a ser pintada (em m²), e será informado sobre a quantidade de produtos necessários para cobrir a área indicada.

Acrescente 10% à tinta necessária, como folga para erros.

As tintas são vendidas em dois tipos de recipientes:

Recipiente | Conteúdo
--- | ---
Lata | 18 litros
Galão | 3,6 litros

Considere um rendimento fixo de 3m²/l de tinta.

Exemplo:
```
--- Casa de Tintas ---

Área a ser pintada (m²)...: 60m²

Serão necessários 22 litros de tinta.

Distribuição:
Latas...: 1
Galões..: 2
```

---
## Exercício `MaiorDeTres`

Receba três números inteiros. Exiba somente o maior dos 3.


---
## Exercício `Multiplo`

Determine se um número é múltiplo de outro.

Exemplos:
```
--- Múltiplo ---

Digite um número...........: 187
Avaliar se é múltiplo de...: 11

187 é múltiplo de 11
```

```
--- Múltiplo ---

Digite um número...........: 188
Avaliar se é múltiplo de...: 11

188 não é múltiplo de 11
```

---
## Exercício `Bissexto`

Determine se um ano fornecido pelo usuário [é ou não bissexto](https://escolakids.uol.com.br/matematica/calculo-do-ano-bissexto.htm).

[Regra para o cálculo dos anos bissextos](https://pt.wikipedia.org/wiki/Ano_bissexto):

1. A cada 400 anos temos com certeza um ano bissexto.
2. A cada 100 anos o ano não é bissexto, exceto quando é bissexto pela regra 1.
3. A cada 4 anos o ano é bissexto, exceto quando não é bissexto pela regra 2.

Exemplos de valores para teste:
- Bissextos pela regra 1: 400, 800, 1200, 1600, 2000, 2400
- Não bissextos pela regra 2: 100, 200, 300, 500, 600,... , 1500, 1700, 1800, 1900, 2100
- Bissextos pela regra 3: 4, 8, 12, ..., 1992, 1996, 2004, ..., 2092, 2096, 2104

---
## Exercício `FluxogramaEngenharia`

Faça um programa que implemente o meme _Fluxograma da Engenharia_.

![](
https://imageproxy.ifunny.co/crop:x-20,resize:640x,quality:90x75/images/e0c42862553bc72e5f217b247b3212e1ea913e08617232137a533299d6d0d3f5_1.jpg)

Exemplos:
```
--- Fluxograma da Engenharia ---

O objeto está se movendo (S/N)? N
Deveria? S

Use WD-40.
```

```
--- Fluxograma da Engenharia ---

O objeto está se movendo (S/N)? S
Deveria? N

Use Silver Tape.
```

```
--- Fluxograma da Engenharia ---

O objeto está se movendo (S/N)? N
Deveria? N

Ótimo!
```

---
## Exercício `Estacionamento`

Um estacionamento possui a seguinte política de preços:

- Primeira hora: R$ 20,00
- Horas adicionais:
	- Carros grandes: R$ 20,00/hora adicional
	- Carros pequenos: R$ 10,00/hora adicional
- Diária (5 horas ou mais):
	- Carros grandes: R$ 80,00
	- Carros pequenos: R$ 50,00
- Tolerância (na saída): 5min
- _Valet_ (manobrista): 20% adicional no valor final
- Lavagem:
	- Carros grandes: R$ 100,00
	- Carros pequenos: R$ 50,00

Faça um programa que receba o tamanho do veículo (P/G), o total de minutos que o veículo ficou estacionado, se foi utilizado o serviço de _valet_ (S/N) e a inclusão de serviço de lavagem (S/N). Exiba o valor final a ser pago.

Exemplos:
```
--- Estacionamento ---

Tamanho do veículo (P/G).....: P
Tempo de permanência (min)...: 473
Serviço de valet (S/N).......: N
Serviço de lavagem (S/N).....: N

Valor total: R$50,00
```

```
--- Estacionamento ---

Tamanho do veículo (P/G).....: G
Tempo de permanência (min)...: 123
Serviço de valet (S/N).......: S
Serviço de lavagem (S/N).....: S

Valor total: R$148,00
```

---
## Exercício `CaixaEletronico`

Ao realizar um saque, um caixa eletrônico calcula a quantidade de notas a entregar ao solicitante. Faça um programa que dado um valor desejado para saque (o número deve ser positivo e não pode conter centavos), calcule a quantidade de cada nota a ser entregue. Dê preferência para notas de valor mais alto.

Notas disponíveis: 1, 2, 5, 10, 20, 50, 100 e 200 reais

Exemplo:
```
--- Caixa Eletrônico ---

Digite o valor a ser sacado...: 298,00

O caixa deve entregar:
1 nota(s) de R$200,00
1 nota(s) de R$50,00
2 nota(s) de R$20,00
1 nota(s) de R$5,00
1 nota(s) de R$2,00
1 nota(s) de R$1,00
```

# Exercícios: Sub-rotinas

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[xxxxxxx](#Exercício-xxxxxxx) | _em breve_ | 

# Exercícios: Laços

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[EntradaValida](#Exercício-EntradaValida) | _em breve_ | 
[UrnaPlebiscito](#Exercício-UrnaPlebiscito) | _em breve_ | 
[Potencia](#Exercício-Potencia) | _em breve_ | 
[AmortizacaoConstante](#Exercício-AmortizacaoConstante) | _em breve_ | 
[AmortizacaoFrancesa](#Exercício-AmortizacaoFrancesa) | _em breve_ | 

---
## Exercício `EntradaValida`

Solicite que o usuário entre com um valor inteiro entre 1 e 9, inclusive. Informe que a entrada 0 sinaliza um cancelamento. Não finalize o programa enquanto não houver uma entrada válida ou um cancelamento.

---
## Exercício `UrnaPlebiscito`

Faça uma urna eletrônica para um plebiscito organizado pelo grêmio estudantil de uma escola  _fictícia_.

A pergunta a ser realizada é: _Você é a favor da aprovação automática de alunos carecas canhotos?_

As alternativas possíveis são:
- `S` - Sim, sou a favor
- `N` - Não, sou contra
- `A` - Me abstenho de responder

Mantenha o registro da quantidade de votos em cada alternativa.

Garanta que um eleitor não possa ver o voto do eleitor anterior.

Antes de cada voto, o mesário deverá liberar o voto para o eleitor. Peça que o mesário indique a ação subsequente. Aceite as seguintes opções (sem mostrar as opções na tela):

- `P` - Liberar votação do próximo eleitor
- `s234f$WR` - Código secreto para fechar a urna (finalizar votação)

Ao finalizar, exibir a contagem de votos em cada opção, o percentual de votos válidos (abstenção não conta como _válido_), e o resultado final:

- O total de `SIM` + `NÃO` deve ser maior do que a metade do total de votos. Caso não seja, o resultado é `INDETERMINADO`.
- Caso contrário, o maior vence: `APROVADO` ou `REPROVADO`.

Exemplo:

_(limpa a tela)_

```
--- Urna Eletrônica ---

Plebiscito: Você é a favor da aprovação automática de alunos carecas canhotos?

Aguarde a intervenção do mesário... _
```

Mesário digita `P`:

_(limpa a tela)_

```
--- Urna Eletrônica ---

Você é a favor da aprovação automática de alunos carecas canhotos? S

Você votou "Sim, sou a favor"

Pressione uma tecla para finalizar sua votação... _
```

_(limpa a tela)_

```
--- Urna Eletrônica ---

Aguarde a intervenção do mesário... _
```

Mesário digita `s234f$WR`:

_(limpa a tela)_

```
--- Urna Eletrônica ---

Plebiscito: Você é a favor da aprovação automática de alunos carecas canhotos?

Eleição finalizada com o total de 1 voto(s).

Contagem de votos:
S - Sim, sou a favor         - 1 
N - Não, sou contra          - 0
A - Me abstenho de responder - 0

Votos válidos: 100%

Resultado do plebiscito: APROVADO
```

---
## Exercício `Potencia`

Receba dois números positivos informados pelo usuário, base e expoente. Calcule o valor do primeiro número elevado ao segundo número. Não utilize `Math.Pow`.

---
## Exercício `AmortizacaoConstante`

Simule um financiamento utilizando o sistema de amortização constante (Tabela SAC). Nessa modalidade, é pago um valor fixo a cada mês, acrescidos os juros sobre o saldo devedor anterior. Na prática, a prestação é menor a cada período.

Receba o valor total do financiamento (`Principal`), a quantidade de meses (`Períodos`) e a taxa de juros (`Taxa`). Exiba uma tabela com período, amortização, juros, prestação, valor pago e saldo devedor.

Valor constante em todos os períodos:
- `Amortização` = `Principal` / `Períodos`

Valores variáveis por período:
- `Juros` = (`SaldoDevedor` do período anterior) * `Taxa`
- `Prestação` = `Amortização` + `Juros`
- `ValorPago` = Soma dos valores de todas as prestações anteriores
- `SaldoDevedor` = `Principal` - `Amortização`

Exemplo:
```
--- Tabela SAC ---

Principal (em R$)..: 1000,00
Períodos...........: 4
Taxa (em %)........: 5
```

Período | Amortização | Juros | Prestação | Valor Pago | Saldo Devedor
--- | --- | --- | --- | --- | ---
0 |  |  |  |  | 1000,00
1 | 250,00 | 50,00 | 300,00 | 300,00 | 750,00
2 | 250,00 | 37,50 | 287,50 | 587,50 | 500,00
3 | 250,00 | 25,00 | 275,00 | 862,50 | 250,00
4 | 250,00 | 12,50 | 262,50 | 1125,00 | 0,00

Você pode simular valores para teste [aqui](https://ermogenes.github.io/sac-price-js/).

---
## Exercício `AmortizacaoFrancesa`

Simule um financiamento utilizando o sistema de amortização francês (Tabela PRICE). Nessa modalidade, é paga uma prestação fixa a cada mês. Os juros são rateados a cada período de forma que o valor da prestação se mantenha sempre igual.

Receba o valor total do financiamento (`Principal`), a quantidade de meses (`Períodos`) e a taxa de juros (`Taxa`). Exiba uma tabela com período, prestação, juros, amortização, valor pago e saldo devedor.

Valor constante em todos os períodos:
- `CoeficientePrice` = [(1 + `Taxa`)<sup>`Períodos`</sup> x `Taxa`] / [(1 + `Taxa`)<sup>`Períodos`</sup> - 1]
- `Prestação` = `Principal` x `CoeficientePrice`

Valores variáveis por período:
- `Juros` = (`SaldoDevedor` do período anterior) * `Taxa`
- `Amortização` = `Prestação` - `Juros`
- `ValorPago` = Soma dos valores de todas as prestações anteriores
- `SaldoDevedor` = `Principal` - `Amortização`

Exemplo:
```
--- Tabela PRICE ---

Principal (em R$)..: 1000,00
Períodos...........: 4
Taxa (em %)........: 5
```

Período | Prestação | Juros | Amortização | Valor Pago | Saldo Devedor
--- | --- | --- | --- | --- | ---
0 |  |  |  |  | 1000,00
1 | 282,01 | 50,00 | 232,01 | 282,01 | 767,99
2 | 282,01 | 38,40 | 243,61 | 564,02 | 524,38
3 | 282,01 | 26,22 | 255,79 | 846,04 | 268,58
4 | 282,01 | 13,43 | 268,58 | 1128,05 | 0,00


Você pode simular valores para teste [aqui](http://drcalc.net/price.asp).

# Exercícios: Arranjos

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[InverteString](#Exercício-InverteString) | _em breve_ | 
[Palindromo](#Exercício-Palindromo) | _em breve_ | 

---
## Exercício `InverteString`

Receba uma string. Exiba a string reversa (do final para o início).

Exemplo:

```
--- Inversor de strings ---

Digite algo: Olá Mundo

Reverso:
odnuM álO
```

Dica: use o método `ToCharArray()` para converter uma string em um `char[]`.

---
## Exercício `Palindromo`

Um palíndromo é uma palavra ou frase que se pode ler, indiferentemente, da esquerda para a direita ou vice-versa.

Exemplos: osso, arara, Ana, reviver, omissíssimo (superlativo de omisso, a maior da língua portuguesa), "a base do teto desaba", "a dama amada", "a mala na lama", "assim a aia ia à missa", "a cara rajada da jararaca", "socorram-me, subi no ônibus em Marrocos", "[Sator Arepo Tenet Opera Rotas](https://en.wikipedia.org/wiki/Sator_Square)" (_o semeador, com o seu carro, mantém com destreza as rodas_, em latim), "Was it a car or a cat I saw?" (_Foi um carro ou um gato que eu vi?_, em inglês).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Sator_Square_at_Opp%C3%A8de.jpg/485px-Sator_Square_at_Opp%C3%A8de.jpg)

Faça um programa que receba uma frase e avalie se ela é um palíndromo ou não.

Dica: Antes de verificar se é um palíndromo remova pontuações, espaços e caracteres especiais, converta letras acentuadas em suas versões sem acentuação e transforme as letras para um caso único (minúsculas, por exemplo).

# Exercícios: Classes

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[xxxxxxx](#Exercício-xxxxxxx) | _em breve_ | 

# Exercícios: Listas

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

Enunciado | Correção | Extras
--- | --- | ---
[BateriaSurf](#Exercício-BateriaSurf) | _em breve_ | 

## Exercício `BateriaSurf`

Faça um programa que calcule a nota de um surfista em uma bateria.

A nota de um surfista em uma onda surfada é dada por 5 juízes, em valores entre 0 e 10 incluindo decimais. A maior e a menor nota são descartadas, e a nota obtida na onda é dada pela média das notas restantes.

Exemplo: Foram dadas as notas ~~5~~, 8.3, 7.0, ~~10~~ e 8.5. Nota da onda = (8.3 + 7.0 + 8.5)/3 = 7.93

Em uma bateria, um surfista pode pegar quantas ondas conseguir. As duas maiores pontuações serão somadas, constituindo a pontuação final.

Exemplo: O surfista obteve as seguintes notas na sua bateria: ~~7.93~~, 10.0, ~~0.0~~ e 10.0. Pontos na bateria = 20.0

A maior pontuação possível em uma bateria é 20 pontos, situação conhecida como _bateria perfeita_ ([feito atingido somente 8 vezes na história](https://pt.wikipedia.org/wiki/Bateria_perfeita)).

Exiba um aviso caso ocorra uma bateria perfeita.

Exemplo:
```
--- Bateria de Surf ---

-- 1ª onda --
Juiz 1: 5
Juiz 2: 8.3
Juiz 3: 7.0
Juiz 4: 10
Juiz 5: 8.5
Nota obtida = 7.93

Mais uma onda (S/N)? S

-- 2ª onda --
Juiz 1: 9.5
Juiz 2: 10
Juiz 3: 10
Juiz 4: 10
Juiz 5: 10
Nota obtida = 10.00

Mais uma onda (S/N)? S

-- 3ª onda --
Juiz 1: 0
Juiz 2: 0
Juiz 3: 0
Juiz 4: 0
Juiz 5: 0
Nota obtida = 0.00

Mais uma onda (S/N)? S

-- 4ª onda --
Juiz 1: 10
Juiz 2: 10
Juiz 3: 10
Juiz 4: 10
Juiz 5: 10
Nota obtida = 10.00

Mais uma onda (S/N)? N

Pontos na bateria = 20.00

BATERIA PERFEITA!
```

# TODO
sons

https://dfilitto.com.br/desenvolvimento/c-sharp/c-modo-console-musicas-com-o-console-beep/
http://www.dsc.ufcg.edu.br/~jacques/cursos/p2/html/listaexer.htm
