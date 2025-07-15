# Ereditarietà

Nella programmazione orientata agli oggetti, l'ereditarietà è un concetto fondamentale che consente di derivare nuove classi da classi esistenti, permettendo così il riutilizzo del codice e la creazione di gerarchie di classi. 

## Concetto di ereditarietà

L'ereditarietà si basa sul concetto di classe base e classe derivata. La classe base è la classe originale da cui si desidera derivare nuove classi, mentre le classi derivate sono le classi che ereditano attributi e metodi dalla classe base. 

## Vantaggi dell'ereditarietà

L'ereditarietà offre diversi vantaggi nella progettazione del software. Innanzitutto, permette di evitare la duplicazione del codice, migliorando la manutenibilità e riducendo il rischio di errori. Inoltre, consente di creare gerarchie di classi che rappresentano in modo più accurato le relazioni tra gli oggetti del dominio del problema. Infine, l'ereditarietà favorisce la modularità del codice, permettendo di separare le responsabilità delle varie classi e facilitando la comprensione e la gestione del software.

## Utilizzo dell'ereditarietà

Per utilizzare l'ereditarietà in un linguaggio di programmazione orientato agli oggetti, è necessario definire una classe base e una o più classi derivate che estendono la classe base. Le classi derivate ereditano tutti gli attributi e metodi della classe base e possono aggiungere nuovi attributi e metodi o ridefinire quelli esistenti. 

Ad esempio, supponiamo di avere una classe `Veicolo` come classe base e due classi derivate `Auto` e `Camion`. La classe `Veicolo` potrebbe contenere attributi e metodi comuni a tutti i veicoli, mentre le classi `Auto` e `Camion` potrebbero aggiungere attributi e metodi specifici per le auto e i camion rispettivamente. 

```java
public class Veicolo {
    private String targa;
    private int anno;
    
    public Veicolo(String targa, int anno) {
        this.targa = targa;
        this.anno = anno;
    }
    
    // Metodi comuni a tutti i veicoli
}

public class Auto extends Veicolo {
    private int numeroPorte;
    
    public Auto(String targa, int anno, int numeroPorte) {
        super(targa, anno);
        this.numeroPorte = numeroPorte;
    }
    
    // Metodi specifici per le auto
}

public class Camion extends Veicolo {
    private int capacitaCarico;
    
    public Camion(String targa, int anno, int capacitaCarico) {
        super(targa, anno);
        this.capacitaCarico = capacitaCarico;
    }
    
    // Metodi specifici per i camion
}
```

## Conclusioni

L'ereditarietà è un concetto potente che consente di creare gerarchie di classi e di riutilizzare il codice in modo efficiente. Utilizzando l'ereditarietà in modo corretto, è possibile migliorare la manutenibilità, la modularità e