# ChemCSS
Acest proiect reprezinta o librarie CSS pentru a creea structuri chimice (substante) si ecuatii folosind doar HTML.
###Documentatia nu suporta diacritice!!!

![Exmplu de compus](/compus_organic_2.png)

###Cuprinsul documentatiei:

1) Cum il pornim? <br>
2) Adaugarea de noi elemente <br>
3) Adaugarea legaturilor intr-o substanta <br>
4) Tipuri de legaturi <br>

##Cum il pornim?
Pentru a folosi tabla (este un concept prin care ii spunem unde sa plaseze acele legaturi), mai intai declaram ca vom efectua e ecuatie (care poate contine 1, 2 sau chiar mai multe substante) folosind ```chembox```.

```HTML
<div chembox>

</div>
```

##Adaugarea de noi elemente
In interiorul tablei (chembox), vom declara elemente folosind atributul ```chempart```. De asemenea, trebuie adaugata si locatia unde va fi plasata substanta pe tabla, folosind atributul ```boxX_Y```, unde X_Y (X, Y reprezinta pozitia pe abscisa, respectiv ordonata). Fiecare dintre cele doua valori pot lua valori astfel: X: 1 - 10 si Y: 1 - 20.
Exista mai mult de atat, a fost introdus atributul ```zoom``` pentru a face redimensionarea mai usoara.

```HTML
<div chembox>
	<div chempart box2_2>0</div>
</div>
```

##Adaugarea legaturilor intr-o substanta
Adaugarea legaturilor se va face utilizand tag-ul ```<hr>``` ca o metoda de delimitare a legaturilor. Exemplu de utilizare:
```HTML
<div chembox>
	<div chempart box2_2>
		<hr singlebond> <!-- Legatura din dreapta-sus -->
		<hr> <!-- Legatura nula -->
		<hr> <!-- Legatura nula -->
		<hr singlebond> <!-- Legatura din partea de jos-->
	</div>
</div>
```
!!!Ordinea in care sunt asezate tag-urile de tip ```<hr>``` conteaza, asadar exemplul acesta:
```HTML
<div chembox>
    <div chempart box2_2>O</div>
        <hr singlebond>
        <hr>
        <hr>
        <hr partialdoublebond>
    <div chempart box3_1>C</div>
        <hr>
        <hr>
        <hr doublebond>
    <div chempart box4_2>C</div>
        <hr singlebond>
        <hr>
        <hr>
        <hr singlebond>
    <div chempart box4_3>C</div>
    <div chempart box3_4>C</div>
        <hr triplebond>
    <div chempart box2_3>N</div>
        <hr>
        <hr>
        <hr singlebond>
</div>
```
Va genera urmatoarea imagine:
![Exemplu de compus](/compus_organic_1.png)

##Tipuri de legaturi
Sunt deja facute cateva tipuri de legaturi comune. Aceasta este lista lor: <br>
```singlebond```, ```doublebond```, ```triplebond```, ```partialdoublebond```, 
```partialsinglebond```, ```partialtriplebond```.

###Autor (Enciu Bianca-Elena, CNVA Galati): In acest proiect nu au fost utilizate alte surse / fragmente din alte surse, tot proiectul a fost integral facut de la 0, de catre mine.  
