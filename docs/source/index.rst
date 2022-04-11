Korpusomat
===================================

**Korpusomat** jest aplikacją webową służącą do tworzenia oznakowanych fleksyjnie korpusów tekstów, z których można korzystać za pomocą wyszukiwarki MTAS. Aplikacja w zasadzie nie stanowi nowego narzędzia informatycznego, a jedynie łączy narzędzia, które powstały przed laty lub wciąż są rozwijane w Zespole Inżynierii Lingwistycznej Instytutu Podstaw Informatyki PAN. Zasadniczym celem Korpusomatu jest udostępnienie wyników działań tych narzędzi bez konieczności szczegółowego poznawania technicznej strony ich działania, co do tej pory nie było możliwe.

Na działanie Korpusomatu składają się:
 - analizator morfologiczny Morfeusz stworzony w oparciu o dane lingwistyczne Słownika gramatycznego języka polskiego,
 - tager Concraft,
 - Liner 2 wykorzystany do rozpoznawania nazw własnych,
 - TermoPL,
 - wyszukiwarka korpusowa MTAS.

Dwa pierwsze z programów, czyli Morfeusz i Concraft, są wciąż rozwijane i ich nowsze wersje będą sukcesywnie włączane do Korpusomatu. Liner2 to narzędzie do rozpoznawania i znakowania nazw własnych, wyrażeń temporalnych i opisów sytuacji w tekście - w Korpusomacie aktualnie wykorzystywany jest jedynie do znakowania nazw własnych, ale w przyszłości zostaną włączone również inne jego moduły. TermoPL jest narzędziem do ekstrakcji terminologii z podanych tekstów - jest używane na ekranie statystyk korpusu. MTAS jest wyszukiwarką korpusową stworzoną przez holenderski Meertens Instituut w ramach projektu Clarin.

Korpusomat przetwarza pliki tekstowe (txt) oraz większość innych formatów służących do przechowywania danych tekstowych (np. epub, mobi, doc, rtf czy pdf – pełna lista możliwych formatów dostępna jest pod adresem http://tika.apache.org/1.17/formats.html). Narzędzia, z których korzysta, wymagają stosowania kodowania UTF-8, jeśli jednak użytkownik prześle plik w innym stosowanym dla języka polskiego kodowaniu, np. ISO-8859-2 czy CP-1250, Korpusomat automatycznie skonwertuje je do kodowania UTF-8 na swój wewnętrzny użytek.

Korpusomat pozwala również na dodawanie artykułów ze stron internetowych. W takim przypadku wskazana strona zostaje przetworzona za pomocą biblioteki newspaper, której opis dostępny jest tutaj.

Dokumentacja
--------

.. toctree::

   instrukcja/index
   mtas
   profile-slow
   statystyki
   narzedzia
   publikacje
   cytowanie
