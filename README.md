# mgr.cls
#### LATEXowa klasa dokumentu do składania pracy dyplomowej magisterskiej / inżynierskiej na wydziale Elektroniki Politechniki Wrocławskiej

## Instalacja
* Umieścić `mgr.cls` w katalogu, w którym znajduje się plik źródłowy tworzonej pracydyplomowej

lub

* Umieścić `mgr.cls` w jednym z katalogów, które domyślnie są przeszukiwane podczas przetwarzania, na przykład katalog `tex/latex/base/` a następnie odświeżyć strukturę plików i katalogów

## Opcje
Użycie:

    \documentclass[option0, option1, option2]{mgr}

### `8pt`, `10pt`, `11pt`
Wybór czcionki.

### `eng`
Zamienia treść napisu „PRACA DYPLOMOWA MAGISTERSKA” na napis „PROJEKT INŻYNIERSKI” oraz zamienia treść napisów przy promotorze i ocenie na stronie tytułowej.

### `oneside`
Opcja przydatna do wydruku jednostronnego, polecam w przypadku, gdypraca dyplomowa nie zawiera za dużo stron, charakteryzuje się numeracjąstron umieszczoną po prawej stronie kartki.
### `twoside` 
Opcja druku dwustronnego, charakteryzuje się numeracją stron zawsze pozewnętrznej stronie kartki, czyli naprzemiennie raz z prawej, raz z lewej. Należy używać, gdy praca dyplomowa zawiera większą liczbę stron.

### `openright`
Nowy rozdział rozpoczyna się zawsze od prawej strony, uwaga: możewystąpić pojedyncza pusta strona przed nowym rozdziałem.openanynowy rozdział rozpoczyna się od dowolnej strony.

### `leqno` 
Numerowanie formuł matematycznych po lewej stronie, raczej mało przy-datne.

### `fleqn` 
Formuły matematyczne nie będą centrowane tylko wcinane z lewej stronyo wartość parametru `\mathindent`, podobnie jak wyżej, raczej nie przydatne.

### `draft` 
Wersja robocza, oznacza linie, w których występuje **Overfull hbox** czarnym prostokątem. Ponadto, przyspiesza przetwarzanie poprzez wstawianie ramek zamiast grafiki (zależne od pakietu graficznego), przydatne podczas pracy z dużym manuskryptem.

### `final`
Finalna wersja, „przeciwieństwo” opcji `draft`.

### `openbib`
Dotyczy otoczenia `thebibligraphy`, inny sposób generowania spisu literatury.

### `printmodeta` 
Opcja jest równoważna następującej liście opcji: `[12pt,twoside,final,openright]` i jest jednocześnie opcją domyślną.

### `archivemodeta` 
Opcja jest równoważna następującej liście opcji: `[8pt,twoside,final,openany` oraz dodatkowo z dokumentu usuwana jest strona z opcjonalną dedykacją, opcja ta jest przydatna do wygenerowania kopii pracy dyplomowej, którą należy złożyć do archiwum. 

### `pl`
Wsparcie dla języka polskiego (opcja domyślna)

### `en` 
Wsparcie dla języka angielskiego.

## Polecenia

### `\author{Imię Nazwisko}`
Redefiniowane polecenie w celu przechowywania nazwiska autora, jego brak powoduje ostrzeżenie (Warning) podczas przetwarzania.

### `\title{Polski tytuł pracy}` 
Redefiniowane polecenie w celu przechowywaniapolskiego tytułu pracy magisterskiej, jego brak powoduje ostrzeżenie (Warning) podczas przetwarzania.

### `\engtitle{English title}` 
Polecenie zdefiniowane w celu przechowywania angielskiego tytułu pracy magisterskiej, jego brak powoduje ostrzeżenie (Warning)podczas przetwarzania.
### `\supervisor{tytuł, Imię Nazwisko, jednostka}` 
Polecenie zdefiniowane w celu przechowywania danych osobowych prowadzącego pracę.\

### `\guardian{tytuł, Imię Nazwisko, jednostka}` 
Polecenie zdefiniowane w celuprzechowywania danych osobowych opiekuna pracy. W przypadku gdy jest to ta sama osoba co `\supervisor`, nie należy używać tego polecenia. Jego brak usunie ze strony tytułowej zbędną informację.

### `\field{Nazwa kierunku (SKRÓT)}` 
Polecenie zdefiniowane w celu przechowywania nazwy kierunku studiów.

### `\specialisation{Nazwa specjalności (SKRÓT)}` 
Polecenie zdefiniowane w celu przechowywania nazwy specjalności studiów.

### `\date{rok}`
Redefiniowane polecenie w celu przechowywania roku. Standardowo u dołu strony tytułowej wstawiany jest bieżący rok, użycie tego poleceniapozwala wstawić dowolny rok.

### `\dedication{szer}{tekst}`
Polecenie w miejscu swojego wystąpienia łamie bie-żącą stronę i na następnej (w przypadku `openright` na następnej prawej) wstawia po prawej u dołu treść dedykacji z argumentu tekst. Argument `szer` musi mieć wartość sztywnej długości i definiuje szerokość pola tekstowego z treścią dedykacji.

## Domyślne długości marginesów
* `\topmargin -18mm` - górny margines
* `\headheight <wartość zależna od rozmiaru czcionki + 2pt>` - wysokość nagłówka
* `\headsep 3mm` - odstęp nagłówka od tekstu
* `\oddsidemargin -0.04cm`  - lewy margines strony nieparzystej
* `\evensidemargin -0.04cm` - lewy margines strony parzystej
* `\textwidth 16cm` - szerokość tekstu
* `\textheight 25cm` - wysokość tekstu
* `\footheight <nieużywane>` - wysokość stopki

Based on work of Adam Ratajczak:
http://rab.ict.pwr.wroc.pl/~ar/LaTeX/mgr.php
