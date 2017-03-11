# Building blocks
<!-- .slide: data-background-image="https://s-media-cache-ak0.pinimg.com/originals/2f/ae/e1/2faee1afb1444950f14b8feea47620ff.jpg" -->

What is nowadays' web application made of?

You can think of it on maaaany levels.
E.g.
- domain name
- "look and feel"
- content to appear on the site
- hosting

But on the programming level...

---

#### Building blocks
## A brief explanation of how Internet works

Let's assume I have a webpage with a quote. Wee.
```
<html>
    <body>After all this time? Always.</body>
</html>
```
I keep it in index.html file.
Note:
- When you type eestec.net... 
- it resolves eestec.net to IP address that identifies the computer that has our site
- then our browser sends a HTTP request to this server: "hey, GET me this page"
- server has a process listening on :80 port 
- looks up the file on the HDD
- the page is like this (sample html page with a quote from HP)
- and sends it back to you
- your browser parses it
- and displays
- TADA

So what do we need to get achieve this behaviour?

1. A computer with Internet connection. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Process listening and responding to requests.  <!-- .element: class="fragment" data-fragment-index="2" -->
3. Content. <!-- .element: class="fragment" data-fragment-index="3 " -->
Note:
The computer that hosts our site is called "server". But it's nothing special really. Just a computer, usually without a screen and with great Internet connection.
No magic here :(.

---

#### Building blocks
## Dynamic Web

But... we don't want our site to have just a quote. Or text.
We want fireworks, login pages, and randomized quotes!!11!
Note:
Not sure if it's proper naming though.

## Let's start with a randomized quote.

#### You can...
## have different files with different quotes.
Naive, but ok. May work for a few quotes, but difficult in maintenance. <!-- .element: class="fragment" data-fragment-index="2" -->

#### You can...
### have quotes as array of strings and make a process return a randomized quote instead of a html file
This might work, but it's hard to return sth more than that. <!-- .element: class="fragment" data-fragment-index="2" -->

#### You can...
### have quotes as array of strings and create a HTML template and make your process replace the {{place for quote}}
That's just fine... but array of strings isn't the best possible way to do that, right? <!-- .element: class="fragment" data-fragment-index="2" -->

#### You can...
### store quotes somewhere and create a HTML template and make your process replace the {{place for quote}}
Scalable and cool. <!-- .element: class="fragment" data-fragment-index="2" -->

1. A computer with Internet connection. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Place to store some stuff. <!-- .element: class="fragment" data-fragment-index="2" -->
3. Process listening and responding to requests. <!-- .element: class="fragment" data-fragment-index="1" -->
4. Template for the content. <!-- .element: class="fragment" data-fragment-index="1" -->

## And what about these fireworks?

#### You can...
## add some photos as set of JPEGs
Meh, not dynamic at all.

#### You can...
## add some animations as GIFs
Kinda works... but I want the fireworks to follow the mouse!!!1!

Turns out... you can't! Why?

Because currently the page, once it's downloaded, cannot change. 

Javascript & client-side computation to the rescue! :)

1. A computer with Internet connection. <!-- .element: class="fragment" data-fragment-index="1" -->
2. Place to store some stuff.  <!-- .element: class="fragment" data-fragment-index="1" -->
3. Process listening and responding to requests.  <!-- .element: class="fragment" data-fragment-index="1" -->
4. Template for the content.  <!-- .element: class="fragment" data-fragment-index="1" -->
5. Styles for the page to look nice.  <!-- .element: class="fragment" data-fragment-index="2" -->
6. Client-side scripts allowing interaction.  <!-- .element: class="fragment" data-fragment-index="3" -->

1. Server.
2. Database.
3. Server process.
4. HTML.
5. CSS.
6. JS.

---

#### Building blocks
## Modular architecture

## Nowadays
Web service (usually) = Back-end + Front-end

1. BACKEND - Server
2. BACKEND - Database.
3. BACKEND - Server process.
4. FRONTEND - HTML.
5. FRONTEND - CSS.
6. FRONTEND - JS.

### Why do you think it's worth to separate it?
(that's a question)

### Reason 1: Easier to maintain
Note:
When code is modular, it's much easier to work on it. 

### Reason 2: Many front-end apps to one back-end...
Note:
Mobile, destkop and web app use the same server.

### Reason 3: And many back-end apps to one front-end...
Note:
Frontend 

### Reason 4: Programmers like to ABSTRACT
Note:
Frontend dev doesn't need to know how the backend works - treats it like blackbox.
Backend dev doesn't need to know how data is presented.

---

#### Building blocks
## Technology stack

**Stack** is a common name for a set of technologies used in project.

### LAMP vs MEAN
![http://andyshora.com/img/stacks-change.jpg](http://andyshora.com/img/stacks-change.jpg)



