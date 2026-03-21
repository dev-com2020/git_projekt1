Dokumentacja repozytorium
========================

Cel repozytorium
----------------

To repozytorium zawiera kilka prostych, niezaleznych plikow skryptowych i tekstowych.
W obecnym stanie nie tworza one jednej aplikacji ani wspolnego workflow uruchomieniowego.

Zawartosc kodu
--------------

### Skrypty Python

- `witaj_katarzyna.py`
  - wypisuje na standardowe wyjscie: `Witaj!`

- `witaj_maciej.py`
  - wypisuje: `Hejka`
  - nastepnie wykonuje petle `for i in range(5)` i drukuje:
    - `wirus nr 0`
    - `wirus nr 1`
    - `wirus nr 2`
    - `wirus nr 3`
    - `wirus nr 4`

- `witaj_tomek.py`
  - wypisuje:
    - `witaj! $#$#`
    - `test nr 11`

### Skrypt PowerShell

- `PP_test.ps1`
  - zawiera polecenie `Get-NetAdapter`
  - druga linia to `hh`
  - z samego repozytorium nie wynika jednoznacznie, jaki jest zamierzony cel drugiej komendy, dlatego nie nalezy zakladac dodatkowego zachowania bez sprawdzenia w srodowisku uruchomieniowym

### Plik JavaScript

- `Marcin.js`
  - zawiera pojedyncza linie `Zmianas;`
  - plik nie dokumentuje zadnego stabilnego interfejsu ani modulu i nie ma tu dodatkowego kontekstu wyjasniajacego jego role

Uruchamianie
------------

### Python

Kazdy skrypt Python mozna uruchomic osobno:

```bash
python3 witaj_katarzyna.py
python3 witaj_maciej.py
python3 witaj_tomek.py
```

Skrypty nie przyjmuja argumentow i nie eksportuja funkcji lub klas.
Ich dzialanie polega wylacznie na wypisaniu tekstu.

### PowerShell

Skrypt `PP_test.ps1` jest przeznaczony dla srodowiska PowerShell:

```powershell
./PP_test.ps1
```

Przed uruchomieniem nalezy uwzglednic:

- `Get-NetAdapter` jest komenda zwiazana z systemem Windows / PowerShell
- zachowanie drugiej linii (`hh`) nie jest opisane w repozytorium
- repozytorium nie zawiera runbooka z wymaganiami uprawnien lub oczekiwanym wynikiem

Ograniczenia i uwagi
--------------------

- Brak katalogu `docs/` oraz bardziej rozbudowanego README w formacie Markdown.
- Brak wspolnego punktu startowego, testow i procesu budowania.
- Brak publicznego API: w kodzie nie ma funkcji, klas ani opisanych kontraktow wejscia/wyjscia.

Zasady ignorowania plikow
-------------------------

Plik `.gitignore` ignoruje:

- `pass.py`
- wszystkie pliki `*.log`
- katalog `config/`
- katalog `node_modules/`

Wyjatek:

- `important.log` nie jest ignorowany, mimo wzorca `*.log`

Kiedy aktualizowac te informacje
--------------------------------

Ten plik warto zaktualizowac przy kazdej zmianie, ktora:

- dodaje nowy skrypt uruchamialny
- zmienia wypisywane komunikaty lub wejscia skryptow
- wprowadza wymagania srodowiskowe
- dodaje rzeczywisty workflow uruchomienia lub utrzymania