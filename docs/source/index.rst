.. role:: todo
    :class: todo

.. role:: lex
    :class: lex


Korpusomat
===================================

**Korpusomat** jest aplikacją webową służącą do tworzenia wielowarstwowo oznakowanych korpusów tekstów, z których można korzystać za pomocą wyszukiwarki MTAS. Do znakowania wykorzystywane są nowoczesne wielojęzyczne zestawy narzędzi programistycznych spaCy i Stanza. Zasadniczym celem Korpusomatu jest udostępnienie badaczom wyników działań tych narzędzi na dowolnych tekstach bez konieczności szczegółowej znajomości technicznej strony ich działania.

Korpusomat przetwarza pliki tekstowe (txt) oraz większość innych formatów służących do przechowywania danych tekstowych (np. epub, mobi, doc, rtf czy pdf – pełna lista możliwych formatów dostępna jest pod adresem http://tika.apache.org/1.17/formats.html). Narzędzia, z których korzysta, wymagają stosowania kodowania UTF-8, jeśli jednak użytkownik prześle plik w innym kodowaniu, np. ISO-8859-2 czy CP-1250 (w wypadku języka polskiego), Korpusomat automatycznie skonwertuje je do kodowania UTF-8 na swój wewnętrzny użytek.

Korpusomat pozwala również na dodawanie artykułów ze stron internetowych. W takim przypadku wskazana strona zostaje przetworzona za pomocą biblioteki newspaper, której opis dostępny jest pod adresem: https://newspaper.readthedocs.io/. 

Dokumentacja
--------

.. toctree::

   manual/index
   mtas
   word-profiles
   statistics
   tools-resources
   licence
   citing
   authors
   
..
   profile-slow
   statystyki
   publikacje
   cytowanie
