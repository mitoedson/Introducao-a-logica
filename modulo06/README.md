# 📂 Módulo 6: Técnicas de Prova e Dedução Natural

Módulo de demonstrações avançadas. O método de dedução natural evita a construção de tabelas-verdade excessivamente extensas para muitos átomos (onde $N$ variáveis necessitam de $2^N$ linhas de tabela) (Martins, 2012).


## 1. Regras de Inferência Clássicas (Primitivas)

As regras de inferência são esquemas clássicos estruturados de argumentos logicamente válidos (Marietto, 2013):

*   **Modus Ponens (MP):**
    $$P \to Q, \quad P \quad \vdash \quad Q$$ (Martins, 2012)
*   **Modus Tollens (MT):**
    $$P \to Q, \quad \sim Q \quad \vdash \quad \sim P$$ (Martins, 2012)
*   **Silogismo Hipotético (SH):**
    $$P \to Q, \quad Q \to R \quad \vdash \quad P \to R$$ (Martins, 2012)
*   **Silogismo Disjuntivo (SD):**
    $$P \lor Q, \quad \sim P \quad \vdash \quad Q$$ (Martins, 2012)
*   **Conjunção (C):**
    $$P, \quad Q \quad \vdash \quad P \land Q$$ (Martins, 2012)
*   **Simplificação (S):**
    $$P \land Q \quad \vdash \quad P$$ (Martins, 2012)
*   **Adição (AD):**
    $$P \quad \vdash \quad P \lor Q$$ (Martins, 2012)


## 2. Técnicas de Prova Sintática

### Prova Direta
Consiste em partir puramente do conjunto de hipóteses/premissas e, linha após linha, aplicar regras de equivalência e inferência básicas até derivar e registrar a conclusão final do teorema (Martins, 2012; Mortari, 2016).

### Prova Indireta (Por Contradição / Redução ao Absurdo - RAA)
1.  Introduz-se temporariamente a negação da conclusão desejada ($\sim Q$) como uma nova hipótese de trabalho (Martins, 2012; Mortari, 2016).
2.  Realiza-se o cálculo proposicional até deduzir um absurdo ou contradição explícita da forma $B \land \sim B$ (Martins, 2012; Mortari, 2016).
3.  Ao atingir o absurdo, descarta-se a hipótese temporária por contradizer os axiomas clássicos, provando que a conclusão $Q$ original é necessariamente verdadeira (Martins, 2012; Mortari, 2016).


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MARTINS, Luiz Gustavo. **Apostila de Lógica Proposicional**: dedução natural, sintaxe e semântica. Santo André: Universidade Federal do ABC, 2012.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
