# Markdown Cheatsheet

###### Reference: Wes Bos

## Tekst utheving o.l.

**Utheving/ bold**
Alternativ 1:

```markdown
**Utheving/ bold**
```

Alternativ 2:

```markdown
**Utheving/ bold**
```

_Italic_

Alternativ 1:

```markdown
_Italic_
```

Alternativ 2:

```markdown
_Italic_
```

~~Strikethrough~~

```markdown
~~Strikethrough^^
```

## Titler

# H1 skrives med en

## H2 skrives med 2x

### H3 skrives med 3x

#### H4 skrives med 4x

##### H5 skrives med 5x

###### H6 skrives med 6x

```markdown
# H1 skrives med en

## H2 skrives med 2x

### H3 skrives med 3x

#### H4 skrives med 4x

##### H5 skrives med 5x

###### H6 skrives med 6x
```

etc.

## Links

Alternativ 1:

[Min portfolio](https://rhellenes.me "Dette er linken til min portfolio").

```markdown
[Min portfolio](https://rhellenes.me "Dette er linken til min portfolio")
```

Alternativ 2:
Ved lange linker kan det være lurt å gjøre om linken til en variabel.
Denne variabelen legges på bunnen av siden med denne syntaksen:

Min andre link til [min portfolio][1].

```markdown
Min andre link til [min portfolio][1].

[...]

[1]: https://rhellenes.me
```

[1]: https://rhellenes.me

###### Note: denne metoden gir ikke muligheten til title attribute

## Bilder

Alternativ 1

e.g.
![Bilde fra min portfolio](https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg "Et av bildene i Tælahiv prosjektet mitt")

```markdown
![Bilde fra min portfolio](https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg "Et av bildene i Tælahiv prosjektet mitt")
```

Bilder kan linkes med variabel på samme måte som linker bare med ! først

```markdown
![Bilde fra min portfolio][taelahiv]

[...]

[taelahiv]: https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg
```

### Kontrollere størrelse på bildet:

Du kan kontrollere størrelsen på bildet ved å bruke vanlig HTML kode med inline css:
<img src="https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg" width="500px" height="500px" alt="Et av bildene i Tælahiv prosjektet mitt">

<img class="styleattribute" src="https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg" width="500px" height="500px" alt="Et av bildene i Tælahiv prosjektet mitt">

![Bilde fra min portfolio][taelahiv]

[taelahiv]: https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg
