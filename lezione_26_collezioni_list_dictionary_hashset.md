# Collezioni: List, Dictionary, HashSet

Le collezioni sono un concetto fondamentale nella programmazione. Consentono di gestire e organizzare un insieme di elementi in modo efficiente e flessibile. In questo articolo esamineremo tre tipi di collezioni generiche molto utilizzate in C#: List, Dictionary e HashSet.

## List

La classe List è una collezione ordinata di elementi, che possono essere di qualsiasi tipo. È possibile aggiungere, rimuovere, cercare e ordinare gli elementi all'interno di una List. Ad esempio, per creare una List di interi si può utilizzare il seguente codice:

```csharp
List<int> numeri = new List<int>();
```

Per aggiungere un elemento alla List si può utilizzare il metodo Add:

```csharp
numeri.Add(10);
```

Per accedere agli elementi all'interno della List si può utilizzare l'indice:

```csharp
int primoElemento = numeri[0];
```

## Dictionary

Il Dictionary è una collezione di coppie chiave-valore, dove la chiave è univoca all'interno del Dictionary. È possibile aggiungere, rimuovere e cercare elementi all'interno di un Dictionary in modo efficiente. Ad esempio, per creare un Dictionary di stringhe e interi si può utilizzare il seguente codice:

```csharp
Dictionary<string, int> studentiVoti = new Dictionary<string, int>();
```

Per aggiungere una coppia chiave-valore al Dictionary si può utilizzare il metodo Add:

```csharp
studentiVoti.Add("Mario", 8);
```

Per accedere al valore associato a una determinata chiave si può utilizzare la sintassi seguente:

```csharp
int votoMario = studentiVoti["Mario"];
```

## HashSet

Il HashSet è una collezione non ordinata di elementi univoci, che non consente duplicati. È possibile aggiungere, rimuovere e verificare la presenza di elementi all'interno di un HashSet in modo efficiente. Ad esempio, per creare un HashSet di stringhe si può utilizzare il seguente codice:

```csharp
HashSet<string> nomi = new HashSet<string>();
```

Per aggiungere un elemento al HashSet si può utilizzare il metodo Add:

```csharp
nomi.Add("Alice");
```

Per verificare se un elemento è presente all'interno del HashSet si può utilizzare il metodo Contains:

```csharp
bool contieneAlice = nomi.Contains("Alice");
```

## Conclusioni

Le collezioni List, Dictionary e HashSet sono tre tipi di collezioni generiche molto utili in C#. Ognuna di esse ha caratteristiche specifiche che le rendono adatte a diversi scenari di utilizzo. È importante comprendere quando e come utilizzare ciascuna di queste collezioni per scrivere codice efficiente e manutenibile.