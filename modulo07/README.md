# 📂 Módulo 7: Regras de Inferência

## 1. Definição

**Inferência** é o processo pelo qual chegamos a uma conclusão. Para a Lógica, o que importa não é o "caminho" (divagação, associação de ideias, imaginação), mas sim o **argumento** — a forma da inferência precisa ser examinada para verificar se é **justificável** chegar a determinada conclusão.

Formalmente, uma **inferência lógica** é uma **tautologia** da forma:

$$(p_1 \land p_2 \land \dots \land p_n) \rightarrow q$$

- As proposições $p_i$ são chamadas de **hipóteses** ou **premissas** (antecedente).
- A proposição $q$ é a **conclusão** (consequente).

As regras de inferência são **formas válidas de raciocínio** — esquemas clássicos de argumentos válidos que permitem concluir o consequente, uma vez que se considera o antecedente verdadeiro.


## 2. Lista de Regras de Inferência

### 2.1 Modus Ponens

$$p \rightarrow q,\ p \ \vdash\ q$$

| Premissas | Exemplo |
|---|---|
| $p \rightarrow q$ | Se Deus existe, então não há mal |
| $p$ | Deus existe |
| ∴ $q$ | Logo, não há mal |

---

### 2.2 Modus Tollens

$$p \rightarrow q,\ \sim q\ \vdash\ \sim p$$

| Premissas | Exemplo |
|---|---|
| $p \rightarrow q$ | Se o metal é ouro, então brilha |
| $\sim q$ | O metal não brilha |
| ∴ $\sim p$ | Logo, o metal não é ouro |

---

### 2.3 Silogismo Hipotético

$$p \rightarrow q,\ q \rightarrow r\ \vdash\ p \rightarrow r$$

| Premissas | Exemplo |
|---|---|
| $p \rightarrow q$ | Se o cérebro é preciso para que haja pensamentos, então o pensamento ocorre sempre na cabeça |
| $q \rightarrow r$ | Se o pensamento ocorre sempre na cabeça, então nenhum espírito sem corpo pensa |
| ∴ $p \rightarrow r$ | Logo, se o cérebro é preciso para o pensamento, nenhum espírito sem corpo pensa |

---

### 2.4 Silogismo Disjuntivo

$$p \lor q,\ \sim p\ \vdash\ q$$

| Premissas | Exemplo |
|---|---|
| $p \lor q$ | Ou se evita as guerras, ou os inocentes sofrem |
| $\sim p$ | Não se evita as guerras |
| ∴ $q$ | Logo, os inocentes sofrem |

---

### 2.5 Silogismo Conjuntivo (Incompatibilidade)

$$\sim(p \land q),\ q\ \vdash\ \sim p$$

| Premissas | Exemplo |
|---|---|
| $\sim(p \land q)$ | É falso que eu estudo e trabalho |
| $q$ | Eu trabalho |
| ∴ $\sim p$ | Logo, eu não estudo |

---

### 2.6 Eliminação da Conjunção (Simplificação)

$$p \land q\ \vdash\ p \qquad\qquad p \land q\ \vdash\ q$$

| Premissas | Exemplo |
|---|---|
| $p \land q$ | João e Marcelo jogarão futebol este sábado |
| ∴ $p$ | Logo, Marcelo jogará futebol este sábado |

---

### 2.7 Introdução da Conjunção

$$p,\ q\ \vdash\ p \land q$$

| Premissas | Exemplo |
|---|---|
| $p$ | A sala está vazia |
| $q$ | O professor está dando aula |
| ∴ $p \land q$ | Logo, a sala está vazia e o professor está dando aula |

---

### 2.8 Introdução da Disjunção (Adição)

$$p\ \vdash\ p \lor q$$

| Premissas | Exemplo |
|---|---|
| $p$ | A sala está vazia |
| ∴ $p \lor q$ | Logo, a sala está vazia ou o professor está na sala |

---

### 2.9 Eliminação da Disjunção

$$p \lor q,\ p \rightarrow r,\ q \rightarrow r\ \vdash\ r$$

| Premissas | Exemplo |
|---|---|
| $p \lor q$ | Eu ou meu irmão ficaremos em casa esta noite |
| $p \rightarrow r$ | Se eu ficar em casa, então a geladeira ficará vazia |
| $q \rightarrow r$ | Se meu irmão ficar em casa, então ele esvaziará a geladeira |
| ∴ $r$ | Logo, a geladeira ficará vazia |

---

### 2.10 Dilema Construtivo

$$p \rightarrow q,\ r \rightarrow s,\ p \lor r\ \vdash\ q \lor s$$

| Premissas | Exemplo |
|---|---|
| $p \rightarrow q$ | Se você conhece as coisas que existem, então você pode conhecer as que não existem |
| $r \rightarrow s$ | Se você é um guerreiro, então você é um estrategista |
| $p \lor r$ | Ora, você conhece as coisas que existem ou você é um guerreiro |
| ∴ $q \lor s$ | Logo, você pode conhecer as coisas que não existem ou é um estrategista |

---

### 2.11 Dilema Destrutivo

$$p \rightarrow q,\ r \rightarrow s,\ \sim q \lor \sim s\ \vdash\ \sim p \lor \sim r$$

| Premissas | Exemplo |
|---|---|
| $p \rightarrow q$ | Se você conhece as coisas que existem, então pode conhecer as que não existem |
| $r \rightarrow s$ | Se você é um guerreiro, então você é um estrategista |
| $\sim q \lor \sim s$ | Ora, você NÃO pode conhecer as coisas que não existem ou você NÃO é um estrategista |
| ∴ $\sim p \lor \sim r$ | Logo, você não conhece as coisas que existem ou não é um guerreiro |

---

## 3. Tabela-Resumo

| Regra | Esquema |
|---|---|
| Modus Ponens | $p \rightarrow q,\ p \vdash q$ |
| Modus Tollens | $p \rightarrow q,\ \sim q \vdash \sim p$ |
| Silogismo Hipotético | $p \rightarrow q,\ q \rightarrow r \vdash p \rightarrow r$ |
| Silogismo Disjuntivo | $p \lor q,\ \sim p \vdash q$ |
| Silogismo Conjuntivo (Incompatibilidade) | $\sim(p \land q),\ q \vdash \sim p$ |
| Eliminação da Conjunção | $p \land q \vdash p$ (ou $q$) |
| Introdução da Conjunção | $p, q \vdash p \land q$ |
| Introdução da Disjunção | $p \vdash p \lor q$ |
| Eliminação da Disjunção | $p \lor q,\ p \rightarrow r,\ q \rightarrow r \vdash r$ |
| Dilema Construtivo | $p \rightarrow q,\ r \rightarrow s,\ p \lor r \vdash q \lor s$ |
| Dilema Destrutivo | $p \rightarrow q,\ r \rightarrow s,\ \sim q \lor \sim s \vdash \sim p \lor \sim r$ |

---

## 4. Exercícios Resolvidos

Para cada argumento, identifica-se a regra de inferência aplicada e a conclusão.

**1)** *Se o sinaleiro está amarelo, então eu freio o carro. O sinaleiro está amarelo. Logo, ...*
- $p$: O sinaleiro está amarelo | $q$: Eu freio o carro
- $p \rightarrow q,\ p \vdash q$ → **Logo, eu freio o carro** (*Modus Ponens*)

**2)** *A verdadeira beleza está em fazer o bem, e ter equilíbrio é ter domínio do espírito sobre a matéria. Logo, ...*
- $p \land q \vdash p$ (ou $q$) → **Logo, a verdadeira beleza está em fazer o bem** (*Eliminação da Conjunção*)

**3)** *Se você tem carteira de motorista, então você pode dirigir um carro. Você tem carteira de motorista. Logo, ...*
- $p \rightarrow q,\ p \vdash q$ → **Logo, você pode dirigir um carro** (*Modus Ponens*)

**4)** *O que somos é a consequência lógica do que pensamos, ou, nosso espírito nasce com nenhuma ideia. Ora, nosso espírito não nasce com nenhuma ideia. Logo, ...*
- $p \lor q,\ \sim q \vdash p$ → **Logo, o que somos é a consequência lógica do que pensamos** (*Silogismo Disjuntivo*)

**5)** *Se um único homem chegar à plenitude do amor, neutraliza o ódio de milhões. Se neutralizar o ódio de milhões, então a solidariedade é o sentido moral que vincula o indivíduo aos interesses de um grupo social. Isto implica que...*
- $p \rightarrow q,\ q \rightarrow r \vdash p \rightarrow r$ → **Logo, $p \rightarrow r$** (*Silogismo Hipotético*)

**6)** *O homem é consciente e livre. Se o homem é consciente e livre, então ele é criador de cultura e construtor de história. Isto implica em que...*
- $p,\ p \rightarrow q \vdash q$ → **Logo, ele é criador de cultura e construtor de história** (*Modus Ponens*)

**7)** *Se você dissipou suas dúvidas pelo caminho que traçou a si mesmo, então você é um sábio. Você não é um sábio. Logo...*
- $p \rightarrow q,\ \sim q \vdash \sim p$ → **Logo, você não dissipou suas dúvidas pelo caminho que traçou a si mesmo** (*Modus Tollens*)

**8)** *O paciente não pode estar bem e estar com febre. O paciente está bem. Logo...*
- $\sim(p \land q) \equiv \sim p \lor \sim q$ (De Morgan); com $p$ verdadeiro: $\sim p \lor \sim q,\ p \vdash \sim q$ → **Logo, o paciente não está com febre** (*Silogismo Disjuntivo*)

**9)** *Pensa ou empobrece. Não empobrece. Logo...*
- $p \lor q,\ \sim q \vdash p$ → **Logo, pensa** (*Silogismo Disjuntivo*)

**10)** *Se Deus existe, então a vida tem significado. Deus existe. Portanto...*
- $p \rightarrow q,\ p \vdash q$ → **Logo, a vida tem significado** (*Modus Ponens*)

**11)** *Se hoje for quinta-feira, então amanhã será sexta-feira. Se amanhã for sexta, então depois de amanhã será sábado. Portanto...*
- $p \rightarrow q,\ q \rightarrow r \vdash p \rightarrow r$ → **Logo, se hoje for quinta-feira, então depois de amanhã será sábado** (*Silogismo Hipotético*)

**12)** *Se você tem uma senha, então você pode efetuar login na rede. Você tem uma senha. Portanto...*
- $p \rightarrow q,\ p \vdash q$ → **Logo, você pode efetuar login na rede** (*Modus Ponens*)

**13)** *Se Zeus é humano, então Zeus é mortal. Zeus não é mortal. Logo...*
- $p \rightarrow q,\ \sim q \vdash \sim p$ → **Logo, Zeus não é humano** (*Modus Tollens*)

**14)** *"Está abaixo de zero agora." Portanto, "está abaixo de zero agora ou está chovendo agora"*
- $p \vdash p \lor q$ → **Logo, está abaixo de zero agora ou está chovendo agora** (*Introdução da Disjunção*)

**15)** *Está abaixo de zero e chovendo agora. Logo, ...*
- $p \land q \vdash p$ (ou $q$) → **Logo, está abaixo de zero** (ou: **está chovendo agora**) (*Eliminação da Conjunção*)

**16)** *Está chovendo ou está nevando. Não está nevando. Logo...*
- $p \lor q,\ \sim q \vdash p$ → **Logo, está chovendo** (*Silogismo Disjuntivo*)

---

## 5. Observação Importante

Repare que, na maioria dos exercícios, o processo de resolução segue os mesmos três passos:

1. **Traduzir** cada proposição simples da frase para uma variável ($p$, $q$, $r$, ...)
2. **Identificar** o esquema/regra de inferência que corresponde à estrutura das premissas
3. **Aplicar** a regra para obter a conclusão, "traduzindo" de volta para a linguagem natural

Esse é exatamente o tipo de exercício comum em provas de concurso, e a maior dificuldade costuma estar na **tradução da linguagem natural para a lógica formal** — não na aplicação da regra em si, que é praticamente mecânica uma vez identificado o padrão correto.

## 📚 Referências Bibliográficas

*   MARIETTO, Maria das Graças Bruno. **Lógica Básica**: cálculo proposicional, tabelas-verdade, equivalências e inferências. Santo André: Universidade Federal do ABC, 2013.
*   MARTINS, Luiz Gustavo. **Apostila de Lógica Proposicional**: dedução natural, sintaxe e semântica. Santo André: Universidade Federal do ABC, 2012.
*   MORTARI, Cezar A. **Introdução à lógica**. 2. ed. São Paulo: Editora Unesp, 2016.
