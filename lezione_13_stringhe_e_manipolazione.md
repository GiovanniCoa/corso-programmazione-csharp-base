# Stringhe e manipolazione

Le stringhe sono uno dei tipi di dati fondamentali in qualsiasi linguaggio di programmazione e sono utilizzate per rappresentare sequenze di caratteri. In Java, le stringhe sono gestite tramite la classe String, che fornisce numerosi metodi per manipolare e lavorare con le stringhe.

## Creazione di stringhe

Per creare una stringa in Java, è possibile utilizzare il costruttore della classe String passando come argomento la sequenza di caratteri desiderata:

```java
String nome = new String("Mario");
```

Oppure è possibile utilizzare la sintassi letterale per la creazione di stringhe:

```java
String cognome = "Rossi";
```

## Concatenazione di stringhe

La concatenazione di stringhe è un'operazione comune e può essere eseguita utilizzando l'operatore `+` o il metodo `concat` della classe String:

```java
String nomeCompleto = nome + " " + cognome;
String saluto = "Ciao ".concat(nome);
```

## Accesso ai singoli caratteri

Per accedere ai singoli caratteri di una stringa, è possibile utilizzare il metodo `charAt` della classe String, che restituisce il carattere corrispondente alla posizione specificata:

```java
char primoCarattere = nome.charAt(0);
char ultimoCarattere = cognome.charAt(cognome.length() - 1);
```

## Manipolazione delle stringhe

La classe String fornisce numerosi metodi per manipolare le stringhe, tra cui:

- `length()`: restituisce la lunghezza della stringa
- `toUpperCase()`: converte la stringa in maiuscolo
- `toLowerCase()`: converte la stringa in minuscolo
- `trim()`: rimuove gli spazi bianchi all'inizio e alla fine della stringa
- `substring(int beginIndex, int endIndex)`: restituisce una sottostringa della stringa originale

```java
String testo = "   Ciao Mondo   ";
int lunghezza = testo.length(); // 15
String testoMaiuscolo = testo.toUpperCase(); // "   CIAO MONDO   "
String testoTrimmed = testo.trim(); // "Ciao Mondo"
String sottostringa = testo.substring(5, 10); // "Mondo"
```

## Conclusioni

La classe String in Java fornisce numerosi metodi per manipolare e lavorare con le stringhe in modo efficiente e flessibile. Conoscere i principali metodi della classe String è fondamentale per poter gestire correttamente le operazioni di manipolazione delle stringhe all'interno di un programma Java.