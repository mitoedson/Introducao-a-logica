
# Exercícios: FBF

Prove que a expressão $((P \land Q) \lor (\neg P \land \neg Q))$ é uma fórmula proposicional válida.*

**Solução (aplicando as regras indutivas passo a passo):**

1.  $P$ e $Q$ são fórmulas pela **Regra 2** (símbolos proposicionais).
2.  $(P \land Q)$ é uma fórmula pela **Regra 4.2** aplicada ao passo 1.
3.  $(\neg P)$ e $(\neg Q)$ são fórmulas pela **Regra 3** aplicada ao passo 1.
4.  $(\neg P \land \neg Q)$ é uma fórmula pela **Regra 4.2** aplicada ao passo 3.
5.  $((P \land Q) \lor (\neg P \land \neg Q))$ é uma fórmula pela **Regra 4.1** aplicada aos passos 2 e 4.  
*(Demonstração concluída com sucesso)*.

---