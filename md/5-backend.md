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
#### Ok, but handling requests like that manually sucks.

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

1. Model - what is the data? <!-- .element: class="fragment" data-fragment-index="1" -->
2. Controller - what am I doing? <!-- .element: class="fragment" data-fragment-index="2" -->
3. View - what do I see? <!-- .element: class="fragment" data-fragment-index="3" -->

![http://doriansobacki.pl/wp-content/uploads/2016/03/mvc_role_diagram.png](http://doriansobacki.pl/wp-content/uploads/2016/03/mvc_role_diagram.png)

### Why?
- reusability of code <!-- .element: class="fragment" data-fragment-index="1" -->
- less mess <!-- .element: class="fragment" data-fragment-index="2" -->
- easy to test and troubleshoot <!-- .element: class="fragment" data-fragment-index="3" -->
- de facto a standard <!-- .element: class="fragment" data-fragment-index="4" -->

![](http://s2.quickmeme.com/img/21/2142bd8b63c2985b650a7796ee0767f0e07f8de2f6540dab06d1760b68faa134.jpg)

---

#### Backend
# Databases

Ok, so we want to have plenty of spells. And the desciption of spells. And difficulty level. Cool. 

How do we store it?
(that's a question)

#### You can...
### store spells as an array of strings
We already discussed that - it should be separated! <!-- .element: class="fragment" data-fragment-index="2" -->

#### You can...
### store spells in a separate file
Cool, that may work... <!-- .element: class="fragment" data-fragment-index="2" -->

spells.txt
```
Alohomora - a spell used to open doors. Difficulty: easy.
Crucio - a spell that makes someone hurt. Difficulty: hard.
Serpensortia - something with snakes. Difficulty: hard.
Flipendo - moves snails, lol. Difficulty: easy.
...
```
Note:
This actually works. And people use it. And it's completely fine. You need a proper format to store the data, right? Otherwise, how would you tell apart the description from the name from the difficulty?

### CSV - Comma Separated Values
```
name,descriptions,difficulty
Alohomora,a spell used to open doors,easy.
Crucio,a spell that makes someone hurt,hard.
Serpensortia,something with snakes,hard.
Flipendo,moves snails\, lol,easy.
...
```

A few problems with that though...

```
name,descriptions,difficulty
Alohomora,a spell used to open doors,easy.
Crucio,a spell that makes someone hurt,hard.
Serpensortia,something with snakes,hard.
Flipendo,moves snails\, lol,easy.
Accio,This charm summons an object to the caster, potentially over a significant distance. It can be used in two ways; either by casting the charm and then naming the object desired, or by pointing your wand at the desired object during or immediately following the incantation to "pull" the target toward the caster; in either case, the caster must concentrate on the object they wish to summon in order for the charm to succeed. The caster doesn't necessarily need to know the location of the target if they say the name of the object to be summoned, such as when Hermione Granger summoned some books from Dumbledore's office simply by saying "Accio Horcrux books!" while in Gryffindor Tower.,hard
...
```
Note:
Too much data
hard to find one to delete, update, search, etc...

### Remember
1. Engineers are lazy. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Engineers like to abstract. <!-- .element: class="fragment" data-fragment-index="2" -->

## Need is the mother of invention

Let's abstract this information to a **table**.

Table: **spells**
<table>
<thead>
    <td>Name</td>
    <td>Description</td>
    <td>Difficulty</td>
</thead>
<tbody>
    <tr>
        <td>Alohomora</td>
        <td>a spell used to open doors</td>
        <td>easy</td>
    </tr>
    <tr>
        <td>Crucio</td>
        <td>a spell that makes someone hurt</td>
        <td>hard</td>
    </tr>
    <tr>
        <td>Flipendo</td>
        <td>moves snails, lol</td>
        <td>easy</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

---

#### Backend
# SQL 101

<!-- .slide: data-background-image="https://m.popkey.co/248c7d/8yrLO.gif" -->
## STAY WITH ME.
#### This part might be tough.

### SQL -  Structured Query Language 
Kinda like English.
```
select * from spells;
select * from spells where difficulty="easy";
select name from spells;
```
Note:
You can do all cool stuff with that that you couldn't do with a file. Let's say that we want to match who's favourite spell it is. And we have a table of famous wizards and data about their fav spells. Cool!

<!-- .slide: data-background-image="http://www.edselby.com/wp-content/uploads/2013/12/monkey.png" -->
### A philosophical one:
### What can be ever done with anything?

#### CRUD
- Create <!-- .element: class="fragment" data-fragment-index="1" -->
- Read <!-- .element: class="fragment" data-fragment-index="2" -->
- Update <!-- .element: class="fragment" data-fragment-index="3" -->
- Delete <!-- .element: class="fragment" data-fragment-index="4" -->

#### CRUD
- Create = CREATE, INSERT INTO
- Read = SELECT
- Update = UPDATE 
- Delete = DELETE

Table: **spells**
<table>
<thead>
    <td>Name</td>
    <td>Description</td>
    <td>Difficulty</td>
</thead>
<tbody>
    <tr>
        <td>Alohomora</td>
        <td>a spell used to open doors</td>
        <td>easy</td>
    </tr>
    <tr>
        <td>Crucio</td>
        <td>a spell that makes someone hurt</td>
        <td>hard</td>
    </tr>
    <tr>
        <td>Flipendo</td>
        <td>moves snails, lol</td>
        <td>easy</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>
Note:
examples of selects etc...

Table: **famous_wizards**
<table>
<thead>
    <td>Name</td>
    <td>Origins</td>
</thead>
<tbody>
    <tr>
        <td>Harry Potter</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>Tom Riddle</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>Newt Scamander</td>
        <td>US or something</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

Table: **spells**
<table>
<thead>
    <td>Name</td>
    <td>Description</td>
    <td>Difficulty</td>
    <td>Faved by</td>
</thead>
<tbody>
    <tr>
        <td>Alohomora</td>
        <td>...</td>
        <td>easy</td>
        <td>Harry Potter</td>
    </tr>
    <tr>
        <td>Crucio</td>
        <td>...</td>
        <td>hard</td>
        <td>Tom Riddle</td>
    </tr>
    <tr>
        <td>Flipendo</td>
        <td>...</td>
        <td>easy</td>
        <td>Harry Potter</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

```
select * from spells where favedBy = "Tom Riddle";
```
Crucio. <br />
Yay?

Not quite. <br />
What if Tom Riddle... decides to change his name?

```
update famous_wizards set name = "Voldemort" where name = "Tom Riddle";
```
Table: **famous_wizards**
<table>
<thead>
    <td>Name</td>
    <td>Origins</td>
</thead>
<tbody>
    <tr>
        <td>Harry Potter</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>Voldemort</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>Newt Scamander</td>
        <td>US or something</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>
Note:
Two problems: what if there's more Tom Riddles? And what happens to the favedBy?

```
select * from spells where favedBy = "Tom Riddle";
```
0 Results :(

Table: **famous_wizards**
<table>
<thead>
    <td>Wizard ID</td>
    <td>Name</td>
    <td>Origins</td>
</thead>
<tbody>
    <tr>
        <td>1</td>
        <td>Harry Potter</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Voldemort</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Newt Scamander</td>
        <td>US or something</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

Table: **spells**
<table>
<thead>
    <td>Name</td>
    <td>Description</td>
    <td>Difficulty</td>
    <td>Faved by</td>
</thead>
<tbody>
    <tr>
        <td>Alohomora</td>
        <td>...</td>
        <td>easy</td>
        <td>1</td>
    </tr>
    <tr>
        <td>Crucio</td>
        <td>...</td>
        <td>hard</td>
        <td>2</td>
    </tr>
    <tr>
        <td>Flipendo</td>
        <td>...</td>
        <td>easy</td>
        <td>1</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

```
select * from famous_wizards where name = "Voldemort"; // returns 1
select * from spells where favedBy = 1;
```

## E.g. a subquery
```
select * from spells 
where favedBy = (select * from famous_wizards where name = "Voldemort");
```

But hey... Wojtek likes Flipendo as well.

Table: **famous_wizards**
<table>
<thead>
    <td>Wizard ID</td>
    <td>Name</td>
    <td>Origins</td>
</thead>
<tbody>
    <tr>
        <td>1</td>
        <td>Harry Potter</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Voldemort</td>
        <td>Hogwart</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Newt Scamander</td>
        <td>US or something</td>
    </tr>
    <tr>
        <td>4</td>
        <td>Boitec the Sparrow</td>
        <td>Dębica</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

Table: **spells**
<table>
<thead>
    <td>Spell ID</td>
    <td>Name</td>
    <td>Description</td>
    <td>Difficulty</td>
    <td>Faved by</td>
</thead>
<tbody>
    <tr>
        <td>1</td>
        <td>Alohomora</td>
        <td>...</td>
        <td>easy</td>
        <td>1</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Crucio</td>
        <td>...</td>
        <td>hard</td>
        <td>2</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Flipendo</td>
        <td>...</td>
        <td>easy</td>
        <td>1,4</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

Not cool.

Table: **favourite_spells**
<table>
<thead>
    <td>Wizard ID</td>
    <td>Spell ID</td>
</thead>
<tbody>
    <tr>
        <td>1</td>
        <td>1</td>
    </tr>
    <tr>
        <td>2</td>
        <td>2</td>
    </tr>
    <tr>
        <td>4</td>
        <td>1</td>
    </tr>
    <tr>
        <td>...</td>
        <td>...</td>
        <td>...</td>
    </tr>
</tbody>
</table>

Now one wizard can like many spells. And one spells can be liked by many wizards.

```
select wizard.name from wizards 
join favourite_spells on wizard.id = favourite_spells.wizard_id
join spells on spells.id = favourite_spells.spell_id
where spells.name = "Flipendo";
```

<!-- .slide: data-background-image="https://media.giphy.com/media/qucJWFolJN6rS/giphy.gif" -->
## WHY COMPLICATE SO MUCH!!?1/?!!

It's consistent. And structured.

---

#### Backend
# NoSQL

<!-- .slide: data-background-image="http://x3.wykop.pl/cdn/c3201142/comment_uP0wKqaQuBoO5hh9Fpm8w2glgHcGQssd.jpg" -->
### What if I don't know the database structure?

<!-- .slide: data-background-image="http://x3.wykop.pl/cdn/c3201142/comment_uP0wKqaQuBoO5hh9Fpm8w2glgHcGQssd.jpg" -->
### What if I have shitload of data?

<!-- .slide: data-background-image="http://x3.wykop.pl/cdn/c3201142/comment_uP0wKqaQuBoO5hh9Fpm8w2glgHcGQssd.jpg" -->
### What if I'm hipster?

NoSQL = Not Only SQL

- Horizontal scalability
- Performance
- Schema flexibility
- More natural way of representing data
Note:
- DB SQL i nieSQL - relacyjne i nierelacyjne
- Rózne typy danych - w róznych miejscach - odpowiada to róznym tabelom 
- trzeba to w jakis sposob ze sobą powiązac, czyli albo tworzyc dupną tablice gdzie beda te wszystkie informacje albo podejść do tego mądrzej

```
{
    "name": "Accio",
    "description": "This charm summons an object to the caster, potentially over a significant distance. It can be used in two ways; either by casting the charm and then naming the object desired, or by pointing your wand at the desired object during or immediately following the incantation to "pull" the target toward the caster; in either case, the caster must concentrate on the object they wish to summon in order for the charm to succeed. The caster doesn't necessarily need to know the location of the target if they say the name of the object to be summoned, such as when Hermione Granger summoned some books from Dumbledore's office simply by saying "Accio Horcrux books!" while in Gryffindor Tower.",
    "difficulty": "hard",
    "favedBy": ["Harry Potter", "Boitec the Sparrow"]
}
```

---

#### Backend
# ORM



---

#### Backend
# Server

<!-- .slide: data-background-image="http://cdn.softlayer.com/innerlayer/softlayerrackfront_s.gif" -->
## Mostly Linux. Why?
Note:
- scalable
- maintainable
- open source
- CLI > clicking

<!-- .slide: data-background-image="http://www.penguins-world.com/wp-content/uploads/Information_page.jpg" -->
#### Because...
# Software
Note:
Web servers, caches, FTP servers, web applications, DNS severs, and on and on. They are available for Linux and Unix first and in a wide variety.

<!-- .slide: data-background-image="https://uploads.toptal.io/blog/image/121113/toptal-blog-image-1472630963773-cd27e655dbde285a9698badbd83d5ed8.png" -->
#### Because...
# History
Note:
Windows was designed for the single user desktop, whereas Unix was designed as a multiuser networked machine early on, even before Windows existed. Secondly, Unix was commercial, and the BSDs were tied up in court when Linux rose to power.

<!-- .slide: data-background-image="https://betanews.com/wp-content/uploads/2015/04/makeitrain-592x600.jpg" -->
#### Because...
# Price
Note:
Linux systems are free. A company can grab a Linux variant and have an industrial strength server for free. Sure, they can get support and such if they pay - but the fact is many companies let support go.

<!-- .slide: data-background-image="http://i.imgur.com/daF13vl.gif" -->
#### Because...
# Security
Note:
Linux was designed as a multiuser environment from the start, as was Unix. Windows had to be retrofitted with multiuser support, and the user base was used to their Windows system being all their own.

So, some knowledge of Linux CLI is mandatory. <br />
CLI = Command Line Interface.

---

#### Backend
# Microservices

Fancy idea of how to structurize your app.
![yt](CKL3fV5UR8w)
