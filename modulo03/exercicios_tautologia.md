# Exercícios sobre Tautologia

Ano: 2022<br>
Banca: PRGP UNIFEI<br>
Cargo: Assistente em Administração (UNIFEI)<br>
Órgão: UNIFEI - Universidade Federal de Itajubá

Assinale a alternativa que indica uma tautologia.


(A) se hoje é domingo ou está chovendo, então hoje é domingo e está chovendo.

(B) se hoje é domingo e está chovendo, então hoje não é domingo ou não está chovendo.

(C) se hoje é domingo ou está chovendo, então hoje não é domingo e não está chovendo.

(D) se hoje é domingo e está chovendo, então hoje é domingo ou está chovendo.


**Solução:**

variáveis proposicional<br>
p: hoje é domingo<br>
q: está chovendo<br>
¬p: hoje não é domingo<br>
¬q: não está chovendo<br>

(A) (p ∨ q) → (p ∧ q) NÃO É UMA TAUTOLOGIA

| p | q | p∨q | p∧q | (p∨q)→(p∧q) |
|---|---|-----|-----|-------------|
| V | V |  V  |  V  |  V |
| V | F |  V  |  F  |  F |
| F | V |  V  |  F  |  F |
| F | F |  F  |  F  |  V |

(B) (p ∧ q) → (¬p ∨ ¬q) NÃO É UMA TAUTOLOGIA

| p | q | p∧q | ¬p∨¬q | (p∧q)→(¬p∨¬q) |
|---|---|-----|-------|---------------|
| V | V |  V  |   F   |  F |
| V | F |  F  |   V   |  V |
| F | V |  F  |   V   |  V |
| F | F |  F  |   V   |  V |

(C) (p ∨ q) → (¬p ∧ ¬q) NÃO É UMA TAUTOLOGIA

| p | q | p∨q | ¬p∨¬q | (p∨q)→(¬p∧¬q) |
|---|---|-----|-------|-----------------|
| V | V |  V  |   F   | F |
| V | F |  V  |   V   | V |
| F | V |  V  |   V   | V |
| F | F |  F  |   V   | V |


(D) (p ∧ q) → (p ∨ q) É UMA TAUTOLOGIA

| p | q | p∧q | p∨q | (p∧q)→(p∨q) |
|---|---|-----|-----|-------------|
| V | V |  V  |  V  |  V |
| V | F |  F  |  V  |  V |
| F | V |  F  |  V  |  V |
| F | F |  F  |  F  |  V |

---

Ano: 2019<br>
Banca: FUNDATEC<br>
Cargo: Auxiliar (Pref Tapejara)<br>
Órgão: Pref Tapejara - Prefeitura Municipal de Tapejara

É uma tautologia, ou seja, uma proposição sempre verdadeira, a proposição mostrada na alternativa:

(A) A prova está difícil.

(B) João é alto.

(C) Tapejara é uma cidade bonita.

(D) O Brasil é um país localizado na América do Sul.

(E) Maria é alta.


**Solução:**

(A) A prova está difícil. (Julgamento subjetivo — difícil para quem? Depende de cada pessoa)

(B) João é alto. (Subjetivo/relativo — alto comparado a quê? E depende de qual João)

(C) Tapejara é uma cidade bonita. (Julgamento de valor (estético), não é um fato objetivo)

(D) O Brasil é um país localizado na América do Sul. (Fato geográfico objetivo e imutável)

(E) Maria é alta. (Subjetivo e relativo)


Resposta: D

---

Ano: 2019<br>
Banca: PRGP UNIFEI<br>
Cargo: Assistente em Administração (UNIFEI)<br>
Órgão: UNIFEI - Universidade Federal de Itajubá

Com relação às proposições a seguir, avalie se é tautologia, contradição ou contingência:

I. (A ^ A) → (B v A) <br>
II. (A v B) → (A ^ B)<br>
III. A ^ ~A<br>
IV. ~B v B


Assinale a alternativa que apresenta a resposta correta:

(A) (I) é uma tautologia, (II) é uma contingência, (III) é uma contradição, (IV) é uma tautologia.

(B) (I) é uma tautologia, (II) é uma contingência, (III) é uma contradição, (IV) é uma contradição.

(C) (I) é uma tautologia, (II) é uma contradição, (III) é uma contradição, (IV) é uma tautologia.

(D) (I) é uma contradição, (II) é uma contradição, (III) é uma contradição, (IV) é uma tautologia.


**Solução:**

I. (A ^ A) → (B v A) (É Tautologia)

| A | A ^ A | B | B v A | (A ^ A) → (B v A) |
|---|-------|---|-------|-------------------|
| V |   V   | V |   V   | V |
| F |   F   | V |   V   | V |
| V |   V   | F |   V   | V |
| F |   F   | F |   F   | V |


II. (A v B) → (A ^ B) (É Contingência)


| A | B | A v B | A ^ B | (A v B) → (A ^ B) |
|---|---|-------|-------|-------------------|
| V | V |   V   |   V   | V |
| F | V |   V   |   F   | F |
| V | F |   V   |   F   | F |
| F | F |   F   |   F   | F |


III. A ^ ~A (É Contradição)

| A | ~A | A ∧ ~A |
|---|----|--------|
| V | F  | F  |
| F | V  | F  |


IV. ~B v B (É Tautologia)

| ~B | B | ~B v B |
|---|----|--------|
| V | F  | V  |
| F | V  | V  |

Resposta: A

---