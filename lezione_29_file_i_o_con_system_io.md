# File I/O con System.IO

Il namespace `System.IO` fornisce le classi necessarie per effettuare operazioni di input/output su file di testo e binari in un'applicazione C#. Grazie a queste classi è possibile leggere e scrivere dati da e verso file, gestire la creazione di file, le operazioni di copia e di spostamento.

## Lettura di file di testo

Per leggere un file di testo si utilizza la classe `StreamReader`, che permette di aprire un file e leggerne il contenuto riga per riga. Ecco un esempio di come leggere un file di testo:

```csharp
using System;
using System.IO;

class Program
{
    static void Main()
    {
        using (StreamReader sr = new StreamReader("testo.txt"))
        {
            string line;
            while ((line = sr.ReadLine()) != null)
            {
                Console.WriteLine(line);
            }
        }
    }
}
```

## Scrittura di file di testo

Per scrivere su un file di testo si utilizza la classe `StreamWriter`, che permette di aprire un file e scriverci del testo. Ecco un esempio di come scrivere su un file di testo:

```csharp
using System;
using System.IO;

class Program
{
    static void Main()
    {
        using (StreamWriter sw = new StreamWriter("output.txt"))
        {
            sw.WriteLine("Hello, World!");
        }
    }
}
```

## Lettura e scrittura di file binari

Per leggere e scrivere file binari si utilizzano le classi `BinaryReader` e `BinaryWriter`. Queste classi permettono di leggere e scrivere dati in formato binario. Ecco un esempio di come leggere e scrivere un file binario:

```csharp
using System;
using System.IO;

class Program
{
    static void Main()
    {
        using (BinaryWriter bw = new BinaryWriter(File.Open("dati.bin", FileMode.Create)))
        {
            bw.Write(42);
        }

        using (BinaryReader br = new BinaryReader(File.Open("dati.bin", FileMode.Open)))
        {
            int value = br.ReadInt32();
            Console.WriteLine(value);
        }
    }
}
```

Con le classi fornite dal namespace `System.IO` è possibile gestire in modo efficiente le operazioni di input/output su file di testo e binari in un'applicazione C#.