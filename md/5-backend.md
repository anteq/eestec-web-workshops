# Backend
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg"; background-size: 80% -->

Remember how internet works?

Backend = server process. <br />
Any language, really.

Let's start... in C. :D <br />
<img src="http://kimkarpeles.com/wp-content/uploads/2013/05/work-in-progress1.png" height="300px"></img>
Note:
Exercise

---

#### Backend
# MVC

## Model 
#### representation of problem or application logic

## View 
#### describes how to present certain Model's part in user interface

## Controller 
#### for input gets user's data and replays by updating Model and refresh View
Note:
- MVC (wzorzec Model View Controller i jego odmiany) i jak jest robione gdzie indziej

![](http://s2.quickmeme.com/img/21/2142bd8b63c2985b650a7796ee0767f0e07f8de2f6540dab06d1760b68faa134.jpg)

## All you need is... backend
### You already did it!
Note:
- do zrobienia dobrej strony potrzebny jest tylko dobrze zrobiony backend 
- frontendowe frameworki są głównie potrzebne do komunikacji z api

## It all depends on <br />
<img src="http://www.etrainingpedia.com/wp-content/uploads/2015/11/8df1715368055f5cc8b8c69ef0e05641_c5e3c55967a2c8dcc83a77ca41d88461_w548_.jpg"></img>
Note:
- modele tworzenia aplikacji (strony statyczne/dynamiczne i takie które wystawiają api)

## Why API?
- Because we don't want to be selfish
- It's smart <br />
![](md/5-backend/LUKE.jpg)
Note:
- jakie sa róznice w performance modularnych frameworków:
	- z jednego api moze korzystac wiecej niz jedna aplikacjca (przykład - aplikacje mobilne i desktopowe czy webowe)
	- połączenia Computer-to-Computer ()

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

---

#### Backend
# CLI