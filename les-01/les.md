# Les 1: Starten met Sonic Pi op een Raspberry Pi

Onze eerste stapjes op de Raspberry Pi, een micro computer met grote ambities. In deze les leren we de Raspberry Pi kennen, hoe het computertje op te zetten en de absolute beginselen van het programmeren.

## Samenvatting

  - Voorbereiding
  - Sonic Pi opstarten
  - Het eerste muzikale programma

## Voorbereiding

1. Sluit de volgende onderdelen aan op de Raspberry Pi:
  - toetsenbord
  - muis
  - boxen / hoofdtelefoon
  - (micro)SD geheugenkaart
  - voeding
  - monitor
  - monitor kabel

2. Open Sonic Pi via het menu (Main Menu \ Education \ Sonic Pi)

3. Klik de tab "Workspace 1"

## De eerste code

1. Type:

    ```ruby
    play 60
    ```

2. Klik de _Run_ knop bovenaan het scherm en luister goed...

3. Wat gebeurt er als je de tekst wijzigt naar `pley 60` en op het play icoon klikt?
    Dit is een voorbeeld van een fout (bug) in je code. Later zal je, dankzij de tekst in het error panel, merken dat je een fout hebt gemaakt die je moet corrigeren. Bijvoorbeeld dat je ```play``` fout hebt gespeld.

4. Geef nu het volgende in:

    ```ruby
    play 60
    play 67
    play 69
    ```

5. Klik op het play icoon bovenaan het scherm. Wat gebeurt er?

    De computer voert de commando's na mekaar uit, maar dat gebeurt zo snel dat het voor ons klinkt alsof het spelen van alle noten samen start. Je kan dit ook zien in de logs omdat ze allemaal dezelfde tijd vertonen.

6. We moeten de computer vertellen dat hij even moeten wachten voor hij de volgende noot afspeelt. Dat doen we met het sleep (slaap) commando:

    ```ruby
    sleep 1
    ```

    De waarde achter `sleep` geeft de lengte van de pauze aan. De waarde 1 staat voor 1 seconde. Wat zou je typen voor een halve seconde?

7. Schrijf nu een sequentie van `play` en `sleep` commando's om een cool muziekje te maken!

## Iets complexer: Broeder Jakob

Nu je de basics achter de kiezen heb, tijd voor echte muziek!

De waarden die na `play` komen, stellen noten voor; het zijn zelfs MIDI noot nummers. Dit betekent dat we pianostukjes kunnen vertalen naar onze Raspberry Pi!

We gaan *Broeder Jakob* coderen. Het lied begint als volgt:

`C D E C` of `60 62 64 60` in MIDI noten.

**Tabel van Muzieknoten en overeenkomende MIDI nummers**

| C       | D      | E     | F     | G     | A     | B     |
| :-----: |:------:|:-----:|:-----:|:-----:|:-----:|:-----:|
| 60      | 62     | 64    | 65    | 67    | 69    | 71    |

1. Kies "Workspace 2".

2. Typ de volgende code:

    ```ruby
    play 60
    sleep 0.5
    play 62
    sleep 0.5
    play 64
    sleep 0.5
    play 60
    sleep 0.5
    ```

3. Klik nu op de play knop en luister aandachtig.
