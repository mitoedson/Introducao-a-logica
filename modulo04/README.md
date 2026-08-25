# 📂 Módulo 4: Equivalências Lógicas e Simplificação

Mapeamento de identidades e transformações axiomáticas de proposições compostas.


## 1. Tabela de Leis de Equivalência Notáveis

Duas fórmulas $G$ e $H$ são semanticamente equivalentes ($G \equiv H$) se a fórmula condicional dupla $G \leftrightarrow H$ for uma tautologia (Marietto, 2013).

*   **Comutativas:**
    *   $p \land q \equiv q \land p$ 
    *   $p \lor q \equiv q \lor p$ 
*   **Associativas:**
    *   $(p \land q) \land r \equiv p \land (q \land r)$
    *   $(p \lor q) \lor r \equiv p \lor (q \lor r)$
*   **Distributivas:**
    *   $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$
    *   $p \lor (q \land r) \equiv (p \lor q) \land (p \lor q)$
*   **Leis de De Morgan:**
    *   $\sim(p \land q) \equiv \sim p \lor \sim q$ 
    *   $\sim(p \lor q) \equiv \sim p \land \sim q$
*   **Absorção:**
    *   $p \land (p \lor q) \equiv p$
    *   $p \lor (p \land q) \equiv p$
*   **Dupla Negação:**
    *   $\sim(\sim p) \equiv p$
*   **Lei da Condicional:**
    *   $p \to q \equiv \sim p \lor q$
*   **Regra de Clavius:**
    *   $\sim p \to p \equiv p$


## 2. Método Dedutivo para Equivalências

Em vez de construir tabelas-verdade com $2^N$ linhas (Martins, 2012), utiliza-se uma sequência ordenada de substituições baseadas nas equivalências axiomáticas conhecidas para demonstrar a equivalência e simplificar fórmulas complexas (Martins, 2012; Marietto, 2013).

### Tabela-resumo para consulta rápida

| Nome | Fórmula |
|---|---|
| Idempotência | p∧p≡p / p∨p≡p |
| Comutativa | p∧q≡q∧p / p∨q≡q∨p |
| Associativa | (p∧q)∧r≡p∧(q∧r) |
| Distributiva | p∧(q∨r)≡(p∧q)∨(p∧r) |
| Absorção | p∧(p∨q)≡p |
| De Morgan | ¬(p∧q)≡¬p∨¬q |
| Dupla negação | ¬(¬p)≡p |
| Identidade | p∧V≡p / p∨F≡p |
| Anulamento | p∨V≡V / p∧F≡F |
| Complementação | p∧¬p≡F / p∨¬p≡V |
| Condicional | p→q≡¬p∨q |
| Contraposição | p→q≡¬q→¬p |
| Exportação | p→(q→r)≡(p∧q)→r |
| Neg. condicional | ¬(p→q)≡p∧¬q |
| Neg. bicondicional | ¬(p↔q)≡p⊻q |


**Dica de estratégia para simplificação:** normalmente o processo segue essa ordem:
1. **Elimine → e ↔** primeiro, deixando só ∧, ∨, ¬
2. **Aplique De Morgan** para "empurrar" as negações para dentro, até ficarem coladas nas variáveis
3. **Use distributiva, absorção, idempotência** para reduzir termos repetidos ou redundantes
4. **Aplique identidade/anulamento** para eliminar V, F que sobrarem no meio do caminho


### Exemplo Prático de Simplificação

Simplificar a expressão: $(p \lor q) \land \sim p \equiv \sim p \land q$ 

1.  $(p \lor q) \land \sim p$ *(Fórmula Inicial)*
2.  $\sim p \land (p \lor q)$ *(Lei da Comutatividade em 1)*
3.  $(\sim p \land p) \lor (\sim p \land q)$ *(Lei da Distributividade em 2)* 
4.  $F \lor (\sim p \land q)$ *(Princípio da Não Contradição / Conjunção do Absurdo em 3)* 
5.  $\sim p \land q$ *(Lei da Identidade em 4)*


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MARTINS, Luiz Gustavo. **Apostila de Lógica Proposicional**: dedução natural, sintaxe e semântica. Santo André: Universidade Federal do ABC, 2012.
