Benutzerdefinierte Formate
==============================

* * *

SAS bietet die Möglichkeit, eigene Formate zu schreiben. Das wird mittels PROC FORMAT-Statement in folgender Form gemacht:  

> proc format;  
> value < Formatname >  
>    \[...hier wird das Format definiert...\];  
> run;


Anwendungsbeispiel:

`proc format;
value fmt_alter
	0-19 = "bis 20 Jahre"  
	20-60 = "20 bis 60 Jahre"  
	61-high = "über 60 Jahre";
run;`

Sortieren mittels Format
-------------------

`proc format;
value fmt_alter (notsorted)
	61-high = "über 60 Jahre"
	20-60 = "20 bis 60 Jahre" 
	0-19 = "bis 20 Jahre";
run;`





Mulitlabel
-------------------

`proc format;
value fmt_alter (multilabel)
	0-19 = "bis 20 Jahre"  
	20-60 = "20 bis 60 Jahre"  
	61-high = "über 60 Jahre"
	0-60 = "Total 0 bis 60 Jahre";  ;
run;`




* * *