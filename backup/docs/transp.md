#Transponieren
---
Die Anwendungsroutine «Transponieren» ermöglicht es, die Struktur eines Datensatzes zu ändern. Der Datensatz kann entweder vertikal oder horizontal strukturiert sein.  

Beispiel: Ein Datensatz enthält für jede Person drei numerische Variablen - das Alter, die Grösse und das Gewicht.

* In der <em>vertikalen</em> Form sind die Werte für Alter, Grösse und Gewicht alle untereinander, also in einer Variable, erfasst. Für jede Person im Datensatz sind also drei Beobachtungen vorhanden.  
![](img/Transp_1.png)
* In der <em>horizontalen</em> Form sind die Werte auf drei verschiedene Variablen aufgeteilt, folglich existiert nur eine Beobachtung pro Person.   
![](img/Transp_2.png)
##Horizontalisierung  
Liegen die Daten in der vertikalen Form vor, werden aber für die Weiterverarbeitung in der horizontalen Form gebraucht, so kann das mittels «Transponieren» erreicht werden.  
![](img/Transp_1.png)  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;<span style="font-size:1.5em;">**&darr;**</span>  
![](img/Transp_3.png)

####Lösungsweg SAS Enterprise Guide  

<em>Schritt 1</em>: Anwendungsroutine «Transponieren» auswählen. Wo diese im neuen SAS Enterprise Guide zu finden ist, kann <a href="neweg.html">hier</a> nachgelesen werden. 
![](img/Transp_4.png)  

<em>Schritt 2</em>: Die Variablen den richtigen Rollen zuordnen:

*  `Variable transponieren`: Hier muss die Analysevariable ausgewählt werden, deren Werte auf verschiedene Spalten aufgeteilt werden sollen. In diesem Beispiel also _Wert_.  
*  `Neue Spaltennamen (Maximal: 1)`: Hier wird die Variable ausgewählt, deren Ausprägungen die neuen Variablen bilden bzw. benennen sollen. In diesem Beispiel also _Merkmal_.  
*  `Analyse gruppieren nach`: In diesem Beispiel die Variablen _Name_ und _Geschlecht_. Hier können auch noch mehr Variablen gewählt werden, z.B. wenn der Wert nicht nur nach Name und Geschlecht, sondern z.B. auch noch nach Nationalität ausgewiesen wird.  

![](img/Transp_5.png)  
<em>Schritt 3</em>: Das Häkchen bei «Präfix verwenden» rausnehmen, damit die neuen Spaltennamen nicht mit dem Wort «Spalte» (Default) ergänzt werden.  
![](img/Transp_6.png)  

## Vertikalisierung  
Liegen die Daten in der horizontalen Form vor, werden aber für die Weiterverarbeitung in der vertikalen Form gebraucht, so kann das ebenfalls mittels «Transponieren» erreicht werden.  
![](img/Transp_2.png)  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;<span style="font-size:1.5em;">**&darr;**</span>  
![](img/Transp_1_1.png)  

####Lösungsweg SAS Enterprise Guide  

<em>Schritt 1</em>: Anwendungsroutine «Transponieren» auswählen.
![](img/Transp_4.png)  

<em>Schritt 2</em>: Die Variablen den richtigen Rollen zuordnen:  

* `Variable transponieren`: Hier müssen die Analysevariablen ausgewählt werden, deren Werte in einer Spalte zusammengefasst werden sollen. In diesem Beispiel also _Alter_, _Grösse_ und _Gewicht_.  
* `Analyse gruppieren nach`: In diesem Beispiel die Variablen _Name_ und _Geschlecht_. Hier können auch noch mehr Variablen gewählt werden, z.B. wenn der Wert nicht nur nach Name und Geschlecht, sondern z.B. auch noch nach Nationalität ausgewiesen würde.  
![](img/Transp_8.png)  
<em>Schritt 3</em>: Namen für Quellspalte setzen, in diesem Fall soll sie _Merkmal_ heissen.
![](img/Transp_9.png)  