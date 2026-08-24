# 📂 Módulo 2: Cálculo Proposicional e Sintaxe

Este módulo detalha os aspectos formais de construção e representação matemática das sentenças.


## 1. Alfabeto e a Sintaxe de Fórmulas Bem Formadas (FBF)


A lógica proposicional adota uma linguagem formalizada para evitar as ambiguidades inerentes às línguas naturais (Marietto, 2013). As fórmulas são construídas de modo indutivo e estruturado a partir de um alfabeto estrito (constituído por símbolos verdade, variáveis proposicionais, conectivos e símbolos de pontuação) (Martins, [201-]). 

### **O Alfabeto Formal**
O alfabeto da lógica proposicional clássica é constituído por quatro grupos de símbolos:
1.  **Símbolos verdade:** `true` e `false`.
2.  **Símbolos proposicionais (Variáveis):** Letras representativas como $P, Q, R, S, P_1, P_2 \dots$ (ou minúsculas como $p, q, r \dots$). Não há uma regra ou padrão que estabelece o uso restrito para cada um.
3.  **Conectivos lógicos:** $\neg$ (negação), $\lor$ (ou inclusivo), $\land$ (e), $\to$ (implica) e $\leftrightarrow$ (equivalência).
4.  **Símbolos de pontuação:** Parênteses $( e )$ para delimitar o escopo das operações.

### **Regras de Construção Indutiva**
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


### 📝 **Exercício Resolvido 1: Demonstração Sintática**
* Prove que a expressão $((P \land Q) \lor (\neg P \land \neg Q))$ é uma fórmula proposicional válida.*

**Solução (aplicando as regras indutivas passo a passo):**

1.  $P$ e $Q$ são fórmulas pela **Regra 2** (símbolos proposicionais).
2.  $(P \land Q)$ é uma fórmula pela **Regra 4.2** aplicada ao passo 1.
3.  $(\neg P)$ e $(\neg Q)$ são fórmulas pela **Regra 3** aplicada ao passo 1.
4.  $(\neg P \land \neg Q)$ é uma fórmula pela **Regra 4.2** aplicada ao passo 3.
5.  $((P \land Q) \lor (\neg P \land \neg Q))$ é uma fórmula pela **Regra 4.1** aplicada aos passos 2 e 4.  
*(Demonstração concluída com sucesso)*.


## 2. Comprimento de Fórmula e Subfórmulas

Para analisar a complexidade de uma expressão lógica ou utilizá-la em provas de indução matemática, recorremos a duas definições formais: o comprimento da fórmula e o mapeamento de suas subfórmulas.

### **Comprimento de uma Fórmula ($COMP[H]$)**
O comprimento mede a complexidade estrutural de uma fórmula $H$ contando seus átomos e conectivos lógicos, ignorando os parênteses de pontuação. É definido de forma indutiva:
*   Se $H$ é um símbolo proposicional ou verdade, então **$COMP[H] = 1$**.
*   Se a fórmula é uma negação $\neg H$, então **$COMP[\neg H] = COMP[H] + 1$**.
*   Se a fórmula possui um conectivo binário $(P \circ Q)$, então **$COMP[P \circ Q] = COMP[P] + COMP[Q] + 1$**.

Calcular o comprimento de uma fórmula lógica permite medir o seu tamanho sintático de forma precisa.

O objetivo principal é viabilizar demonstrações por indução matemática sobre a estrutura das fórmulas e analisar o custo computacional de algoritmos que processam expressões lógicas.

A definição formal do comprimento — frequentemente denotado como c(H), COMP(H), comp(P) ou len(H) — funciona da seguinte maneira:

1. Caso Base (Átomos/Variáveis): Se a fórmula é uma variável (letra) proposicional ou constante ($P, Q, R, p, q,r$):

        COMP(P) = 1


    Quando a variável proposicional está sozinha, sem conectivos, o comprimento é 1.

    Obs.: em alguns livros pode-se encontrar COMP(P)=0, assim como o uso das variáveis proposicionais maíusculas, ou minúsculas, desde que o autor convencione-as como notação. 

---

2. Passo Indutivo (Conectivos Lógicos).Se as fórmulas H e G já possuem comprimentos definidos:

* Negação ($\neg H$): 

    $COMP(\neg H)=COM(H)+1$ 

    Como a variável proposicional vale 1, o +1 vem do conectivo de negação.

---
* Conjunção (H $\wedge$ G):    
  
    $COM(H \land G)=COM(H)+COM(G)+1$
  
   (O conectivo $\land$ contribui com 1).

---

* Disjunção (H $\vee$ G): 

    $COM(H \lor G)=COM(H)+COM(G)+1$
    
    (O conectivo $\lor$ contribui com 1)

---

* Implicação (H $\rightarrow$ G):

    $COM(H \rightarrow G)=COM(H)+COM(G)+1$
        
    (O conectivo $\rightarrow$ contribui com 1).

---

* Biimplicação (H $\leftrightarrow$ G):

    $COM(H \leftrightarrow G)=COM(H)+COM(G)+1$
        
    (O conectivo $\leftrightarrow$ contribui com 1).


#### Principais Objetivos

* O grande uso do comprimento/complexidade é como ferramenta em provas por indução na complexidade da fórmula: você prova que uma propriedade vale para todas as fórmulas atômicas (caso base) e depois mostra que, se vale para A e B, também vale para ¬A, A∧B, etc. (passo indutivo). É assim que se demonstram teoremas gerais sobre toda a lógica proposicional (por exemplo, que toda fórmula tem uma única leitura, ou propriedades de valorações).

* Existe também uma noção separada de "comprimento" como tamanho literal da string (contando cada símbolo, inclusive parênteses) — essa é mais usada em lógica computacional, quando se fala da complexidade de algoritmos como o SAT em função do tamanho da entrada.


* Análise de Algoritmos: Ajuda a estimar o tempo de processamento e o uso de memória em programas que avaliam ou traduzem expressões lógicas.

* Otimização de Fórmulas: Permite comparar o tamanho de diferentes expressões equivalentes para encontrar a forma mais simples ou curta.


### **Subfórmulas**
O conjunto de subfórmulas representa todos os "pedaços válidos" que constituem uma fórmula principal, incluindo ela mesma. Formalmente:
1.  $H$ é subfórmula de $H$.
2.  Se $H = (\neg P)$, então $P$ é subfórmula de $H$.
3.  Se $H = (P \circ Q)$, então $P$ e $Q$ são subfórmulas de $H$.
4.  Se $P$ é subfórmula de $H$, então toda subfórmula de $P$ também é subfórmula de $H$.

> No exemplo $H = \neg(P \lor \neg Q)$, as subfórmulas são:  
> $\{\neg(P \lor \neg Q),\ (P \lor \neg Q),\ P,\ \neg Q,\ Q\}$.


## 3. Conectivos Lógicos e Ordem de Precedência


Os conectivos realizam operações sobre proposições, modificando ou combinando seus valores lógicos de acordo com regras matemáticas bem-definidas (Martins, [201-]; Mortari, 2016). Na lógica clássica bivalente, essas operações funcionam como funções veritativas, onde o valor-verdade do enunciado composto é determinado unicamente pelos valores-verdade de suas partes componentes (Marietto, 2013; Mortari, 2016).

Abaixo estão definidos os conectivos lógicos clássicos e suas respectivas regras de valoração semântica:

#### **Tabela de Conectivos Lógicos e Comportamento Semântico**

| Conectivo | Representação | Descrição Semântica / Regra de Valoração | Equivalente em Linguagem Natural |
| :---: | :---: | :--- | :--- |
| **Negação** | $\neg$ ou $\sim$ | Inverte o valor lógico de entrada. Se $P$ é V, $\neg P$ é F. | "não", "não é verdade que" |
| **Conjunção** | $\land$ | Verdadeiro **apenas** se ambos os operandos forem verdadeiros. | "e", "mas", "todavia", "entretanto" |
| **Disjunção** | $\lor$ | Falso **apenas** se ambos os operandos forem falsos. | "ou" (inclusivo) |
| **Disjunção Exclusiva** | $\oplus$ | Verdadeiro se os operandos tiverem valores **diferentes**. | "ou... ou..." (exclusivo) |
| **Condicional** | $\to$ | Falso **unicamente** se o antecedente for V e o consequente for F. | "se... então..." (implicação material) |
| **Bicondicional** | $\leftrightarrow$ | Verdadeiro **apenas** se ambos tiverem o mesmo valor lógico. | "...se e somente se..." (dupla implicação) |

### **Regras de Precedência (Omissão de Parênteses)**

Para simplificar a leitura e evitar o excesso de parênteses de pontuação, as fórmulas lógicas podem omitir delimitadores desde que se respeite uma ordem fixa decrescente de precedência dos conectivos lógicos (Marietto, 2013; Martins, [201-]). Na ausência de parênteses, os conectivos devem ser avaliados de acordo com a seguinte hierarquia (Marietto, 2013; Martins, [201-]):


1.  **Negação ($\neg$)** — *Maior prioridade*.
2.  **Conjunção ($\land$) e Disjunção ($\lor$)** — *Prioridade intermediária*.
3.  **Condicional ($\to$)** — *Prioridade inferior*.
4.  **Bicondicional ($\leftrightarrow$)** — *Menor prioridade*.

### **Associatividade**
Quando há conectivos de mesma prioridade em sequência, adota-se a regra de associatividade: as conjunções e disjunções associam-se à esquerda, enquanto os condicionais e bicondicionais associam-se à direita (Martins, [201-]).

*   $\land$ e $\lor$ associam-se **à esquerda** (ex: $P \land Q \land R$ equivale a $(P \land Q) \land R$).
*   $\to$ e $\leftrightarrow$ associam-se **à direita** (ex: $P \to Q \to R$ equivale a $P \to (Q \to R)$).

> 📝 **Exemplo de eliminação:** A fórmula $(((\neg P) \land Q) \to R)$ pode ser reescrita simplesmente como $\neg P \land Q \to R$. A negação é aplicada primeiro ao $P$, depois a conjunção une $\neg P$ e $Q$, e finalmente a implicação é calculada.



## Referências Bibliográficas (Padrão ABNT)

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013. 1 recurso online (slides). 
*   MARTINS, Luiz Gustavo A. **Lógica Proposicional**: sintaxe, semântica, propriedades e métodos de validação. Uberlândia: Universidade Federal de Uberlândia, [20--].
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016. 512 p.
