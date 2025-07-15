# Introduzione a Entity Framework Core

Entity Framework Core è un ORM (Object-Relational Mapping) che permette agli sviluppatori di gestire facilmente la persistenza dei dati in un database relazionale utilizzando il linguaggio di programmazione C#. Questo framework fornisce un'interfaccia di programmazione semplice e intuitiva per interagire con il database, senza la necessità di scrivere query SQL manualmente.

## Funzionalità principali

Entity Framework Core offre numerose funzionalità che semplificano lo sviluppo di applicazioni basate su database relazionali. Tra le principali caratteristiche troviamo:

- Mapping delle entità: Entity Framework Core permette di mappare le classi C# alle tabelle del database in modo automatico, riducendo al minimo la necessità di scrivere codice di mapping personalizzato.
- Query LINQ: è possibile utilizzare LINQ (Language Integrated Query) per scrivere query in modo dichiarativo, facilitando la manipolazione dei dati.
- Migrazioni del database: Entity Framework Core supporta le migrazioni del database, consentendo di aggiornare lo schema del database in modo incrementale tramite codice C#.
- Gestione delle transazioni: è possibile gestire le transazioni in modo semplice e intuitivo utilizzando Entity Framework Core.
- Supporto per database relazionali: Entity Framework Core supporta una vasta gamma di database relazionali, tra cui SQL Server, MySQL, PostgreSQL e SQLite.

## Utilizzo di Entity Framework Core

Per utilizzare Entity Framework Core all'interno di un progetto C#, è necessario installare il pacchetto NuGet `Microsoft.EntityFrameworkCore`. Una volta installato il pacchetto, è possibile definire le entità del modello di dati utilizzando classi C# e annotazioni per configurare il mapping delle entità al database.

Di seguito un esempio di definizione di un'entità utilizzando Entity Framework Core:

```csharp
public class Customer
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Email { get; set; }
}
```

Una volta definita l'entità, è possibile creare un contesto del database che erediti dalla classe `DbContext` di Entity Framework Core e definire le proprietà di tipo `DbSet` per rappresentare le entità del modello di dati.

```csharp
public class AppDbContext : DbContext
{
    public DbSet<Customer> Customers { get; set; }
}
```

Infine, è possibile utilizzare il contesto del database per interagire con il database utilizzando query LINQ e le API messe a disposizione da Entity Framework Core.

## Conclusioni

Entity Framework Core è uno strumento potente e flessibile per la gestione della persistenza dei dati in un database relazionale utilizzando C#. Grazie alle sue numerose funzionalità e alla sua facilità di utilizzo, questo framework risulta essere una scelta ideale per lo sviluppo di applicazioni basate su database relazionali.