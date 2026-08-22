# Introducao-a-logica
Compreensão da lógica como a ciência que estuda a natureza do raciocínio, do conhecimento e os princípios e métodos de inferência.

## Guia de Referência de Estudos
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

---

## 📂 Módulo 1: Fundamentos e Conceitos Iniciais

Este módulo é dedicado à compreensão conceitual e filosófica da lógica e à definição de seus constituintes mínimos.

### 1. O que é Lógica?
A lógica é a ciência que investiga os princípios e métodos de inferência [105]. Seu objeto principal de estudo é determinar em que condições certas conclusões se seguem (ou não) de um conjunto de suposições ou premissas [85, 105]. Trata-se do estudo formal da natureza do raciocínio e da estruturação abstrata do conhecimento [50, 187, 188].

### 2. Sentenças vs. Proposições
Nem toda sentença emitida na linguagem verbal constitui uma proposição:
*   **Proposição (ou Enunciado):** É uma sentença declarativa (exprime uma afirmação ou negação de um fato) que possui um caráter bivalente, ou seja, pode assumir opcionalmente e unicamente um de dois valores-verdade: **Verdadeiro (V)** ou **Falso (F)** [50].
*   **Sentenças Não-Proposicionais:** Sentenças exclamativas, imperativas (ordens), interrogativas (perguntas) ou expressões sem definição de sujeito (fórmulas abertas como "$x$ é par") não possuem valor lógico clássico determinável e, portanto, ficam fora do cálculo proposicional clássico [50].

As proposições dividem-se em:
*   **Simples (Atômicas):** Expressam uma única ideia indivisível e são representadas por variáveis de proposição ($p, q, r, s, \dots$) [51, 68].
*   **Compostas (Moleculares):** São obtidas através da combinação de duas ou mais proposições simples mediante o uso de conectivos lógicos [68].

### 3. Os Três Princípios da Lógica Clássica
O raciocínio dedutivo clássico repousa sobre três leis fundamentais do pensamento formalizadas desde a Grécia Antiga [15, 89]:
1.  **Princípio da Identidade:** Se uma proposição é verdadeira, ela é verdadeira ($p \to p$ ou $p \leftrightarrow p$, ou $\forall x (x = x)$) [3, 181].
2.  **Princípio da Não Contradição:** Uma proposição não pode ser verdadeira e falsa simultaneamente sob a mesma interpretação ($\sim(p \land \sim p)$) [4, 72].
3.  **Princípio do Terceiro Excluído:** Uma proposição ou é verdadeira ou é falsa; não há uma terceira possibilidade ou meio-termo ($p \lor \sim p$) [5, 72].

---

## 📂 Módulo 2: Cálculo Proposicional e Sintaxe

Este módulo detalha os aspectos formais de construção e representação matemática das sentenças.

### 1. Conectivos Lógicos e Operações
Os conectivos conectam proposições e modificam seus valores lógicos com regras bem definidas [33, 35, 38]:

| Operação | Conectivo Natural | Símbolo Proposicional | Regra de Valoração Semântica |
| :--- | :--- | :---: | :--- |
| **Negação** | não $p$ | $\sim p$ ou $\neg p$ | Inverte o valor lógico da proposição de entrada [33]. |
| **Conjunção** | $p$ e $q$ | $p \land q$ | Verdadeiro apenas se **ambos** forem verdadeiros [35]. |
| **Disjunção Inclusiva** | $p$ ou $q$ | $p \lor q$ | Falso apenas se **ambos** forem falsos [37]. |
| **Disjunção Exclusiva** | ou $p$, ou $q$ | $p \oplus q$ | Verdadeiro se os valores de $p$ e $q$ forem **diferentes** [37]. |
| **Condicional (Implicação)** | se $p$ então $q$ | $p \to q$ | Falso unicamente se o antecedente ($p$) for V e o consequente ($q$) for F [38]. |
| **Bicondicional (Equivalência)**| $p$ se e somente se $q$ | $p \leftrightarrow q$ | Verdadeiro apenas se ambos tiverem o **mesmo valor lógico** [40]. |

### 2. Sintaxe de Fórmulas Bem Formadas (FBF)
As fórmulas são construídas de modo indutivo a partir de um alfabeto de variáveis, constantes de verdade ($true$, $false$), parênteses e conectivos [17, 51]. Uma expressão é uma FBF se e somente se puder ser construída aplicando-se as seguintes regras indutivas [17, 51, 52]:
1. Todo símbolo verdade e símbolo proposicional é uma FBF [52].
2. Se $P$ é uma FBF, então $(\sim P)$ é uma FBF [52].
3. Se $P$ e $Q$ são FBFs, então $(P \land Q)$, $(P \lor Q)$, $(P \to Q)$ e $(P \leftrightarrow Q)$ são FBFs [52].

O **comprimento de uma fórmula** $COMP[H]$ indica seu nível de complexidade indutiva [57]:
*   Se $H$ é um símbolo proposicional/verdade $\to COMP[H] = 1$ [57].
*   Se $H$ é $\sim P \to COMP[\sim P] = COMP[P] + 1$ [57].
*   Se $H$ é $(P \circ Q) \to COMP[P \circ Q] = COMP[P] + COMP[Q] + 1$ [57].

### 3. Ordem de Precedência dos Operadores
Na falta de parênteses, os conectivos devem ser avaliados respeitando a seguinte precedência decrescente [41, 55]:
1.  **Negação** ($\sim$ ou $\neg$) — *Maior prioridade* [41, 55].
2.  **Conjunção** ($\land$) e **Disjunção** ($\lor$) — *Prioridade intermediária* [41, 55].
3.  **Condicional** ($\to$) — *Prioridade inferior* [41, 55].
4.  **Bicondicional** ($\leftrightarrow$) — *Menor prioridade* [41].

---

## 📂 Módulo 3: Propriedades Semânticas das Fórmulas

Estudo da valoração de tabelas-verdade completas sob todas as interpretações possíveis (linhas de entrada).

### 1. Tautologias
Uma fórmula proposicional é uma **tautologia** (representada pelo símbolo $\vDash$) se, e somente se, ela assume o valor Verdadeiro (V) para **todas** as suas interpretações de entrada (todas as linhas na última coluna da tabela-verdade) [1, 2, 3].
*   *Exemplo clássico:* $p \to q \leftrightarrow \sim p \lor q$ [2].

### 2. Contradições
Uma fórmula proposicional é uma **contradição** (ou fórmula insatisfazível/inconsistente) se, e somente se, assume o valor Falso (F) sob qualquer combinação possível de valoração de suas proposições componentes [6, 7].
*   *Exemplo clássico:* $p \leftrightarrow \sim p$ [7].

### 3. Contingências
Uma fórmula é uma **contingência** se assume valores Verdadeiros para certas linhas e Falsos para outras [8]. O valor de uma contingência não é resolvido apenas por análise semântica estrutural, necessitando de observação empírica dos fatos no mundo real [8, 124].
*   *Exemplo clássico:* $p \leftrightarrow (p \land q)$ [8].

---

## 📂 Módulo 4: Equivalências Lógicas e Simplificação

Mapeamento de identidades e transformações axiomáticas de proposições compostas.

### 1. Tabela de Leis de Equivalência Notáveis
Duas fórmulas $G$ e $H$ são semanticamente equivalentes ($G \equiv H$) se a fórmula condicional dupla $G \leftrightarrow H$ for uma tautologia [61, 122].

*   **Comutativas:**
    *   $p \land q \equiv q \land p$ [72]
    *   $p \lor q \equiv q \lor p$ [72]
*   **Associativas:**
    *   $(p \land q) \land r \equiv p \land (q \land r)$ [72]
    *   $(p \lor q) \lor r \equiv p \lor (q \lor r)$ [72]
*   **Distributivas:**
    *   $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$ [72]
    *   $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$ [72]
*   **Leis de De Morgan:**
    *   $\sim(p \land q) \equiv \sim p \lor \sim q$ [26, 72]
    *   $\sim(p \lor q) \equiv \sim p \land \sim q$ [26]
*   **Absorção:**
    *   $p \land (p \lor q) \equiv p$ [80]
    *   $p \lor (p \land q) \equiv p$
*   **Dupla Negação:**
    *   $\sim(\sim p) \equiv p$ [24, 26, 34]
*   **Lei da Condicional:**
    *   $p \to q \equiv \sim p \lor q$ [79]
*   **Regra de Clavius:**
    *   $\sim p \to p \equiv p$ [24]

### 2. Método Dedutivo para Equivalências
Em vez de construir tabelas-verdade com $2^N$ linhas [10], utiliza-se uma sequência ordenada de substituições baseadas nas equivalências axiomáticas conhecidas para demonstrar a equivalência e simplificar fórmulas complexas [27, 28].

*Exemplo de demonstração de $(p \lor q) \land \sim p \equiv \sim p \lor q$ no modelo do repositório [79]:*
1.  $(p \lor q) \land \sim p$ *(Fórmula Inicial)* [79]
2.  $\sim p \land (p \lor q)$ *(Lei da Comutatividade em 1)* [79]
3.  $(\sim p \land p) \lor (\sim p \land q)$ *(Lei da Distributividade em 2)* [79]
4.  $F \lor (\sim p \land q)$ *(Princípio da Não Contradição / Conjunção do Absurdo em 3)* [79]
5.  $\sim p \land q$ *(Lei da Identidade em 4)* [79]

---

## 📂 Módulo 5: Teoria da Argumentação e Validade

Este módulo é a ponte entre a formalização matemática e a argumentação textual de linguagem natural.

### 1. Estrutura de um Argumento
Um argumento é uma estrutura de raciocínio composta por um conjunto finito de declarações iniciais chamadas **Premissas** ($P_1, P_2, \dots, P_n$) que dão sustentação lógica para uma alegação final denominada **Conclusão** ($Q$), denotada formalmente pela assinatura $P_1, P_2, \dots, P_n \vdash Q$ [11, 21].

### 2. Argumento Válido vs. Inválido
*   **Válido:** Um argumento é válido se, e somente se, a verdade das premissas obriga e garante logicamente a verdade da conclusão [21, 107]. Em outras palavras, é impossível que as premissas sejam verdadeiras e a conclusão seja falsa sob a mesma circunstância [107, 138].
*   **Inválido (Falácia):** Quando existe pelo menos uma circunstância (interpretação) na qual todas as premissas são verdadeiras e, mesmo assim, a conclusão é falsa. A esse cenário chamamos **Contraexemplo** [99, 191].

### 3. Argumento Adequado / Correto
Na lógica formal, a validade diz respeito unicamente à forma do argumento e à conexão sintática, e não ao seu conteúdo de fato [110, 188]. No entanto, na pragmática filosófica, um argumento é considerado **Adequado (ou Correto/Sólido)** se, e somente se, ele satisfaz simultaneamente duas condições:
1. Ele é formalmente **válido** [99, 109].
2. Todas as suas **premissas são de fato verdadeiras** na realidade prática [23, 99, 109].

---

## 📂 Módulo 6: Técnicas de Prova e Dedução Natural

Módulo de demonstrações avançadas. O método de dedução natural evita a construção de tabelas-verdade excessivamente extensas para muitos átomos (onde $N$ variáveis necessitam de $2^N$ linhas de tabela) [10, 11].

### 1. Regras de Inferência Clássicas (Primitivas)
As regras de inferência são esquemas clássicos estruturados de argumentos logicamente válidos [43, 47]:

*   **Modus Ponens (MP):**
    $$P \to Q, \quad P \quad \vdash \quad Q$$ [63]
*   **Modus Tollens (MT):**
    $$P \to Q, \quad \sim Q \quad \vdash \quad \sim P$$ [63]
*   **Silogismo Hipotético (SH):**
    $$P \to Q, \quad Q \to R \quad \vdash \quad P \to R$$ [63]
*   **Silogismo Disjuntivo (SD):**
    $$P \lor Q, \quad \sim P \quad \vdash \quad Q$$ [63]
*   **Conjunção (C):**
    $$P, \quad Q \quad \vdash \quad P \land Q$$ [63]
*   **Simplificação (S):**
    $$P \land Q \quad \vdash \quad P$$ [63]
*   **Adição (AD):**
    $$P \quad \vdash \quad P \lor Q$$ [63]

### 2. Técnicas de Prova Sintática
*   **Prova Direta:** Consiste em partir puramente do conjunto de hipóteses/premissas e, linha após linha, aplicar regras de equivalência e inferência básicas até derivar e registrar a conclusão final do teorema [11, 12, 153].
*   **Prova Indireta (Por Contradição / Redução ao Absurdo - RAA):**
    1. Introduz-se temporariamente a negação da conclusão desejada ($\sim Q$) como uma nova hipótese de trabalho [30, 162].
    2. Realiza-se o cálculo proposicional até deduzir um absurdo ou contradição explícita da forma $B \land \sim B$ [30, 162].
    3. Ao atingir o absurdo, descarta-se a hipótese temporária por contradizer os axiomas clássicos, provando que a conclusão $Q$ original é necessariamente verdadeira [30, 64, 162].

---

## 📂 Módulo 7: Lógica de Primeira Ordem (Predicados)

Este módulo trata da expansão do cálculo proposicional clássico para lidar com quantificadores e analisar a estrutura interna das sentenças.

### 1. Limitações da Lógica Proposicional
O cálculo proposicional trata as proposições atômicas de forma fechada e monolítica [135]. Ele é incapaz de analisar propriedades de objetos ou relações individuais (ex: não consegue deduzir de "Todo gato gosta de peixe" e "Miau é um gato" que "Miau gosta de peixe" sem reescrever tudo como átomos desligados) [172].

### 2. Estrutura da Lógica de Predicados
A lógica de primeira ordem decompõe a proposição em:
*   **Indivíduos (Termos/Constantes):** Elementos específicos do universo de discurso ($a, b, c$) [102, 172].
*   **Predicados:** Atributos ou propriedades atribuídas a indivíduos (ex: $P(x)$) [102].
*   **Quantificadores:**
    *   **Universal ($\forall$):** Assegura que todos os indivíduos do universo satisfazem o predicado ("Para todo") [117].
    *   **Existencial ($\exists$):** Assegura que há pelo menos um indivíduo que satisfaz o predicado ("Existe") [117].

---

## 📂 Módulo 8: História, Filosofia e Sistemas Não-Clássicos

Exploração das fronteiras do pensamento lógico clássico e suas evoluções modernas.

### 1. Breve História da Lógica
*   **Aristóteles de Estagira (384 – 322 a.C.):** Considerado o "pai da lógica" [86]. Sua obra reunida no livro ***Órganon*** ("ferramenta") introduziu a teoria clássica dos silogismos [86, 187].
*   **Escola Megárico-Estóica:** Responsável pelo estudo embrionário das conexões e condicionais proposicionais aplicadas a proposições completas (Crisipo e Diodoro Cronos) [115].
*   **Lógica Simbólica Contemporânea:** Desenvolvimento da álgebra lógica por George Boole no século XIX, pavimentando o caminho para o projeto de computadores e portas lógicas [88].

### 2. Críticas e Sistemas Não-Clássicos
Sistemas que contestam, eliminam ou estendem os dogmas bivalentes clássicos:
*   **Lógica Paraconsistente:** Desenvolvida para contornar o "princípio da explosão" (onde uma única contradição colapsa todo o sistema, tornando possível provar qualquer coisa). Ela abriga e tolera contradições locais sem inutilizar a teoria dedutiva [90].
*   **Computação Quântica e Limitações Físicas:** Na escala quântica, a propriedade de sobreposição de estados (qubits que podem estar simultaneamente em estados representados por 0 e 1) desafia a bivalência estrita e empírica do princípio do terceiro excluído absoluto e da não-contradição mecânica macroscópica tradicional [90, 91].
*   **Lógicas Relevantes:** Sistemas que exigem que o antecedente de uma implicação material tenha uma relação de significado e relevância estreita com o consequente, eliminando anomalias matemáticas do cálculo clássico como "se a Terra é plana, então o Sol é uma estrela" [185].

---

> **Nota de Referência Acadêmica:** Este guia de estudos e o respectivo repositório foram projetados com base na ementa e materiais de Lógica Básica (UFABC), compilando definições formais, esquemas de tabelas-verdade e regras sintáticas unificadas.
