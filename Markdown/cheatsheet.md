# Markdown Cheatsheet

###### Reference: Wes Bos

## Tekst utheving o.l.

**Utheving/ bold** eller **Bold** bruk 2x \* eller \_ for å starte og slutt, e.g. \_\_ / \*\*

_Italic_ eller _Italic v2_ bruk en \* eller \_ for å starte og slutt

~~Strikethrough~~ bruk 2x ~ (hold ALT nede og trykk [*/@])

## Titler

# H1 skrives med en

## H2 skrives med 2x

### H3 skrives med 3x

#### H4 skrives med 4x

##### H5 skrives med 5x

###### H6 skrives med 6x

etc.

## Links

syntax: [Tekst]+(link "title attribute")

[Min portfolio](https://rhellenes.me "Dette er linken til min portfolio").

Ved lange linker kan det være lurt å gjøre om linken til en variabel.
Denne variabelen legges på bunnen av siden med denne syntaksen:

Min andre link til [min portfolio][1].

[identifikator e.g. 1]+:+ Link

[1]: https://rhellenes.me

###### Note: denne metoden gir ikke muligheten til title attribute

## Bilder

syntax !+[Alternativ tekst]+(link "title attribute")

e.g.
![Bilde fra min portfolio](https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg "Et av bildene i Tælahiv prosjektet mitt")

Bilder kan linkes med variabel på samme måte som linker bare med ! først

### Kontrollere størrelse på bildet:

Du kan kontrollere størrelsen på bildet ved å bruke vanlig HTML kode med inline css:
<img src="https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg" width="500px" height="500px" alt="Et av bildene i Tælahiv prosjektet mitt">

<img class="styleattribute" src="https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg" width="500px" height="500px" alt="Et av bildene i Tælahiv prosjektet mitt">

<style>
  img{
    width: 200px;
    height:200px;
  }
  </style>
