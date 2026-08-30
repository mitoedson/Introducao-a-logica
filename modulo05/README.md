# 📂 Módulo 5: Teoria da Argumentação e Validade

Este módulo é a ponte entre a formalização matemática e a argumentação textual de linguagem natural.


## 1. Estrutura de um Argumento

**Definição 1:** Um argumento é um sequência finita de
sentenças, onde:

* Uma delas é considerada a conclusão;
* Enquanto as outras são definidas como suas premissas, que são justificativas para a conclusão.(Marietto, 2013)


**Definição 2:** Um argumento é o encadear de proposições em que se pretende que uma delas (a conclusão) seja justificada, sustentada e antecedida por outras (as premissas). (Marietto, 2013)

**Definição 3:** Chama-se argumento toda a afirmação de que uma dada sequência finita $P_1$, $P_2$, ..., $P_n$ ($n≥1$) de proposições tem como consequência, ou acarreta, uma proposição final Q. (Marietto, 2013)

As proposições $P_1, P_2, ..., P_n$ dizem-se premissas do argumento, e a proposição final Q diz-se a conclusão do argumento. Um argumento de premissas $P_1, P_2, ..., P_n$ e de conclusão Q indica-se por:
$P_1, P_2, ..., P_n \vdash Q$
e se lê de uma das seguintes maneiras:
* $P_1, P_2, ..., P_n$ acarretam Q
* Q decorre de $P_1, P_2, ..., P_n$
* Q se deduz de $P_1, P_2, ..., P_n$
* Q se infere de $P_1, P_2, ..., P_n$

### Estrutura de um argumento:

* Uma proposição apresentada como uma tese, ou uma
conclusão;
* Outras proposições apresentadas como justificativa da tese, ou premissas para a conclusão.

#### Exemplo:

Um argumento que consiste de duas premissas e
uma conclusão chama-se silogismo.

Premissa 1: Se neva, então faz frio<br>
Premissa 2: Está nevando<br>
Conclusão: Logo, está fazendo frio

$$n:\text{Neva},f:\text{Faz frio}\\
\lbrace n→f, n\rbrace \vdash f$$

Obs.: O símbolo ├ (turnstile, ou traço de asserção) significa derivabilidade sintática, provabilidade ou que uma fórmula é consequência dedutiva de outra em um sistema formal. Significa que uma conclusão pode ser provada ou derivada a partir de um conjunto de premissas usando apenas as regras mecânicas de um sistema dedutivo (sem olhar para o significado ou tabela-verdade). (Wikipedia)

### Identificando um argumento:

Há indicadores (palavras ou frases) que servem para
introduzir as premissas de um argumento, como por
exemplo:
* Porque
* Desde que
* Pois que
* Como
* Dado que
* Tanto mais que
* Pela razão de que

Há certos indicadores (palavras ou frases) que servem para introduzir a conclusão de um argumento, como por
exemplo:
* Portanto
* Daí
* Logo
* Assim
* Consequentemente
* Segue-se que
* Podemos inferir

#### Exemplo 1:

Se os objetos de arte são expressivos, então são uma linguagem.

O que é: Uma proposição condicional (Se $P$, então $Q$).

Por que não é um argumento? Ela não afirma que a arte é expressiva, nem que ela é uma linguagem. Ela apenas estabelece uma conexão hipotética entre as duas ideias. Não há pretensão de provar nada.



#### Exemplo 2:
Premissa 1: Porque os objetos de arte são expressivos.<br>
Conclusão: Eles são uma linguagem.

O que é: Um argumento (especificamente, uma forma de Modus Ponens implícito).

Por que é um argumento? Aqui existe uma afirmação factual de partida ("os objetos de arte são expressivos") que é usada como justificativa lógica para sustentar e inferir a conclusão ("Eles são uma linguagem"). A palavra "Porque" funciona como um indicador de premissa.Usando o símbolo $\vdash$ que vimos antes, a estrutura condicional isolada seria apenas uma fórmula matemática: $P \rightarrow Q$. 

Já o segundo exemplo se torna uma dedução formal: 
$\lbrace P, P \rightarrow Q \rbrace \vdash Q$


### Premissas e conclusões
A forma canônica de um argumento baseia-se em enunciar
as premissas em primeiro, e as conclusões no fim.
Mas nem todos argumentos são dispostos dessa maneira.
Pode-se ter a conclusão enunciada em primeiro, e depois
as premissas:

#### Exemplo:
Em uma democracia o pobre tem mais poder do que o rico, porque há mais dos primeiros e a vontade da maioria é suprema.

Premissa 1: Há mais pobres do que ricos<br>
Premissa 2: A vontade da maioria é suprema<br>
Conclusão: Em uma democracia o pobre tem mais poder que
o rico

Nenhuma proposição é isoladamente uma premissa ou
conclusão.

* Só é premissa quando ocorre como pressuposição em um
argumento ou raciocínio.
* Só é conclusão quando ocorre em um argumento em que se
afirma decorrer das proposições pressupostas nesse
argumento.



## 2. Argumento Válido vs. Inválido

**Definição:** Um argumento $P_1, P_2, ..., P_n \vdash Q$ diz-se válido se e somente se a conclusão Q é verdadeira todas as vezes que as premissas $P_1, P_2, ..., P_n$ são verdadeiras.

Em outros termos, um argumento $P_1, P_2, ..., P_n \vdash Q$ é válido se e somente se for V o valor lógico da conclusão Q todas as vezes que as premissas $P_1, P_2, ..., P_n$ tiverem valor lógico V. 


### Argumento válido

*   **Válido:** Um argumento é válido se, e somente se, a verdade das premissas obriga e garante logicamente a verdade da conclusão (Marietto, 2013; Mortari, 2016). Em outras palavras, é impossível que as premissas sejam verdadeiras e a conclusão seja falsa sob a mesma circunstância (Mortari, 2016).

Todo argumento válido goza da seguinte propriedade:
A verdade das premissas é incompatível com a
falsidade da conclusão. Um argumento é válido se a sua conclusão é uma consequência lógica de suas premissas, ou seja, a veracidade da conclusão está implícita na veracidade das premissas.


### Argumento inválido

*   **Inválido (Falácia):** Quando existe pelo menos uma circunstância (interpretação) na qual todas as premissas são verdadeiras e, mesmo assim, a conclusão é falsa. A esse cenário chamamos **Contraexemplo** (Mortari, 2016).

Um argumento é inválido se existe pelo menos uma
interpretação que torna as premissas verdadeiras e a
conclusão falsa.

#### Exemplo:

Premissa 1: Alguns treinadores de futebol ganham mais de 100.000 reais por mês<br>
Premissa 2: Scolari é um treinador de futebol<br>
Conclusão: Logo, Scolari ganha mais de 100.000 reais por mês

Não é válido porque não é impossível que as premissas sejam verdadeiras e a conclusão falsa. Portanto, o argumento é inválido: embora as premissas sejam verdadeiras, a conclusão é falsa.

### Prova dos 9 para definir a validade de um argumento

Consegue imaginar alguma circunstância em que,
considerando as premissas verdadeiras, a conclusão é
falsa?
* Se sim, então o argumento não é válido.
* Se não, então o argumento é válido.

#### Exemplo 1:
Premissa 1: Se eu ganhar sozinho na Sena, fico
milionário <br>
Premissa 2: Ganhei sozinho na Sena<br>
Conclusão: Logo, fiquei milionário

Argumento válido... Porque se as duas premissas forem verdadeiras a conclusão tem que, necessariamente, ser verdadeira

#### Exemplo 2:
Premissa 1: Se eu ganhar sozinho na Sena, fico milionário<br>
Premissa 2: Não ganhei sozinho na Sena<br>
Conclusão: Logo, não fiquei milionário

Argumento inválido... porque mesmo que as
duas premissas sejam verdadeiras a conclusão pode ser falsa (na hipótese, por exemplo, de eu herdar uma fortuna.)



## 3. Argumento Adequado / Correto

Na lógica formal, a validade diz respeito unicamente à forma do argumento e à conexão sintática, e não ao seu conteúdo de fato (Mortari, 2016; Beraldo-de-Araújo, 2016). No entanto, na pragmática filosófica, um argumento é considerado **Adequado (ou Correto/Sólido)** se, e somente se, ele satisfaz simultaneamente duas condições:

1.  Ele é formalmente **válido** (Mortari, 2016).
2.  Todas as suas **premissas são de fato verdadeiras** na realidade prática (Mortari, 2016).

---

Um problema na análise da validade de um argumento
é que não basta simplesmente a conclusão lógica
ser uma verdade.

É preciso que a relação entre as hipóteses e a conclusão façam sentido. Ou seja, o valor da conclusão só deveria ser verdadeiro baseado única é exclusivamente na relação entre as hipóteses e a conclusão.


1. Considere o seguinte argumento:<br>
Alfred Hitchcock só dirigiu filmes de suspense.<br> Cantando na Chuva não é um filme de suspense. <br>Portanto o dia tem 24 horas.

Esse argumento tem duas hipóteses:<br>
p: Alfred Hitchcock só faz filmes de suspense.<br>
q: Cantando na Chuva não é um filme de suspense.<br>
Conclusão: O dia tem 24 horas.

Embora cada hipótese individual, assim como a
conclusão, sejam verdadeiras, não deveríamos
considerar o argumento válido, pois a conclusão é
um fato verdadeiro independente das hipóteses.

2. Exemplo de argumento válido:<br>
Se Alfred Hitchcock é o diretor, então o filme é de suspense. Cantando na Chuva não é um filme de suspense. Portanto Alfred Hitchcock não é o diretor de Cantando na Chuva.

Esse argumento tem duas hipóteses:<br>
p: Se Alfred Hitchcock é o diretor, então o filme é de
suspense.<br>
q: Cantando na Chuva não é um filme de suspense.<br>
Conclusão: Alfred Hitchcock não é o diretor de
Cantando na Chuva.

---

Uma outra questão a ser considerada na análise da
validade de argumentos é que as premissas do
argumento devem ser verdadeiras.

1. Em uma democracia o pobre tem mais poder do
que o rico, porque há mais dos primeiros e a
vontade da maioria é suprema.

Premissa 1: Há mais pobres do que ricos<br>
Premissa 2: A vontade da maioria é suprema<br>
Conclusão: Em uma democracia o pobre tem mais poder que o rico

Este argumento de Aristóteles é válido na
nossa sociedade??

A segunda premissa não é verdadeira. Não
podemos chegar à conclusão, por este argumento, que em uma democracia o pobre tem mais poder que o rico.

2. 1% da população global detém mesma riqueza dos 99%
restantes, diz estudo.
https://www.bbc.com/portuguese/noticias/2016/01/160118_riqueza_estudo_oxfam_fn
1% da população mundial concentra metade de toda a riqueza do planeta
https://brasil.elpais.com/brasil/2015/10/13/economia/1444760736_267255.html.
Seis brasileiros concentram a mesma riqueza que a metade da população mais pobre
https://brasil.elpais.com/brasil/2017/09/22/politica/1506096531_079176.html.


<a href="exercicios_argumentos.md">Exercícios sobre Argumentos</a>


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
*   BERALDO-DE-ARAÚJO, Anderson. **Lógica Dedutiva**. São Bernardo do Campo: UFABC, 2016.

