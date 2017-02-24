- Ćwiczenie z onetu (20 min)
- MVC (wzorzec Model View Controller i jego odmiany) i jak jest robione gdzie indziej
- do zrobienia dobrej strony potrzebny jest tylko dobrze zrobiony backend 
- frontendowe frameworki są głównie potrzebne do komunikacji z api

- trzeba to przemyslec:
- modele tworzenia aplikacji (strony statyczne/dynamiczne i takie które wystawiają api)
- jakie sa róznice w performance modularnych frameworków:
	- z jednego api moze korzystac wiecej niz jedna aplikacjca (przykład - aplikacje mobilne i desktopowe czy webowe)
	- połączenia Computer-to-Computer ()
- Restowe api co to?
- metody CRUD (Create read update delete) - w api ale takze w innych miejscach (bazy danych itp) - Koncepcja ktora w zalozeniu ma wyczerpac limit operacji na modelu.
- przykład - lista uczniow w Hogwarcie
- i teraz płynne przejscie z Backend do DB - przechowywanie informacji
- dlaczego bazy danych a nie zapisywanie do plikow
- zasada jasna - ale chodzi o wygode i szybkosc dostepu do informacji oraz uporządkowanie tych informacji
- Najbardziej podstawowe db (SQL) mają swój język który, jeszcze bardziej ułatwia prace z nimi
- Baza danych vs program - w programie zmiennie po wylaczeniu giną
- DB SQL i nieSQL - relacyjne i nierelacyjne
- Rózne typy danych - w róznych miejscach - odpowiada to róznym tabelom 
- trzeba to w jakis sposob ze sobą powiązac, czyli albo tworzyc dupną tablice gdzie beda te wszystkie informacje albo podejść do tego mądrzej
# Przykład:
- tablica uczniow, nauczycieli i zajec
- kazdy z wierszy dostaje unikalny identyfikator 
- łączymy to w kolejna tablice gdzie znajduja sie tylko id

- poczytać jakie przewagi nierelacyjnych nad relacyjnymi
- HATEOAS
