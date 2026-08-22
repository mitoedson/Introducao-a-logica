# 📂 Módulo 1: Fundamentos e Conceitos Iniciais

Este material de referência apresenta os conceitos introdutórios e os pilares filosóficos e matemáticos que sustentam a **Lógica Proposicional Clássica**.


## 1. O que é Lógica?
A lógica é o estudo sobre a natureza do raciocínio, do conhecimento e da estruturação abstrata do pensamento. Como disciplina científica, ela investiga os princípios e métodos de inferência, com o objetivo principal de determinar sob quais condições certas conclusões se seguem (são consequências lógicas) de um conjunto de premissas dadas a priori (Mortari, 2016; Beraldo-de-Araújo, 2016).

O foco da lógica formal está na **forma do argumento** e no encadeamento de seus conceitos, e não no conteúdo empírico das sentenças individuais (Mortari, 2016; Beraldo-de-Araújo, 2016).


## 2. Sentenças vs. Proposições

Na lógica clássica bivalente, trabalhamos estritamente com sentenças declarativas completas que expressam proposições (Mortari, 2016; Beraldo-de-Araújo, 2016).

### Proposição (ou Enunciado)
Uma **proposição** é o conteúdo ou significado de um enunciado declarativo que pode ser qualificado univocamente com um de dois valores-verdade: **Verdadeiro (V ou 1)** ou **Falso (F ou 0)** (Mortari, 2016; Beraldo-de-Araújo, 2016).

*   **Exemplos de Proposições:**
    *   "Recife é a capital do Ceará." (Proposição de valor lógico F) (Marietto, 2013).
    *   "O Sol é uma estrela." (Proposição de valor lógico V) (Marietto, 2013).
    *   "$-1 < -7$." (Proposição de valor lógico F) (Marietto, 2013).

### Sentenças Não-Proposicionais
Sentenças que não podem ser valoradas como verdadeiras ou falsas **não expressam proposições** e estão fora do escopo da lógica proposicional clássica (Mortari, 2016; Beraldo-de-Araújo, 2016). Classificam-se em:

1.  **Interrogativas (perguntas):** Desejam obter informação (ex: "Qual o seu nome?") (Marietto, 2013).
2.  **Imperativas (ordens/pedidos):** Expressam ordens, conselhos ou solicitações (ex: "Estude para a prova!") (Marietto, 2013).
3.  **Exclamativas:** Exteriorizam sentimentos ou emoções (ex: "Puxa!") (Marietto, 2013).
4.  **Optativas:** Exprimem um desejo (ex: "Deus te acompanhe!") (Marietto, 2013).
5.  **Auto-referentes (paradoxos lógicos):** Sentenças que se referem ao próprio valor lógico, impossibilitando uma valoração sem contradição (ex: "Esta sentença é falsa") (Mortari, 2016).
6.  **Sentenças Abertas:** Sentenças que contêm variáveis indefinidas cujo valor lógico depende de uma atribuição externa (ex: "$x$ é ímpar") (Marietto, 2013).

### Tratamento de Ambiguidades e Sinonímia
*   **Significado vs. Palavras:** A lógica preocupa-se apenas com o conteúdo semântico do enunciado, não com a ordem ou sequência das palavras. Sentenças na voz ativa ("José comeu o bolo") e na voz passiva ("O bolo foi comido por José") expressam a **mesma proposição** (Mortari, 2016).
*   **Ambiguidade:** Sentenças ambíguas (ex: "Eu vi José com uma luneta") não expressam proposições bem-definidas sem um contexto que clarifique o significado (se José usava a luneta ou se quem o viu a utilizava) (Mortari, 2016).


## 3. Tipos de Proposições

As proposições são estruturadas em dois grandes grupos:

1.  **Proposições Simples (Atômicas ou Átomos):** São aquelas formadas por apenas uma declaração, sem conter nenhuma outra proposição como parte integrante de si mesma (Mortari, 2016; Marietto, 2013). Simbolizam-se por letras minúsculas latinas ($p, q, r, s, t$) (Mortari, 2016).
    *   *Exemplo:* $p$: "Mário foi ao cinema." (Marietto, 2013).
2.  **Proposições Compostas (Moleculares ou Fórmulas):** São obtidas pela combinação de duas ou mais proposições simples conectadas por operadores ou conectivos lógicos (Mortari, 2016). Seu valor lógico final depende inteiramente dos valores-verdade de seus átomos componentes (Mortari, 2016).
    *   *Exemplo:* $p \land q$: "Mário foi ao cinema e Carlos foi ao teatro." (Marietto, 2013).


## 4. Os Três Princípios da Lógica Clássica

O sistema lógico clássico repousa sobre três leis fundamentais do pensamento formuladas originalmente por Aristóteles (Marietto, 2013; Beraldo-de-Araújo, 2016):

### I. Princípio da Identidade
Toda proposição verdadeira é sempre verdadeira (Marietto, 2013). Um conceito ou definição deve permanecer constante ao longo do mesmo raciocínio (Marietto, 2013).
*   **Representação formal:** $\vDash p \to p$ e $\vDash p \leftrightarrow p$ (Marietto, 2013).

### II. Princípio da Não Contradição
Nenhuma proposição pode ser verdadeira e falsa simultaneamente sob o mesmo aspecto (Marietto, 2013). Dito de outra forma, dentre duas proposições contraditórias (onde uma é a negação da outra), pelo menos uma delas é necessariamente falsa (Marietto, 2013).
*   **Representação formal:** $\vDash \neg(p \land \neg p)$ (Marietto, 2013).

### III. Princípio do Terceiro Excluído
Toda proposição ou é verdadeira ou é falsa, não havendo uma terceira possibilidade, meio-termo ou valor indeterminado (Marietto, 2013). Sustenta a visão de um mundo puramente bivalente (Marietto, 2013).
*   **Representação formal:** $\vDash p \lor \neg p$ (Marietto, 2013).


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
*   BERALDO-DE-ARAÚJO, Anderson. **Lógica Dedutiva**. São Bernardo do Campo: UFABC, 2016.
