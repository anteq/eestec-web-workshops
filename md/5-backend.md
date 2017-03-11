# Backend
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg"; background-size: 80% -->

Remember how internet works?

Backend = server process. <br />
Any language, really.

<!-- .slide: data-background-image="http://www.reactiongifs.com/r/rbp.gif" -->
Any?

#### CGI (Common Gateway Interface)
An interface enabling communication between WWW server and other programms that run on server. <br />
![http://www.sergey.com/web_course/images/cgi.jpg](http://www.sergey.com/web_course/images/cgi.jpg)
Note:
Za pomocą programów CGI można dynamicznie (na żądanie klienta) generować dokumenty HTML, uzupełniając je np. treścią pobieraną z bazy danych.

Of course, usually it's in Python. Java. JavaScript. Scala. PHP.

How about a server... in C. :D <br />
<img src="http://kimkarpeles.com/wp-content/uploads/2013/05/work-in-progress1.png" height="300px"></img>
Note:
Exercise

---

#### Backend
# The meat

<!-- .slide: data-background-image="https://68.media.tumblr.com/bde33ad2ec722b87057642e8b9a8af1e/tumblr_nwy9cfQScI1ukrx8mo1_400.gif" --> 
Ok, but handling requests like that manually sucks.

### Remember
1. Engineers are lazy. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Engineers like to abstract. <!-- .element: class="fragment" data-fragment-index="2" -->

Therefore... we can automate this stuff!

<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/39/38/cc/3938cc46030d661fc8d5f29199063447.gif" -->

A **web framework** is a way to automate repeating tasks (like request handling, socket operations, persisting the session etc.).

It also allows you to organize your code properly, use packages developed by community and soooo much more.

---

#### Backend
# MVC

If you'll remember one thing from this workshops - let it be it. :)

MVC = Model View Controller.

It's a *software architecture pattern* - a general reusable solution to a commonly occurring problem. In this case - organizing code in website.

1. Model - represents the problem or application logic <!-- .element: class="fragment" data-fragment-index="1" -->
2. View - describes how to present certain Model's part in user interface <!-- .element: class="fragment" data-fragment-index="2" -->
3. Controller - updates Model and refreshes View <!-- .element: class="fragment" data-fragment-index="3" -->
Note:
- MVC (wzorzec Model View Controller i jego odmiany) i jak jest robione gdzie indziej

1. Model - how do I represent the data? <!-- .element: class="fragment" data-fragment-index="1" -->
2. Controller - what am I doing? <!-- .element: class="fragment" data-fragment-index="2" -->
3. View - what do I see? <!-- .element: class="fragment" data-fragment-index="3" -->

![http://doriansobacki.pl/wp-content/uploads/2016/03/mvc_role_diagram.png](http://doriansobacki.pl/wp-content/uploads/2016/03/mvc_role_diagram.png)

### Why?
- reusability of code <!-- .element: class="fragment" data-fragment-index="1" -->
- less mess <!-- .element: class="fragment" data-fragment-index="2" -->
- easy to test and troubleshoot <!-- .element: class="fragment" data-fragment-index="3" -->
- de facto a standard <!-- .element: class="fragment" data-fragment-index="4" -->

![](http://s2.quickmeme.com/img/21/2142bd8b63c2985b650a7796ee0767f0e07f8de2f6540dab06d1760b68faa134.jpg)

**Not only on backend!**

In API-based solutions: view is the API format.
Note:
Backend: M->C->V -----> M->C->V 

---

#### Backend
# Databases

## When I say Backend you think... DataBase
Note:
- i teraz płynne przejscie z Backend do DB - przechowywanie informacji

![](http://s2.quickmeme.com/img/61/61c1ee2ce9d31c894d188b7b17cacee90ffdece8bc4c4798d10100b7515820de.jpg)

## But there are other ways to store data, right?!
Note:
- dlaczego bazy danych a nie zapisywanie do plikow
- zasada jasna - ale chodzi o wygode i szybkosc dostepu do informacji oraz uporządkowanie tych informacji
- Baza danych vs program - w programie zmiennie po wylaczeniu giną

![](md/5-backend/yo_dbjpg.jpg)
Note:
- Najbardziej podstawowe db (SQL) mają swój język który, jeszcze bardziej ułatwia prace z nimi

## Need is the mother of invention

### relational database
- scalable
- manageability <br />
![](https://cdn.meme.am/cache/instances/folder946/59552946.jpg)

### non relational database
- unstructurised objects
- different types of data <br />
![](http://s.quickmeme.com/img/f9/f9b53ea30771fd3e7dc380ae3db4a0a0e2241b6ba4f2aa4feb438983a3796fdf.jpg)
Note:
- DB SQL i nieSQL - relacyjne i nierelacyjne
- Rózne typy danych - w róznych miejscach - odpowiada to róznym tabelom 
- trzeba to w jakis sposob ze sobą powiązac, czyli albo tworzyc dupną tablice gdzie beda te wszystkie informacje albo podejść do tego mądrzej

# EXAMPLE?
Note:
- tablica uczniow, nauczycieli i zajec
- kazdy z wierszy dostaje unikalny identyfikator 
- łączymy to w kolejna tablice gdzie znajduja sie tylko id

---

#### Backend
# Asynchronous?

## What is that word?
![](http://cdn3.teen.com/wp-content/uploads/2015/07/harry-potter-ron-weasley-confused.jpg)

## An example for thinking.

## What is the single most important reason that we need this?

## When communicating, time of response is *nondeterministic*.

## Short excercise
![](https://img.buzzfeed.com/buzzfeed-static/static/2014-12/30/15/enhanced/webdr10/enhanced-buzz-wide-18359-1419973035-10.jpg)
Note: 
Ćwiczenie z onetu (20 min)

--- 

#### Backend
# Servers

## Mostly Linux. Why?
Note:
- scalable
- maintainable
- open source
- CLI > clicking

![](https://www.mememaker.net/static/images/memes/4282491.jpg)
