# Pattern di progettazione comuni

Nel mondo dello sviluppo software, i pattern di progettazione sono soluzioni comuni ai problemi ricorrenti che si presentano durante la progettazione e l'implementazione di un sistema software. Questi pattern forniscono una guida per la creazione di codice robusto, flessibile e manutenibile.

Tra i pattern di progettazione più comuni e utilizzati vi sono il Singleton, il Factory e l'Observer.

## Singleton

Il pattern Singleton è uno dei pattern più semplici e utilizzati. La sua intenzione è garantire che una classe abbia una sola istanza e fornire un punto di accesso globale a tale istanza. Questo è particolarmente utile quando si vuole garantire che una classe venga istanziata una sola volta e che tutte le parti del sistema condividano lo stesso stato.

```java
public class Singleton {
    private static Singleton instance;

    private Singleton() {}

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}
```

## Factory

Il pattern Factory è utilizzato per creare oggetti senza specificare esplicitamente la classe dell'oggetto da creare. In questo modo si separa la creazione di un oggetto dalla sua implementazione, rendendo il codice più flessibile e facile da estendere.

```java
public interface Shape {
    void draw();
}

public class Circle implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing a circle");
    }
}

public class Square implements Shape {
    @Override
    public void draw() {
        System.out.println("Drawing a square");
    }
}

public class ShapeFactory {
    public Shape createShape(String type) {
        if (type.equals("circle")) {
            return new Circle();
        } else if (type.equals("square")) {
            return new Square();
        }
        return null;
    }
}
```

## Observer

Il pattern Observer è utilizzato per gestire la dipendenza uno-a-molti tra oggetti in modo che quando un oggetto cambia stato, tutti gli oggetti dipendenti vengano notificati e aggiornati automaticamente. Questo pattern è ampiamente utilizzato nell'implementazione di interfacce grafiche e applicazioni che richiedono la notifica di eventi.

```java
import java.util.ArrayList;
import java.util.List;

public interface Observer {
    void update(String message);
}

public class Subject {
    private List<Observer> observers = new ArrayList<>();

    public void addObserver(Observer observer) {
        observers.add(observer);
    }

    public void removeObserver(Observer observer) {
        observers.remove(observer);
    }

    public void notifyObservers(String message) {
        for (Observer observer : observers) {
            observer.update(message);
        }
    }
}

public class ConcreteObserver implements Observer {
    @Override
    public void update(String message) {
        System.out.println("Received message: " + message);
    }
}
```

Questi sono solo alcuni dei pattern di progettazione più comuni e utilizzati nel mondo dello sviluppo software. Ogni pattern ha le proprie caratteristiche e vantaggi, e la loro corretta applicazione può contribuire a migliorare la qualità e la manutenibilità del codice. È importante familiarizzare con questi pattern e saperli utilizzare in modo appropriato per affront