Korpusy równoległe
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Korpusomat umożliwia tworzenie korpusów równoległych czyli takich, w których teksty w różnych językach są ze sobą powiązane
zdaniowo — każde zdanie w jednym języku odpowiada zdaniu (lub grupie zdań) w drugim języku.
Dzięki temu możliwe jest wyszukiwanie odpowiedników słów, zwrotów i konstrukcji między językami.

Obsługiwane formaty plików
==========================

Pliki z tekstami można dodać na dwa sposoby:

a) **plik TMX** 
- Zawiera już zdania sparowane w dwóch (lub więcej) językach.
Korpusomat automatycznie odczytuje te pary i zachowuje ich powiązanie.

b) **Oddzielne pliki tekstowe TXT**
- Możliwe jest przesłanie dwóch osobnych plików tekstowych, po jednym dla każdego języka.
    - Pliki z wierszami odpowiadającymi sobie: każdy wiersz odpowiada jednemu zdaniu, a wiersze w obu plikach są sparowane.

    - Pliki z wierszami nieodpowiadającymi sobie: na przykład książka napisana w języku polskim oraz jej tłumaczenie na język angielski.
      Pliki nie mają powiązań między zdaniami. W takim przypadku dopasowanie zdań zostanie wykonane przez narzędzie **Hunalign**, które porównuje długość zdań i korzysta ze słowników dwujęzycznych, aby dopasować do siebie odpowiadające zdania w obu językach.


Instrukcja
==================

Podczas tworzenia korpusu należy zaznaczyć checkbox **Korpus równoległy** oraz określić języki dodawanych tekstów.

|image1|

Następnie należy wybrać zrównoleglony wcześniej plik (DODAJ TEXT ZRÓWNOLEGLONY (TMX)) lub osobne pliki tekstowe (DODAJ TEKSTY DO ZRÓWNOLEGLENIA)

|image2|
|image3|

Jeżeli w plikach, które dodajemy wiersz w jednym pliku odpowiada wierszowi w drugim pliku należy zaznaczyć checkbox **Wiersze w obu plikach odpowiadają sobie**.

|image4|
|image5|

Wskazówki dla najlepszych rezultatów
=====================================

Dla najdokładniejszego dopasowania używaj plików TMX lub plików, w których wiersze odpowiadają sobie.

Unikaj bardzo długich akapitów w jednym wierszu. Podział zdań poprawia dokładność dopasowania.

.. |image1| image:: img/parallel/1.png
   :class: center-block
.. |image2| image:: img/parallel/3.png
   :class: center-block
.. |image3| image:: img/parallel/2.png
   :class: center-block
.. |image4| image:: img/parallel/4.png
   :class: center-block
.. |image5| image:: img/parallel/5.png
   :class: center-block
