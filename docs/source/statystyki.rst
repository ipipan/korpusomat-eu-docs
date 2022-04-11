Ekran statystyk
===============

Lista frekwencyjna
------------------

W tym polu wyświetlana jest lista frekwencyjna ze względu na lematy słów. Wstępnie odfiltrowana jest do słów pełnoznacznych, jednak za pomocą przycisku na górze można ją odfiltrować do dowolnie wybranych części mowy. Po kliknięciu przycisku „Pobierz” zostanie pobrana pełna lista frekwencyjna bez zastosowanego filtrowania, natomiast zawierająca pierwszy 1000 najczęściej występujących lematów.

Słownictwo charakterystyczne
----------------------------

Słownictwo charakterystyczne generowane jest przez aplikację TermoPL. Opis jej działania, instrukcja i dodatkowe informacje dostępne są na tej stronie.

W polu na stronie informacje ograniczone są do formy bazowej, wartości C-value oraz liczby wystąpień, posortowane wg C-value. Po kliknięciu przycisku „Pobierz” pobrany zostaje plik zawierający wszystkie dane wygenerowane przez TermoPL w formacie wyjściowym aplikacji.

Pliki wygenerowane przez Korpusomat są kompatybilne z aplikacją TermoPL – po pobraniu „plików źródłowych korpusu” (przycisk dostępny na ekranie korpusu) można samodzielnie uruchomić aplikację TermoPL z wybranymi przez siebie opcjami.

Wykres wg metadanych
--------------------

W tym polu wyświetlany jest wykres przedstawiający podział segmentów w korpusie ze względu na wybraną metadaną, wybraną przez użytkownika.

Kolokacje
---------

To pole zawiera wyznaczone najbardziej prawdopodobne związki wyrazowe dla zadanego schematu. Domyślnie wyświetlone są formy bazowe każdego ze słów składających się na dane wystąpienie, liczba wystąpień oraz symetryczne prawdopodobieństwo warunkowe. Wyświetlanych jest 50 związków posortowanych wg prawdopodobieństwa.

W pliku dostępnym do pobrania znajdują się wszystkie związki spełniające dane kryterium wyszukiwania oraz kilka miar je charakteryzujących.

Te miary to:
 - Liczba wystąpień danego związku
 - Prawdopodobieństwo warunkowe symetryczne.
 - Maksymalne prawdopodobieństwo warunkowe.
 - Miara Dice.
 - Prawdopodobieństwo warunkowe obliczone dla każdego ze składników związku.
 - Liczba wystąpień każdego ze składników związku.

Słowa kluczowe
--------------

Słowa kluczowe obliczone są na podstawie porównania listy frekwencyjnej korpusu z listą frekwencyjną korpusu referencyjnego. Korpusem referencyjnym w tym przypadku jest milionowy korpus NKJP.

Rozkład słów kluczowych
-----------------------

Wizualizacja przedstawia występowanie słów kluczowych korpusu w ramach każdego dokumentu tekstowego. Położenie i wielkość są oparte na sumach wystąpień poszczególnych słów kluczowych w kolejnych zdaniach dokumentu. Regulacja zagęszczenia pozwala na sumowanie wystąpień słów z kilku zdań do jednego punktu na wizualizacji, domyślnie ustawiona wartość zagęszczenia ma na celu zwiększenie czytelności wizualizacji.
