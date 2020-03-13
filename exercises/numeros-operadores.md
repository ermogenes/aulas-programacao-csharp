# Exercícios da Semana 6 - Números e operadores

Para cada exercício abaixo crie um novo projeto com o template indicado, e o nome indicado.

---

`[console: Soma2Numeros]` Leia 2 números inteiros e exiba o resultado da soma:

```
Cálculo da soma entre dois números.

Digite o primeiro número: 30
Digite o segundo número: 40

Soma: 70
```

---

`[console: MilhasParaKm]` Receba uma medida em milhas e exiba seu equivalente em quilômetros. A medida em km é 1,609 vezes a medida em milhas.

```
Entre com a medida (em milhas): 1
1,609 Km
```

---

`[console: Medidas]` Receba uma medida em metros e exiba seus equivalentes em quilômetros e centímetros.

```
Entre com a medida (em metros): 150

--- Equivalência ---
15000 cm
150 m
0,15 Km
```

---

`[console: AreaTrianguloRet]` Calcule a área de um triângulo retângulo, dados base (b) e altura (h). A área é dada pela metade do produto da base pela altura.

```
Base..: 3
Altura: 5

Área..: 7.5
```

---

`[console: Heron]` Calcule a área de um triângulo qualquer, dadas as medidas dos 3 lados. Exiba o semiperímetro e a área.

Área (A): 

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/bde3239088f69abf01f5c3f487b18d4fd3ae4505)

Semiperímetro (p): metade da soma dos lados

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/08ed8a6e351198e0c4ca8d71fa2e2bc4171e9439)


```
Digite os lados do triângulo desejado.

Lado 1..: 3
Lado 2..: 25
Lado 3..: 26

Semiperímetro..: 27
Área...........: 36
```

Ref.: 
https://pt.wikipedia.org/wiki/Teorema_de_Her%C3%A3o
https://mundoeducacao.bol.uol.com.br/matematica/formula-heron.htm

---

`[console: GrausCF]` Converta uma temperatura digitada pelo usuário em °C para °F.

°F = °C × 1,8 + 32

Ref.: https://pt.wikipedia.org/wiki/Celsius

```
°C = 0
0°C equivalem a 32°F
```

---

`[console: GrausFC]` Converta uma temperatura digitada pelo usuário em °F para °C.

°C = (°F − 32) / 1,8

Ref.: https://pt.wikipedia.org/wiki/Celsius

```
°F = 0
0°F equivalem a -17,78°F
```

---

`[console: MediaAritmetica]` Calcule a média aritmética entre 3 números reais digitados pelo usuário.

```
Média Aritmética de 3 números

Digite o primeiro número: 7
Digite o segundo número: 9
Digite o terceiro número: 5

Média: 7.0
```

---

`[console: VelocMedia]` Calcule a velocidade, a partir da distância (Δd, em metros) e do tempo (Δt, em segundos).

v = Δd / Δt

```
Distância percorrida (m): 100
Tempo gasto (s): 15

Velocidade média: 6 m/s
```

---

`[console: IMC]` Calcule o índice de massa corporal de uma pessoa, dados altura (em m) e peso (em kg).

IMC = peso / altura²

```
Altura (m)..: 2
Peso (kg)...: 80

IMC: 20,0 kg/m²
```

---

`[console: FGTS]` Calcule a parcela do FGTS sobre o salário de um funcionário (8%).

```
Salário (R$)..: 2000,00

FGTS: R$ 160,00
```

---

`[console: JurosSimples]` Calcule o montante final de um investimento a juros simples.

j = c . i . t

m = c + j

```c
Juros simples (j)

Capital [c] (R$).......: 1200,00
Taxa de juros [i] (%)..: 2
Tempo [t] (meses)......: 15

Juros (R$).....: 360,00
Montante (R$)..: 1560,00
```

---

`[console: Projetil]` Um projétil é lançado em um ângulo `θ°` (teta graus) a uma velocidade inicial `v0 m/s`. Calcule, em metros, o alcance máximo `xmax` e a altura máxima atingida `hmax`.

Para isso, precisamos:

1. Da constante `π` (pi) = 3,14159 radianos
1. Da constante `g` = 9,80665 m/s²
1. Converter o ângulo de graus para radianos, como no exemplo: 180° × π/180 = 3rad
1. Aplicar a Equação de Torricelli para o alcance, e
1. Aplicar a equação de Torricelli para a altura.

![](https://github.com/ermogenes/aulas-logica-programacao/raw/master/exercises/lancamento_obliquo.png)

Exemplo:

```c
-- Projétil --

Entre com a velocidade, em m/s..: 30
Entre com o ângulo, em graus....: 30

Alcance........: 79,48 m
Altura máxima..: 11,47 m
```

Ref.: https://alunosonline.uol.com.br/fisica/lancamento-obliquo.html