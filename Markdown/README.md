# Markdown Cheatsheet


&nbsp;

## Tekst utheving o.l.

&nbsp;

**Utheving/ bold**

**Alternativ 1:**

```markdown
**Utheving/ bold**
```

&nbsp;

**Alternativ 2:**

```markdown
**Utheving/ bold**
```

&nbsp; &nbsp;

**_Italic_**

**Alternativ 1:**

```markdown
_Italic_
```

&nbsp;

**Alternativ 2:**

```markdown
_Italic_
```

&nbsp; &nbsp;

**~~Strikethrough~~**

```markdown
~~Strikethrough^^
```

&nbsp; &nbsp;

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

&nbsp; &nbsp;

## Links

**Alternativ 1:**

[Min portfolio](https://rhellenes.me "Dette er linken til min portfolio").

```markdown
[Min portfolio](https://rhellenes.me "Dette er linken til min portfolio")
```

&nbsp;

**Alternativ 2:**

Ved lange linker kan det være lurt å gjøre om linken til en variabel. Denne variabelen legges på bunnen av siden med denne syntaksen:

Min andre link til [min portfolio][1].

```markdown
Min andre link til [min portfolio][1].

[...]

[1]: https://rhellenes.me
```

[1]: https://rhellenes.me

###### Note: denne metoden gir ikke muligheten til title attribute

&nbsp; &nbsp;

## Bilder

&nbsp;

**Alternativ 1:**

```markdown
![Bilde fra min portfolio](https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg "Et av bildene i Tælahiv prosjektet mitt")
```

e.g.

![Bilde fra min portfolio](https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg "Et av bildene i Tælahiv prosjektet mitt")

&nbsp;

**Bilder kan linkes med variabel**

```markdown
![Bilde fra min portfolio][taelahiv]

[...]

[taelahiv]: https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg
```

e.g.

![Bilde fra min portfolio][taelahiv]

[taelahiv]: https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg

&nbsp;

**Kontrollere størrelse på bildet:**

Du kan kontrollere størrelsen på bildet ved å bruke vanlig HTML kode med inline css:

```html
<img src="https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg" width="500px" height="500px" alt="Et av bildene i Tælahiv prosjektet mitt">
```

e.g.

<img src="https://rhellenes.me/portfolio/portfolio-images/Taelahiv/bottle-front.jpeg" width="500px" height="500px" alt="Et av bildene i Tælahiv prosjektet mitt">

&nbsp; &nbsp;

## List

#### Unordered list

Bruk enten -, + eller \* foran hver bullet.

- Punkt 1
- Punkt 2
- Punkt 3

```markdown
- Punkt 1
- Punkt 2
- Punkt 3
```

&nbsp;

#### Ordered list

**Alternativ 1**

1. first
2. second
3. third

**Alternativ 2**

1. first
1. second
1. third

&nbsp;

```markdown
Alternativ 1

1. first
2. second
3. third

Alternativ 2

1. first
1. second
1. third
```

&nbsp;
### Nøsting (nested list)
- Punkt 1
  1. One
  2. Two
  3. Three
- Punkt 2

  - Small paragraph

    Dette er en paragraph inni listen

    
- Punkt 3

```markdown
- Punkt 1
  1. One
  2. Two
  3. Three
- Punkt 2

  - Small paragraph

    Dette er en paragraph inni listen

- Punkt 3
```

&nbsp;
&nbsp;

## Line breaks

First sentence</br> with a break


```markdown
First sentence</br> with a break
```
&nbsp;
&nbsp;

## Horizontal rules 

**Alternative 1**

---

**Alternative 2**

===

```markdown
**Alternative 1**

---

**Alternative 2**

===
```



###### Det er viktig at ---/ === ikke er rett under en paragraf for da blir det en tittel. 

&nbsp;
&nbsp;

## BlockQuotes

> "Your work is going to fill a large part of your life, and the only way to be truly satisfied is to do what you believe is great work. And the only way to do great work is to love what you do. If you haven't found it yet, keep looking. Don't settle. As with all matters of the heart, you'll know when you find it."
>
> **-Steve Jobs**


&nbsp;
&nbsp;

## Code blocks

(sammenlign med raw code)

**Større blokker:**

´´´js
const x = 100;
const weather = 'nice';
```


´´´php
$age = 'unknown';
$name = 'René';

echo $name;

```
&nbsp;

**Inline block**

Hey, hva om du prøver `const x = 101;`?

&nbsp;

**Code review**

Vise hva du har endret med diff

```diff

const x = 100;
- const weather = 'nice';
+ const weather = 'bad';

```


&nbsp;
&nbsp;

## Tables / tabeller

Det er litt tungvint å skrive, men det finnes markdown table generatorer. 

&nbsp;

|Name| Age| Gender|
|:---|:---|:------|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|


|Name| Age| Gender|
|---:|---:|------:|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|


|Name| Age| Gender|
|:--:|:--:|:-----:|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|

|Name| Age| Gender|
|:---|:--:|------:|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|

&nbsp;

Legg merke til ` : ` på andre linje

&nbsp;

```markdown


|Name| Age| Gender|
|:---|:---|:------|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|


|Name| Age| Gender|
|---:|---:|------:|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|


|Name| Age| Gender|
|:--:|:--:|:-----:|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|

|Name| Age| Gender|
|:---|:--:|------:|
|Sara|27|Female|
|René|23|Male|
|Robert|32|Male|
|Katie|42|Female|
```

&nbsp;
&nbsp;

## Checkboxes

- [ ] Klipp plenen
- [x] Gå tur
- [ ] Vask opp

```markdown
- [ ] Klipp plenen
- [x] Gå tur
- [ ] Vask opp
```
&nbsp;
&nbsp;

## Accordion

It's possible to hide content in an accorion with the HTML5 tag `<details>  </details>`. The accordion text is defined inside a following `<summary>Accordion-text</summary>`. The structure is as shown here: 

```html
<details>
    <summary>Accordion-text</summary>

    Content goes here

</details>

```
&nbsp;

<details><summary>
Basic Accordion - <b><i>Click me!</i></b>
</summary>


#### There is possible to write normal markdown inside here aswell

```js
console.log('Success!!11')
```


</details>

&nbsp;

The code from the accordion above:
```html
<details>
<summary>Basic Accordion - <b><i>Click me!</i></b> </summary>


#### There is possible to write normal markdown inside here aswell

Hidden text and other stuff

</details>

```

&nbsp;
&nbsp;

## Markdown between or after HTML-tags

To write markdown right after a HTML-tag you have to have a empty line between. This goes for between two tags aswell as after. 

<h4>This doesn't work</h4>
*This doesn't work*

<h4>This does work</h4>

*This does work*


```html

<h4>Text</h4>
*This doesn't work*

<h4>Text</h4>

*This does work*
```
&nbsp;
&nbsp;

## Displaying keyboard keys 

When you'd like to display keyboard keys, say for example to guide the reader on what to press in what sequence, such as <kbd>cmd</kbd> + <kbd>c</kbd>. To access this function use the `<kbd></kbd>`-tag

```md
(...) such as <kbd>cmd<kbd> + <kbd>z<kbd>. 
```