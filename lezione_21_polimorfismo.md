# Polimorfismo

Il polimorfismo è uno dei concetti fondamentali della programmazione orientata agli oggetti, che permette di scrivere codice più flessibile e riutilizzabile. In particolare, il polimorfismo si manifesta attraverso la sovrascrittura dei metodi e il polimorfismo dinamico.

## Sovrascrittura dei metodi

La sovrascrittura dei metodi è una tecnica che consente a una classe figlia di ridefinire un metodo già definito nella classe madre. In questo modo, è possibile personalizzare il comportamento di un metodo senza doverlo riscrivere da zero. Ad esempio, se abbiamo una classe `Animale` con un metodo `emettereSuono()`, possiamo definire una classe `Cane` che estende `Animale` e ridefinire il metodo `emettereSuono()` per far sì che il cane abbaia invece che emettere un suono generico.

```java
public class Animale {
    public void emettereSuono() {
        System.out.println("Suono generico");
    }
}

public class Cane extends Animale {
    @Override
    public void emettereSuono() {
        System.out.println("Bau bau");
    }
}
```

## Polimorfismo dinamico

Il polimorfismo dinamico si manifesta quando si utilizza un riferimento di tipo di una classe madre per riferirsi a un oggetto della classe figlia. In questo modo, è possibile invocare i metodi ridefiniti nella classe figlia utilizzando il riferimento della classe madre. Ad esempio, se abbiamo un array di oggetti di tipo `Animale` che contiene anche oggetti di tipo `Cane`, possiamo invocare il metodo `emettereSuono()` su ciascun oggetto e ottenere il comportamento corretto in base al tipo effettivo dell'oggetto.

```java
Animale[] animali = new Animale[2];
animali[0] = new Animale();
animali[1] = new Cane();

for (Animale animale : animali) {
    animale.emettereSuono(); // Stampa "Suono generico" e "Bau bau"
}
```

In conclusione, il polimorfismo è un concetto potente che permette di scrivere codice più flessibile e scalabile, consentendo una maggiore modularità e facilitando la manutenzione del codice. Grazie alla sovrascrittura dei metodi e al polimorfismo dinamico, è possibile scrivere codice più generico e riutilizzabile, migliorando la qualità e la leggibilità del software.