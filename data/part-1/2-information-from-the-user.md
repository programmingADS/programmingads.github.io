---
path: '/part-1/2-information-from-the-user'
title: 'Informatie van de gebruiker'
hidden: false
---

<text-box variant='learningObjectives' name='Leerdoelen'>

Na deze sectie:

- Weet je hoe je een programma schrijft dat gebruikmaakt van invoer van de gebruiker.
- Weet je hoe je variabelen kunt gebruiken om invoer op te slaan en weer af te drukken.
- Kun je strings combineren.

</text-box>

_Input_ verwijst naar alle informatie die een gebruiker aan het programma geeft. Specifiek leest het Python-commando `input` een regel met invoer die door de gebruiker is getypt. Het kan ook worden gebruikt om een bericht aan de gebruiker weer te geven en specifieke invoer op te vragen.

Het volgende programma leest de naam van de gebruiker in met behulp van het `input`-commando en drukt het vervolgens af met het `print`-commando:

```python
name = input("Wat is je naam? ")
print("Hallo, ")
print(name)
```

De uitvoering van dit programma kan er als volgt uitzien (invoer van de gebruiker in het rood):

<sample-output>

Wat is je naam? **Paul Python**
Hallo,
Paul Python

</sample-output>

<sample-output>

Wat is je naam? **Paula Programmeur**
Hallo,
Paula Programmeur

</sample-output>

Het woord 'name' in dit programma is een _variabele_. In de context van programmeren is een variabele een locatie om een bepaalde _waarde_ op te slaan, zoals een string of een getal. Deze waarde kan later worden gebruikt en kan ook worden gewijzigd.

<text-box variant="hint" name="Variabelen benoemen">

In principe kunnen variabelen vrij worden benoemd, binnen bepaalde limieten die zijn gespecificeerd in de Python-taal.

Het is gebruikelijk om variabelen in het Engels te benoemen. De naam van de variabele heeft geen directe invloed op de inhoud ervan, dus de naam doet er in die zin niet toe. Het kan echter vaak handig zijn om te begrijpen hoe code werkt als variabelen logisch en in het Engels worden benoemd.

</text-box>

<in-browser-programming-exercise name="Tweemaal de naam" tmcname="part01-06_name_twice">

Schrijf een programma dat de naam van de gebruiker vraagt en deze vervolgens tweemaal, op twee opeenvolgende regels, afdrukt.

Een voorbeeld van hoe het programma zou moeten werken:

<sample-output>

Wat is je naam? **Paul**
Paul
Paul

</sample-output>

</in-browser-programming-exercise>

## Meer dan één invoer

Een programma kan om meer dan één invoer vragen. Let op hoe elk `input`-commando de ontvangen waarde opslaat in een andere variabele.

```python
name = input("Wat is je naam? ")
email = input("Wat is je e-mailadres? ")
nickname = input("Wat is je bijnaam? ")

print("Laten we zeker weten dat we het goed hebben")
print("Je naam: ")
print(name)
print("Je e-mailadres: ")
print(email)
print("Je bijnaam: ")
print(nickname)
```

Het programma kan bijvoorbeeld het volgende afdrukken:

<sample-output>

Wat is je naam? **Raghad Fictitious**
Wat is je e-mailadres? **raghad99@example.com**
Wat is je bijnaam? **Raggy**
Laten we zeker weten dat we het goed hebben
Je naam:
Raghad Fictitious
Je e-mailadres:
raghad99@example.com
Je bijnaam:
Raggy

</sample-output>

Als dezelfde variabele wordt gebruikt om meerdere invoeren op te slaan, wordt elke nieuwe waarde de vorige waarde vervangen. Bijvoorbeeld:

```python
adres = input("Wat is je adres? ")
print("Dus je woont op adres:")
print(adres)

adres = input("Typ alstublieft een nieuw adres in: ")
print("Je adres is nu:")
print(adres)
```

Een voorbeelduitvoering van het programma:

<sample-output>

Wat is je adres? **Pythonpad 101, Flat 3D**
Dus je woont op adres:
Pythonpad 101, Flat 3D
Typ alstublieft een nieuw adres in: **Nieuwe Weg 999**
Je adres is nu:
Nieuwe Weg 999

</sample-output>

Dit betekent dat als dezelfde variabele wordt gebruikt om twee opeenvolgende invoeren op te slaan, er geen manier is om de eerste invoerwaarde te benaderen nadat deze is vervangen door de tweede:

```python
adres = input("Wat is je adres? ")
adres = input("Typ alstublieft een nieuw adres in: ")

print("Je adres is nu:")
print(adres)
```

Een voorbeeld van hoe de uitvoer van het programma eruit zou kunnen zien:

<sample-output>

Wat is je adres? **Pythonpad 10**
Typ alstublieft een nieuw adres in: **Programmeurslaan 23**
Je adres is nu:
Programmeurslaan 23

</sample-output>

## Afdrukken met f-strings

Wat als we meer flexibiliteit en controle willen over wat we afdrukken? Zogenaamde _f-strings_ zijn een andere manier om tekst op te maken in Python. De manier van schrijven kan in het begin wat verwarrend lijken, maar uiteindelijk zijn f-strings vaak de eenvoudigste manier om tekst op te maken.

Met f-strings zou het vorige voorbeeld er als volgt uitzien:

```python
resultaat = 10 * 25
print(f"De uitkomst is {resultaat}")
```

Laten we dit uit elkaar halen. Aan het begin van de string die we willen afdrukken staat het karakter _f_. Dit vertelt Python dat wat volgt een f-string is. Binnen de string, omringd door accolades, staat de variabelenaam `resultaat`. De waarde die het bevat, wordt een deel van de afgedrukte string. De uitvoer is precies hetzelfde als in de vorige voorbeelden:

<sample-output>

De uitkomst is 250

</sample-output>

Eén enkele f-string kan meerdere variabelen bevatten. Bijvoorbeeld, deze code

```python
naam = "Mark"
leeftijd = 37
woonplaats = "Palo Alto"
print(f"Hallo {naam}, je bent {leeftijd} jaar oud. Je woont in {woonplaats}.")
```

drukt het volgende af:

<sample-output>

Hallo Mark, je bent 37 jaar oud. Je woont in Palo Alto.

</sample-output>

<in-browser-programming-exercise name="Naam en adres" tmcname="part01-08_name_and_address">

Schrijf een programma dat de naam en het adres van de gebruiker vraagt. Het programma moet ook de gegeven informatie afdrukken door print f-strings, als volgt:

<sample-output>

Voornaam: **Aisha**
Achternaam: **Aydın**
Straatadres: **Hommelstraat 7b**
Stad en postcode: **Rotterdam 3061VA**
Aisha Aydın
Hommelstraat 7b
Londen EC05 6AW

</sample-output>

</in-browser-programming-exercise>


<in-browser-programming-exercise name="Verhaal" tmcname="part01-10_story">

Schrijf een programma dat het volgende verhaal afdrukt. De gebruiker geeft een naam en een jaar, die in de tekst moeten worden ingevoegd.

<sample-output>

Typ een naam in: **Mary**
Typ een jaar in: **1572**

Mary is a valiant knight, born in the year 1572. One morning Mary woke up to an awful racket: a dragon was approaching the village. Only Mary could save the village's residents.

</sample-output>


Het verhaal moet veranderen op basis van de invoer die door de gebruiker wordt gegeven.

</in-browser-programming-exercise>
