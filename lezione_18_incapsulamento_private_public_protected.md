# Incapsulamento: private, public, protected

L'incapsulamento è uno dei principi fondamentali della programmazione orientata agli oggetti che permette di controllare l'accesso ai membri di una classe, garantendo un livello di sicurezza e protezione dei dati. In particolare, in linguaggi come Java e C++, è possibile specificare tre livelli di visibilità per i membri di una classe: private, public e protected.

## Private

I membri dichiarati come private sono accessibili solo all'interno della stessa classe in cui sono definiti. Questo significa che non è possibile accedere direttamente a tali membri da altre classi o oggetti. L'incapsulamento dei membri come private è particolarmente utile per nascondere dettagli implementativi e proteggere i dati sensibili da modifiche esterne non autorizzate.

```java
public class MyClass {
    private int privateMember;
    
    public void setPrivateMember(int value) {
        this.privateMember = value;
    }
    
    public int getPrivateMember() {
        return this.privateMember;
    }
}
```

Nell'esempio sopra, il campo `privateMember` è accessibile solo all'interno della classe `MyClass` attraverso i metodi `setPrivateMember` e `getPrivateMember`.

## Public

I membri dichiarati come public sono accessibili da qualsiasi classe o oggetto. Questo significa che i membri pubblici possono essere modificati e letti da qualsiasi parte del codice che ne ha accesso. L'incapsulamento dei membri come public è utile per esporre l'interfaccia pubblica di una classe e consentire l'interazione con altri oggetti.

```java
public class MyClass {
    public int publicMember;
}
```

Nell'esempio sopra, il campo `publicMember` è accessibile da qualsiasi parte del codice che ha accesso alla classe `MyClass`.

## Protected

I membri dichiarati come protected sono accessibili all'interno della stessa classe, delle sottoclassi e delle classi nello stesso package. Questo livello di visibilità è utile per garantire che i membri siano accessibili solo alle classi che ne hanno bisogno per estendere o implementare funzionalità.

```java
public class MyClass {
    protected int protectedMember;
}
```

Nell'esempio sopra, il campo `protectedMember` è accessibile all'interno della classe `MyClass`, delle sue sottoclassi e delle classi nello stesso package.

In conclusione, l'incapsulamento dei membri di una classe come private, public o protected permette di controllare l'accesso ai dati e alle funzionalità della classe, garantendo un codice più sicuro, manutenibile e flessibile. È importante scegliere il livello di visibilità appropriato per ogni membro in base alle esigenze di progettazione e alla logica dell'applicazione.