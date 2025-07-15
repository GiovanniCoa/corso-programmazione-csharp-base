# Metodi: definizione e chiamata

I metodi sono blocchi di codice riutilizzabili all'interno di un programma che eseguono una specifica operazione. Essi permettono di organizzare il codice in maniera modulare, migliorando la leggibilità e facilitando la manutenzione. In questo articolo, esploreremo la definizione e la chiamata dei metodi, concentrandoci sull'utilizzo di parametri e valori di ritorno.

## Definizione di un metodo

Un metodo è definito all'interno di una classe e può avere zero o più parametri di input e un valore di ritorno. La sintassi per la definizione di un metodo in Java è la seguente:

```java
public tipoValoreDiRitorno nomeMetodo(tipoParametro1 nomeParametro1, tipoParametro2 nomeParametro2, ...) {
    // corpo del metodo
}
```

Nella definizione di un metodo, è possibile specificare il tipo di dato del valore di ritorno e dei parametri, nonché il modificatore di accesso (public, private, protected) e altre proprietà come static o final.

## Chiamata di un metodo

Per chiamare un metodo, è necessario utilizzare il nome del metodo seguito da parentesi tonde che contengono eventuali parametri di input. Se il metodo restituisce un valore, è possibile utilizzarlo in diverse modalità:

```java
tipoValoreDiRitorno risultato = nomeOggetto.nomeMetodo(valoreParametro1, valoreParametro2, ...);
```

## Utilizzo di parametri e ritorno

I parametri consentono di passare informazioni al metodo per eseguire operazioni specifiche. È possibile utilizzare parametri di diversi tipi di dati, come interi, stringhe, oggetti personalizzati, ecc. Ad esempio:

```java
public int somma(int a, int b) {
    return a + b;
}
```

Nell'esempio sopra, il metodo `somma` prende due parametri di tipo intero e restituisce la loro somma.

Il valore di ritorno di un metodo può essere di qualsiasi tipo di dato, incluso void se il metodo non restituisce alcun valore. Ad esempio:

```java
public void stampaMessaggio(String messaggio) {
    System.out.println(messaggio);
}
```

In questo caso, il metodo `stampaMessaggio` prende una stringa come parametro e non restituisce alcun valore.

In conclusione, l'utilizzo di metodi con parametri e valori di ritorno è fondamentale per la scrittura di codice modulare e ben strutturato. La corretta definizione e chiamata dei metodi permette di migliorare la manutenibilità del codice e favorisce la riutilizzabilità delle operazioni definite.