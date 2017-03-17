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

<!-- .slide: data-background-image="https://i.kinja-img.com/gawker-media/image/upload/s--iKy29BwN--/18s14vugshn3sjpg.jpg" -->

## Middle ages 
- GIF fever 
- table-based layouts
- page hit counters
- animated text

<!-- .slide: data-background-image="https://s3.amazonaws.com/media-p.slid.es/uploads/marcosplacona/images/545172/lings_cars.gif" -->

## Renaissance
- Flash
- marriage of virtual graphics and interaction
- enhanced visual effect from previous period
- the beginning of visitor-focused design
- structure and navigation became important considerations
Note:
dodać filmik z yt albo gif z flashem (queen)

<!-- .slide: data-background-image="http://www.zanetinewebdesign.com/wp-content/uploads/2009/08/pic2-1023x706.jpg" -->

## The Enlightenment
- separation of content and design (css)
- websites easier to maintain, more flexible and quicker to load 
- links began to attach to icons rather than text 
- usability started to become more important than other design elements

<!-- .slide: data-background-image="http://www.objectivistliving.com/forums/olimages/NB-Facebook-July28-2009.jpg" -->

## The Industrial Revolution
- WEB2.0
- growth of multimedia applications
- implementation of interactive content
- rise of the social web
- better color distribution, increased use of icons, and greater attention to typography
- design became about content

![https://v4-alpha.getbootstrap.com/examples/screenshots/jumbotron.jpg](https://v4-alpha.getbootstrap.com/examples/screenshots/jumbotron.jpg)

## Modern Days
- well... you can see for yourself 
- UX
- infinite scrolling 
- SPA

<!-- .slide: data-background-image="https://colorlib.com/wp/wp-content/uploads/sites/2/simplicity-flat-wordpress-template.jpg" -->

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

Y'all can trigger JS console in your browser using F12.

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
- czyli sprawdzanie z jakiej przeglądarki korzystamy
- dzisiaj juz nie ma takich różnic - największe róznice w css ale wciąż Jquery jest bardzo popularne bo ma wiele pluginów (gotowców) z których łatwo można korzystać
- Antek jest purystą jezykowym dlatego jesli nie musi korzystac z Jquery to tego nie robi

---

#### Frontend
# DOM

DOM = Document Object Model

![http://www.openbookproject.net/tutorials/getdown/css/images/lesson4/HTMLDOMTree.png](http://www.openbookproject.net/tutorials/getdown/css/images/lesson4/HTMLDOMTree.png)

## History digression 
- At the beginning there was no DOM standard so Netscape and Microsoft made their own incompatible implementations
- Finally W3C saved the day
- DOM levels

---

#### Frontend 
# Browsers

<!-- .slide: data-background-image="https://media.tenor.co/images/88ea617faa7436f1cbee99d6aac57151/raw" -->
## Chrome, Firefox, Safari, Internet Explorer...
Note:
dodać zdjęcie
dla web developera dużym problem jest różnorodność przeglądarkowa - niektóre rzeczy się inaczej renderują w róznych przeglądarkach (PRZYKŁAD!!)

![https://www.smashingmagazine.com/wp-content/uploads/2010/06/forms-browsers.jpg](https://www.smashingmagazine.com/wp-content/uploads/2010/06/forms-browsers.jpg)

[Stats](http://gs.statcounter.com/)

```
element {
    -moz-border-radius: 2em;
    -ms-border-radius: 2em;
    -o-border-radius: 2em;
    -webkit-border-radius: 2em;
}
```

```
element {
    border-radius: 2em;
}
```

## Everybody hates IE6
Note:
śmieszne zdjęcie
- IE6 - największy koszmar programisty - brak wsparcia dla nowych funkcjonalności, wszystkie starsze przeglądarki zostały wycofane z użytku
warto podać przykłady !!!!!!!!!!!!!!!

![http://static2.hypable.com/wp-content/uploads/2015/03/IE11.jpg](http://static2.hypable.com/wp-content/uploads/2015/03/IE11.jpg)

![http://img.memecdn.com/Internet-explorer_o_110439.jpg](http://img.memecdn.com/Internet-explorer_o_110439.jpg)

![http://i.imgur.com/1VIbP.png](http://i.imgur.com/1VIbP.png)

### caniuse.com
![https://meta-s3-cdn.global.ssl.fastly.net/original/3X/0/a/0a0fcf288da6a9512311680fa6b1e85000b165a6.png](https://meta-s3-cdn.global.ssl.fastly.net/original/3X/0/a/0a0fcf288da6a9512311680fa6b1e85000b165a6.png)


---

### Frontend
# Modern JS

You remember API?

**Not only on backend!**

In API-based solutions: view is the API format.
Note:
Backend: M->C->V -----> M->C->V 

## WebGL because we CAN!
- JS extension
- 3D graphics
- ![click blik lol](http://www.webglgames.com/cube-slam/)
Note:
gra w 3D

### Minification & uglification

<!-- .slide: data-background="white" -->
![http://blog.jamesdbloom.com/images_2013_11_17_17_56/minification.png](http://blog.jamesdbloom.com/images_2013_11_17_17_56/minification.png)

# ES6

<!-- .slide: data-background="white" -->
![https://derickbailey.com/wp-content/uploads/2015/08/arrow-functions.jpg](https://derickbailey.com/wp-content/uploads/2015/08/arrow-functions.jpg)

# Typing
Javascript is not typed. Hot or not?

There're languages like TypeScript.

## Transpilation

<!-- .slide: data-background="white" -->
![https://spzone-simpleprogrammer.netdna-ssl.com/wp-content/uploads/2016/05/Transpilation.png](https://spzone-simpleprogrammer.netdna-ssl.com/wp-content/uploads/2016/05/Transpilation.png)

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
