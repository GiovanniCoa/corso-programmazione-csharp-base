# Programmazione orientata agli oggetti: classi e oggetti

La programmazione orientata agli oggetti è un paradigma di programmazione che si basa sull'organizzazione del codice in classi e oggetti. Le classi rappresentano modelli astratti di entità del mondo reale, mentre gli oggetti sono le istanze concrete di tali classi.

## Concetti base

Le classi definiscono la struttura e il comportamento degli oggetti. Ogni classe è composta da attributi, che rappresentano le caratteristiche dell'oggetto, e metodi, che definiscono il comportamento dell'oggetto. Gli oggetti sono le istanze delle classi, cioè le entità concrete che possiamo manipolare nel codice.

La programmazione orientata agli oggetti si basa su quattro principi fondamentali: incapsulamento, ereditarietà, polimorfismo e astrazione. L'incapsulamento permette di nascondere i dettagli implementativi di una classe, favorendo la modularità e la manutenibilità del codice. L'ereditarietà consente di creare nuove classi basate su classi esistenti, ereditando attributi e metodi. Il polimorfismo permette a oggetti di classi diverse di rispondere allo stesso messaggio in modi diversi. L'astrazione permette di definire classi che rappresentano concetti astratti, senza dover specificare tutti i dettagli implementativi.

## Creazione di oggetti

Per creare un oggetto, dobbiamo prima definire la relativa classe. Ad esempio, se vogliamo creare una classe `Persona` con attributi `nome` e `cognome`, e un metodo `saluta`, possiamo procedere nel seguente modo:

```python
class Persona:
    def __init__(self, nome, cognome):
        self.nome = nome
        self.cognome = cognome

    def saluta(self):
        print(f"Ciao, sono {self.nome} {self.cognome}")
```

Una volta definita la classe `Persona`, possiamo creare un oggetto di tipo `Persona` utilizzando il costruttore `__init__`:

```python
persona1 = Persona("Mario", "Rossi")
persona1.saluta()  # Output: Ciao, sono Mario Rossi
```

In questo modo abbiamo creato un oggetto di tipo `Persona` con attributi `nome` e `cognome` impostati rispettivamente a "Mario" e "Rossi", e abbiamo invocato il metodo `saluta` sull'oggetto creato.

In conclusione, la programmazione orientata agli oggetti ci permette di organizzare il codice in classi e oggetti, facilitando la gestione e la manipolazione dei dati. La corretta comprensione dei concetti base e la pratica nella creazione di oggetti sono fondamentali per sfruttare appieno i vantaggi di questo paradigma di programmazione.