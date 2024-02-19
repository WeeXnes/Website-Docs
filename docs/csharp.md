# C# OOP Zusammenfassung

### Grundlagen
Variablen Deklaration:

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
        // Code, wenn kein Fall übereinstimmt        break;}
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
    //Wird ausgeführt solange bedingung erfüllt ist    //Kopf gesteuert}  

//Do-While-Schleife
do  
{  
    //Wird ausgeführt solange bedingung erfüllt ist    //Fuß gesteuert
} while (bedingung == true);
```


