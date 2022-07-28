# Exercícios: Arranjos

Para cada exercício abaixo crie um repositório no GitHub contendo uma aplicação console com o nome indicado.

Correção no [GitHub](https://github.com/ermogenes/correcoes-dev-cs).

**Temporada 1**

Nenhum exercício disponível.

**Temporada 2**

| Enunciado                                             | Correção                                                                                         | Extras |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------ |
| [ExibeMatriz](#exercício-exibematriz)                 | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/ExibeMatriz/Program.cs)         |
| [PreencheVetor](#exercício-preenchevetor)             | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/PreencheVetor/Program.cs)       |
| [InverteString](#exercício-invertestring)             | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/InverteString/Program.cs)       |
| [Palindromo](#exercício-palindromo)                   | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/Palindromo/Program.cs)          |
| [Virtudes](#exercício-virtudes)                       | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/Virtudes/Program.cs)            |
| [NoiteDeTerror](#exercício-noitedeterror)             | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/NoiteDeTerror/Program.cs)       |
| [GeradorDeNomes](#exercício-geradordenomes)           | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/GeradorDeNomes/Program.cs)      |
| [Surpresinha](#exercício-surpresinha)                 | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/Surpresinha/Program.cs)         |
| [Mandelbrot](#exercício-mandelbrot)                   | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/Mandelbrot/Program.cs)          |
| [DreamTeam](#exercício-dreamteam)                     | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/DreamTeam/Program.cs)           |
| [DistanciaPercorrida](#exercício-distanciapercorrida) | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/DistanciaPercorrida/Program.cs) |
| [CifraDeCesar](#exercício-cifradecesar)               | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/CifraDeCesar/Program.cs)        |
| [NoThanks](#exercício-nothanks)                       | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/NoThanks/Program.cs)            |
| [RLE](#exercício-rle)                                 | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/RLE/Program.cs)                 |
| [PedraPapelTesoura](#exercício-pedrapapeltesoura)     | [GitHub](https://github.com/ermogenes/correcoes-dev-cs/blob/main/PedraPapelTesoura/Program.cs)   |

---

## Exercício `ExibeMatriz`

Considere a matriz abaixo:

```csharp
string[,] imagem ={
  { " "," "," "," "," "," ","_","_"," "," "," "," "," "," "," " },
  { " ","w"," "," ","c","(",".",".",")","o"," "," "," ","("," " },
  { " "," ","\\","_","_","(","-",")"," "," "," "," ","_","_",")" },
  { " "," "," "," "," "," ","/","\\"," "," "," ","("," "," "," " },
  { " "," "," "," "," ","/","(","_",")","_","_","_",")"," "," " },
  { " "," "," "," "," ","w"," ","/","|"," "," "," "," "," "," " },
  { " "," "," "," "," "," ","|"," ","\\"," "," "," "," "," "," " },
  { " "," "," "," "," ","m"," "," ","m"," "," "," "," "," "," " }
};
```

<!--
      __
 w  c(..)o   (
  \__(-)    __)
      /\   (
     /(_)___)
     w /|
      | \
     m  m
-->

Exiba no console a imagem _ASCII Art_ contida na matriz.

---

## Exercício `PreencheVetor`

Receba um número inteiro. Preencha um vetor com os 100 primeiros números pares a partir do número digitado. Exiba os 5 primeiros e os 5 últimos números.

Exemplo:

```
--- Preenche Vetor ---

Digite um número: 523

524 526 528 530 532 (...) 714 716 718 720 722
```

---

## Exercício `InverteString`

Receba uma string. Exiba a string reversa (do final para o início).

Exemplo:

```
--- Inversor de strings ---

Digite algo: Olá Mundo

odnuM álO
```

Dicas: use o método `ToCharArray()` para converter uma string em um `char[]`. Use `String.Join("", <char[]>)` para fazer o processo inverso.

---

## Exercício `Palindromo`

Um palíndromo é uma palavra ou frase que se pode ler, indiferentemente, da esquerda para a direita ou vice-versa.

Exemplos: osso, arara, Ana, reviver, omissíssimo (superlativo de omisso, a maior da língua portuguesa), "a base do teto desaba", "a dama amada", "a mala na lama", "assim a aia ia à missa", "a cara rajada da jararaca", "socorram-me, subi no ônibus em Marrocos", "[Sator Arepo Tenet Opera Rotas](https://en.wikipedia.org/wiki/Sator_Square)" (_o semeador, com o seu carro, mantém com destreza as rodas_, em latim), "Was it a car or a cat I saw?" (_Foi um carro ou um gato que eu vi?_, em inglês).

![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Sator_Square_at_Opp%C3%A8de.jpg/485px-Sator_Square_at_Opp%C3%A8de.jpg)

Faça um programa que receba uma frase e avalie se ela é um palíndromo ou não.

Dica: Antes de verificar se é um palíndromo remova pontuações e espaços, converta letras acentuadas em suas versões sem acentuação e transforme as letras para um caso único (minúsculas, por exemplo).

---

## Exercício `Virtudes`

André Comte-Sponville enumera¹ 18 virtudes:

- a polidez;
- a fidelidade;
- a prudência;
- a temperança;
- a coragem;
- a justiça;
- a generosidade;
- a compaixão;
- a misericórdia;
- a gratidão;
- a humildade;
- a simplicidade;
- a tolerância;
- a pureza;
- a doçura;
- a boa-fé;
- o humor;
- o amor.

Faça um programa que sorteie três virtudes e exiba o "conselho do dia" no formato `Pratique <virtude1> e cultive <virtude2>, sem esperar em troca <virtude3>`.

¹ Pequeno Tratado das Grandes Virtudes, França, 1995. Publicado no Brasil pela [Martins Fontes](https://www.martinsfontespaulista.com.br/pequeno-tratado-das-grandes-virtudes-776504/p).

---

## Exercício `NoiteDeTerror`

Em uma noite de terror, os monstros buscam suas vítimas após ouvir o chamado das estrelas.

Descubra qual o mostro que perseguirá a vítima de acordo com uma data de nascimento e a tabela abaixo.

| Nome      | Mês de nascimento |
| --------- | ----------------- |
| Janeiro   | O Zumbi           |
| Fevereiro | O Assassino       |
| Março     | O Psicopata       |
| Abril     | O Alienígena      |
| Maio      | O Carniceiro      |
| Junho     | O Matador         |
| Julho     | O Vampiro         |
| Agosto    | O Maluco          |
| Setembro  | O Vingador        |
| Outubro   | O Monstro         |
| Novembro  | O Bruxo           |
| Dezembro  | O Demônio         |

| Sobrenome | Dia de nascimento |
| --------- | ----------------- |
| 1         | Endiabrado        |
| 2         | Radioativo        |
| 3         | Endemoniado       |
| 4         | Vermelho          |
| 5         | Possuído          |
| 6         | Macabro           |
| 7         | Sombrio           |
| 8         | Sem Cabeça        |
| 9         | Desconhecido      |
| 10        | Inconsciente      |
| 11        | Oculto            |
| 12        | Esquecido         |
| 13        | Lúgubre           |
| 14        | Invocado          |
| 15        | Caído             |
| 16        | Costurado         |
| 17        | Amaldiçoado       |
| 18        | Anormal           |
| 19        | Perturbado        |
| 20        | Sanguinário       |
| 21        | Tenebroso         |
| 22        | Imortal           |
| 23        | Ressuscitado      |
| 24        | do Pântano        |
| 25        | da Encruzilhada   |
| 26        | do Porão          |
| 27        | do Velho Poço     |
| 28        | sem Perdão        |
| 29        | do Cemitério      |
| 30        | da Meia-Noite     |
| 31        | da Lua Cheia      |

Exemplo:

```
--- Noite de Terror ---

Qual o dia de nascimento da vítima (1 a 31): 27
Qual o mês de nascimento da vítima (1 a 12): 5

Fuja! Lá vem O Carniceiro do Velho Poço!
```

---

## Exercício `GeradorDeNomes`

Armazene um arranjo de nomes e um de sobrenomes, com pelo menos 10 itens em cada um deles.

Sorteie e exiba aleatoriamente 5 nomes completos.

Exemplo:

```
--- Gerador de Nomes ---

Vitor Borges
Ana Nascimento
Julia Ramos
Gabriela Costa
Larissa Andrade
```

---

## Exercício `Surpresinha`

Em uma jogada do tipo _Surpresinha_ na Mega-Sena, os números não são escolhidos pelo usuário, e sim aleatoriamente pelo sistema.

Faça um gerador de jogadas _Surpresinha_.

Solicite a quantidade de jogos a sortear:

- Sorteie 6 números por jogada.
- Garanta que não há números repetidos em uma jogada.
- Exiba os números sorteados em ordem crescente.

Exemplo:

```
--- Surpresinha ---

Quantas jogadas? 4

16 - 22 - 40 - 56 - 58 - 60
23 - 30 - 34 - 41 - 46 - 52
12 - 15 - 37 - 54 - 57 - 60
30 - 35 - 40 - 44 - 45 - 56
```

---

## Exercício `Mandelbrot`

Um fractal é um objeto geométrico que pode ser dividido em partes, cada uma das quais semelhante ao objeto original, infinitamente. São encontrados frequentemente na natureza:

Brássica oleracea (brócolis romanescos)

![](https://paisagismodigital.com/Noticias/img/439-000.jpg)

Girassol

![](https://paisagismodigital.com/Noticias/img/439-004.jpg)

Floco de neve

![](https://www.nsf.gov/news/mmg/media/images/Snowflake1.jpg)

Repolho

![](https://paisagismodigital.com/Noticias/img/439-008.jpg)

Pulmões

![](https://www.marcelouva.com.br/wp-content/uploads/2019/08/fractal.png)

Imagens: [PaisagismoDigital](https://paisagismodigital.com/noticias/?id=plantas-matematicas:-os-fractais-na-natureza-|-paisagismo-digital&in=439) e [NSF](https://www.nsf.gov/news/mmg/mmg_disp.jsp?med_id=80874&from=)

Benoit Mandelbrot foi o primeiro a obter imagens em alta qualidade geradas por computador em 1980, baseado no estudo de Robert W. Brooks e Peter Matelski de 1978.

Parte do algoritmo que gera fractais é baseado na geração de números com aquela que ficou conhecida como a série de Mandelbrot:

- o primero número da série é `0`;
- o próximo número da série é o quadrado do item anterior somado com o número `c`.

![](https://static.packt-cdn.com/products/9781787120495/graphics/33907ca6-9f25-439c-bb21-4e0ddbc9272e.jpg)

Faça um programa que preencha um arranjo com os 10 primeiros números da série de Mandelbrot para um número `c` informado pelo usuário (aceite números reais no intervalo `0 > c >= 10`).

Exiba o arranjo.

Exemplo:

```
--- Série de Mandelbrot ---

Entre com o valor de [c] (entre 0 e 10)...:1

Para c = 1:

z(0) = 0,0000
z(1) = 1,0000
z(2) = 2,0000
z(3) = 5,0000
z(4) = 26,0000
z(5) = 677,0000
z(6) = 458.330,0000
z(7) = 210.066.388.901,0000
z(8) = 44.127.887.745.906.175.377.408,0000
z(9) = 1.947.270.476.915.296.285.689.291.011.464.375.055.838.871.552,0000
```

Saiba mais [aqui](https://pt.wikipedia.org/wiki/Conjunto_de_Mandelbrot), [aqui](https://pt.wikipedia.org/wiki/Fractal), [aqui](http://galileo.phys.virginia.edu/compfac/courses/practical-c/12.pdf), [aqui](https://rosettacode.org/wiki/Mandelbrot_set), [aqui](https://loiseaujc.github.io/Scientific_Computing_on_a_Laptop/Maths/Mandelbrot/binary_mandelbrot.html) e [aqui](https://www.javatpoint.com/how-to-draw-the-mandelbrot-set-in-python).

---

## Exercício `DreamTeam`

Uma equipe de basquete é formada por 5 jogadores.

Faça um programa para indicação de um time dos sonhos somente com jogadores Top 20 da lista de [75 maiores de todos os tempos da ESPN](https://www.torcedores.com/noticias/2022/02/espn-lista-75-melhores-nba).

Top 20:

- 20 - Elgin Baylor (Ala)
- 19 - Jerry West (Armador)
- 18 - Giannis Antetokounmpo (Ala-pivô)
- 17 - Dirk Nowitzki (Ala-pivô)
- 16 - Stephen Curry (Armador)
- 15 - Moses Malone (Pivô)
- 14 - Julius Erving (Ala)
- 13 - Hakeem Olajuwon (Pivô)
- 12 - Kevin Durant (Ala)
- 11 - Shaquille O’Neal (Pivô)
- 10 - Kobe Bryant (Armador)
- 09 - Oscar Robertson (Armador)
- 08 - Tim Duncan (Ala-pivô)
- 07 - Larry Bird (Ala)
- 06 - Bill Russell (Pivô)
- 05 - Wilt Chamberlain (Pivô)
- 04 - Magic Johnson (Armador)
- 03 - Kareem Abdul Jabbar (Pivô)
- 02 - LeBron James (Ala)
- 01 - Michael Jordan (Armador)

O usuário selecionará os seus preferidos indicando sua posição. Um jogador não pode ser adicionado mais de uma vez.

Ao final, exiba o time escolhido em ordem crescente de posição no Top 75.

Exemplo:

```
--- Time dos Sonhos da NBA ---

Top 20 jogadores:

         1 - Michael Jordan (Armador)
         2 - LeBron James (Ala)
         3 - Kareem Abdul Jabbar (Pivô)
         4 - Magic Johnson (Armador)
         5 - Wilt Chamberlain (Pivô)
         6 - Bill Russell (Pivô)
         7 - Larry Bird (Ala)
         8 - Tim Duncan (Ala-pivô)
         9 - Oscar Robertson (Armador)
        10 - Kobe Bryant (Armador)
        11 - Shaquille O'Neal (Pivô)
        12 - Kevin Durant (Ala)
        13 - Hakeem Olajuwon (Pivô)
        14 - Julius Erving (Ala)
        15 - Moses Malone (Pivô)
        16 - Stephen Curry (Armador)
        17 - Dirk Nowitzki (Ala-pivô)
        18 - Giannis Antetokounmpo (Ala-pivô)
        19 - Jerry West (Armador)
        20 - Elgin Baylor (Ala)

0 jogador(es) selecionados. Adicionar o Top # 1
1 jogador(es) selecionados. Adicionar o Top # 10
2 jogador(es) selecionados. Adicionar o Top # 2
3 jogador(es) selecionados. Adicionar o Top # 1
Atleta já incluído no seu time.
3 jogador(es) selecionados. Adicionar o Top # 4
4 jogador(es) selecionados. Adicionar o Top # 25
Entrada inválida.
4 jogador(es) selecionados. Adicionar o Top # 11

Seu time dos sonhos é:

         1 - Michael Jordan (Armador)
         2 - LeBron James (Ala)
         4 - Magic Johnson (Armador)
        10 - Kobe Bryant (Armador)
        11 - Shaquille O'Neal (Pivô)
```

---

## Exercício `DistanciaPercorrida`

O quadro abaixo indica as distâncias rodoviárias entre as capitais do sudeste brasileiro (em km):

| Origem / Destino   | Belo Horizonte | Rio de Janeiro | São Paulo | Vitória |
| ------------------ | -------------- | -------------- | --------- | ------- |
| **Belo Horizonte** | 0              | 434            | 586       | 524     |
| **Rio de Janeiro** | 434            | 0              | 429       | 521     |
| **São Paulo**      | 586            | 429            | 0         | 882     |
| **Vitória**        | 524            | 521            | 882       | 0       |

Considere a codificação 0 = Belo Horizonte, 1 = Rio de Janeiro, 2 = São Paulo e 3 = Vitória, e crie uma matriz contendo o quadro de distâncias.

Solicite que o usuário digite uma sequência de números entre 0 e 3, indicando uma rota percorrida em uma viagem. Por exemplo, a entrada `1,2,0,1` indica uma viagem partindo do Rio de Janeiro, passando por São Paulo e Belo Horizonte e voltando ao Rio.

Exiba a distância percorrida na viagem.

Exemplo:

```
--- Distância Percorrida ---

0 = Belo Horizonte
1 = Rio de Janeiro
2 = São Paulo
3 = Vitória

Digite o percurso (ex.: 1,2,0,1): 1,2,0,1

429km de Rio de Janeiro a São Paulo
586km de São Paulo a Belo Horizonte
434km de Belo Horizonte a Rio de Janeiro

1449km percorridos.
```

---

## Exercício `CifraDeCesar`

A [Cifra de César](https://pt.wikipedia.org/wiki/Cifra_de_C%C3%A9sar) é uma das mais simples e conhecidas técnicas de criptografia. É um tipo de cifra de substituição na qual cada letra do texto é substituída por outra, que se apresenta no alfabeto abaixo dela um número fixo de vezes. Por exemplo, com uma troca de três posições, A seria substituído por D, B se tornaria E, e assim por diante. O nome do método é em homenagem a Júlio César, que o usou para se comunicar com os seus generais.

Como há 26 letras (2 × 13) no alfabeto latino básico, [ROT13](https://pt.wikipedia.org/wiki/ROT13) (_ROTacionar 13 vezes_) é sua própria inversão; isto é, para desfazer ROT13, o mesmo algoritmo é aplicado, então a mesma ação pode ser usada para codificação e decodificação.

Implemente um programa que cifre/decifre uma string digitada pelo usuário usando ROT13.

Para isso transforme o texto em maiúsculas e substitua cada letra pela letra 13 posições à frente no alfabeto (após `Z` volte para `A`). Repita os demais caracteres na saída (espaços, pontuações, acentuações, etc.).

![](https://datagenetics.com/blog/july42015/rot13.png)

Imagem: [DataGenetics](https://datagenetics.com/blog/july42015/index.html)

Exemplos:

```
ERMOGENES
REZBTRARF

A ETEC ADOLPHO BEREZIN É A MELHOR!
N RGRP NQBYCUB ORERMVA É N ZRYUBE!
```

Mais exemplos [aqui](https://rot13.com/).

---

## Exercício `NoThanks`

Em No Thanks! (Thorsten Gimmler, 2004, lançado no Brasil pela [PaperGames](https://papergames.com.br/no-thanks/)) o baralho é formado por cartas numeradas de 3 a 35. Nesse jogo, a pontuação de uma sequência de cartas é dada pela soma dos valores das cartas, ignorando os valores de cartas imediatamente subsequentes.

Por exemplo, na sequência `8`, `13`, `14`, `15`, `17` não pontuam-se `14` e `15` pois estão presentes seus antecessores diretos. Assim, a pontuação é `8` + `13` + `17` = `38`.

Faça um programa que receba uma sequência com até 10 números inteiros únicos entre 3 e 35. Exiba a pontuação da sequência.

Exemplo:

```
--- No Thanks ---

1º número (-1 para finalizar): 13
2º número (-1 para finalizar): 17
3º número (-1 para finalizar): 8
4º número (-1 para finalizar): 13
Número já está na sequência. Entradas: 13 17 8
4º número (-1 para finalizar): 15
5º número (-1 para finalizar): 14
6º número (-1 para finalizar): 14
Número já está na sequência. Entradas: 13 17 8 15 14
6º número (-1 para finalizar): -1

Sequência: 8 13 14 15 17
Pontos na sequência = 38
```

---

## Exercício `RLE`

O arranjo abaixo contém uma imagem _ASCII Art_ compactada usando a [técnica RLE](https://pt.wikipedia.org/wiki/Codifica%C3%A7%C3%A3o_run-length).

```csharp
int[,] imagem = {
    {  2, 44, 207 },
    { 14, 35,   7 },
    {  2, 44,  49 },
    { 14, 35,  15 },
    {  2, 44,  41 },
    { 14, 35,   5 },
    { 14, 47,   1 },
    {  9, 44,  11 },
    { 14, 40,   1 },
    { 14, 35,   5 },
    {  2, 44,  33 },
    { 14, 35,   7 },
    {  9, 44,  17 },
    { 14, 35,   7 },
    {  2, 44,  25 },
    { 14, 35,  11 },
    { 15, 64,   1 },
    {  2, 44,   1 },
    { 15, 64,   1 },
    {  8, 40,   1 },
    {  8, 47,   1 },
    {  2, 44,   1 },
    { 15, 64,   1 },
    {  2, 44,   1 },
    { 15, 64,   2 },
    {  9, 44,   9 },
    { 14, 35,  10 },
    {  2, 44,  17 },
    {  2, 47,   1 },
    { 14, 35,  12 },
    {  9, 44,  14 },
    {  3, 42,   1 },
    {  8, 47,   1 },
    { 15, 64,   1 },
    {  9, 44,   4 },
    { 14, 35,  12 },
    {  2, 42,   1 },
    {  2, 44,  14 },
    { 14, 35,  12 },
    {  9, 44,  18 },
    { 15, 64,   3 },
    { 14, 35,  12 },
    {  2, 44,  18 },
    { 14, 35,  10 },
    {  9, 44,  18 },
    { 15, 64,   1 },
    { 14, 35,  10 },
    {  2, 44,  25 },
    { 14, 35,   7 },
    {  9, 44,  12 },
    { 15, 64,   1 },
    {  9, 44,   4 },
    { 14, 35,   7 },
    {  2, 44,  33 },
    { 14, 35,   6 },
    {  9, 44,  11 },
    { 14, 35,   6 },
    {  2, 44,  41 },
    { 14, 35,  15 },
    {  2, 44,  49 },
    { 14, 35,   7 },
    {  2, 44, 145 }
};
```

<!--
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,,,,,#######,,,,,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,###############,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,#####/,,,,,,,,,,,(#####,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,#######,,,,,,,,,,,,,,,,,#######,,,,,,,,,,,,,,
,,,,,,,,,,,##########@,@(/,@,@@,,,,,,,,,##########,,,,,,,,,,
,,,,,,,/############,,,,,,,,,,,,,,*/@,,,,############*,,,,,,
,,,,,,,,############,,,,,,,,,,,,,,,,,,@@@############,,,,,,,
,,,,,,,,,,,##########,,,,,,,,,,,,,,,,,,@##########,,,,,,,,,,
,,,,,,,,,,,,,,,#######,,,,,,,,,,,,@,,,,#######,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,######,,,,,,,,,,,######,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,###############,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,,,,,#######,,,,,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
-->

Cada elemento da matriz possui 3 números inteiros:

- A cor para exibição, no formato [ConsoleColor](../content/saida-console.md#mudar-a-cor-da-letra);
- O código ASCII do caractere a ser exibido;
- A quantidade de repetições.

Por exemplo, `{12, 65, 10}` significa uma sequência de 10 caracteres `A` em letra vermelha.

Exiba a imagem no console. A imagem possui 60 caracteres de largura (faça as quebras manualmente).

---

## Exercício `PedraPapelTesoura`

[Jokenpô](https://pt.wikipedia.org/wiki/Pedra,_papel_e_tesoura), também conhecido como _Pedra papel e tesoura_ ou _escoteirinho_, é um jogo de mãos para duas pessoas, onde os jogadores devem simultaneamente esticar a mão, na qual cada um formou um símbolo (que significa pedra, papel ou tesoura). Então, os jogadores comparam os símbolos para decidir quem ganhou, da seguinte forma:

- Pedra ganha da tesoura (quebrando-a).
- Tesoura ganha do papel (cortando-o).
- Papel ganha da pedra (cobrindo-a).

A pedra é simbolizada por um punho fechado; a tesoura, por dois dedos esticados; e o papel, pela mão aberta. Caso dois jogadores façam o mesmo gesto, ocorre um empate, e geralmente se joga de novo até desempatar. Este jogo possui uma única regra: não é permitido mostrar pedra duas vezes seguidas.

Implemente o jogo utilizando as dicas abaixo. Ganha o jogador que primeiro ganhar 5 mãos.

Represente as jogadas usando `0` para pedra, `1` para papel e `2` para tesoura. A jogada humana é feita via teclado e a IA realiza uma jogada aleatória.

A tabela abaixo mapeia as frases a serem exibidas de acordo com as jogadas:

| Jogada  | Pedra                            | Papel                         | Tesoura                         |
| ------- | -------------------------------- | ----------------------------- | ------------------------------- |
| Pedra   | Houve um empate.                 | A pedra é coberta pelo papel. | A pedra quebra a tesoura.       |
| Papel   | O papel cobre a pedra.           | Houve um empate.              | O papel é cortado pela tesoura. |
| Tesoura | A tesoura é quebrada pela pedra. | A tesoura corta o papel.      | Houve um empate.                |

O jogador vitorioso pode ser avaliado a partir da tabela abaixo, onde `1` significa vitória, `0` empate e `-1` derrota:
Resultado | Pedra | Papel | Tesoura
--- | --- | --- | ---
Pedra | 0 | -1 | 1
Papel | 1 | 0 | -1
Tesoura | -1 | 1 | 0

---

## 🏁 Orientações para entrega (alunos do curso presencial)

Confira no Teams o link da tarefa equivalente. Lá você postará o link dos repositórios que você criou, um para cada exercício.

**Repositório de exemplo:**
[Exercício `EtecAB` (Saída em console)](https://github.com/ermogenes/EtecAB)

Exemplo de link a ser postado: `https://github.com/ermogenes/EtecAB`
