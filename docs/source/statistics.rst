Statystyki korpusu
^^^^^^^^^^^^^^^

Lista frekwencyjna
==================

W tym polu wyświetlana jest lista frekwencyjna ze względu na lematy słów.
Wstępnie odfiltrowana jest do słów pełnoznacznych, jednak za pomocą przycisku
na górze można ją odfiltrować do dowolnie wybranych części mowy. Po kliknięciu
przycisku „Pobierz” zostanie pobrana pełna lista frekwencyjna bez zastosowanego
filtrowania.

Miary dyspersji i skorygowanej frekwencji
-----------------------------------------

Oprócz standardowej listy frekwencyjnej w polu „Lista frekwencyjna” wyświetlane są również miary dyspersji oraz skorygowanej frekwencji słów.

Poniższa lista przedstawia wszystkie dostępne miary. W podanych wzorach przyjęto następujące oznaczenia:

* :math:`N` - liczba tekstów w korpusie.
* :math:`N_t` - liczba tekstów, w których występuje dane słowo.
* :math:`L` – liczba słów w korpusie.
* :math:`L_i` – liczba słów w i-tym tekście korpusu.
* :math:`F` - liczba wystąpień słowa w całym korpusie.
* :math:`F_i` – liczba wystąpień słowa w i-tym tekście korpusu.
* :math:`\bar{F}` - średnia liczba wystąpień danego słowa w tekście korpusu: :math:`\bar{F} = \frac{\sum_{i=1}^{N}F_i}{N}`.
* :math:`P_i` – stosunek liczby wystąpień danego słowa do liczby wszystkich słów w i-tym tekście korpusu. 
* :math:`\bar{P}` - średnia częstość wystąpień danego słowa w tekście korpusu: :math:`\bar{P} = \frac{\sum_{i=1}^{N}P_i}{N}`.
* :math:`S_i` – stosunek liczby słów w i-tym tekście korpusu do liczby słów we wszystkich tekstach korpusu: :math:`S_i = \frac{L_i}{L}`


Miary dyspersji i skorygowanej frekwencji:

* Frekwencja – liczba wystąpień danego słowa w korpusie.

  .. math::
    F
* *IDF* – miara ilości informacji wiążącej się z użyciem danego słowa. Przyjmuje wartość 0, jeśli słowo występuje we wszystkich tekstach korpusu, i wartości tym większe im mniejsza jest liczba tekstów, w których występuje słowo.

  .. math::
    \\log_2\frac{N}{N_t}
* Współczynnik zmienności (*vc*).

  .. math::
    \sigma_F = \sqrt{\frac{\sum_{i=1}^N(F_i - \bar{F})^2}{N}}

  .. math::
    vc = \frac{\sigma_F}{\bar{F}}

* *D* i *U* Juillanda – miara dyspersji (*D*) i skorygowanej frekwencji (*U*). Miary obliczane są przy pomocy skorygowanej formuły, która uwzględnia różne objętości tekstów należących do korpusu. *D* przyjmuje wartości z przedziału :math:`[0, 1]`, natomiast *U* – z przedziału :math:`[0, F]`.

  .. math::
    \sigma_P = \sqrt{\frac{\sum_{i=1}^N(P_i - \bar{P})^2}{N}}

  .. math::
    D_{adj} = 1 - \frac{\sigma_P}{\bar{P}\sqrt{N - 1}}

  .. math::
    U = D_{adj} \cdot F
    
  *Uwaga: odchylenie standardowe wykorzystane do obliczania D i U Juillanda obliczane jest przy pomocy innej formuły, niż w przypadku współczynnika zmienności.*

* *DP* Griesa (odwrotne *DP*, standaryzowane *DP*) – miary dyspersji. Oprócz standardowej miary *DP* obliczane są wartości odwrotnego *DP* (:math:`DP_{rev}`), które łatwiej można porównać z wartościami innych metryk dyspersji, a także standarydowanego *DP* (:math:`DP_{norm}`), wartości którego można porównać z korpusami składającymi się z innej liczby tekstów. Wyższe wartości *DP* i standaryzowanego *DP* (lub niższe wartości odwróconego *DP*)  reprezentują bardziej nierównomierne występowanie słowa w korpusie. *DP* przyjmuje wartości z przedziału :math:`[0, 1-min\left\{S_i \right\}_{i=1}^N]`, standaryzowane *DP* – z przedziału :math:`[0, 1]`, a odwrotne *DP* – z przedziału :math:`[min \left\{S_i \right\}_{i=1}^N, 1]`.

  .. math::
    DP = \frac{\sum_{i=1}^{N}|\frac{F_i}{F}-S_i|}{2}
   
  .. math::
    DP_{rev} = 1 - DP 

  .. math::
    DP_{norm} = \frac{DP}{1 - \frac{1}{N}}

* *D2* i *Um* Carolla – miara dyspersji (*D2*) i skorygowanej frekwencji (*Um*). Miara *D2* przyjmuje wartości z przedziału :math:`[0, 1]`, przy czym wyższe wartości *D2* świadczą o bardziej równomiernej dystrybuji słowa w korpusie. *Um* przyjmuje wartości z przedziału :math:`[\frac{F}{N}, F]`.

  .. math::
    D_2 = \frac{- \sum_{i=1}^{N} \left( \frac{P_i}{\sum_{i=1}^{N} P_i} \cdot \log_2\frac{P_i}{\sum_{i=1}^{N}P_i} \right)}{\log_2{N}}

  .. math::
    U_m = F \cdot D_2 + (1 - D_2) \cdot \frac{F}{N}
* Rozbieżność KL (*KLD*) – niesymetryczna miara różnic w rozkładach prawdopodonieństwa, używana jako miara dyspersji. Przy obliczaniu wartości tej metryki przyjmuje się, że :math:`\\log_2 0 = 0`. Miara przyjmuje nieujemne wartości – tym wyższe, im mniej równomiernie dane słowo występuje w korpusie. 
  
  .. math::
    KLD = \sum_{i=1}^N \Bigg( \frac{F_i}{F} \cdot \log_2 \left( \frac{F_i}{F} \cdot \frac{1}{S_i} \right) \Bigg)
* *S* i *AF* Roesengrena – miara dyspersji (*S*) oraz frekwencji (*AF*). Miary obliczane są przy pomocy skorygowanej formuły, która uwzględnia różnie objętości tekstów należących do korpusu. *S* przyjmuje wartości z przedziału :math:`[\frac{1}{N}, 1]`, przy czym wyższe wartości odzwierciedlają bardziej równomierną dystrybuję słowa. AF przyjmuje natomiast wartości z przedziału :math:`[\frac{F}{N}, F]`.

  .. math::
    S_{adj} = \frac{1}{F} \left( \sum_{i=1}^N \sqrt{F_i \cdot S_i} \right)^2
  .. math::
    AF = F \cdot S_{adj}

* *ARF* – miara zmodyfikowanej frekwencji oparta o odległości pomiędzy wystąpieniami danego słowa. W poniższym wzorze zmienna :math:`d_j` oznacza dystans między j-tym i j+1-szym wystąpienie słowa (a dla :math:`j = F` – odległość pomiędzy pierwszym i ostatnim wystąpieniem słowa zakładając, że pierwsze i ostatnie słowo korpusu sąsiadują ze sobą). Miara przyjmuje wartości z przedziału :math:`[1, F]`, tym wyższe, im bardziej równomierna jest dystrybuja słowa w korpusie.

  .. math::
    ARF = \frac{F}{L} \sum_{i=1}^F min \left\{ d_i, \frac{L}{F} \right\}


Dla korpusów składających się tylko z jednego tekstu obliczane są jedynie frekwencja oraz ARF.

Dostępne miary zostały opisane w artykule „Dispersions and adjusted frequencies
in corpora” (Gries, 2008) oraz rozdziale 5. podręcznika „A Practical Handbook of Corpus Linguistics” (Gries, 2021).

Słownictwo charakterystyczne
============================

Słownictwo charakterystyczne generowane jest przez aplikację TermoPL. Opis jej działania, instrukcja i dodatkowe informacje dostępne `tutaj <https://clarin-pl.eu/dspace/bitstream/handle/11321/266/TermoPL.pdf?sequence=6&isAllowed=y>`__.

W zakładce Terminologii informacje ograniczone są do formy bazowej, wartości C-value oraz liczby wystąpień, posortowane wg C-value. Po kliknięciu przycisku „Pobierz” pobrany zostaje plik txt zawierający wszystkie dane wygenerowane przez TermoPL.

Pliki wygenerowane przez Korpusomat są kompatybilne z aplikacją TermoPL – po pobraniu „plików źródłowych korpusu” (przycisk dostępny na ekranie korpusu) można samodzielnie uruchomić aplikację TermoPL z wybranymi przez siebie opcjami.

..
    Wykres wg metadanych
    ====================

    W tym polu wyświetlany jest wykres przedstawiający podział segmentów w korpusie ze względu na wybraną metadaną, wybraną przez użytkownika.

    Kolokacje
    =========

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
    ==============

    Słowa kluczowe obliczone są na podstawie porównania listy frekwencyjnej korpusu z listą frekwencyjną korpusu referencyjnego. Korpusem referencyjnym w tym przypadku jest milionowy korpus NKJP.

    Rozkład słów kluczowych
    =======================

    Wizualizacja przedstawia występowanie słów kluczowych korpusu w ramach każdego dokumentu tekstowego. Położenie i wielkość są oparte na sumach wystąpień poszczególnych słów kluczowych w kolejnych zdaniach dokumentu. Regulacja zagęszczenia pozwala na sumowanie wystąpień słów z kilku zdań do jednego punktu na wizualizacji, domyślnie ustawiona wartość zagęszczenia ma na celu zwiększenie czytelności wizualizacji.
