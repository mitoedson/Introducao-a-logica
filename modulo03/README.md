# 📂 Módulo 3: Propriedades Semânticas das Fórmulas

Estudo da valoração de tabelas-verdade completas sob todas as interpretações possíveis (linhas de entrada).

## 1. Tautologias

Uma fórmula proposicional é uma **tautologia** (representada pelo símbolo $\vDash$) se, e somente se, ela assume o valor Verdadeiro (V) para **todas** as suas interpretações de entrada (todas as linhas na última coluna da tabela-verdade) (Marietto, 2013).
*   *Exemplo clássico:* $p \to q \leftrightarrow \sim p \lor q$ (Marietto, 2013).

#### Verificação pela tabela-verdade

Todas as linhas do resultado final dão **V**, então confirmamos que é uma tautologia.

| p | q | ¬p | p→q | ¬p∨q | (p→q)↔(¬p∨q) |
|---|---|----|----|------|----------------|
| V | V | F  | V  | V    | **V**          |
| V | F | F  | F  | F    | **V**          |
| F | V | V  | V  | V    | **V**          |
| F | F | V  | V  | V    | **V**          |

---

*   *Exemplo clássico:* **p ∨ ¬p** ("p ou não p")

#### Verificação pela tabela-verdade:

Não importa se p é V ou F, o resultado é sempre V. Isso é uma tautologia — conhecida como **princípio do terceiro excluído**.


| p | ¬p | p ∨ ¬p |
|---|----|--------|
| V | F  | V      |
| F | V  | V      |


---

* Princípio da não contradição (negação): ¬(p ∧ ¬p) — "não é o caso que p e não-p sejam ambos verdadeiros"

#### Verificação pela tabela-verdade

| p | ¬p | p ^ ¬p | ¬(p ^ ¬p) |
|---|----|--------|-----------|
| V | F  | F | V | 
| F | V  | F | V |

---

*  Modus Ponens: [(p → q) ∧ p] → q

#### Verificação pela tabela-verdade

| p | q | p→q | (p→q)^p | [(p→q)^p]→q |
|---|---|-----|------|----------------|
| V | V | V  | V    | **V**          |
| V | F | F  | F    | **V**          |
| F | V | V  | F    | **V**          |
| F | F | V  | F    | **V**          |

---

* Lei de De Morgan (como equivalência/tautologia):
¬(p ∧ q) ↔ (¬p ∨ ¬q)

#### Verificação pela tabela-verdade

| p | q | p^q | ¬(p^q) | ¬p | ¬q | ¬p ∨ ¬q | ¬(p ∧ q) ↔ (¬p ∨ ¬q) |
|---|---|-----|--------|----|----|---------|---------------|
| V | V |  V  |   F    |  F |  F | F  |  V  |
| V | F |  F  |   V    |  F |  V | V  |  V  |
| F | V |  F  |   V    |  V |  F | V  |  V  |
| F | F |  F  |   V    |  V |  V | V  |  V  |


---

### Objetivo da Tautologia

O objetivo central da tautologia é dar uma garantia absoluta de verdade estrutural — algo que serve de alicerce confiável para construir raciocínios, provas e sistemas que não falham, não importa o valor das variáveis envolvidas.


1. Garantir validade de argumentos

O principal objetivo é verificar se um raciocínio (argumento) é válido. Um argumento é logicamente válido quando a fórmula que representa "premissas → conclusão" é uma tautologia. Isso permite testar se uma conclusão realmente decorre das premissas, independente do conteúdo — só a forma lógica importa.

2. Estabelecer equivalências lógicas

Como vimos no exemplo anterior (p→q ↔ ¬p∨q), tautologias na forma de bicondicional (↔) servem para provar que duas expressões diferentes significam exatamente a mesma coisa. Isso é a base para:

Simplificar expressões lógicas complexas
Reescrever fórmulas em formas mais convenientes (ex: só com ∧, ∨, ¬)

3. Fundamentar regras de inferência

Tautologias como o Modus Ponens [(p→q)∧p]→q justificam as regras que usamos para deduzir novas verdades a partir de outras já conhecidas. Elas são o "esqueleto" que sustenta demonstrações matemáticas e provas formais.

4. Servir de leis lógicas universais

Tautologias representam verdades que não dependem de fatos do mundo, só da estrutura lógica. Por isso funcionam como axiomas ou leis (De Morgan, terceiro excluído, não contradição) que podem ser aplicadas em qualquer contexto, seja matemática, filosofia ou ciência da computação.

5. Aplicações práticas
Circuitos digitais: verificar se dois circuitos com portas lógicas diferentes produzem sempre a mesma saída (equivalência de circuitos)
Programação: simplificar condições em código (if, while), otimizar expressões booleanas
Verificação formal de software/hardware: provar que um sistema sempre se comporta de determinada forma, sem exceções
Inteligência artificial e IA simbólica: sistemas de prova automática de teoremas usam tautologias como base


## 2. Contradições

Uma fórmula proposicional é uma **contradição** (ou fórmula insatisfazível/inconsistente) se, e somente se, assume o valor Falso (F) sob qualquer combinação possível de valoração de suas proposições componentes (Mortari, 2016).

*   *Exemplo clássico:* $p \leftrightarrow \sim p$ (Mortari, 2016).

| p | ¬p | p $\leftrightarrow$ ¬p |
|---|----|--------|
| V | F  | **F**  |
| F | V  | **F**  |


---

* p ∧ ¬p

"p e não-p" — a contradição mais básica, conhecida como princípio da não contradição (na forma negativa).

| p | ¬p | p ∧ ¬p |
|---|----|--------|
| V | F  | **F**  |
| F | V  | **F**  |

---

* (p → q) ∧ (p ∧ ¬q)

| p | q | p→q | p∧¬q | (p→q)∧(p∧¬q) |
|---|---|-----|------|----------------|
| V | V | V   | F    | **F**          |
| V | F | F   | V    | **F**          |
| F | V | V   | F    | **F**          |
| F | F | V   | F    | **F**          |

---

* (p ∨ q) ∧ ¬p ∧ ¬q

| p | q | p∨q | ¬p∧¬q | (p ∨ q) ∧ ¬p ∧ ¬q |
|---|---|-----|------|----------------|
| V | V | V   | F    | **F**          |
| V | F | V   | F    | **F**          |
| F | V | V   | F    | **F**          |
| F | F | F   | V    | **F**          |

---

* p ∧ (¬p ∨ q) ∧ ¬q

| p | ¬p | q | ¬q | ¬p∨q | p∧(¬p∨q) | p ∧ (¬p ∨ q) ∧ ¬q |
|---|----|---|----|------|----------|-------------------|
| V | F  | V | F  |   V  |    V     |     **F**         |
| V | F  | F | V  |   F  |    F     |     **F**         |
| F | V  | V | F  |   V  |    F     |     **F**         |
| F | V  | F | V  |   V  |    F     |     **F**         |

---

Contradições são a base do **método de prova por absurdo** (reductio ad absurdum): você assume o oposto do que quer provar, deriva uma contradição, e conclui que a suposição original era falsa. Esse é um dos métodos de demonstração mais usados em matemática.

Também são importantes em:
- **Verificação de consistência** de sistemas de regras ou especificações (se um conjunto de premissas leva a uma contradição, o sistema é inconsistente)
- **Detecção de erros lógicos** em programação (condições que nunca podem ser satisfeitas, tipo `if (x > 10 && x < 5)`)



## 3. Contingências

Uma fórmula é uma **contingência** se assume valores Verdadeiros para certas linhas e Falsos para outras (Marietto, 2013). O valor de uma contingência não é resolvido apenas por análise semântica estrutural, necessitando de observação empírica dos fatos no mundo real (Marietto, 2013; Mortari, 2016).

Diferente das tautologias e contradições (que são "verdades/falsidades estruturais", válidas por sua forma), as contingências são o que usamos para **representar fatos do mundo real** — proposições cujo valor de verdade depende do contexto, não da lógica pura. É por isso que a maior parte da matemática, ciência e programação lida com contingências: "se chover, levo guarda-chuva" só é verdadeiro ou falso dependendo se realmente choveu.

---

*   *Exemplo clássico:* $p \leftrightarrow (p \land q)$ (Marietto, 2013).

---

* p ∧ q**

| p | q | p∧q |
|---|---|-----|
| V | V | V   |
| V | F | F   |
| F | V | F   |
| F | F | F   |

Nem sempre V, nem sempre F → contingência.

--- 

* p ∨ q

| p | q | p∨q |
|---|---|-----|
| V | V | V   |
| V | F | V   |
| F | V | V   |
| F | F | F   |

---

* p → q

| p | q | p→q |
|---|---|-----|
| V | V | V   |
| V | F | F   |
| F | V | V   |
| F | F | V   |

---

* p → ¬p

| p | ¬p | p→¬p |
|---|----|------|
| V | F  | **F**  |
| F | V  | **V**  |

Varia entre F e V → contingência (diferente de p↔¬p, que é sempre F).

--- 

* (p ∧ q) ∨ r

Uma fórmula com três variáveis também pode ser contingência — basta ter pelo menos uma linha V e uma linha F na tabela.

---

### Resumo comparativo


Depois de montar a tabela-verdade da fórmula:
- Todas as linhas V → **tautologia**
- Todas as linhas F → **contradição**
- Mistura de V e F → **contingência**


| Fórmula | Tipo |
|---|---|
| p ∨ ¬p | Tautologia |
| p ∧ ¬p | Contradição |
| p ↔ ¬p | Contradição |
| p → ¬p | Contingência |
| p ∧ q | Contingência |
| p → q | Contingência |


## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
