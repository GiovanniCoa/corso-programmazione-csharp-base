# Cicli: while e do-while

I cicli sono una caratteristica fondamentale dei linguaggi di programmazione, in quanto consentono di eseguire ripetutamente un blocco di istruzioni fino a quando una determinata condizione viene soddisfatta. Tra i cicli più utilizzati troviamo il ciclo `while` e il ciclo `do-while`, entrambi utilizzati per ripetere un blocco di istruzioni finché una certa condizione risulta vera.

## Ciclo while

Il ciclo `while` è un ciclo a condizione pre-test, ossia la condizione viene valutata all'inizio di ogni iterazione. Se la condizione è vera, il blocco di istruzioni viene eseguito, altrimenti il ciclo termina. Il ciclo `while` ha la seguente struttura:

```python
while condizione:
    istruzione1
    istruzione2
    ...
```

Il blocco di istruzioni viene eseguito finché la condizione specificata risulta vera. È importante prestare attenzione affinché la condizione venga modificata all'interno del blocco, altrimenti si rischia di incorrere in un ciclo infinito.

## Ciclo do-while

Il ciclo `do-while` è un ciclo a condizione post-test, ossia la condizione viene valutata alla fine di ogni iterazione. Ciò significa che il blocco di istruzioni viene eseguito almeno una volta, indipendentemente dalla condizione. La struttura del ciclo `do-while` è la seguente:

```python
do:
    istruzione1
    istruzione2
    ...
while condizione
```

Il blocco di istruzioni viene eseguito almeno una volta, dopodiché la condizione viene valutata. Se la condizione è vera, il blocco viene eseguito di nuovo, altrimenti il ciclo termina.

## Conclusione

In conclusione, i cicli `while` e `do-while` sono due strumenti fondamentali per gestire ripetizioni all'interno di un programma. È importante comprendere le differenze tra i due cicli e utilizzarli in base alle esigenze specifiche del problema da risolvere. Entrambi i cicli consentono di automatizzare il processo di esecuzione di un blocco di istruzioni fino a quando una determinata condizione viene soddisfatta.