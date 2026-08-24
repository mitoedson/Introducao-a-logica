# Exercício: Cálculo de Comprimento

Calcule o comprimento da fórmula $H = ((P \land Q) \lor R)$.

**Solução:**

$$ \begin{aligned}
COMP[((P \land Q) \lor R)] &= COMP[P \land Q] + COMP[R] + 1 \\
&= (COMP[P] + COMP[Q] + 1) + COMP[R] + 1 \\
&= (1 + 1 + 1) + 1 + 1 \\
&= 5
\end{aligned} $$

O comprimento da fórmula H é 5.

---

Calcule o comprimento da fórmula $H = (p \Rightarrow (q \land \neg r))$.

**Solução:**

$$COMP(p) = 1\\
COMP(q) = 1\\
COMP(r) = 1\\
COMP(\neg r) = COMP(r) + 1 = 1 + 1 = 2\\
COMP(q \land \neg r) = COMP(q) + COMP(¬r) + 1 = 1 + 2 + 1 = 4\\
COMP(p \Rightarrow (q \land \neg r)) = comp(p) + comp(q∧¬r) + 1 = 1 + 4 + 1 = 6$$

Adoto o mesmo passo, separando as variáveis propocionais, que valem 1, e em seguida analiso os conectivos, somando 1.

O comprimento da fórmula H é 6.

---