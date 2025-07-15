# Data binding in WPF

Il data binding è una delle caratteristiche fondamentali del Windows Presentation Foundation (WPF), che consente di collegare facilmente i controlli dell'interfaccia utente (UI) ai dati sottostanti. Questo meccanismo permette di sincronizzare automaticamente i dati tra la UI e il modello dati, garantendo coerenza e facilitando la gestione dei dati all'interno dell'applicazione.

## Vantaggi del data binding in WPF

Il data binding in WPF offre numerosi vantaggi, tra cui:

- **Risparmio di codice**: grazie al data binding è possibile evitare la scrittura di codice boilerplate per aggiornare manualmente i controlli UI quando i dati sottostanti cambiano.
- **Separazione tra UI e logica di business**: il data binding consente di separare in modo chiaro la presentazione dei dati dall'elaborazione logica, migliorando la manutenibilità e la scalabilità dell'applicazione.
- **Aggiornamenti in tempo reale**: i cambiamenti nei dati vengono immediatamente riflesse nella UI, consentendo agli utenti di visualizzare informazioni aggiornate in tempo reale.
- **Supporto per la validazione dei dati**: il data binding offre un supporto integrato per la validazione dei dati in input, garantendo che solo dati corretti vengano inseriti nel sistema.

## Come funziona il data binding in WPF

Il data binding in WPF si basa su tre principali componenti:

1. **Source**: rappresenta l'origine dei dati, che può essere un oggetto CLR, una proprietà, una raccolta di dati o qualsiasi altro tipo di origine dati.
2. **Target**: rappresenta il controllo UI che visualizza o modifica i dati.
3. **Path**: definisce la relazione tra l'origine dei dati e il controllo UI.

Il data binding in WPF può essere unidirezionale o bidirezionale, consentendo di aggiornare i dati sia dalla UI al modello dati che viceversa. Inoltre, è possibile utilizzare convertitori di valori per modificare i dati durante il processo di binding.

## Esempio di data binding in WPF

Di seguito è riportato un esempio di come utilizzare il data binding in WPF per collegare un TextBox al testo di un'etichetta:

1. Definire il modello dati:

```csharp
public class ViewModel : INotifyPropertyChanged
{
    private string _text;

    public string Text
    {
        get { return _text; }
        set
        {
            _text = value;
            OnPropertyChanged(nameof(Text));
        }
    }

    public event PropertyChangedEventHandler PropertyChanged;

    protected void OnPropertyChanged(string propertyName)
    {
        PropertyChanged?.Invoke(this, new PropertyChangedEventArgs(propertyName));
    }
}
```

2. Configurare il data binding nel file XAML:

```xaml
<Window.DataContext>
    <local:ViewModel/>
</Window.DataContext>
<StackPanel>
    <TextBox Text="{Binding Text, Mode=TwoWay, UpdateSourceTrigger=PropertyChanged}"/>
    <Label Content="{Binding Text}"/>
</StackPanel>
```

In questo modo, il testo inserito nel TextBox verrà automaticamente aggiornato nell'etichetta senza la necessità di scrivere codice aggiuntivo.