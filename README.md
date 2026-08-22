# 📚 Introdução à Lógica: Guia de Referência de Estudos

Bem-vindo ao repositório de referência de estudos sobre **Lógica Clássica Proposicional, Técnicas de Demonstração e Introdução a Sistemas Não-Clássicos**. Este roteiro serve de base para estruturar um repositório no GitHub completo, organizado em módulos de aprendizado progressivo, fundamentado diretamente nos materiais didáticos de Lógica Básica.

## 🗺️ Sumário

*   [Módulo 1: Fundamentos e Conceitos Iniciais](#-módulo-1-fundamentos-e-conceitos-iniciais)
*   [Módulo 2: Cálculo Proposicional e Sintaxe](#-módulo-2-cálculo-proposicional-e-sintaxe)
*   [Módulo 3: Propriedades Semânticas das Fórmulas](#-módulo-3-propriedades-semânticas-das-fórmulas)
*   [Módulo 4: Equivalências Lógicas e Simplificação](#-módulo-4-equivalências-lógicas-e-simplificação)
*   [Módulo 5: Teoria da Argumentação e Validade](#-módulo-5-teoria-da-argumentação-e-validade)
*   [Módulo 6: Técnicas de Prova e Dedução Natural](#-módulo-6-técnicas-de-prova-e-dedução-natural)
*   [Módulo 7: Lógica de Primeira Ordem (Predicados)](#-módulo-7-lógica-de-primeira-ordem-predicados)
*   [Módulo 8: História, Filosofia e Sistemas Não-Clássicos](#-módulo-8-história-filosofia-e-sistemas-não-clássicos)

## 📂 Módulo 1: Fundamentos e Conceitos Iniciais

Este módulo é dedicado à compreensão conceitual e filosófica da lógica e à definição de seus constituintes mínimos.

### 1. O que é Lógica?
A lógica é a ciência que investiga os princípios e métodos de inferência. Seu objeto principal de estudo é determinar em que condições certas conclusões se seguem (ou não) de um conjunto de suposições ou premissas. Trata-se do estudo formal da natureza do raciocínio e da estruturação abstrata do conhecimento (Mortari, 2016).

### 2. Sentenças vs. Proposições
Nem toda sentença emitida na linguagem verbal constitui uma proposição:
*   **Proposição (ou Enunciado):** É uma sentença declarativa (exprime uma afirmação ou negação de um fato) que possui um caráter bivalente, ou seja, pode assumir opcionalmente e unicamente um de dois valores-verdade: **Verdadeiro (V)** ou **Falso (F)** (Mortari, 2016).
*   **Sentenças Não-Proposicionais:** Sentenças exclamativas, imperativas (ordens), interrogativas (perguntas) ou expressões sem definição de sujeito (fórmulas abertas como "$x$ é par") não possuem valor lógico clássico determinável e, portanto, ficam fora do cálculo proposicional clássico (Mortari, 2016).

As proposições dividem-se em:
*   **Simples (Atômicas):** Expressam uma única ideia indivisível e são representadas por variáveis de proposição ($p, q, r, s, \dots$) (Marietto, 2013).
*   **Compostas (Moleculares):** São obtidas através da combinação de duas ou mais proposições simples mediante o uso de conectivos lógicos (Marietto, 2013).

### 3. Os Três Princípios da Lógica Clássica
O raciocínio dedutivo clássico repousa sobre três leis fundamentais do pensamento formalizadas desde a Grécia Antiga (Mortari, 2016):
1.  **Princípio da Identidade:** Se uma proposição é verdadeira, ela é verdadeira ($p \to p$ ou $p \leftrightarrow p$, ou $\forall x (x = x)$) (Mortari, 2016).
2.  **Princípio da Não Contradição:** Uma proposição não pode ser verdadeira e falsa simultaneamente sob a mesma interpretação ($\sim(p \land \sim p)$) (Mortari, 2016).
3.  **Princípio do Terceiro Excluído:** Uma proposição ou é verdadeira ou é falsa; não há uma terceira possibilidade ou meio-termo ($p \lor \sim p$) (Mortari, 2016).


## 📂 Módulo 2: Cálculo Proposicional e Sintaxe

Este módulo detalha os aspectos formais de construção e representação matemática das sentenças.

### 1. Conectivos Lógicos e Operações
Os conectivos conectam proposições e modificam seus valores lógicos com regras bem definidas (Marietto, 2013):

| Operação | Conectivo Natural | Símbolo Proposicional | Regra de Valoração Semântica |
| :--- | :--- | :---: | :--- |
| **Negação** | não $p$ | $\sim p$ ou $\neg p$ | Inverte o valor lógico da proposição de entrada (Marietto, 2013). |
| **Conjunção** | $p$ e $q$ | $p \land q$ | Verdadeiro apenas se **ambos** forem verdadeiros (Marietto, 2013). |
| **Disjunção Inclusiva** | $p$ ou $q$ | $p \lor q$ | Falso apenas se **ambos** forem falsos (Marietto, 2013). |
| **Disjunção Exclusiva** | ou $p$, ou $q$ | $p \oplus q$ | Verdadeiro se os valores de $p$ e $q$ forem **diferentes** (Marietto, 2013). |
| **Condicional (Implicação)** | se $p$ então $q$ | $p \to q$ | Falso unicamente se o antecedente ($p$) for V e o consequente ($q$) for F (Marietto, 2013). |
| **Bicondicional (Equivalência)**| $p$ se e somente se $q$ | $p \leftrightarrow q$ | Verdadeiro apenas se ambos tiverem o **mesmo valor lógico** (Marietto, 2013). |

### 2. Sintaxe de Fórmulas Bem Formadas (FBF)
As fórmulas são construídas de modo indutivo a partir de um alfabeto de variáveis, constantes de verdade ($true$, $false$), parênteses e conectivos (Marietto, 2013; Martins, [201-]). Uma expressão é uma FBF se e somente se puder ser construída aplicando-se as seguintes regras indutivas (Marietto, 2013; Martins, [201-]):
1. Todo símbolo verdade e símbolo proposicional é uma FBF (Marietto, 2013; Martins, [201-]).
2. Se $P$ é uma FBF, então $(\sim P)$ é uma FBF (Marietto, 2013; Martins, [201-]).
3. Se $P$ e $Q$ são FBFs, então $(P \land Q)$, $(P \lor Q)$, $(P \to Q)$ e $(P \leftrightarrow Q)$ são FBFs (Marietto, 2013; Martins, [201-]).

O **comprimento de uma fórmula** $COMP[H]$ indica seu nível de complexidade indutiva (Marietto, 2013; Martins, [201-]):
*   Se $H$ é um símbolo proposicional/verdade $\to COMP[H] = 1$ (Marietto, 2013; Martins, [201-]).
*   Se $H$ é $\sim P \to COMP[\sim P] = COMP[P] + 1$ (Marietto, 2013; Martins, [201-]).
*   Se $H$ é $(P \circ Q) \to COMP[P \circ Q] = COMP[P] + COMP[Q] + 1$ (Marietto, 2013; Martins, [201-]).

### 3. Ordem de Precedência dos Operadores
Na falta de parênteses, os conectivos devem ser avaliados respeitando a seguinte precedência decrescente (Marietto, 2013):
1.  **Negação** ($\sim$ ou $\neg$) — *Maior prioridade* (Marietto, 2013).
2.  **Conjunção** ($\land$) e **Disjunção** ($\lor$) — *Prioridade intermediária* (Marietto, 2013).
3.  **Condicional** ($\to$) — *Prioridade inferior* (Marietto, 2013).
4.  **Bicondicional** ($\leftrightarrow$) — *Menor prioridade* (Marietto, 2013).

## 📂 Módulo 3: Propriedades Semânticas das Fórmulas

Estudo da valoração de tabelas-verdade completas sob todas as interpretações possíveis (linhas de entrada).

### 1. Tautologias
Uma fórmula proposicional é uma **tautologia** (representada pelo símbolo $\vDash$) se, e somente se, ela assume o valor Verdadeiro (V) para **todas** as suas interpretações de entrada (todas as linhas na última coluna da tabela-verdade) (Marietto, 2013).
*   *Exemplo clássico:* $p \to q \leftrightarrow \sim p \lor q$ (Marietto, 2013).

### 2. Contradições
Uma fórmula proposicional é uma **contradição** (ou fórmula insatisfazível/inconsistente) se, e somente se, assume o valor Falso (F) sob qualquer combinação possível de valoração de suas proposições componentes (Marietto, 2013).
*   *Exemplo clássico:* $p \leftrightarrow \sim p$ (Marietto, 2013).

### 3. Contingências
Uma fórmula é uma **contingência** se assume valores Verdadeiros para certas linhas e Falsos para outras (Marietto, 2013). O valor de uma contingência não é resolvido apenas por análise semântica estrutural, necessitando de observação empírica dos fatos no mundo real (Marietto, 2013).
*   *Exemplo clássico:* $p \leftrightarrow (p \land q)$ (Marietto, 2013).


## 📂 Módulo 4: Equivalências Lógicas e Simplificação

Mapeamento de identidades e transformações axiomáticas de proposições compostas.

### 1. Tabela de Leis de Equivalência Notáveis
Duas fórmulas $G$ e $H$ são semanticamente equivalentes ($G \equiv H$) se a fórmula condicional dupla $G \leftrightarrow H$ for uma tautologia (Marietto, 2013).

*   **Comutativas:**
    *   $p \land q \equiv q \land p$ (Mortari, 2016)
    *   $p \lor q \equiv q \lor p$ (Mortari, 2016)
*   **Associativas:**
    *   $(p \land q) \land r \equiv p \land (q \land r)$ (Mortari, 2016)
    *   $(p \lor q) \lor r \equiv p \lor (q \lor r)$ (Mortari, 2016)
*   **Distributivas:**
    *   $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$ (Mortari, 2016)
    *   $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$ (Mortari, 2016)
*   **Leis de De Morgan:**
    *   $\sim(p \land q) \equiv \sim p \lor \sim q$ (Martins, [201-])
    *   $\sim(p \lor q) \equiv \sim p \land \sim q$ (Martins, [201-])
*   **Absorção:**
    *   $p \land (p \lor q) \equiv p$ (Martins, [201-])
    *   $p \lor (p \land q) \equiv p$
*   **Dupla Negação:**
    *   $\sim(\sim p) \equiv p$ (Martins, [201-])
*   **Lei da Condicional:**
    *   $p \to q \equiv \sim p \lor q$ (Martins, [201-])
*   **Regra de Clavius:**
    *   $\sim p \to p \equiv p$ (Martins, [201-])

### 2. Método Dedutivo para Equivalências
Em vez de construir tabelas-verdade com $2^N$ linhas (Marietto, 2013), utiliza-se uma sequência ordenada de substituições baseadas nas equivalências axiomáticas conhecidas para demonstrar a equivalência e simplificar fórmulas complexas (Martins, [201-]).

*Exemplo de demonstração de $(p \lor q) \land \sim p \equiv \sim p \lor q$ no modelo do repositório (Martins, [201-]):*
1.  $(p \lor q) \land \sim p$ *(Fórmula Inicial)* (Martins, [201-])
2.  $\sim p \land (p \lor q)$ *(Lei da Comutatividade em 1)* (Martins, [201-])
3.  $(\sim p \land p) \lor (\sim p \land q)$ *(Lei da Distributividade em 2)* (Martins, [201-])
4.  $F \lor (\sim p \land q)$ *(Princípio da Não Contradição / Conjunção do Absurdo em 3)* (Martins, [201-])
5.  $\sim p \land q$ *(Lei da Identidade em 4)* (Martins, [201-])


## 📂 Módulo 5: Teoria da Argumentação e Validade

Este módulo é a ponte entre a formalização matemática e a argumentação textual de linguagem natural.

### 1. Estrutura de um Argumento
Um argumento é uma estrutura de raciocínio composta por um conjunto finito de declarações iniciais chamadas **Premissas** ($P_1, P_2, \dots, P_n$) que dão sustentação lógica para uma alegação final denominada **Conclusão** ($Q$), denotada formalmente pela assinatura $P_1, P_2, \dots, P_n \vdash Q$ (Mortari, 2016).

### 2. Argumento Válido vs. Inválido
*   **Válido:** Um argumento é válido se, e somente se, a verdade das premissas obriga e garante logicamente a verdade da conclusão (Mortari, 2016). Em outras palavras, é impossível que as premissas sejam verdadeiras e a conclusão seja falsa sob a mesma circunstância (Mortari, 2016).
*   **Inválido (Falácia):** Quando existe pelo menos uma circunstância (interpretação) na qual todas as premissas são verdadeiras e, mesmo assim, a conclusão é falsa. A esse cenário chamamos **Contraexemplo** (Mortari, 2016).

### 3. Argumento Adequado / Correto
Na lógica formal, a validade diz respeito unicamente à forma do argumento e à conexão sintática, e não ao seu conteúdo de fato (Mortari, 2016). No entanto, na pragmática filosófica, um argumento é considerado **Adequado (ou Correto/Sólido)** se, e somente se, ele satisfaz simultaneamente duas condições:
1. Ele é formalmente **válido** (Mortari, 2016).
2. Todas as suas **premissas são de fato verdadeiras** na realidade prática (Mortari, 2016).


## 📂 Módulo 6: Técnicas de Prova e Dedução Natural

Módulo de demonstrações avançadas. O método de dedução natural evita a construção de tabelas-verdade excessivamente extensas para muitos átomos (onde $N$ variáveis necessitam de $2^N$ linhas de tabela) (Mortari, 2016; Marietto, 2013).

### 1. Regras de Inferência Clássicas (Primitivas)
As regras de inferência são esquemas clássicos estruturados de argumentos logicamente válidos (Mortari, 2016):

*   **Modus Ponens (MP):**
    $$P \to Q, \quad P \quad \vdash \quad Q$$ (Mortari, 2016)
*   **Modus Tollens (MT):**
    $$P \to Q, \quad \sim Q \quad \vdash \quad \sim P$$ (Mortari, 2016)
*   **Silogismo Hipotético (SH):**
    $$P \to Q, \quad Q \to R \quad \vdash \quad P \to R$$ (Mortari, 2016)
*   **Silogismo Disjuntivo (SD):**
    $$P \lor Q, \quad \sim P \quad \vdash \quad Q$$ (Mortari, 2016)
*   **Conjunção (C):**
    $$P, \quad Q \quad \vdash \quad P \land Q$$ (Mortari, 2016)
*   **Simplificação (S):**
    $$P \land Q \quad \vdash \quad P$$ (Mortari, 2016)
*   **Adição (AD):**
    $$P \quad \vdash \quad P \lor Q$$ (Mortari, 2016)

### 2. Técnicas de Prova Sintática
*   **Prova Direta:** Consiste em partir puramente do conjunto de hipóteses/premissas e, linha após linha, aplicar regras de equivalência e inferência básicas até derivar e registrar a conclusão final do teorema (Mortari, 2016).
*   **Prova Indireta (Por Contradição / Redução ao Absurdo - RAA):**
    1. Introduz-se temporariamente a negação da conclusão desejada ($\sim Q$) como uma nova hipótese de trabalho (Mortari, 2016).
    2. Realiza-se o cálculo proposicional até deduzir um absurdo ou contradição explícita da forma $B \land \sim B$ (Mortari, 2016).
    3. Ao atingir o absurdo, descarta-se a hipótese temporária por contradizer os axiomas clássicos, provando que a conclusão $Q$ original é necessariamente verdadeira (Mortari, 2016).

## 📂 Módulo 7: Lógica de Primeira Ordem (Predicados)

Este módulo trata da expansão do cálculo proposicional clássico para lidar com quantificadores e analisar a estrutura interna das sentenças.

### 1. Limitações da Lógica Proposicional
O cálculo proposicional trata as proposições atômicas de forma fechada e monolítica (Mortari, 2016). Ele é incapaz de analisar propriedades de objetos ou relações individuais (ex: não consegue deduzir de "Todo gato gosta de peixe" e "Miau é um gato" que "Miau gosta de peixe" sem reescrever tudo como átomos desligados) (Mortari, 2016).

### 2. Estrutura da Lógica de Predicados
A lógica de primeira ordem decompõe a proposição em:
*   **Indivíduos (Termos/Constantes):** Elementos específicos do universo de discurso ($a, b, c$) (Mortari, 2016).
*   **Predicados:** Atributos ou propriedades atribuídas a indivíduos (ex: $P(x)$) (Mortari, 2016).
*   **Quantificadores:**
    *   **Universal ($\forall$):** Assegura que todos os indivíduos do universo satisfazem o predicado ("Para todo") (Mortari, 2016).
    *   **Existencial ($\exists$):** Assegura que há pelo menos um indivíduo que satisfaz o predicado ("Existe") (Mortari, 2016).

## 📂 Módulo 8: História, Filosofia e Sistemas Não-Clássicos

Exploração das fronteiras do pensamento lógico clássico e suas evoluções modernas.

### 1. Breve História da Lógica
*   **Aristóteles de Estagira (384 – 322 a.C.):** Considerado o "pai da lógica" (Mortari, 2016). Sua obra reunida no livro ***Órganon*** ("ferramenta") introduziu a teoria clássica dos silogismos (Mortari, 2016).
*   **Escola Megárico-Estóica:** Responsável pelo estudo embrionário das conexões e condicionais proposicionais aplicadas a proposições completas (Crisipo e Diodoro Cronos) (Mortari, 2016).
*   **Lógica Simbólica Contemporânea:** Desenvolvimento da álgebra lógica por George Boole no século XIX, pavimentando o caminho para o projeto de computadores e portas lógicas (Mortari, 2016).

### 2. Críticas e Sistemas Não-Clássicos
Sistemas que contestam, eliminam ou estendem os dogmas bivalentes clássicos:
*   **Lógica Paraconsistente:** Desenvolvida para contornar o "princípio da explosão" (onde uma única contradição colapsa todo o sistema, tornando possível provar qualquer coisa). Ela abriga e tolera contradições locais sem inutilizar a teoria dedutiva (Haack, 2002).
*   **Computação Quântica e Limitações Físicas:** Na escala quântica, a propriedade de sobreposição de estados (qubits que podem estar simultaneamente em estados representados por 0 e 1) desafia a bivalência estrita e empírica do princípio do terceiro excluído absoluto e da não-contradição mecânica macroscópica tradicional (Haack, 2002).
*   **Lógicas Relevantes:** Sistemas que exigem que o antecedente de uma implicação material tenha uma relação de significado e relevância estreita com o consequente, eliminando anomalias matemáticas do cálculo clássico como "se a Terra é plana, então o Sol é uma estrela" (Mortari, 2016).


> **Nota de Referência Acadêmica:** Este guia de estudos e o respectivo repositório foram projetados com base na ementa e materiais de Lógica Básica (UFABC), compilando definições formais, esquemas de tabelas-verdade e regras sintáticas unificadas.



## Referências

Em conformidade com a Associação Brasileira de Normas Técnicas (ABNT NBR 6023:2018 e NBR 10520:2023):

*   HAACK, Susan. **Filosofia das lógicas**. Tradução de Cezar A. Mortari e Luiz Henrique de A. Dutra. São Paulo: Editora Unesp, 2002. 359 p.
*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013. 1 recurso online (slides). Slides de aula da disciplina de Lógica Básica.
*   MARTINS, Luiz Gustavo A. **Lógica proposicional e formas normais**. Uberlândia: Universidade Federal de Uberlândia, [201-]. 1 recurso online (apostila).
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016. 512 p.
