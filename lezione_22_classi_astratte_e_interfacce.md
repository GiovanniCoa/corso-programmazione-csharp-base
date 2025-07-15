# Classi astratte e interfacce

Le classi astratte e le interfacce sono concetti fondamentali della programmazione orientata agli oggetti, che permettono di definire classi incomplete e contratti che le classi concrete devono rispettare.

## Classi astratte

Le classi astratte sono classi che non possono essere istanziate direttamente, ma possono contenere metodi astratti, ossia metodi che devono essere implementati dalle sottoclassi. Una classe astratta può contenere anche metodi con implementazioni concrete, che possono essere ereditati dalle sottoclassi.

Per dichiarare una classe astratta in Java, si utilizza la parola chiave `abstract` prima della parola chiave `class`. Ad esempio:

```java
public abstract class Figura {
    public abstract double calcolaArea();
}
```

Nell'esempio sopra, la classe `Figura` è una classe astratta che contiene il metodo astratto `calcolaArea`, che deve essere implementato dalle sottoclassi.

## Interfacce

Le interfacce sono simili alle classi astratte, ma possono contenere solo metodi astratti e costanti. Una classe può implementare più interfacce, ma può estendere una sola classe astratta. Le interfacce permettono di definire contratti che le classi concrete devono rispettare.

Per dichiarare un'interfaccia in Java, si utilizza la parola chiave `interface`. Ad esempio:

```java
public interface Forma {
    double calcolaPerimetro();
}
```

Nell'esempio sopra, l'interfaccia `Forma` contiene il metodo astratto `calcolaPerimetro`, che deve essere implementato dalle classi che la implementano.

## Differenze tra classi astratte e interfacce

Le classi astratte e le interfacce hanno alcune differenze fondamentali. Le classi astratte possono contenere variabili di istanza e metodi con implementazioni concrete, mentre le interfacce possono contenere solo costanti e metodi astratti. Inoltre, una classe può estendere una sola classe astratta, ma può implementare più interfacce.

In generale, si consiglia di utilizzare le interfacce quando si vuole definire un contratto che più classi possono implementare in modo diverso, e le classi astratte quando si vuole fornire una base comune con implementazioni concrete.

In conclusione, le classi astratte e le interfacce sono strumenti potenti della programmazione orientata agli oggetti che permettono di definire classi incomplete e contratti che le classi concrete devono rispettare. È importante comprendere le differenze tra le due e utilizzarle in modo appropriato per progettare un codice robusto e manutenibile.