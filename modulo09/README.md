# 📂 Módulo 9: Equivalência Lógica


## 1. Definição

Diz-se que uma proposição $P(p,q,r,\dots)$ é **logicamente equivalente**, ou apenas **equivalente**, a uma proposição $Q(p,q,r,\dots)$ se as **tabelas-verdade** destas duas proposições são **idênticas**.

O símbolo para equivalência lógica é $\equiv$ ou $\Leftrightarrow$. Assim:

$$P(p,q,r,\dots) \Leftrightarrow Q(p,q,r,\dots) \quad \text{ou} \quad P(p,q,r,\dots) \equiv Q(p,q,r,\dots)$$

### Exemplo introdutório

> "Se Lógica é difícil e Matemática é difícil ou Lógica não é difícil, então Lógica não é difícil"

- $l$: Lógica é difícil
- $m$: Matemática é difícil
- Fórmula: $l \land (m \lor \sim l) \rightarrow \sim l$

| l | m | Valor Verdade |
|---|---|---|
| F | F | V |
| F | V | V |
| V | F | V |
| V | V | F |

Comparando com $\sim m \lor \sim l$:

| l | m | $\sim m \lor \sim l$ | Valor Verdade |
|---|---|---|---|
| F | F | V | V |
| F | V | V | V |
| V | F | V | V |
| V | V | F | F |

Como as duas proposições têm os **mesmos valores para cada interpretação** (mesma tabela-verdade), elas são equivalentes:

$$l \land (m \lor \sim l) \rightarrow \sim l \ \equiv\ \sim m \lor \sim l$$

### Como comparar duas proposições

Para comparar duas proposições, basta utilizar suas tabelas-verdade, observando duas propriedades:

- As tabelas devem envolver os **mesmos valores independentes** (as mesmas variáveis proposicionais).
- Devem assumir os **mesmos valores para cada combinação** de valores-verdade das variáveis independentes (para cada interpretação).

> **Se duas proposições são equivalentes, então possuem a mesma tabela-verdade. E se duas proposições têm a mesma tabela-verdade, são equivalentes.**

### Interpretação intuitiva

Duas proposições são equivalentes quando **traduzem a mesma ideia**, diferindo apenas na forma de apresentar a ideia.

---

## 2. Verificações Clássicas (via Tabela-Verdade)

### 2.1 Dupla Negação

$$\sim\sim p \equiv p$$

| p | ~p | ~~p |
|---|----|----|
| V | F | V |
| F | V | F |

### 2.2 Regra de Clavius

$$\sim p \rightarrow p \equiv p$$

| p | ~p | ~p→p |
|---|----|------|
| V | F | V |
| F | V | F |

### 2.3 Lei da Condicional

$$\sim p \lor q \equiv p \rightarrow q$$

| p | q | ~p | ~p∨q | p→q |
|---|---|----|------|-----|
| V | V | F | V | V |
| V | F | F | F | F |
| F | V | V | V | V |
| F | F | V | V | V |

### 2.4 Bicondicional (forma 1)

$$p \leftrightarrow q \equiv (p \rightarrow q) \land (q \rightarrow p)$$

| p | q | p↔q | p→q | q→p | (p→q)∧(q→p) |
|---|---|-----|-----|-----|-------------|
| V | V | V | V | V | V |
| V | F | F | F | V | F |
| F | V | F | V | F | F |
| F | F | V | V | V | V |

### 2.5 Bicondicional (forma 2)

$$p \leftrightarrow q \equiv (p \land q) \lor (\sim p \land \sim q)$$

| p | q | p↔q | p∧q | ~p∧~q | (p∧q)∨(~p∧~q) |
|---|---|-----|-----|-------|----------------|
| V | V | V | V | F | V |
| V | F | F | F | F | F |
| F | V | F | F | F | F |
| F | F | V | F | V | V |

### 2.6 Leis de De Morgan

$$\sim(p \land q) \equiv \sim p \lor \sim q \qquad\qquad \sim(p \lor q) \equiv \sim p \land \sim q$$

| p | q | ~p | ~q | ~(p∧q) | ~p∨~q | ~(p∨q) | ~p∧~q |
|---|---|----|----|--------|-------|--------|-------|
| V | V | F | F | F | F | F | F |
| V | F | F | V | V | V | F | F |
| F | V | V | F | V | V | F | F |
| F | F | V | V | V | V | V | V |

### Exercício aplicado — negação de frase

> **Negue a frase:** "Ela estudou muito ou teve sorte na prova"

- $p$: ela estudou muito
- $q$: ela teve sorte na prova
- Frase original: $p \lor q$
- Negando: $\sim(p \lor q) \equiv (\sim p \land \sim q)$

**Resultado:** "Ela não estudou muito **E** ela não teve sorte"

---

## 3. Para que serve a Equivalência Lógica

Um recurso importante na argumentação lógica é a **substituição de uma proposição por outra que seja equivalente**.

Qualquer componente de uma proposição composta pode ser substituído por uma proposição equivalente, **sem alterar o valor final** de sua tabela-verdade:

$$l \land (m \lor l) \rightarrow \sim l \ \equiv\ \sim m \lor \sim l$$

Essa é uma forma de **simplificar proposições** ou de **trocar argumentos por outros equivalentes**.

Para usar essa ideia, é preciso ter um **"estoque" de equivalências entre proposições**. Os lógicos desenvolveram muitas dessas equivalências, mostrando que a bicondicional correspondente é uma tautologia (construindo sua tabela-verdade).

---

## 4. Tabela Completa das Equivalências Lógicas Notáveis

| Nome | Equivalência |
|---|---|
| Comutatividade | $p \land q \equiv q \land p$ |
| | $p \lor q \equiv q \lor p$ |
| Associatividade | $(p \land q) \land r \equiv p \land (q \land r)$ |
| | $(p \lor q) \lor r \equiv p \lor (q \lor r)$ |
| Distributividade | $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$ |
| | $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$ |
| De Morgan | $\sim(p \land q) \equiv \sim p \lor \sim q$ |
| | $\sim(p \lor q) \equiv \sim p \land \sim q$ |
| Idempotência | $p \land p \equiv p$ |
| | $p \lor p \equiv p$ |
| Identidade | $p \land V \equiv p$ |
| | $p \lor F \equiv p$ |
| Limite Superior (Anulamento) | $p \land F \equiv F$ |
| | $p \lor V \equiv V$ |
| Dupla Negação | $\sim(\sim p) \equiv p$ |
| Condicional (Implicação) | $p \rightarrow q \equiv \sim p \lor q$ |
| Bicondicional | $p \leftrightarrow q \equiv (p \rightarrow q) \land (q \rightarrow p)$ |
| | $p \leftrightarrow q \equiv (p \land q) \lor (\sim p \land \sim q)$ |
| Absorção | $p \lor (p \land q) \equiv p$ |
| | $p \land (p \lor q) \equiv p$ |
| Contrapositiva | $p \rightarrow q \equiv \sim q \rightarrow \sim p$ |

### Exemplos de interpretação intuitiva

- **De Morgan:** "É falso que José tenha ido ao cinema e ao teatro" equivale a "Ou José não foi ao cinema ou não foi ao teatro".
- **Dupla Negação:** "Não é o caso de que o lixo não está vazio" ⟺ "O lixo está vazio".
- **Condicional:** "Se continuar chovendo, o rio vai transbordar" equivale a "Ou pára de chover ou o rio vai transbordar".
- **Bicondicional:** "Ou as duas proposições são verdadeiras, ou as duas são falsas."

### Prova das Leis da Absorção (via tabela-verdade)

$$p \lor (p \land q) \equiv p$$

| p | q | p∧q | p∨(p∧q) |
|---|---|-----|---------|
| V | V | V | **V** |
| V | F | F | **V** |
| F | V | F | **F** |
| F | F | F | **F** |

Os valores-verdade são idênticos para $p$ e $p \lor (p \land q)$ — confirmado.

### Prova da Lei da Contrapositiva (via tabela-verdade)

$$p \rightarrow q \equiv \sim q \rightarrow \sim p$$

| p | q | ~p | ~q | p→q | ~q→~p |
|---|---|----|----|----|-------|
| V | V | F | F | V | V |
| V | F | F | V | F | F |
| F | V | V | F | V | V |
| F | F | V | V | V | V |

---

## 5. Proposições Associadas a uma Condicional

**Definição:** dada a condicional $p \rightarrow q$, chamam-se **proposições associadas** a $p \rightarrow q$ as três seguintes proposições condicionais que contêm $p$ e $q$:

| Nome | Fórmula |
|---|---|
| **Recíproca** de $p \rightarrow q$ | $q \rightarrow p$ |
| **Contrária** de $p \rightarrow q$ | $\sim p \rightarrow \sim q$ |
| **Contrapositiva** de $p \rightarrow q$ | $\sim q \rightarrow \sim p$ |

### Tabela-verdade das quatro proposições

| p | q | p→q | q→p | ~p | ~q | ~p→~q | ~q→~p |
|---|---|-----|-----|----|----|-------|-------|
| V | V | V | V | F | F | V | V |
| V | F | F | V | F | V | V | F |
| F | V | V | F | V | F | F | V |
| F | F | V | V | V | V | V | V |

### Duas propriedades importantes

$$p \rightarrow q \ \equiv\ \sim q \rightarrow \sim p \qquad \text{(condicional e contrapositiva)}$$

$$q \rightarrow p \ \equiv\ \sim p \rightarrow \sim q \qquad \text{(recíproca e contrária)}$$

Ou seja:
- A **condicional** e sua **contrapositiva** são equivalentes.
- A **recíproca** e a **contrária** são equivalentes entre si.

> **Atenção (pegadinha clássica de concurso):** a condicional $p \rightarrow q$ **NÃO** é equivalente à sua recíproca $q \rightarrow p$, nem à sua contrária $\sim p \rightarrow \sim q$! Isso é confirmado pela tabela: as colunas de $p \rightarrow q$ e $q \rightarrow p$ diferem nas linhas 2 e 3.

---

# Método Dedutivo de Equivalência Lógica

## 6. Por que usar o Método Dedutivo

Até aqui, todas as equivalências foram demonstradas pelo **método da tabela-verdade**. Esse método funciona sempre, mas se torna trabalhoso conforme aumenta o número de variáveis (assim como nas provas diretas de validade de argumentos).

O **Método Dedutivo** é uma alternativa mais eficiente: consiste em partir de uma fórmula e, aplicando **sucessivamente as leis de equivalência já conhecidas** (tabela da Seção 4), transformá-la passo a passo até chegar na fórmula equivalente desejada — sem precisar montar tabela-verdade nenhuma.

---

## 7. Exercícios Resolvidos — Demonstração de Equivalências

### Exercício 1

**Demonstrar:** $p \lor q \rightarrow q \ \equiv\ p \rightarrow q$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \lor q \rightarrow q$ | Fórmula bem formada |
| L2 | $\sim(p \lor q) \lor q$ | L1, Lei da Condicional |
| L3 | $(\sim p \land \sim q) \lor q$ | L2, Leis de De Morgan |
| L4 | $q \lor (\sim p \land \sim q)$ | L3, Lei da Comutatividade |
| L5 | $(q \lor \sim p) \land (q \lor \sim q)$ | L4, Lei da Distributividade |
| L6 | $(q \lor \sim p) \land V$ | L5, Princípio do Terceiro Excluído |
| L7 | $q \lor \sim p$ | L6, Leis da Identidade |
| L8 | $\sim p \lor q$ | L7, Lei da Comutatividade |
| L9 | $p \rightarrow q$ | L8, Lei da Condicional |

---

### Exercício 2

**Demonstrar:** $(p \rightarrow q) \land (p \rightarrow \sim q) \ \equiv\ \sim p$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $(p \rightarrow q) \land (p \rightarrow \sim q)$ | Fórmula bem formada |
| L2 | $(\sim p \lor q) \land (\sim p \lor \sim q)$ | L1, Lei da Condicional |
| L3 | $((\sim p \lor q) \land \sim p) \lor ((\sim p \lor q) \land \sim q)$ | L2, Lei da Distributividade |
| L4 | $(\sim p \land (\sim p \lor q)) \lor ((\sim p \lor q) \land \sim q)$ | L3, Lei da Comutatividade |
| L5 | $\sim p \lor ((\sim p \lor q) \land \sim q)$ | L4, Leis da Absorção |
| L6 | $\sim p \lor (\sim q \land (\sim p \lor q))$ | L5, Lei da Comutatividade |
| L7 | $\sim p \lor ((\sim q \land \sim p) \lor (\sim q \land q))$ | L6, Lei da Distributividade |
| L8 | $\sim p \lor ((\sim q \land \sim p) \lor F)$ | L7, Princípio da Não Contradição |
| L9 | $\sim p \lor (\sim q \land \sim p)$ | L8, Leis da Identidade |
| L10 | $\sim p$ | L9, Lei da Absorção |

---

## 8. Exercícios Resolvidos — Simplificação de Proposições

### Exercício 1

**Simplificar:** $p \lor (q \land \sim p)$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \lor (q \land \sim p)$ | Fórmula bem formada |
| L2 | $(p \lor q) \land (p \lor \sim p)$ | L1, Lei da Distributividade |
| L3 | $(p \lor q) \land V$ | L2, Princípio do Terceiro Excluído (Tautologia) |
| L4 | $p \lor q$ | L3, Lei da Identidade |

**Resultado: $p \lor q$**

---

### Exercício 2

**Simplificar:** $(p \land (\sim(\sim p \lor q))) \lor (p \land q)$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $(p \land (\sim(\sim p \lor q))) \lor (p \land q)$ | Fórmula bem formada |
| L2 | $(p \land (p \land \sim q)) \lor (p \land q)$ | L1, Lei de De Morgan |
| L3 | $((p \land p) \land \sim q) \lor (p \land q)$ | L2, Lei da Associatividade |
| L4 | $(p \land \sim q) \lor (p \land q)$ | L3, Lei da Idempotência |

**Resultado: $(p \land \sim q) \lor (p \land q)$**

---

### Exercício 3

**Simplificar:** $(p \land q) \leftrightarrow \sim q$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $(p \land q) \leftrightarrow \sim q$ | Fórmula bem formada |
| L2 | $((p \land q) \land \sim q) \lor (\sim(p \land q) \land \sim\sim q)$ | L1, Lei da Bicondicional |
| L3 | $((p \land q) \land \sim q) \lor (\sim(p \land q) \land q)$ | L2, Lei da Dupla Negação |
| L4 | $(\sim q \land (p \land q)) \lor (q \land \sim(p \land q))$ | L3, Lei da Comutatividade |
| L5 | $(\sim q \land (p \land q)) \lor (q \land (\sim p \lor \sim q))$ | L4, Leis de De Morgan |
| L6 | $(\sim q \land (q \land p)) \lor (q \land (\sim p \lor \sim q))$ | L5, Lei da Comutatividade |
| L7 | $((\sim q \land q) \land p) \lor (q \land (\sim p \lor \sim q))$ | L6, Lei da Associatividade |
| L8 | $(F \land p) \lor (q \land (\sim p \lor \sim q))$ | L7, Princípio do Terceiro Excluído |
| L9 | $F \lor (q \land (\sim p \lor \sim q))$ | L8, Lei do Limite Superior |
| L10 | $F \lor ((q \land \sim p) \lor (q \land \sim q))$ | L9, Lei da Distributividade |
| L11 | $F \lor ((q \land \sim p) \lor F)$ | L10, Princípio da Não Contradição |
| L12 | $F \lor (q \land \sim p)$ | L11, Lei da Identidade |
| L13 | $q \land \sim p$ | L12, Lei da Identidade |

**Resultado: $q \land \sim p$**

---

### Exercício 4

**Simplificar:** $p \land (p \rightarrow q) \land (p \rightarrow \sim q)$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \land (p \rightarrow q) \land (p \rightarrow \sim q)$ | Fórmula bem formada |
| L2 | $p \land (\sim p \lor q) \land (\sim p \lor \sim q)$ | L1, Lei da Condicional |
| L3 | $p \land (((\sim p \lor q) \land \sim p) \lor ((\sim p \lor q) \land \sim q))$ | L2, Lei da Distributividade |
| L4 | $p \land (\sim p \lor ((\sim p \lor q) \land \sim q))$ | L3, Leis da Absorção |
| L5 | $p \land (\sim p \lor ((\sim q \land \sim p) \lor (\sim q \land q)))$ | L4, Lei da Distributividade |
| L6 | $p \land (\sim p \lor ((\sim q \land \sim p) \lor F))$ | L5, Princípio da Não Contradição |
| L7 | $p \land (\sim p \lor (\sim q \land \sim p))$ | L6, Lei da Identidade |
| L8 | $p \land \sim p$ | L7, Leis da Absorção |
| L9 | $F$ (Contradição) | L8, Princípio da Não Contradição |

**Resultado: $F$ — a proposição é uma contradição.**

Isso faz sentido intuitivamente: a fórmula afirma "$p$ é verdadeiro, e se $p$ então $q$, e se $p$ então não-$q$" — ou seja, exige que $q$ e $\sim q$ sejam ambos verdadeiros ao mesmo tempo, o que é logicamente impossível.

---

## 9. Resumo do Método

A estratégia geral para demonstrar/simplificar uma equivalência pelo Método Dedutivo segue este roteiro:

1. **Escreva a fórmula original** como a primeira linha.
2. **Elimine condicionais e bicondicionais** primeiro, usando a Lei da Condicional ($p \rightarrow q \equiv \sim p \lor q$) e a Lei da Bicondicional, deixando a fórmula apenas com $\land$, $\lor$ e $\sim$.
3. **Aplique De Morgan** para "empurrar" as negações para dentro da fórmula, até ficarem coladas nas variáveis.
4. **Use Distributividade, Comutatividade e Associatividade** livremente para reorganizar os termos de forma conveniente.
5. **Aplique Absorção e Idempotência** para eliminar termos redundantes.
6. **Aplique Identidade, Limite Superior, Terceiro Excluído e Não Contradição** para eliminar $V$ (tautologia) ou $F$ (contradição) que surgirem no meio do caminho.
7. **Justifique cada linha**, citando de qual linha anterior ela decorre e qual lei foi aplicada.
8. **Pare quando a fórmula não puder mais ser simplificada** ou quando alcançar a forma-alvo desejada.

Esse método é o análogo, para **equivalências**, do que a Prova Direta é para **validade de argumentos**: evita o crescimento exponencial de linhas da tabela-verdade e formaliza um processo de simplificação passo a passo.


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MARTINS, Luiz Gustavo. **Apostila de Lógica Proposicional**: dedução natural, sintaxe e semântica. Santo André: Universidade Federal do ABC, 2012.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
