# Exercícios: Sub-rotinas

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

**Temporada 1**

Nenhum exercício disponível.

**Temporada 2**

| Enunciado                                         | Correção                                                                                       | Extras |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ------ |
| [AlarmeFalso](#exercício-alarmefalso)             | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/AlarmeFalso/Program.cs)       |
| [Escada](#exercício-escada)                       | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/Escada/Program.cs)            |
| [FibonacciBinet](#exercício-fibonaccibinet)       | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/HorasExtras/Program.cs)       |
| [HorasExtras](#exercício-horasextras)             | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/HorasExtras/Program.cs)       |
| [RaioETrovao](#exercício-raioetrovao)             | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/RaioETrovao/Program.cs)       |
| [Granizo](#exercício-granizo)                     | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/Granizo/Program.cs)           |
| [AlcoolOuGasolina](#exercício-alcoolougasolina)   | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/AlcoolOuGasolina/Program.cs)  |
| [ColisaoCircular2D](#exercício-colisaocircular2d) | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/ColisaoCircular2D/Program.cs) |

<!-- [ParadoxoDoAniversario](#Exercício-ParadoxoDoAniversario) | _em breve_ | -->

---

## Exercício `AlarmeFalso`

Imagine que um paciente faz um exame para uma doença e recebe um resultado positivo. Tal exame apresenta uma precisão de 87% e a doença incide em 1% da população. O médico, conhecedor de estatística, diz ao paciente que não se preocupe, já que provavelmente é um alarme falso (chances de exatamente 93.7%).

A intuição errada de resultados sem levar em consideração a base de incidência é conhecida como _mito de probabilidade de base_.

Escreva uma função que calcule a probabilidade de um exame médico positivo indicar um alarme falso `f` dados a precisão do exame `p` e a incidência na população `i`.

Usando o [teorema de Bayes](https://pt.wikipedia.org/wiki/Teorema_de_Bayes), temos que `f = (1-p)(1-i) / ( p.i + (1-p)(1-i) )`.

Valores para teste:
`p` | `i` | `f`
--- | --- | ---
0,87 | 0,01 | 0,937
0,999 | 0,01 | 0,09
0,999 | 0,0001 | 0,91

---

## Exercício `Escada`

Uma escada ficará enconstada em uma parede caso forme entre ela e o chão um ângulo menor do que 90˚.

Escreva uma função que calcule a altura alcançada pela escada dados o comprimento da escada (em m) e o ângulo em relação ao chão (em graus).

_Converta o ângulo em graus para radianos, fazendo `(π graus) / 180`._

Para calcular a altura, saiba que o comprimento da escada equivale à razão entre a altura e o seno do ângulo.

Em ![](escada-1.svg), `b = c.senβ`.

Valores para teste:
escada | ângulo | parede
--- | --- | ---
4 | 70 | 3,76
4 | 45 | 2,83
5 | 70 | 4,70

Mais valores de teste [aqui](https://www.calculat.org/pt/area-perimetro/triangulo-retangulo.html).

---

## Exercício `FibonacciBinet`

Escreva uma função que calcule o _n-ésimo_ (1 <= n <= 70) termo da sequência de Fibonnaci utilizando a fórmula de Binet baseada no número de ouro φ (_phi_).

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/451078e3f7c9ae5d67abd6a1e770602d3c9ebc63)

Use a função para listar os [70 primeiros](https://oeis.org/A000045/b000045.txt) termos da sequência.

---

## Exercício `HorasExtras`

Escreva uma função que calcule o salário de um funcionário a partir salário-hora base, o total de horas trabalhadas e número de horas-extras executadas. Considere que cada hora-extra é paga com acréscimo de 40%.

---

## Exercício `RaioETrovao`

Escreva uma função que retorne a distância (em km) entre um observador e o local de queda de um raio. Receba como entrada o tempo decorrido entre o raio e o trovão (em segundos).

Aproxime a velocidade do som para 340,29m/s.

Valores para teste

| Tempo (s) | Distância (km) |
| --------- | -------------- |
| 3         | 1,02087        |
| 6         | 2.04174        |

---

## Exercício `Granizo`

Em 1937, o matemático alemão Lothar Collatz propôs uma [sequência numérica](https://pt.wikipedia.org/wiki/Conjectura_de_Collatz) que seria conhecida posteriormente como **números de granizo**, pois "_como o granizo nas nuvens antes de cair, os números saltam de um lugar ao outro antes de chegar ao 4, 2, 1_". O problema chega sempre ao mesmo ponto, não importa como.

Escreva uma sub-rotina que receba um número inteiro `x` e exiba a sequência de Collatz iniciando em `x`.

- Se `x` é par, divida-o por 2;
- Se `x` é ímpar, multiplique-o por 3 e some 1;
- Repita o processo enquanto `x` for maior que 1.

Saiba mais [aqui](https://www.bbc.com/portuguese/geral-36702054).

---

## Exercício `AlcoolOuGasolina`

Um automóvel _flex_ pode ser abastecido com gasolina ou com etanol (_álcool_). O senso comum diz que é mais vantajoso abastecer com gasolina caso a relação entre os preços seja maior do que 70%. [Esta pesquisa](https://autopapo.uol.com.br/noticia/porcentagem-gasolina-ou-etanol/) diz que o percentual ideal deve ser próximo de 73%.

Escreva uma sub-rotina que retorne a razão entre o preço do etanol e da gasolina (etanol ÷ gasolina). Escreva outra sub-rotina que utilize o resultado da primeira para retornar um booleano indicando se vale a pena ou não abastecer com gasolina (_considere o percentual de 73%_).

Escreva um programa que recebe o valor do etanol e o valor da gasolina. Exiba a razão entre os preços e a recomendação de uso. Utilize as sub-rotinas criadas.

Exemplos:

```
--- Etanol ou Gasolina? ---

Digite o preço do etanol (R$).....: 4,00
Digite o preço da gasolina (R$)...: 6,00

O preço do etanol corresponde a 66,7% do preço da gasolina.

Recomendação: Abasteça com ETANOL.
```

```
--- Etanol ou Gasolina? ---

Digite o preço do etanol (R$).....: 5,20
Digite o preço da gasolina (R$)...: 7,00

O preço do etanol corresponde a 74,3% do preço da gasolina.

Recomendação: Abasteça com GASOLINA.
```

---

## Exercício `ColisaoCircular2D`

Chamamos de algoritmos de detecção de colisão 2D os procedimentos que permitem avaliar se dois objetos em um mesmo plano se sobrepõem. A principal aplicação é a computação gráfica, em especial para simulações de física em jogos.

Escreva uma função que recebe as coordenadas cartesianas e o raio de duas circunferências, que representam o espaço ocupado por dois objetos. Retorne um _booleano_ indicando se os objetos colidem ou não.

Exemplos com os objetos `A` de raio 4 e `B` de raio 2:

Com `A` centrado em `(-2,0)` e `B` centrado em `(4,4)` não há colisão.

<img height="500" src="colisao-circ-1.png" alt="">

Com `A` centrado em `(-2,0)` e `B` centrado em `(2,4)` há colisão.

<img height="570" src="colisao-circ-2.png" alt="">

Saiba mais [aqui](https://developer.mozilla.org/pt-BR/docs/Games/Techniques/2D_collision_detection).

<!--

## Exercício `ParadoxoDoAniversario`

O paradoxo do aniversário afirma que dado um grupo de 23 pessoas escolhidas aleatoriamente, a chance de que duas pessoas terão a mesma data de aniversário é de mais de 50%. Para 57 ou mais pessoas, a probabilidade é maior do que 99%, entretanto, ela não pode ser exatamente 100% exceto que se tenha pelo menos 367 pessoas. Calcular essa probabilidade (e as relacionadas a ela) é o problema do aniversário, apresentado pela primeira vez pelo matemático polonês Richard von Mises (irmão mais novo do famoso economista Ludwig von Mises).

Escreva uma função que calcule a probabilidade de um grupo de tamanho `n` possuir duas ou mais pessoas com a mesma data de aniversário. Desconsidere variações como anos bissextos e gêmeos.

Essa probabilidade é dada por:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/c9d215da459cb58833058a449c2aba29f0d25f25)

Valores para teste:
`n` | `f(n)`
--- | ---
10 | 12%
20 | 41%
23 | 50.7%
30 | 70%
50 | 97%
100 | 99.99996%
200 | 99.9999999999999999999999999998%
367 | 100%
-->

---

## 🏁 Orientações para entrega (alunos do curso presencial)

Confira no Teams o link da tarefa equivalente. Lá você postará o link dos repositórios que você criou, um para cada exercício.

**Repositório de exemplo:**
[Exercício `EtecAB` (Saída em console)](https://github.com/ermogenes/EtecAB)

Exemplo de link a ser postado: `https://github.com/ermogenes/EtecAB`
