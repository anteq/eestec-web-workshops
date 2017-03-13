# Frontend
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg" -->

Remember the building blocks?

1. A computer with Internet connection.
2. Place to store some stuff. 
3. Process listening and responding to requests.  
4. Template for the content. 
5. Styles for the page to look nice.  
6. Client-side scripts allowing interaction.

1. 
2. 
3. 
4. Template for the content. 
5. Styles for the page to look nice.  
6. Client-side scripts allowing interaction.

1. 
2. 
3. 
4. HTML
5. CSS  
6. JS

![http://scontent.cdninstagram.com/t51.2885-15/e35/12383373_840841069358317_1096055011_n.jpg?ig_cache_key=MTIyNDYzMTMyNzczNjI3NTEwMg%3D%3D.2](http://scontent.cdninstagram.com/t51.2885-15/e35/12383373_840841069358317_1096055011_n.jpg?ig_cache_key=MTIyNDYzMTMyNzczNjI3NTEwMg%3D%3D.2)

---

#### Frontend
# Design

## Antiquity
- 90s
- low internet speed as a constraint
- text based (no funny kittens pictures)

## Middle ages 
- GIF fever 
- table-based layouts
- page hit counters
- animated text

## Renaissance
- Flash
- marriage of virtual graphics and interaction
- enhanced visual effect from previous period
- the beginning of visitor-focused design
- structure and navigation became important considerations
Note:
dodać filmik z yt albo gif z flashem (queen)

## The Enlightenment
- separation of content and design (css)
- websites easier to maintain, more flexible and quicker to load 
- links began to attach to icons rather than text 
- usability started to become more important than other design elements

## The Industrial Revolution
- WEB2.0
- growth of multimedia applications
- implementation of interactive content
- rise of the social web
- better color distribution, increased use of icons, and greater attention to typography
- design became about content

## Modern Days
- well... you can see for yourself 
- UX
- infinite scrolling 
- SPA

---

#### Frontend
# HTML

The content. <br />
Definitely **not** a programming language.

![https://cdn.meme.am/cache/instances/folder948/62774948.jpg](https://cdn.meme.am/cache/instances/folder948/62774948.jpg)

Just a way of organizing content. Srsly.

```
<!DOCTYPE html>
<html>
    <body>
        <h1> Welcome to my homepage </h1>
        <p> I Am Lord Voldemort <p>
    </body>
</html>
```

---

#### Frontend
# CSS

CSS = Cascading Style Sheets <br />
Also, definitely **not** a programming language.

```
h1 {
    color: red;
}
```

### #id, .class
```
<!DOCTYPE html>
<html>
    <body>
        <h1 id="title"> Welcome to my homepage </h1>
        <p class="paragraph"> I Am Lord Voldemort <p>
        <p class="paragraph"> formerly known as Tom Marvolo Riddle <p>
    </body>
</html>
```

```
#title {
    color: red;
}
.paragraph {
    text-decoration: underline;
}
```

If you're not an expert...
![http://i.imgur.com/Q3cUg29.gif](http://i.imgur.com/Q3cUg29.gif)

### CSS3
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/38/58/a8/3858a82d3a7a6e26ca4edf9a5d1ec883.jpg" -->

E.g. [here](https://pattle.github.io/simpsons-in-css/). Or [here](http://www.csstardis.co.uk/);

### Nerd humor sample #2
[https://speckyboy.com/css-puns-jokes/](https://speckyboy.com/css-puns-jokes/)

## Grid system

We have frameworks :)

<!-- .slide: data-background-image="https://v4-alpha.getbootstrap.com/examples/screenshots/justified-nav.jpg" -->
### Bootstrap

<!-- .slide: data-background-image="https://media.licdn.com/mpr/mpr/AAEAAQAAAAAAAAPdAAAAJDRkNDhiM2FlLWRmY2ItNGZjOS05YTY0LTc4Y2U5ZmNmNmUzZQ.jpg" -->
### Materialize

Foundation, Pure, Semantic...

---

#### Frontend
# Javascript

### Why there's only one language?
<!-- .slide: data-background-image="http://mrwgifs.com/wp-content/uploads/2013/08/But-Im-The-Chosen-One-Harry-Potter-GIf.gif" -->

JavaScript works in a browser.

<!-- .slide: data-background-image="https://media.giphy.com/media/yjI5G3pE3NH3O/giphy.gif" -->
## Created in 10 days. Seriously. May 1995.

<!-- .slide: data-background-image="https://admin.mashable.com/wp-content/gallery/productivity-gifs/community-idea.gif" -->

<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/b2/56/8e/b2568e20328938e4286ee907762bf4e4.gif" -->
### People say that it's poorly designed, but...
Note:
0.1 + 0.2, try it.
Netscape Communications realized that the Web needed to become more dynamic. Marc Andreessen, the founder of the company believed that HTML needed a "glue language" that was easy to use by Web designers and part-time programmers to assemble components such as images and plugins, where the code could be written directly in the Web page markup. In 1995, the company recruited Brendan Eich with the goal of embedding the Scheme programming language into its Netscape Navigator. Before he could get started, Netscape Communications collaborated with Sun Microsystems to include in Netscape Navigator Sun's more static programming language Java, in order to compete with Microsoft for user adoption of Web technologies and platforms.[11] Netscape Communications then decided that the scripting language they wanted to create would complement Java and should have a similar syntax, which excluded adopting other languages such as Perl, Python, TCL, or Scheme. To defend the idea of JavaScript against competing proposals, the company needed a prototype. Eich wrote one in 10 days, in May 1995.
Microsoft script technologies including VBScript and JScript were released in 1996. JScript, a reverse-engineered implementation of Netscape's JavaScript, was part of Internet Explorer 3.

> JS had to "look like Java" only less so, be Java's dumb kid brother or boy-hostage sidekick. Plus, I had to be done in ten days or something worse than JS would have happened. <br />
~ Brendan Eich

#### The language that has been designed for simple animations now is the most used language in the world.

<!-- .slide: data-background-image="http://i.imgur.com/JlaTqEa.gif" -->

Actually... Javascript = ECMAScript.

<!-- .slide: data-background-image="http://i3.kym-cdn.com/photos/images/original/000/692/708/c09.gif" -->
# JAVASCRIPT != JAVA

- functional
- interpreted 
- classless

### Nerd humor sample
[https://www.destroyallsoftware.com/talks/wat](https://www.destroyallsoftware.com/talks/wat)

![https://c1.staticflickr.com/5/4066/4704268314_bb0e9d0ff3_b.jpg](https://c1.staticflickr.com/5/4066/4704268314_bb0e9d0ff3_b.jpg)

## jQuery
- very popular JS library
- widely supportted by community
- but if you are language purist... you will use it anyway
Note:
- Jquery - najpopularniejsza biblioteka JS - po to, żeby ułatwić życie developerowi
PRZYKŁAD
- czyli sprawdzanie z jakiej przeglądarki korzystamy
- dzisiaj juz nie ma takich różnic - największe róznice w css ale wciąż Jquery jest bardzo popularne bo ma wiele pluginów (gotowców) z których łatwo można korzystać
- Antek jest purystą jezykowym dlatego jesli nie musi korzystac z Jquery to tego nie robi

---

#### Frontend
# DOM

# DOM
## House on a tree
Note:
- drzewo DOM - html to drzewo, style zczytywane do odpowiednich miejsc w drzewach, JS może operowac na tym wszystkim w jaki sposób jej się podoba
- narysować

## History digression 
- At the beginning there was no DOM standard so Netscape and Microsoft made their own incompatible implementations
- Finally W3C saved the day
- DOM levels

---

#### Frontend 
# Issues

<!-- .slide: data-background-image="https://media.tenor.co/images/88ea617faa7436f1cbee99d6aac57151/raw" -->
## Chrome, Firefox, Safari, Internet Explorer...
Note:
dodać zdjęcie
dla web developera dużym problem jest różnorodność przeglądarkowa - niektóre rzeczy się inaczej renderują w róznych przeglądarkach (PRZYKŁAD!!)

## Everybody hates IE6
Note:
śmieszne zdjęcie
- IE6 - największy koszmar programisty - brak wsparcia dla nowych funkcjonalności, wszystkie starsze przeglądarki zostały wycofane z użytku
warto podać przykłady !!!!!!!!!!!!!!!

---

### Frontend
# Modern JS

## WebGL because we CAN!
### JS extension
### 3D graphics
- webGL
Note:
gra w 3D
http://www.webglgames.com/cube-slam/

## ES6
todo

# Typing
Javascript is not typed. Hot or not?

## Going deeper in JS
- it's evolving so there are some functionalities not supported by all browsers
- trans(com)pilation
- minification
Note:
- w nowych wersjach JS są funkcjonalnosci które jeszcze nie są wspierane przez wszystkie przeglądarki
- transpilacja - przetworzenie kodu w taki sposób, że nowa składania zostaje zamieniona w starą żeby nie powodować problemów

---

### Frontend
# Frameworks

Not many people are writing in plain ("vanilla") JS. We have *frameworks*.

- Don't Reinvent The Wheel
- Do More With Less Code
- Save Time -- You Don't Code Your Own OS, Do You?
- Chances Are, You Aren't The Expert
- Speed Thrills
- Avoid Cryptic JavaScript Base Code - Abstract It

However - **you should learn Vanilla JS whenever possible**.

# Angular

- MVVM
- by Google
- blah blah

# React

- Reactive
- by Facebook
- blah blah

---

### Frontend
# PHP

## Who doesn't love PHP?
- PHP is designed to be an HTML templating language (and maybe should have stayed that way)
- “You can write great code in any language.” Yeah, and Leonardo could’ve produced great art with human shit, if he cared to, but he knew better.
- it is relatively easy to deploy easy website
- nowadays so many alternatives 
Note:
do poprawki
- Dawniej moda na php - przyklad jak dziala php i to jak jest dzisiaj
- bardzo wazny jest jasny i prosty przyklad

--- 

### Why not to make a computer with just browser capabilities?
![md/3-history/chromebook.jpg](md/3-history/chromebook.jpg)
### Quick test:
### In your everyday life when last time you didn't have a browser opened in background?
Note:
- coraz mnie potrzeba instalować programów a coraz wiecej dostępne jest w przeglądarce

## HOT 2017 TOPIC
### Progressive web Applications
Note:
Jakiś przykład
- hot temat 2017 roku - progressive web application - głównie na mobilkach - czyli wchodzac przez przeglądarke pokaże się dokładnie ta sama aplikacja co zainstalowana przez app store
