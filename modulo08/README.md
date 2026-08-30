# 📂 Módulo 8: Técnicas de Prova 


# Prova Direta — Lógica Proposicional

Consiste em partir puramente do conjunto de hipóteses/premissas e, linha após linha, aplicar regras de equivalência e inferência básicas até derivar e registrar a conclusão final do teorema (Martins, 2012; Mortari, 2016).


## 1. Validade de Argumentos

O método das **tabelas-verdade** permite demonstrar, verificar ou testar a validade de qualquer argumento. Mas seu emprego torna-se cada vez mais trabalhoso à medida que aumenta o número de proposições simples componentes.

> **Exemplo do problema:** para testar a validade de um argumento com 5 proposições simples, é necessário construir uma tabela-verdade com $2^5 = 32$ linhas.

Um método mais eficiente para demonstrar, verificar ou testar a validade de um argumento

$$P_1, P_2, \dots, P_n \ \vdash\ Q$$

consiste em **deduzir a conclusão $Q$ a partir das premissas** $P_1, P_2, \dots, P_n$, mediante o uso de **regras de inferência** e **regras de equivalência**.

---

## 2. Definição de Prova Direta

Na **prova direta**, parte-se das premissas e chega-se à conclusão, com o uso de regras de inferência e regras de equivalência.

- Também é chamada de **dedução lógica** ou **dedução natural**.
- A prova direta procura formalizar a forma humana de "tirar conclusões", evitando o trabalho tedioso e mecânico das tabelas-verdade.

---

## 3. Exemplo Guiado

**Prove que o seguinte argumento lógico é válido:**

> Se as uvas caem, então a raposa as come.
> Se a raposa as come, então estão maduras.
> As uvas estão verdes ou caem.
> Logo, a raposa come as uvas se e só se as uvas caem.

**Simbolização:**
- $p$: as uvas caem
- $q$: a raposa come as uvas
- $r$: as uvas estão maduras

$$\{p \rightarrow q,\ q \rightarrow r,\ \sim r \lor p\} \ \vdash\ q \leftrightarrow p$$

**Linha de raciocínio:** queremos chegar em $q \leftrightarrow p$. Já temos como premissa $p \rightarrow q$. Falta provar $q \rightarrow p$.

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \rightarrow q$ | Premissa 1 |
| L2 | $q \rightarrow r$ | Premissa 2 |
| L3 | $\sim r \lor p$ | Premissa 3 |
| L4 | $r \rightarrow p$ | L3, Equiv. Lei da Condicional |
| L5 | $q \rightarrow p$ | L2, L4, Silogismo Hipotético |
| L6 | $(p \rightarrow q) \land (q \rightarrow p)$ | L1, L5, Introdução da Conjunção |
| L7 | $p \leftrightarrow q$ | L6, Equiv. Lei da Bicondicional |

---

## 4. Exercícios de Prova Direta

### Exercício 1

$$\{p,\ p \rightarrow q,\ q \rightarrow r\} \ \vdash\ r$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p$ | Premissa 1 |
| L2 | $p \rightarrow q$ | Premissa 2 |
| L3 | $q \rightarrow r$ | Premissa 3 |
| L4 | $q$ | L1, L2, Modus Ponens |
| L5 | $r$ | L3, L4, Modus Ponens |

---

### Exercício 2

$$\{\sim p \rightarrow \sim(\sim q),\ \sim(\sim(\sim p))\} \ \vdash\ q$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $\sim p \rightarrow \sim(\sim q)$ | Premissa 1 |
| L2 | $\sim(\sim(\sim p))$ | Premissa 2 |
| L3 | $\sim p$ | L2, Equiv. Lei da Dupla Negação |
| L4 | $\sim(\sim q)$ | L1, L3, Modus Ponens |
| L5 | $q$ | L4, Equiv. Lei da Dupla Negação |

---

### Exercício 3

$$\{p\} \ \vdash\ (p \lor q) \land (p \lor r)$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p$ | Premissa 1 |
| L2 | $p \lor q$ | L1, Introdução da Disjunção |
| L3 | $p \lor r$ | L1, Introdução da Disjunção |
| L4 | $(p \lor q) \land (p \lor r)$ | L2, L3, Introdução da Conjunção |

---

### Exercício 4

$$\{p \rightarrow (q \land r),\ p\} \ \vdash\ (p \land q)$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \rightarrow (q \land r)$ | Premissa 1 |
| L2 | $p$ | Premissa 2 |
| L3 | $q \land r$ | L1, L2, Modus Ponens |
| L4 | $q$ | L3, Eliminação da Conjunção |
| L5 | $p \land q$ | L2, L4, Introdução da Conjunção |

---

### Exercício 5

$$\{p \lor r,\ p \rightarrow f,\ r \rightarrow f\} \ \vdash\ f$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \lor r$ | Premissa 1 |
| L2 | $p \rightarrow f$ | Premissa 2 |
| L3 | $r \rightarrow f$ | Premissa 3 |
| L4 | $f$ | L1, L2, L3, Eliminação da Disjunção |

---

### Exercício 6

$$\{a \rightarrow (b \rightarrow c),\ a \land b\} \ \vdash\ c$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $a \rightarrow (b \rightarrow c)$ | Premissa 1 |
| L2 | $a \land b$ | Premissa 2 |
| L3 | $a$ | L2, Eliminação da Conjunção |
| L4 | $b$ | L2, Eliminação da Conjunção |
| L5 | $b \rightarrow c$ | L1, L3, Modus Ponens |
| L6 | $c$ | L4, L5, Modus Ponens |

---

### Exercício 7

$$\{p,\ p \rightarrow \sim q,\ s \rightarrow q\} \ \vdash\ \sim s$$

**Resolução 1:**

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p$ | Premissa 1 |
| L2 | $p \rightarrow \sim q$ | Premissa 2 |
| L3 | $s \rightarrow q$ | Premissa 3 |
| L4 | $\sim q$ | L1, L2, Modus Ponens |
| L5 | $\sim s$ | L3, L4, Modus Tollens |

**Resolução 2 (caminho alternativo, via Contraposição):**

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p$ | Premissa 1 |
| L2 | $p \rightarrow \sim q$ | Premissa 2 |
| L3 | $s \rightarrow q$ | Premissa 3 |
| L4 | $\sim q$ | L1, L2, Modus Ponens |
| L5 | $\sim q \rightarrow \sim s$ | L3, Contraposição |
| L6 | $\sim s$ | L4, L5, Modus Ponens |

---

### Exercício 8

$$\{(\sim p \lor q) \rightarrow r,\ s \rightarrow q,\ p \rightarrow s,\ \sim q\} \ \vdash\ r$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $(\sim p \lor q) \rightarrow r$ | Premissa 1 |
| L2 | $s \rightarrow q$ | Premissa 2 |
| L3 | $p \rightarrow s$ | Premissa 3 |
| L4 | $\sim q$ | Premissa 4 |
| L5 | $p \rightarrow q$ | L2, L3, Silogismo Hipotético |
| L6 | $\sim p \lor q$ | L5, Equiv. Lei da Condicional |
| L7 | $r$ | L1, L6, Modus Ponens |

---

### Exercício 9

$$\{\sim a \rightarrow c,\ c \rightarrow \sim m,\ m \lor r,\ \sim r\} \ \vdash\ a$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $\sim a \rightarrow c$ | Premissa 1 |
| L2 | $c \rightarrow \sim m$ | Premissa 2 |
| L3 | $m \lor r$ | Premissa 3 |
| L4 | $\sim r$ | Premissa 4 |
| L5 | $m$ | L3, L4, Silogismo Disjuntivo |
| L6 | $\sim c$ | L2, L5, Modus Tollens |
| L7 | $a$ | L1, L6, Modus Tollens |

---

### Exercício 10

$$\{p \lor \sim q,\ p \rightarrow r,\ \sim r \lor q\} \ \vdash\ p \leftrightarrow q$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \lor \sim q$ | Premissa 1 |
| L2 | $p \rightarrow r$ | Premissa 2 |
| L3 | $\sim r \lor q$ | Premissa 3 |
| L4 | $q \rightarrow p$ | L1, Lei da Condicional |
| L5 | $r \rightarrow q$ | L3, Lei da Condicional |
| L6 | $p \rightarrow q$ | L2, L5, Silogismo Hipotético |
| L7 | $(p \rightarrow q) \land (q \rightarrow p)$ | L4, L6, Introdução da Conjunção |
| L8 | $p \leftrightarrow q$ | L7, Lei da Bicondicional |

---

## 5. Argumentos Verbais

Um argumento em língua natural (por exemplo, o resumo de um advogado em um tribunal, uma propaganda, um discurso político etc.), formado por declarações/proposições simples, pode ser testado logicamente por um processo em **duas etapas**:

1. **Simbolizar** cada declaração usando fórmulas bem formadas proposicionais;
2. **Provar** a validade do argumento construindo uma sequência de demonstrações através das regras de dedução da Lógica Proposicional (leis de equivalência e regras de inferência).

### Exemplo Guiado

> Se as taxas de juros cairem, o mercado imobiliário vai melhorar. A taxa federal de desconto vai cair, ou o mercado imobiliário não vai melhorar. As taxas de juros vão cair. Portanto, a taxa federal de descontos vai cair.

**Simbolização:**
- $p$: a taxa de juros vai cair
- $q$: o mercado imobiliário vai melhorar
- $r$: a taxa federal de desconto vai cair

$$\{p \rightarrow q,\ r \lor \sim q,\ p\} \ \vdash\ r$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \rightarrow q$ | Premissa 1 |
| L2 | $r \lor \sim q$ | Premissa 2 |
| L3 | $p$ | Premissa 3 |
| L4 | $q$ | L1, L3, Modus Ponens |
| L5 | $r$ | L2, L4, Silogismo Disjuntivo |

---

### Argumentos Verbais: Exercício 1

> Se a procura do produto aumentar, seu preço subirá; se o preço subir, o produto não será exportado; se não houver importação ou se o produto for exportado, o produto escassear**á**. A procura do produto aumentou e não haverá importação. Logo, o produto não será exportado e escassear**á**.

**Simbolização:**
- $p$: a procura aumenta
- $q$: o preço vai subir
- $r$: o produto será exportado
- $s$: haverá importação
- $t$: o produto irá escassear

$$\{p \rightarrow q,\ q \rightarrow \sim r,\ \sim s \lor r \rightarrow t,\ p \land \sim s\} \ \vdash\ \sim r \land t$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \rightarrow q$ | Premissa 1 |
| L2 | $q \rightarrow \sim r$ | Premissa 2 |
| L3 | $\sim s \lor r \rightarrow t$ | Premissa 3 |
| L4 | $p \land \sim s$ | Premissa 4 |
| L5 | $p$ | L4, Eliminação da Conjunção |
| L6 | $\sim s$ | L4, Eliminação da Conjunção |
| L7 | $q$ | L1, L5, Modus Ponens |
| L8 | $\sim r$ | L2, L7, Modus Ponens |
| L9 | $\sim s \lor r$ | L6, Introdução da Disjunção |
| L10 | $t$ | L3, L9, Modus Ponens |
| L11 | $\sim r \land t$ | L8, L10, Introdução da Conjunção |

---

### Argumentos Verbais: Exercício 2

> Se o programa possui erro de sintaxe, sua compilação produz mensagem de erro. Se o programa não possui erro de sintaxe, sua compilação produz um programa executável. Se tivermos um programa executável, podemos rodá-lo para obter um resultado. Não temos como executar o programa para obter um resultado. Logo, a compilação do programa produz uma mensagem de erro.

**Simbolização:**
- $p$: o programa possui erro de sintaxe
- $q$: a compilação do programa produz uma mensagem de erro
- $r$: a compilação do programa produz um programa executável
- $s$: podemos rodar o programa para obter um resultado

$$\{p \rightarrow q,\ \sim p \rightarrow r,\ r \rightarrow s,\ \sim s\} \ \vdash\ q$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \rightarrow q$ | Premissa 1 |
| L2 | $\sim p \rightarrow r$ | Premissa 2 |
| L3 | $r \rightarrow s$ | Premissa 3 |
| L4 | $\sim s$ | Premissa 4 |
| L5 | $\sim r \lor s$ | L3, Lei da Condicional |
| L6 | $\sim r$ | L4, L5, Silogismo Disjuntivo |
| L7 | $p \lor r$ | L2, Lei da Condicional |
| L8 | $p$ | L6, L7, Silogismo Disjuntivo |
| L9 | $q$ | L1, L8, Modus Ponens |

---

### Argumentos Verbais: Exercício 3

> Se o time joga bem, então ganha o campeonato. Se o time não joga bem, então o técnico é culpado. Se o time ganha o campeonato, então os torcedores ficam contentes. Os torcedores não estão contentes. Portanto, o técnico é culpado.

**Simbolização:**
- $p$: o time joga bem
- $q$: o time ganha o campeonato
- $r$: o técnico é culpado
- $s$: os torcedores ficam contentes

$$\{p \rightarrow q,\ \sim p \rightarrow r,\ q \rightarrow s,\ \sim s\} \ \vdash\ r$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \rightarrow q$ | Premissa 1 |
| L2 | $\sim p \rightarrow r$ | Premissa 2 |
| L3 | $q \rightarrow s$ | Premissa 3 |
| L4 | $\sim s$ | Premissa 4 |
| L5 | $p \rightarrow s$ | L1, L3, Silogismo Hipotético |
| L6 | $\sim p \lor s$ | L5, Lei da Condicional |
| L7 | $\sim p$ | L4, L6, Silogismo Disjuntivo |
| L8 | $r$ | L2, L7, Modus Ponens |

---

### Argumentos Verbais: Exercício 4

> S quer ir ao cinema. Se M estiver certa, então J está enganado. Se J estiver enganado, então L está enganado. Se L estiver enganado, então o filme não está sendo exibido. Ora, o filme está sendo exibido ou S não irá ao cinema. Verificou-se que M está certa. Logo, L e J estão enganados.

**Simbolização:**
- $p$: S quer ir ao cinema
- $q$: M está certa
- $r$: J está enganado
- $s$: L está enganado
- $t$: o filme está sendo exibido

$$\{p,\ q \rightarrow r,\ r \rightarrow s,\ s \rightarrow \sim t,\ t \lor \sim p,\ q\} \ \vdash\ r \land s$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p$ | Premissa 1 |
| L2 | $q \rightarrow r$ | Premissa 2 |
| L3 | $r \rightarrow s$ | Premissa 3 |
| L4 | $s \rightarrow \sim t$ | Premissa 4 |
| L5 | $t \lor \sim p$ | Premissa 5 |
| L6 | $q$ | Premissa 6 |
| L7 | $r$ | L2, L6, Modus Ponens |
| L8 | $q \rightarrow s$ | L2, L3, Silogismo Hipotético |
| L9 | $s$ | L6, L8, Modus Ponens |
| L10 | $r \land s$ | L6, L9, Introdução da Conjunção |

> **Observação:** o material original mostra L10 como $r \land s$ concluído a partir de L6 e L9 — note que a numeração das premissas 5 ($t \lor \sim p$) e 4 ($s \rightarrow \sim t$) não chega a ser usada diretamente nesse caminho de resolução, o que sugere que existe mais de uma rota de prova possível para o mesmo argumento.

---

### Argumentos Verbais: Exercício 5

> Maria estuda ou não está cansada. Se Maria estuda, então dorme tarde. Maria não dorme tarde ou está cansada. Portanto, Maria está cansada se e somente se estuda.

**Simbolização:**
- $p$: Maria estuda
- $q$: Maria está cansada
- $r$: Maria dorme tarde

$$\{p \lor \sim q,\ p \rightarrow r,\ \sim r \lor q\} \ \vdash\ q \leftrightarrow p$$

| Linha | Fórmula | Justificativa |
|---|---|---|
| L1 | $p \lor \sim q$ | Premissa 1 |
| L2 | $p \rightarrow r$ | Premissa 2 |
| L3 | $\sim r \lor q$ | Premissa 3 |
| L4 | $q \rightarrow p$ | L1, Lei da Condicional |
| L5 | $r \rightarrow q$ | L3, Lei da Condicional |
| L6 | $p \rightarrow q$ | L2, L5, Silogismo Hipotético |
| L7 | $(q \rightarrow p) \land (p \rightarrow q)$ | L4, L6, Introdução da Conjunção |
| L8 | $q \leftrightarrow p$ | L7, Lei da Bicondicional |

---

## 6. Resumo do Método

A estratégia geral para construir uma prova direta segue este roteiro:

1. **Liste as premissas** como as primeiras linhas da prova.
2. **Identifique o objetivo** (a conclusão a ser alcançada) e trabalhe "de trás para frente" mentalmente, verificando o que falta provar.
3. **Aplique regras de equivalência** (De Morgan, Lei da Condicional, Dupla Negação, etc.) para reescrever premissas em formas mais úteis — por exemplo, transformar $p \rightarrow q$ em $\sim p \lor q$ quando precisar usar Silogismo Disjuntivo.
4. **Aplique regras de inferência** (Modus Ponens, Modus Tollens, Silogismo Hipotético, Silogismo Disjuntivo, Eliminação/Introdução da Conjunção e Disjunção, etc.) para derivar novas linhas a partir das anteriores.
5. **Justifique cada linha**, citando de quais linhas anteriores ela decorre e qual regra foi aplicada.
6. **Pare quando a conclusão desejada aparecer** como uma das linhas da prova.

Esse método evita o crescimento exponencial de linhas de uma tabela-verdade e reflete melhor o processo natural de raciocínio dedutivo usado em argumentos verbais do dia a dia.



# Prova Indireta (Por Contradição / Redução ao Absurdo - RAA)
1.  Introduz-se temporariamente a negação da conclusão desejada ($\sim Q$) como uma nova hipótese de trabalho (Martins, 2012; Mortari, 2016).
2.  Realiza-se o cálculo proposicional até deduzir um absurdo ou contradição explícita da forma $B \land \sim B$ (Martins, 2012; Mortari, 2016).
3.  Ao atingir o absurdo, descarta-se a hipótese temporária por contradizer os axiomas clássicos, provando que a conclusão $Q$ original é necessariamente verdadeira (Martins, 2012; Mortari, 2016).


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MARTINS, Luiz Gustavo. **Apostila de Lógica Proposicional**: dedução natural, sintaxe e semântica. Santo André: Universidade Federal do ABC, 2012.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
