## Short excercise for a perfect start
Note: 
Ćwiczenie z onetu (20 min)

# Model View Controller (MVC)
- Model - representation of problem or application logic
- View - describes how to present certain Model's part in user interface
- Controller - for input gets user's data and replays by updating Model and refresh View
Note:
- MVC (wzorzec Model View Controller i jego odmiany) i jak jest robione gdzie indziej

## All you need is... backend
### You already did it!
Note:
- do zrobienia dobrej strony potrzebny jest tylko dobrze zrobiony backend 
- frontendowe frameworki są głównie potrzebne do komunikacji z api

## It all depends on your needs
Note:
- modele tworzenia aplikacji (strony statyczne/dynamiczne i takie które wystawiają api)

## Why API?
- Because we don't want to be selfish
- It's smart
Note:
- jakie sa róznice w performance modularnych frameworków:
	- z jednego api moze korzystac wiecej niz jedna aplikacjca (przykład - aplikacje mobilne i desktopowe czy webowe)
	- połączenia Computer-to-Computer ()

# Let's have a REST
Note:
- Restowe api co to?

## CRUD
- Create
- Read
- Update
- Delete
Note:
- metody CRUD (Create read update delete) - w api ale takze w innych miejscach (bazy danych itp) - Koncepcja ktora w zalozeniu ma wyczerpac limit operacji na modelu.
- przykład - lista uczniow w Hogwarcie

## When I say Backend you think... DataBase
Note:
- i teraz płynne przejscie z Backend do DB - przechowywanie informacji

## But there are other ways to store data?!
Note:
- dlaczego bazy danych a nie zapisywanie do plikow
- zasada jasna - ale chodzi o wygode i szybkosc dostepu do informacji oraz uporządkowanie tych informacji
- Baza danych vs program - w programie zmiennie po wylaczeniu giną

## We can see that you like programming so we created a programming language for your database so you can program while you access your DB.
Note:
- Najbardziej podstawowe db (SQL) mają swój język który, jeszcze bardziej ułatwia prace z nimi

## Need is the mother of invention
### relational database
- scalable
- manageability
### non relational database
- unstructurised objects
- different types of data
Note:
- DB SQL i nieSQL - relacyjne i nierelacyjne
- Rózne typy danych - w róznych miejscach - odpowiada to róznym tabelom 
- trzeba to w jakis sposob ze sobą powiązac, czyli albo tworzyc dupną tablice gdzie beda te wszystkie informacje albo podejść do tego mądrzej

# EXAMPLE:
- tablica uczniow, nauczycieli i zajec
- kazdy z wierszy dostaje unikalny identyfikator 
- łączymy to w kolejna tablice gdzie znajduja sie tylko id