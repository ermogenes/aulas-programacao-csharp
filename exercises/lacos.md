# Exercícios: Laços

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

**Atenção**: Caso o exercício possua um _desafio_, faça-o somente após concluir o exercício principal. Caso seja um exercício marcado para entrega no curso presencial, não é necessário cumprir os desafios.

---
## Exercício `SequenciaCentena`

Exiba os 100 primeiros números naturais não nulos.

Ex.:
```
1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97 98 99 100
```

---
## Exercício `SequenciaPares`

Receba um número inteiro positivo. Exiba todos os números pares entre zero e o número digitado (inclusive).

Ex.:
```
Números pares entre 0 e ? 15
0 2 4 6 8 10 12 14
```

---
## Exercício `SequenciaLimites`

Receba 2 números inteiros. Se o segundo for menor que o primeiro, exibir uma mensagem de erro. Caso contrário, exibir todos os números inteiros entre eles (inclusive).

Ex.:
```
Início: -3
Fim: 7
-3 -2 -1 0 1 2 3 4 5 6 7
```

---
## Exercício `Tabuada`

Receba um número. Exiba sua tabuada.

Ex.:
```
Tabuada do número: 7

7 x 0 = 0
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
7 x 6 = 42
7 x 7 = 49
7 x 8 = 56
7 x 9 = 63
7 x 10 = 70
```

---
## Exercício `MediaDecimal`

Receba a quantidade de números a serem digitados. Receba a quantidade indicada de números decimais. Exiba a soma e a média entre os valores digitados. Exiba também o maior e o menor número digitado.

Ex.:
```
Quantos números: 4
Número #01: 2,6
Número #02: 8,5
Número #03: 9,47
Número #04: 0,37

Soma...: 20,94
Média..: 5,24
Maior..: 9,47
Menor..: 0,37
```

---
## Exercício `Patinhos`

Exiba a letra da música "_Cinco Patinhos_" (versão brasileira gravada pela Xuxa de "_Five little ducks_" -  _The Wiggles_). Seu programa deve perguntar quantos patinhos o usuário deseja (pelo menos 2).

A canção começa assim:

```
(N) patinhos foram passear
Além das montanhas
Para brincar
A mamãe gritou: Quá, quá, quá, quá
Mas só (N-1) patinhos voltaram de lá.
```

Esse bloco se repete até nenhum patinho voltar. Ao final, todos os patinhos voltam:

```
A mamãe patinha foi procurar
Além das montanhas
Na beira do mar
A mamãe gritou: Quá, quá, quá, quá
E os (N) patinhos voltaram de lá.
```

Ex.:
```
Quantos patinhos? 3

3 patinhos foram passear
Além das montanhas
Para brincar
A mamãe gritou: Quá, quá, quá, quá
Mas só 2 patinhos voltaram de lá.

2 patinhos foram passear
Além das montanhas
Para brincar
A mamãe gritou: Quá, quá, quá, quá
Mas só 1 patinho voltou de lá.

1 patinho foi passear
Além das montanhas
Para brincar
A mamãe gritou: Quá, quá, quá, quá
Mas nenhum patinho voltou de lá.

A mamãe patinha foi procurar
Além das montanhas
Na beira do mar
A mamãe gritou: Quá, quá, quá, quá
E os 3 patinhos voltaram de lá.
```

---
## Exercício `Elefante`

Exiba a letra da música infantil "Um Elefante Incomoda Muita Gente". Comece com 1 elefante e termine na quantidade digitada pelo usuário (um número par maior que 2).

```
1 elefante incomoda muita gente
2 elefantes incomodam incomodam muito mais

3 elefantes incomodam muita gente
4 elefantes incomodam incomodam incomodam incomodam muito mais
```

Ex.:
```
Quantos elefantes: 6

1 elefante incomoda muita gente
2 elefantes incomodam incomodam muito mais

3 elefantes incomodam muita gente
4 elefantes incomodam incomodam incomodam incomodam muito mais

5 elefantes incomodam muita gente
6 elefantes incomodam incomodam incomodam incomodam incomodam incomodam muito mais
```

---
## Exercício `RetPreenchido`

Exiba um retângulo preenchido, com altura e largura digitados pelo usuário (entre 1 e 10).

Ex.:
```
Tamanho do retângulo:
Largura..: 10
Altura...: 4

**********
**********
**********
**********
```

---
## Exercício `RetContorno`

Exiba o contorno de um retângulo, com altura e largura digitados pelo usuário (entre 1 e 10).

Ex.:
```
Tamanho do retângulo:
Largura..: 10
Altura...: 6

**********
*        *
*        *
*        *
*        *
**********
```

---
## Exercício `ASCIITable`

Exiba os caracteres imprimíveis da tabela ASCII (entre 32 e 127).

Ex.:
```
 !"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~
```

_Desafio_: exiba conforme o exemplo:

```
Tabela ASCII - Caracteres Imprimíveis

 Dec    Char    Oct     Hex     | Dec   Char    Oct     Hex     | Dec   Char    Oct     Hex     |
 ---    ----    ---     ---     | ---   ----    ---     ---     | ---   ----    ---     ---     |
 32             40      20      | 33    !       41      21      | 34    "       42      22      |
 35     #       43      23      | 36    $       44      24      | 37    %       45      25      |
 38     &       46      26      | 39    '       47      27      | 40    (       50      28      |
 41     )       51      29      | 42    *       52      2a      | 43    +       53      2b      |
 44     ,       54      2c      | 45    -       55      2d      | 46    .       56      2e      |
 47     /       57      2f      | 48    0       60      30      | 49    1       61      31      |
 50     2       62      32      | 51    3       63      33      | 52    4       64      34      |
 53     5       65      35      | 54    6       66      36      | 55    7       67      37      |
 56     8       70      38      | 57    9       71      39      | 58    :       72      3a      |
 59     ;       73      3b      | 60    <       74      3c      | 61    =       75      3d      |
 62     >       76      3e      | 63    ?       77      3f      | 64    @       100     40      |
 65     A       101     41      | 66    B       102     42      | 67    C       103     43      |
 68     D       104     44      | 69    E       105     45      | 70    F       106     46      |
 71     G       107     47      | 72    H       110     48      | 73    I       111     49      |
 74     J       112     4a      | 75    K       113     4b      | 76    L       114     4c      |
 77     M       115     4d      | 78    N       116     4e      | 79    O       117     4f      |
 80     P       120     50      | 81    Q       121     51      | 82    R       122     52      |
 83     S       123     53      | 84    T       124     54      | 85    U       125     55      |
 86     V       126     56      | 87    W       127     57      | 88    X       130     58      |
 89     Y       131     59      | 90    Z       132     5a      | 91    [       133     5b      |
 92     \       134     5c      | 93    ]       135     5d      | 94    ^       136     5e      |
 95     _       137     5f      | 96    `       140     60      | 97    a       141     61      |
 98     b       142     62      | 99    c       143     63      | 100   d       144     64      |
 101    e       145     65      | 102   f       146     66      | 103   g       147     67      |
 104    h       150     68      | 105   i       151     69      | 106   j       152     6a      |
 107    k       153     6b      | 108   l       154     6c      | 109   m       155     6d      |
 110    n       156     6e      | 111   o       157     6f      | 112   p       160     70      |
 113    q       161     71      | 114   r       162     72      | 115   s       163     73      |
 116    t       164     74      | 117   u       165     75      | 118   v       166     76      |
 119    w       167     77      | 120   x       170     78      | 121   y       171     79      |
 122    z       172     7a      | 123   {       173     7b      | 124   |       174     7c      |
 125    }       175     7d      | 126   ~       176     7e      |

```

---
## Exercício `Fatorial`

Receba um número inteiro positivo. Exiba o seu [fatorial](https://pt.wikipedia.org/wiki/Fatorial).

O fatorial de um número é dado pelo produto entre o número e seus antecessores naturais positivos:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/d1d5bc7b1d7261435336bd75ce881ac70f58e723)

Além disso, há um caso especial:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/22956a0fa255c6c9562eab440f8c23c2954a6cf4)

Ex.:
```
Número: 5
5! = 120
```

_Obs._: O método iterativo para cálculo de fatorial é altamente ineficiente. [Outros algoritmos conhecidos](http://www.luschny.de/math/factorial/FastFactorialFunctions.htm) são mais eficientes.

---
## Exercício `EstimaPi`

Estime o valor de π utilizando o [método de Leibniz](https://pt.wikipedia.org/wiki/F%C3%B3rmula_de_Leibniz_para_%CF%80):

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/564a366471bdc3ca4d5403d3acf90c4370d4145e)

Ex.:
```
-- Estimador do valor de pi pelo método de Leibniz --
Quantas iterações? 1000000
Estimativa: 3,141594
```

_Desafio_: Fixar o número de casas decimais de precisão da estimativa. Dica: verifique o erro entre a estimativa atual e a anterior de forma que a diferença esteja em dígitos menores que a precisão desejada.

Ex.:
```
-- Estimador do valor de pi pelo método de Leibniz --
Quantas casas de precisão (<=10)? 7
Estimativa após 199999997 iterações: 3,1415926486
```

_Desafio 2_: Utilizar [outros métodos](https://en.wikipedia.org/wiki/Approximations_of_%CF%80) mais eficientes.

---
## Exercício `EstimaEuler`

Estime o valor de e (número de Euler), com o número de iterações indicado pelo usuário.

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/2019b8b95ec12a0b8cdc76c92583bc574d37a863)

Ex.:
```
-- Estimador de Euler --
Quantas iterações (<=33)? 33
Estimativa: 2,7182818320
```

---
## Exercício `Fibonacci`

Receba um número inteiro `N`. Exiba os `N` primeiros números da [sequência de Fibonacci](https://pt.wikipedia.org/wiki/Sequ%C3%AAncia_de_Fibonacci).

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/FibonacciBlocks.svg/270px-FibonacciBlocks.svg.png" height="170"><img src="https://upload.wikimedia.org/wikipedia/commons/2/23/Golden_spiral_in_rectangles.png" height="170"><img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/NautilusCutawayLogarithmicSpiral-withGoldenSpiral.jpg" height="170">

Nesta sequência, os dois primeiros números são 0 e 1. Os próximos números são a soma dos dois números anteriores.

```
0
1
0 + 1 = 1
1 + 1 = 2
1 + 2 = 3
2 + 3 = 5
3 + 5 = 8
...
```

Ex.:
```
Sequência de Fibonacci
Quantos termos (>=2)? 21
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597 2584 4181 6765
```

---
## Exercício `MDC`

Calcule o máximo divisor comum entre dois números utilizando o Algoritmo de Euclides (iterativo).

Método: Dados os números `a` e `b`, efetue a divisão e pegue o resto. Se o resto for zero, `a` é o mdc. Senão, `b` é o novo `a`, e o resto é o novo `b`. Repita o processo até que o resto seja zero.

Veja um exemplo de cálculo: https://pt.wikipedia.org/wiki/Algoritmo_de_Euclides#Exemplo

Ex.:
```
Máximo Divisor Comum (método iterativo)
Digite o 1º número (a): 348
Digite o 2º número (b): 156
MDC(a, b) = 12
```

---
## Exercício `SomaDigitos`

Calcule a soma dos dígitos de um número inteiro positivo informado.

Ex.:
```
Digite um número inteiro positivo: 5410587

Dígitos: 7 8 5 0 1 4 5

Soma = 30
```

_Dicas_:

- O resto da divisão de um número por 10 retorna a quantidade de unidades. Ex: `483 % 10 == 3`.
- A divisão inteira de um número por 10 tem o "efeito colateral" de excluir o último dígito. Ex: `483 / 10 == 48`.

---

## 🏁 Orientações para entrega (alunos do curso presencial)

Confira no Teams o link da tarefa equivalente. Lá você postará o link dos repositórios que você criou, um para cada exercício.

**Repositório de exemplo:**
[Exercício `EtecAB` (Saída em console)](https://github.com/ermogenes/EtecAB)

Exemplo de link a ser postado: https://github.com/ermogenes/EtecAB
