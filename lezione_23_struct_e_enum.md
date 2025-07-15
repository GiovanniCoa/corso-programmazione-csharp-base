# Struct e enum

## Introduzione
In questo articolo approfondiremo i concetti di **struct** e **enum** in linguaggi di programmazione come C, C++ e Rust. Questi due tipi di dati sono fondamentali per organizzare e strutturare le informazioni in maniera efficiente e compatta.

## Struct
Una **struct**, abbreviazione di *structure*, è un tipo di dato composto che permette di raggruppare diverse variabili sotto un'unica entità. Le variabili all'interno di una struct sono definite campi o membri e possono essere di diversi tipi, come interi, float, stringhe o altre strutture.

```c
struct Persona {
    char nome[50];
    int eta;
    float altezza;
};
```

Nell'esempio sopra, abbiamo definito una struct chiamata `Persona` con tre campi: `nome`, `età` e `altezza`. Possiamo creare variabili di tipo `Persona` e accedere ai suoi campi utilizzando l'operatore `.`.

```c
struct Persona p;
strcpy(p.nome, "Mario");
p.eta = 30;
p.altezza = 1.75;
```

Le struct sono particolarmente utili quando si desidera rappresentare oggetti complessi e organizzare i dati in modo coerente.

## Enum
Un **enum**, abbreviazione di *enumeration*, è un tipo di dato che permette di definire un insieme di costanti con nomi simbolici. Ogni costante all'interno di un enum ha un valore intero associato, che di default parte da 0 e viene incrementato di 1 per ogni costante successiva.

```c
enum Mesi {
    GENNAIO,
    FEBBRAIO,
    MARZO,
    APRILE,
    MAGGIO,
    GIUGNO,
    LUGLIO,
    AGOSTO,
    SETTEMBRE,
    OTTOBRE,
    NOVEMBRE,
    DICEMBRE
};
```

Nell'esempio sopra, abbiamo definito un enum chiamato `Mesi` con dodici costanti che rappresentano i mesi dell'anno. Possiamo utilizzare queste costanti per rendere il codice più leggibile e manutenibile.

```c
enum Mesi meseCorrente = MAGGIO;
if (meseCorrente == MAGGIO) {
    printf("Stiamo nel mese di Maggio");
}
```

Grazie agli enum possiamo evitare di utilizzare numeri magici nel codice, migliorando la comprensione e la manutenibilità dello stesso.

## Conclusione
Le struct e gli enum sono due tipi di dati fondamentali per organizzare e strutturare le informazioni in maniera efficiente nei linguaggi di programmazione. Le struct ci permettono di creare oggetti complessi con diversi campi, mentre gli enum semplificano la gestione di costanti con nomi simbolici. Utilizzando in modo corretto struct e enum, possiamo rendere il nostro codice più chiaro, leggibile e manutenibile.