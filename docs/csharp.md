# C# OOP Zusammenfassung

## Grundlagen
#### Variablen Deklaration:

```cs
//Datentyp name = Wert;
int beispielZahl = 5;
```

#### Operatoren
##### Vergleichs-Operatoren 
```cs
5 == 5  //gleich
5 > 5   //größer als
5 < 5   //kleiner als
5 <= 5  //kleiner gleich
5 >= 5  //größer gleich
```

##### Zuweisungs-Operatoren
```cs
int zahl1 = 5;  
  
zahl1 += 10;  
//Oder:  
zahl1 = zahl1 + 10;  
  
zahl1 -= 6;  
//Oder:  
zahl1 -= zahl1 - 6;
```

##### Arithmetische-Operatoren
``` cs
int zahl1 = 5 + 3;  
  
zahl1 = 5 - 3;  
  
zahl1 = 5 * 3;  
  
zahl1 = 5 / 3;  
  
zahl1 = 5 % 3;  //Modulo -> Rest bei Divison
  
zahl1++;  //um 1 inkementieren
  
zahl1--;  //um 1 dekrementieren
```

#### Kontrollstrukturen
##### If-Else

```cs
if(bedingung1 == true)
{
	//Wenn bedingung1 erfüllt ist
}
else if(bedingung2 == true)
{
	//Wenn bedingung2 erfüllt ist
}
else
{
	//Wenn keine bedingung erfüllt ist
}
```

#### Grundstruktur eines C# Programmes
##### Wird automatisch beim erstellen eines Projektes generiert

```cs
namespace ApllicationName  
{  
    internal class Program  
    {  
        public static void Main(string[] args)  
        {  
              
        }  
        //...Weitere Funktionen/Methoden  
    }  
}
```

##### Switch-Case

```cs
string wert = "test2";  
switch (wert)  
{  
    case "test1":  
        // Code für test1  
        break;  
    case "test2":  
        // Code für test2  
        break;  
    default:  
        // Code, wenn kein Fall übereinstimmt        
        break;
}
```

##### Schleifen

```cs
// For-Schleife
for (int i = 0; i < 5; i++)  
{  
    //Wird ? mal ausgeführt
}  

//While-Schleife
while (bedingung == true)  
{  
    //Wird ausgeführt solange bedingung erfüllt ist    //Kopf gesteuert
}  

//Do-While-Schleife
do  
{  
    //Wird ausgeführt solange bedingung erfüllt ist    //Fuß gesteuert
} while (bedingung == true);
```

#### Funktionen und Methoden

Beispiel für eine einfache Statische Funktion die keine Parameter und Rückgabewerte hat, und einen Text in der Konsole ausgibt:

```cs
static void AusgabeBeispielText()  
{  
    Console.WriteLine("Ausgabe Beispiel");  
}
```


Beispiel für eine Statische Funktion die 2 Zahlen als eingabe Parameter nimmt und eine Zahl zurück gibt:

```cs
static int Addiere(int zahl1, int zahl2)  
{  
    int summe = zahl1 + zahl2;  
    return summe;  
}
```

## Objektorientierte Programmierung

Statische Beispiel Klasse mit statischer Funktion:

```cs
static class rechenarten  
{  
    static int addieren(int zahl1, int zahl2)  
    {  
        return zahl1 + zahl2;  
    }  
}
```

#### Mögliche Zugriffsmodifikatoren
- Public (Zugriff von Überall im Code)
- Private (Zugriff nur innerhalb der eigenen Klasse)
- Protected (Zugriff innerhalb der eigenen und Abgeleiteten Klassen)
- Internal (Zugriff nur innerhalb derselben Assembly)


#### Nicht Statische Klasse
- Bauplan für Objekte
```cs
class Person  
{  
    //Felder
    private string name;  
    private int alter;  
    //Konstruktor
    public Person(string _name, int _alter)  
    {  
        this.alter = _alter;  
        this.name = _name;  
    }  
	//Methoden
    public void Vorstellen()  
    {  
        Console.WriteLine(this.name + " ist " + this.alter + " Jahre alt");  
    }  
}
```
Beispiel zeigt eine Personen Klasse in deren Objekte Name und Alter gespeichert werden können, und die Methode Vorstellen() diese Infos ausgibt.

#### Abgeleitete Klasse
Beispiel für eine abgeleitete Klasse von vorherigem Beispiel

```cs
class Mitarbeiter : Person  
{  
    private string beruf;  
    public Mitarbeiter(string _name, int _alter, string _beruf) : base(_name, _alter)  
    {  
        this.beruf = _beruf;  
    }  
  
    public void Arbeiten()  
    {  
        Console.WriteLine("Arbeit als " + this.beruf + " wird ausgeführt");  
  
    }
}
```


#### Polymorphie

