# Exercícios: Decisão e operações lógicas

Para cada exercício abaixo crie um novo projeto com o template indicado, e o nome indicado.

---
## Exercício `Negativo`

`[console: Negativo]` Leia um número inteiro e exiba a mensagem "Você digitou um número negativo." caso o número seja menor que zero.

Ex.:
```
Digite um número: -12
Você digitou um número negativo.
```
ou
```
Digite um número: 12
```
_(nada a exibir)_

---
## Exercício `Sinal`

`[console: Sinal]` Leia um número inteiro e exiba "Negativo", "Zero" ou "Positivo", conforme o caso.

Ex.:
```
Digite um número: 35
Positivo
```
ou
```
Digite um número: -10
Negativo
```
ou
```
Digite um número: 0
Zero
```

---
## Exercício `Divisao`

`[console: Divisao]` Receba um numerador e um denominador. Exiba o resultado da divisão ou "Não é possível dividir por zero.", conforme o caso.

Ex.:
```
Digite o numerador....: 12
Digite o denominador..: 3
12 dividido por 3 é 4.
```
ou
```
Digite o numerador....: 0
Digite o denominador..: 5
0 dividido por 5 é 0.
```
ou
```
Digite o numerador....: 12
Digite o denominador..: 0
Não é possível dividir por zero.
```

---
## Exercício `Media4Notas`

`[console: Media4Notas]` Receba 4 notas, com somente uma casa decimal. Valide se todas estão entre 0.0 e 10.0. Se alguma delas não estiver, exiba "Digite somente notas entre 0 e 10.". Caso todas as notas sejam válidas, calcule a média aritmética das notas. Exiba uma mensagem no seguinte padrão: "Você ficou com média 7,5. Resultado: Aprovado".

Resultados possíveis:

- "Reprovado" para médias menores que 5.0
- "Em recuperação" para médias entre 5.0 e 6.0
- "Aprovado", para médias acima de 6.0

Ex.:
```
-- Média --

Digite as suas notas abaixo.
Nota 1: 5,5
Nota 2: -7,0
Nota 3: 10,5
Nota 4: 9,0

Digite somente notas entre 0 e 10.
```
ou
```
-- Média --

Digite as suas notas abaixo.
Nota 1: 5,5
Nota 2: 7,0
Nota 3: 6,5
Nota 4: 9,0

Você ficou com média 7,0. Resultado: Aprovado
```
ou
```
-- Média --

Digite as suas notas abaixo.
Nota 1: 4,5
Nota 2: 3,0
Nota 3: 6,5
Nota 4: 2,0

Você ficou com média 4,0. Resultado: Reprovado
```
ou
```
-- Média --

Digite as suas notas abaixo.
Nota 1: 5,5
Nota 2: 5,5
Nota 3: 5,5
Nota 4: 5,5

Você ficou com média 5,5. Resultado: Em recuperação
```

---
## Exercício `IMC`

`[console: IMC]` Calcule o Índice de Massa Corporal ([IMC](https://pt.wikipedia.org/wiki/%C3%8Dndice_de_massa_corporal)) do usuário.

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/4db320ff2cde68cebea226fb921247d7ebbfad33)

Exemplo:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/1a06f59b0dcbb140bbe47fe3307752bc3dbdce49)

Exiba a situação, conforme tabela.

Resultado | Situação
--- | ---
Abaixo de 17 | Muito abaixo do peso
Entre 17 e 18,49 | Abaixo do peso
Entre 18,5 e 24,99 | Peso normal
Entre 25 e 29,99 | Acima do peso
Entre 30 e 34,99 | Obesidade I
Entre 35 e 39,99 | Obesidade II (severa)
Acima de 40 | Obesidade III (mórbida)

Ex.:
```
-- Calculadora de IMC --

Digite seu peso em kg...: 90
Digite sua altura em m..: 1,75

Seu IMC é 29,39 kg/m².
Diagnóstico: Acima do peso
```

---
## Exercício `Maior2Numeros`

`[console: Maior2Numeros]` Receba dois números. Exiba o maior.

Ex.:
```
Digite o primeiro número..: 7
Digite o segundo número...: 15
O maior número é 15
```

---
## Exercício `Senha`

`[console: Senha]` Solicite ao usuário que digite a sua senha (uma string). Exiba "Acesso permitido" caso a senha digitada seja `1234abcd`, senão exiba "Acesso negado".

Ex.:
```
Olá, usuário. Por favor, digite sua senha: minha_senha_super_secreta
Acesso negado
```
ou
```
Olá, usuário. Por favor, digite sua senha: 1234abcd
Acesso permitido
```

---
## Exercício `DoadorSangue`

`[console: DoadorSangue]` Solicite a idade do usuário. Avalie se ele pode ser doador de sangue (i.e. possui idade entre 18 e 67 anos). Informe o resultado da avaliação.

Ex.:
```
Qual a sua idade: 35
Você pode ser doador de sangue.
```
ou
```
Qual a sua idade: 12
Você não pode ser doador de sangue.
```
ou
```
Qual a sua idade: 80
Você não pode ser doador de sangue.
```

---
## Exercício `ParImpar`

`[console: ParImpar]` Receba um número. Exiba "par" ou "ímpar", conforme o caso.

_Dica: um número é ímpar caso possua resto ao ser dividido por 2._

Ex.:

```
Digite um número: 17
17 é ímpar
```

---
## Exercício `PesoIdeal`

`[console: PesoIdeal]` Solicite que o usuário digite sua altura e o seu sexo ('M' para masculino, 'F' para feminino). Calcule e exiba seu peso ideal.

- Para homens, altura x 72.7 - 58.0
- Para mulheres, altura x 62.1 - 44.7

Ex.:

```
Digite sua altura em m..........: 1,73
Sexo [M]asculino / [F]eminino...: M
Seu peso ideal é 67,7kg.
```
ou
```
Digite sua altura em m..........: 1,73
Sexo [M]asculino / [F]eminino...: F
Seu peso ideal é 62,7kg.
```

---
## Exercício `AnaliseCredito`

`[console: AnaliseCredito]` Um cliente quer solicitar um empréstimo. Receba o valor solicitado, a quantidade de parcelas desejada e a renda mensal comprovada. Só autorize empréstimos cuja parcela não ultrapasse 30% da renda (desconsidere os juros).

---
## Exercício `HeronSeTriangulo`

`[console: HeronSeTriangulo]` Receba três números decimais maiores que zero. Valide se estes números correspondem aos lados de um triângulo (a). Exiba o tipo do triângulo (b). Exiba a sua área (c).

a. Condição de existência de um triângulo:

Para que se possa construir um triângulo é necessário que a medida de qualquer um dos lados seja menor que a soma das medidas dos outros dois e maior que o valor absoluto da diferença entre essas medidas.

Ou seja, todas as condições abaixo devem ser atendidas:

- `a < (b + c)`
- `a > Math.Abs(b - c)`
- `b < (a + c)`
- `b > Math.Abs(a - c)`
- `c < (a + b)`
- `c > Math.Abs(a - b)`

b. Tipo do triângulo:

- Equilátero: três lado com medidas iguais;
- Escaleno: três lados com medidas diferentes;
- Isósceles: demais triângulos.

c. Área do triângulo pelo Teorema de Heron:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/e66e19b74d5ba900c820c2d99de7f62c0513d916)
![](https://wikimedia.org/api/rest_v1/media/math/render/svg/da3d1cfce6b872d360b302f80de119cb9ef5c210)

Ref.: https://pt.wikipedia.org/wiki/Tri%C3%A2ngulo

---
## Exercício `Bhaskara`

`[console: Bhaskara]` Calcule as raízes de uma equação de segundo grau, utilizando o método de Bhaskara.

Uma equação do segundo grau é dada pela expressão abaixo:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/23e70cfa003f402d108ec04d97983fb62f69536e)

Assim, devemos receber do usuário os valores de `a`, `b` e `c`, e aplicar a fórmula de Bhaskara:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/00c22777378f9c594c71158fea8946f2495f2a28)

Dicas:

- Precisamos validar se o valor de `a` não é zero, porque nesse caso a equação não é do segundo grau.
- Calculamos o discriminante Δ (_delta_):

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/1edcf6fef18bec26bcc7988626af5fa4cea3b0f8)

- Como a raiz quadrada de um número negativo não é um número real, precisamos validar se Δ não é negativo.

- Depois, é só calcular e exibir as duas raízes:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/17d4468eb7385fa759d10bf1c36a7aaf02dc3985)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/9d3cd187aefdeaf0b95243342c3eb9db9009d3b6)

Exemplo 1 (`a == 0`): 

```
-- Equação do segundo grau --
(a): 0
(b): 2
(c): 5

Não é uma equação de segundo grau!
```
Exemplo 2 (`Δ < 0`): 

```
-- Equação do segundo grau --
(a): 1
(b): 2
(c): 3

Como delta = -8,00, a equação não possui raízes reais!
```
Exemplo 3: 

```
-- Equação do segundo grau --
(a): 1
(b): 2
(c): -3

x1 = 1,00 e x2 = -3,00
```

---

## 🏁 Orientações para entrega (alunos do curso presencial)

Confira no Teams o link da tarefa equivalente. Lá você postará o link dos repositórios que você criou, um para cada exercício.

**Repositório de exemplo:**
[Exercício `EtecAB` (Saída em console)](https://github.com/ermogenes/EtecAB)

Exemplo de link a ser postado: https://github.com/ermogenes/EtecAB
