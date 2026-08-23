# 📂 Módulo 2: Cálculo Proposicional e Sintaxe

Este módulo detalha os aspectos formais de construção e representação matemática das sentenças.


# 📂 Módulo 2: Cálculo Proposicional e Sintaxe

Este material de referência apresenta os aspectos formais de construção, análise estrutural e representação matemática das sentenças no âmbito da **Lógica Proposicional Clássica** (Marietto, 2013; Martins, [201-]; Mortari, 2016).

---

## 1. Conectivos Lógicos e Operações

Os conectivos realizam operações sobre proposições, modificando ou combinando seus valores lógicos de acordo com regras matemáticas bem-definidas (Martins, [201-]; Mortari, 2016). Na lógica clássica bivalente, essas operações funcionam como funções veritativas, onde o valor-verdade do enunciado composto é determinado unicamente pelos valores-verdade de suas partes componentes (Marietto, 2013; Mortari, 2016).

Abaixo estão definidos os conectivos lógicos clássicos e suas respectivas regras de valoração semântica:

| Operação | Conectivo Natural | Símbolo Proposicional | Regra de Valoração Semântica |
| :--- | :--- | :---: | :--- |
| **Negação** | não $p$ | $\sim p$ ou $
eg p$ | Inverte o valor lógico da proposição de entrada (Mortari, 2016). |
| **Conjunção** | $p$ e $q$ | $p \land q$ | Verdadeiro apenas se **ambos** os operandos forem verdadeiros (Mortari, 2016). |
| **Disjunção Inclusiva** | $p$ ou $q$ | $p \lor q$ | Falso apenas se **ambos** os operandos forem falsos (Mortari, 2016). |
| **Disjunção Exclusiva** | ou $p$, ou $q$ | $p \oplus q$ | Verdadeiro se os valores das proposições de entrada forem **diferentes** (Marietto, 2013). |
| **Condicional (Implicação)** | se $p$ então $q$ | $p \to q$ | Falso unicamente se o antecedente ($p$) for V e o consequente ($q$) for F (Mortari, 2016). |
| **Bicondicional (Equivalência)**| $p$ se e somente se $q$ | $p \leftrightarrow q$ | Verdadeiro apenas se ambos tiverem o **mesmo valor lógico** (Mortari, 2016). |

---

## 2. Sintaxe de Fórmulas Bem Formadas (FBF)

A lógica proposicional adota uma linguagem formalizada para evitar as ambiguidades inerentes às línguas naturais (Marietto, 2013). As fórmulas são construídas de modo indutivo e estruturado a partir de um alfabeto estrito (constituído por símbolos verdade, variáveis proposicionais, conectivos e símbolos de pontuação) (Martins, [201-]). 

Uma expressão é considerada uma **Fórmula Bem Formada (FBF)** se e somente se puder ser gerada pela aplicação recursiva das seguintes regras sintáticas (Marietto, 2013; Martins, [201-]; Mortari, 2016):

1.  **Base:** Todo símbolo verdade ($true$, $false$) e todo símbolo proposicional (variável atômica como $p, q, r, \dots$) é uma FBF.
2.  **Passo da Negação:** Se $P$ é uma FBF, então $(\sim P)$ também é uma FBF.
3.  **Passo dos Conectivos Binários:** Se $P$ e $Q$ são FBFs, então $(P \land Q)$, $(P \lor Q)$, $(P \to Q)$ e $(P \leftrightarrow Q)$ também são FBFs.

### Comprimento de uma Fórmula ($COMP[H]$)
O comprimento mede a complexidade indutiva de uma fórmula proposicional $H$, contando o número total de átomos e conectivos lógicos nela contidos, desconsiderando os parênteses (Martins, [201-]). É definido recursivamente (Martins, [201-]):
*   Se $H$ é um símbolo proposicional ou símbolo verdade $	o COMP[H] = 1$.
*   Se $H$ é uma negação da forma $\sim P 	o COMP[\sim P] = COMP[P] + 1$.
*   Se $H$ é uma fórmula com operador binário da forma $(P \circ Q) 	o COMP[P \circ Q] = COMP[P] + COMP[Q] + 1$ (onde $\circ$ representa qualquer conectivo binário).

---

## 3. Ordem de Precedência dos Operadores

Para simplificar a leitura e evitar o excesso de parênteses de pontuação, as fórmulas lógicas podem omitir delimitadores desde que se respeite uma ordem fixa decrescente de precedência dos conectivos lógicos (Marietto, 2013; Martins, [201-]). Na ausência de parênteses, os conectivos devem ser avaliados de acordo com a seguinte hierarquia (Marietto, 2013; Martins, [201-]):

1.  **Negação** ($\sim$ ou $
eg$) — *Maior prioridade* (Marietto, 2013).
2.  **Conjunção** ($\land$) e **Disjunção** ($\lor$) — *Prioridade intermediária* (Marietto, 2013).
3.  **Condicional** ($	o$) — *Prioridade inferior* (Marietto, 2013).
4.  **Bicondicional** ($\leftrightarrow$) — *Menor prioridade* (Marietto, 2013).

Quando há conectivos de mesma prioridade em sequência, adota-se a regra de associatividade: as conjunções e disjunções associam-se à esquerda, enquanto os condicionais e bicondicionais associam-se à direita (Martins, [201-]).

---

## Referências

Em conformidade com as normas da Associação Brasileira de Normas Técnicas (**ABNT NBR 6023:2018** para referências e **ABNT NBR 10520:2023** para citações):

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013. 1 recurso online (slides). Slides de aula da disciplina de Lógica Básica.
*   MARTINS, Luiz Gustavo A. **Lógica proposicional e formas normais**. Uberlândia: Universidade Federal de Uberlândia, [201-]. 1 recurso online (apostila).
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016. 512 p.

















### 1. Alfabeto e a Sintaxe de Fórmulas Bem Formadas (FBF)

Assim como na língua portuguesa nem toda concatenação de letras forma uma palavra válida, na lógica proposicional existe um conjunto mínimo de regras que define se uma sequência de caracteres é uma **Fórmula Bem Formada (FBF)**.

#### **O Alfabeto Formal**
O alfabeto da lógica proposicional clássica é constituído por quatro grupos de símbolos:
1.  **Símbolos verdade:** `true` e `false`.
2.  **Símbolos proposicionais (Variáveis):** Letras representativas como $P, Q, R, S, P_1, P_2 \dots$ (ou minúsculas como $p, q, r \dots$).
3.  **Conectivos lógicos:** $\neg$ (negação), $\lor$ (ou inclusivo), $\land$ (e), $\to$ (implica) e $\leftrightarrow$ (equivalência).
4.  **Símbolos de pontuação:** Parênteses $( e )$ para delimitar o escopo das operações.

#### **Regras de Construção Indutiva**
Uma expressão é uma fórmula bem formada se, e somente se, puder ser derivada a partir das seguintes regras recursivas:
*   **Regra 1:** Todo símbolo verdade é uma fórmula.
*   **Regra 2:** Todo símbolo proposicional é uma fórmula.
*   **Regra 3:** Se $P$ é uma fórmula, então $(\neg P)$ também é uma fórmula.
*   **Regra 4:** Se $P$ e $Q$ são fórmulas, então as conexões binárias abaixo também são fórmulas:
    *   Disjunção: $(P \lor Q)$
    *   Conjunção: $(P \land Q)$
    *   Implicação (Condicional): $(P \to Q)$
    *   Bi-implicação (Bicondicional): $(P \leftrightarrow Q)$

> ❌ **Exemplos de concatenações inválidas (Não são FBFs):**  
> $PQR$ (falta de conectivos)  
> $(P\ true\ \leftrightarrow)$ (conectivo posicionado incorretamente ao final)  
> $\neg \land p \lor q$ (sequência inválida de conectivos).

---

#### 📝 **Exercício Resolvido 1: Demonstração Sintática**
*Prove que a expressão $((P \land Q) \lor (\neg P \land \neg Q))$ é uma fórmula proposicional válida.*

**Solução (aplicando as regras indutivas passo a passo):**
1.  $P$ e $Q$ são fórmulas pela **Regra 2** (símbolos proposicionais).
2.  $(P \land Q)$ é uma fórmula pela **Regra 4.2** aplicada ao passo 1.
3.  $(\neg P)$ e $(\neg Q)$ são fórmulas pela **Regra 3** aplicada ao passo 1.
4.  $(\neg P \land \neg Q)$ é uma fórmula pela **Regra 4.2** aplicada ao passo 3.
5.  $((P \land Q) \lor (\neg P \land \neg Q))$ é uma fórmula pela **Regra 4.1** aplicada aos passos 2 e 4.  
*(Demonstração concluída com sucesso)*.

---

### 2. Comprimento de Fórmula e Subfórmulas

Para analisar a complexidade de uma expressão lógica ou utilizá-la em provas de indução matemática, recorremos a duas definições formais: o comprimento da fórmula e o mapeamento de suas subfórmulas.

#### **Comprimento de uma Fórmula ($COMP[H]$)**
O comprimento mede a complexidade estrutural de uma fórmula $H$ contando seus átomos e conectivos lógicos, ignorando os parênteses de pontuação. É definido de forma indutiva:
*   Se $H$ é um símbolo proposicional ou verdade, então **$COMP[H] = 1$**.
*   Se a fórmula é uma negação $\neg H$, então **$COMP[\neg H] = COMP[H] + 1$**.
*   Se a fórmula possui um conectivo binário $(P \circ Q)$, então **$COMP[P \circ Q] = COMP[P] + COMP[Q] + 1$**.

#### 📝 **Exercício Resolvido 2: Cálculo de Comprimento**
*Calcule o comprimento da fórmula $H = ((P \land Q) \lor R)$.*

**Solução:**
$$[\begin{aligned}
COMP[((P \land Q) \lor R)] &= COMP[P \land Q] + COMP[R] + 1 \\
&= (COMP[P] + COMP[Q] + 1) + COMP[R] + 1 \\
&= (1 + 1 + 1) + 1 + 1 \\
&= 5
\end{aligned}$$
O comprimento da fórmula é **5**.

#### **Subfórmulas**
O conjunto de subfórmulas representa todos os "pedaços válidos" que constituem uma fórmula principal, incluindo ela mesma. Formalmente:
1.  $H$ é subfórmula de $H$.
2.  Se $H = (\neg P)$, então $P$ é subfórmula de $H$.
3.  Se $H = (P \circ Q)$, então $P$ e $Q$ são subfórmulas de $H$.
4.  Se $P$ é subfórmula de $H$, então toda subfórmula de $P$ também é subfórmula de $H$.

> No exemplo $H = \neg(P \lor \neg Q)$, as subfórmulas são:  
> $\{\neg(P \lor \neg Q),\ (P \lor \neg Q),\ P,\ \neg Q,\ Q\}$.

---

### 3. Conectivos Lógicos e Ordem de Precedência

Na linguagem natural, expressamos relações lógicas por meio de conectivos. Na lógica clássica, essas conexões são representadas por funções veritativas (que determinam o valor final da sentença com base nas partes).

#### **Tabela de Conectivos Lógicos e Comportamento Semântico**

| Conectivo | Representação | Descrição Semântica / Regra de Valoração | Equivalente em Linguagem Natural |
| :---: | :---: | :--- | :--- |
| **Negação** | $\neg$ ou $\sim$ | Inverte o valor lógico de entrada. Se $P$ é V, $\neg P$ é F. | "não", "não é verdade que" |
| **Conjunção** | $\land$ | Verdadeiro **apenas** se ambos os operandos forem verdadeiros. | "e", "mas", "todavia", "entretanto" |
| **Disjunção** | $\lor$ | Falso **apenas** se ambos os operandos forem falsos. | "ou" (inclusivo) |
| **Disjunção Exclusiva** | $\oplus$ | Verdadeiro se os operandos tiverem valores **diferentes**. | "ou... ou..." (exclusivo) |
| **Condicional** | $\to$ | Falso **unicamente** se o antecedente for V e o consequente for F. | "se... então..." (implicação material) |
| **Bicondicional** | $\leftrightarrow$ | Verdadeiro **apenas** se ambos tiverem o mesmo valor lógico. | "...se e somente se..." (dupla implicação) |

#### **Regras de Precedência (Omissão de Parênteses)**
Para evitar o uso excessivo de parênteses que dificulta a leitura das fórmulas lógicas, estabelecemos uma ordem fixa decrescente de precedência para os operadores:
1.  **Negação ($\neg$)** — *Maior prioridade*.
2.  **Conjunção ($\land$) e Disjunção ($\lor$)** — *Prioridade intermediária*.
3.  **Condicional ($\to$)** — *Prioridade inferior*.
4.  **Bicondicional ($\leftrightarrow$)** — *Menor prioridade*.

#### **Associatividade**
Se conectivos de mesma precedência aparecerem em sequência, aplicamos as regras de associatividade:
*   $\land$ e $\lor$ associam-se **à esquerda** (ex: $P \land Q \land R$ equivale a $(P \land Q) \land R$).
*   $\to$ e $\leftrightarrow$ associam-se **à direita** (ex: $P \to Q \to R$ equivale a $P \to (Q \to R)$).

> 📝 **Exemplo de eliminação:** A fórmula $(((\neg P) \land Q) \to R)$ pode ser reescrita simplesmente como $\neg P \land Q \to R$. A negação é aplicada primeiro ao $P$, depois a conjunção une $\neg P$ e $Q$, e finalmente a implicação é calculada.

---

### Referências Bibliográficas (Padrão ABNT)

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013. 1 recurso online (slides). 
*   MARTINS, Luiz Gustavo A. **Lógica Proposicional**: sintaxe, semântica, propriedades e métodos de validação. Uberlândia: Universidade Federal de Uberlândia, [20--].
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016. 512 p.
