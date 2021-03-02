# CSS to the Rescue @cmda-minor-web 2020 - 2021

Voor de eindopdracht van CSS-To-The-Rescue zal ik een samen met mijn medestudenten een CSS Zen Garden maken. Dit was een initiatief om de mogelijkheden van CSS te exploreren door iedere developer de zelfde HTML te geven, maar de css is telkens uniek. Dit ga ik tijdens CSS TTR ook doen.

## live link
[https://max-hauser.github.io/css-to-the-rescue-2021/](https://max-hauser.github.io/css-to-the-rescue-2021/)

## poster

![poster](https://github.com/max-hauser/css-to-the-rescue-2021/blob/master/images/poster.png)

## Week 1: Het plan

#### In het kort:
- Ik heb gekozen voor het maken van een **menu**
- Als context heb ik **print-stylesheet** gekozen
- Ik heb twee eisen:
- - Ik ben lid geworden van **de one-div movement**
- - Responsive **zonder** media queries
- **Geen** id's of classes/ **javascript** gebruiken

#### CSS technieken

Ik zal veel gebruik gaan maken van animaties, transities en filters.

#### Inspiratie

[moodboard](https://www.pinterest.co.uk/maxhauser1997/css-tts/)

# oud plan:

![oudplan](https://github.com/max-hauser/css-to-the-rescue-2021/blob/master/images/idee1.png)

Nadat ik klaar was met webapp from scratch kon ik me volledig focussen op css to the rescue. Eerder had ik een plan en een schets (zie afbeelding hierboven) gemaakt, maar nadat ik er weer terug op kwam voelde ik er niet veel meer voor.

## Nieuw plan!
Van de gastcollges die ik gezien heb, was ik vooral onder de indruk van https://a.singlediv.com/. Hierom besloot ik om te proberen om van het menu een realistische bon te maken. Dit leidde vanzelf tot het toevoegen van een apparaat en een omgeving waarin het apparaat zich bevond.

## Wat heb ik geleerd

Ik heb iets totaal nieuws geleerd: background: linear-gradient(...), linear-gradient(...), ....
Dit was voor mij echt een openbaring! Opeens kon ik met 1 enkel element oneindig veel visuele elementen toevoegen zonder html nodig te hebben. 

Voor dit project heb ik alleen aantal radio-buttons toegevoegd voor het scherm. Maar verder is alles toegevoegd met background linear-gradient! 
Als extra heb ik ook gespeeld met lichtval en skew(). Dit geeft het een 3d gevoel. Vooral door het licht en de schadow toevoegingen.

## Uitgelichte feature

Wat mijn project speciaal maakt is dat het bon-apparaat interactief is. Dit heb ik gedaan door gebruik te maken van de "checkbox hack", of in mijn geval de "radio button hack".

```css
input[type="radio"]:nth-child(13):checked ~ section:nth-child(21) {
  animation: slideDown 0.5s ease-in-out forwards;
}
```  

Hierbij verberg je de daadwerkelijke radio buttons, maar link je de labels waar je vervolgens op kunt klikken. Dit stelt je instaat om een element aan te spreken als er geklikt is om zo'een radio button. Waar je wel rekening mee moet houden is dat de radiobutton en het te selecteren element de zelfde parent element moeten hebben. Dit zorgde voor een extra uitdaging omdat ik alles nu in de main moest doen.

## Wat heeft mij het meest uitgedaagd?

Wat mij het meeste heeft uitgedaagd was het juist animeren van het bonnetje dat uit het apparaat moest komen. met height 0 => height auto, werkte niet. Dus na lang googlen kwam ik op -webkit-mask-image. Met deze methode kon ik een deel van het bonnetje transparant maken, echter dit animeerde niet mooi uit zichzelf. Uiteindelijk heb ik het via heel keyframes een soort van kunnen oplossen:


![keyframes](https://github.com/max-hauser/css-to-the-rescue-2021/blob/master/images/keyframes.png)


