# Stap 2: Iteraties & Functies

We leren efficiënter om te springen met onze code door stukjes te herhalen of hergebruiken.

## Samenvatting

  - Iteraties
  - Functies

## Voorbereiding

Zie [Stap 1](../stap-01/instructies.md)

## Uitvoering van code herhalen

1. Wat zijn iteraties?

    Sonic Pi is gebaseerd op Ruby en de constructie om de computer te vertellen dat bepaalde code meerdere keren uitgevoerd moet worden is dus als volgt:

    ```ruby
    2.times do
      play 60
      sleep 0.5
    end
    ```

    Dit betekent dat alle code tussen `do` en `end` twee maal uitgevoerd moet worden. Programmeurs noemen dit ook wel iteraties of "loops". Op deze manier kunnen we verder met *Broeder Jakob*!

2. Breid je code uit met de bovenstaande iteratie.

    Nota: je kan hieronder zien dat we sommige lijnen laten inspringen. Dit is om de code leesbaarder te maken. Op die manier is het makkelijker fouten terug te vinden als er iets mis gaat wanneer je op de play knop drukt. Je kan tweemaal op de spatiebalk drukken om een lijn te laten inspringen.

    ```ruby
    2.times do
      play 60
      sleep 0.5
      play 62
      sleep 0.5
      play 64
      sleep 0.5
      play 60
      sleep 0.5
    end
    ```

## Code hergebruiken

1. Wat zijn functies?

    Als we vaker dezelfde stukjes code nodig hebben, kan het handig zijn om de betreffende commando's samen te voegen in een lijstje en dit lijstje een naam te geven. Als we daarna dan die naam gebruiken, begrijpt de computer dat dat lijstje van comando's uitgevoerd moet worden.
    In Sonic Pi gebeurt dat met een `define` statement (van "definitie") en dat ziet er als volgt uit:

    ```ruby
    define :speel_noot do
      play 60
      sleep 0.5
    end
    ```

    Dit maakt dus een functie met de naam "speel_noot" en als we die functie later aanroepen door deze naam te gebruiken, zullen de commando's:
    ```ruby
    play 60
    sleep 0.5
    ```
    uitgevoerd worden.

2. Stop het eerste stukje *Broeder Jakob* in een functie:

    ```ruby
    define :broeder do
      play 60
      sleep 0.5
      play 62
      sleep 0.5
      play 64
      sleep 0.5
      play 60
      sleep 0.5
    end
    ```

    Als je nu op play drukt gebeurt er niets (al wordt de functie wel gemaakt en onthouden, daar merk je niets van omdat ze niet wordt aangeroepen). Door op het einde `broeder` toe te voegen en het geheel af te spelen, maak je de functie en roep je ze ook aan.

3. Maak nu het volledige lied *Broeder Jakob* op basis van de volgende noten:

    C   D   E   C   C   D   E   C

    E   F   G   E   F   G

    G   A   G   F   E   C   G   A   G   F   E   C

    C   G   C   C   G   C

    En de volgende omzettingstabel:

    | C       | D      | E     | F     | G     | A     | B     |
    | :-----: |:------:|:-----:|:-----:|:-----:|:-----:|:-----:|
    | 60      | 62     | 64    | 65    | 67    | 69    | 71    |


5. We kunnen echter nog meer doen met functies! We kunnen het gedrag en/of de uitkomst van een functieaanroep veranderen door functies met parameters te maken waarvan we de waarde kunnen wijzigen. Zo'n parameter kunnen we namelijk in de functie definitie gebruiken en wanneer iemand de functie dan aanroept, krijgt de parameter een waarde mee.

    Voor onze *Broeder Jakob* gaat dat als volgt in zijn werk:
   ```ruby
    define :broeder do |n|
      play n
      sleep 0.5
      play n + 2
      sleep 0.5
      play n + 4
      sleep 0.5
      play n
    end
    ```
    n is hier de parameter en deze nieuwe functie kan aangeroepen worden met bijvoorbeeld het commando:
    ```ruby
    broeder 50
    ```
    of
    ```ruby
    broeder 70
    ```
    In het eerste geval zal dan het muziekje spelen met de noten 50, 52, 54 en 50; in het tweede geval 70, 72, 74 en 70.

6. Pas je functies zo aan dat je *Broeder Jakob* op verschillende toonhoogtes kan spelen

7. Extra: pas je code zo aan dat je *Broeder Jakob* aan verschillende snelheden kan afspelen door één parameter te veranderen.
