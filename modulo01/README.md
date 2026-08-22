# 📚 Módulo 1: Fundamentos e Conceitos Iniciais

Este material de referência apresenta os conceitos introdutórios e os pilares filosóficos e matemáticos que sustentam a **Lógica Proposicional Clássica** [8, 35, 214].

## 1. O que é Lógica?
A lógica é o estudo sobre a natureza do raciocínio, do conhecimento e da estruturação abstrata do pensamento [35, 65, 215]. Como disciplina científica, ela investiga os princípios e métodos de inferência, com o objetivo principal de determinar sob quais condições certas conclusões se seguem (são consequências lógicas) de um conjunto de premissas dadas a priori [65, 100, 215]. 

O foco da lógica formal está na **forma do argumento** e no encadeamento de seus conceitos, e não no conteúdo empírico das sentenças individuais [69, 113].


## 2. Sentenças vs. Proposições

Na lógica clássica bivalente, trabalhamos estritamente com sentenças declarativas completas que expressam proposições [12, 35, 203].

### Proposição (ou Enunciado)
Uma **proposição** é o conteúdo ou significado de um enunciado declarativo que pode ser qualificado univocamente com um de dois valores-verdade: **Verdandero (V ou 1)** ou **Falso (F ou 0)** [14, 15, 45, 203].

*   **Exemplos de Proposições:**
    *   "Recife é a capital do Ceará." (Proposição de valor lógico F) [14, 46].
    *   "O Sol é uma estrela." (Proposição de valor lógico V) [55].
    *   "$-1 < -7$." (Proposição de valor lógico F) [63].

### Sentenças Não-Proposicionais
Sentenças que não podem ser valoradas como verdadeiras ou falsas **não expressam proposições** e estão fora do escopo da lógica proposicional clássica [16, 203]. Classificam-se em:

1.  **Interrogativas (perguntas):** Desejam obter informação (ex: "Qual o seu nome?") [9, 37, 45].
2.  **Imperativas (ordens/pedidos):** Expressam ordens, conselhos ou solicitações (ex: "Estude para a prova!") [10, 37, 41].
3.  **Exclamativas:** Exteriorizam sentimentos ou emoções (ex: "Puxa!") [10, 42].
4.  **Optativas:** Exprimem um desejo (ex: "Deus te acompanhe!") [11].
5.  **Auto-referentes (paradoxos lógicos):** Sentenças que se referem ao próprio valor lógico, impossibilitando uma valoração sem contradição (ex: "Esta sentença é falsa") [16, 37, 46].
6.  **Sentenças Abertas:** Sentenças que contêm variáveis indefinidas cujo valor lógico depende de uma atribuição externa (ex: "$x$ é ímpar") [62].

### Tratamento de Ambiguidades e Sinonímia
*   **Significado vs. Palavras:** A lógica preocupa-se apenas com o conteúdo semântico do enunciado, não com a ordem ou sequência das palavras [13]. Sentenças na voz ativa ("José comeu o bolo") e na voz passiva ("O bolo foi comido por José") expressam a **mesma proposição** [13, 43].
*   **Ambiguidade:** Sentenças ambíguas (ex: "Eu vi José com uma luneta") não expressam proposições bem-definidas sem um contexto que clarifique o significado (se José usava a luneta ou se quem o viu a utilizava) [12, 13, 42].


## 3. Tipos de Proposições

As proposições são estruturadas em dois grandes grupos:

1.  **Proposições Simples (Atômicas ou Átomos):** São aquelas formadas por apenas uma declaração, sem conter nenhuma outra proposição como parte integrante de si mesma [19, 49, 123]. Simbolizam-se por letras minúsculas latinas ($p, q, r, s, t$) [19, 49].
    *   *Exemplo:* $p$: "Mário foi ao cinema." [22, 54].
2.  **Proposições Compostas (Moleculares ou Fórmulas):** São obtidas pela combinação de duas ou mais proposições simples conectadas por operadores ou conectivos lógicos [21, 22, 52]. Seu valor lógico final depende inteiramente dos valores-verdade de seus átomos componentes [22, 53].
    *   *Exemplo:* $p \land q$: "Mário foi ao cinema e Carlos foi ao teatro." [22, 54].


## 4. Os Três Princípios da Lógica Clássica

O sistema lógico clássico repousa sobre três leis fundamentais do pensamento formuladas originalmente por Aristóteles [40, 66, 70]:

### I. Princípio da Identidade
Toda proposição verdadeira é sempre verdadeira [18, 48]. Um conceito ou definição deve permanecer constante ao longo do mesmo raciocínio [72].
*   **Representação formal:** $\vDash p \to p$ e $\vDash p \leftrightarrow p$ [1, 57].

### II. Princípio da Não Contradição
Nenhuma proposição pode ser verdadeira e falsa simultaneamente sob o mesmo aspecto [18, 48]. Dito de outra forma, dentre duas proposições contraditórias (onde uma é a negação da outra), pelo menos uma delas é necessariamente falsa [75].
*   **Representação formal:** $\vDash \neg(p \land \neg p)$ [2, 57, 92].

### III. Princípio do Terceiro Excluído
Toda proposição ou é verdadeira ou é falsa, não havendo uma terceira possibilidade, meio-termo ou valor indeterminado [18, 48, 76]. Sustenta a visão de um mundo puramente bivalente [76, 77].
*   **Representação formal:** $\vDash p \lor \neg p$ [3, 57, 92].





