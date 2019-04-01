# Zakres systemu

## Krótki opis projektu
Celem projektu jest stworzenie serwisu internetowego **recipe-search** (nazwa robocza) zawierającego bazę przepisów kulinarnych. Główną funkcjonalnością serwisu będzie wyszukiwanie przepisów na podstawie wybranych przez Użytkownika produktów, które w teorii Użytkownik posiada. Zachowana zostanie również standardowa możliwość wyszukiwania przepisów po nazwie oraz selekcja na bazie wyboru wcześniej określonych kategorii.  
  
Z poziomu strony ze szczegółowym opisem przygotowania dania Użytkownik będzie miał możliwość skorzystania z porównywarki przepisów. W serwisie dostępny będzie również prosty kalkulator BMI (Body Mass Index).  
  
Dla Użytkowników udostępniony zostanie system rejestracji oraz logowania. Zalogowany Użytkownik będzie mógł komentować przeglądane przepisy oraz dodawać własne (wymagana będzie weryfikacja treści przez Administratora). Użytkownik będzie miał także możliwość stworzenia własnego Jadłospisu z wcześniej dodanych do niego przepisów.

## Aktorzy systemu i ich opis

### Aktorzy podstawowi
| Aktor | Opis |
| - | - |
| Użytkownik | Osoba w przedziale wiekowym 10-80 lat, korzystająca z usług udostępnianych przez serwis w celu poszerzenia swojej kulinarnej wiedzy |
| Administrator | Przeszkolona w obsłudze serwisu osoba zajmująca się utrzymaniem serwisu oraz zapewniająca jego sprawne działanie |

### Aktorzy wspomagający
| Aktor | Cele |
| - | - |
| Serwisy kulinarne | Serwisy internetowe o tematyce kulinarnej |

### Aktorzy zewnętrzni
| Aktor | Opis |
| - | - |
| Firma hostingowa | Profesjonalna firma świadcząca usługi hostingowe |

## Tabela aktor-cel

### Aktorzy podstawowi
| Aktor | Cele |
| - | - |
| Użytkownik | Wyszukiwanie przepisu na podstawie wybranych produktów | 
| | Wyszukiwanie przepisu po nazwie |
| | Wyszukiwanie przepisu po kategoriach |
| | Porównywanie przepisów |
| | Obliczanie wartości BMI |
| | Dodawanie przepisu |
| | Komentowanie przepisu |
| | Tworzenie jadłospisu |
| Administrator | Administracja/konserwacja serwisu, naprawa usterek |
|| Zarządzanie bezpieczeństem serwisu ||
|| Ocena oczekujących treści ||

### Aktorzy wspomagający
| Aktor | Cele |
| - | - |
| Serwisy kulinarne | Udostępnianie przepisów kulinarnych do bazy danych naszego serwisu |

### Aktorzy zewnętrzni
| Aktor | Cele |
| - | - |
| Firma hostingowa | Udostępnianie usług hostingowych |

## Lista IN-OUT
| Kategoria | IN | OUT |
| - | - | - |
| Typ aplikacji | Webowa | Mobilna |
| Język systemu | Polski | Pozostałe |
| Baza danych | Dynamiczna (możliwość dodawania danych do bazy) | Statyczna (brak możliwości dodawania danych do bazy) |
| Wyszukiwanie | Na podstawie produktów | Pozostałe |
| | Po nazwie przepisu | |
| | Po kategoriach | |
| Porównywarka | 2 przepisy | Więcej niż 2 przepisy |
| Kalkulator | BMI | BMR |
| Jadłospis | Do 6 posiłków | Więcej niż 6 posiłków |
| Komentarze i oceny | Użytkownik zalogowany | Użytkownik niezalogowany |

## Słownik projektowy
| Pojęcie | Definicja |
| - | - |
| BMI | Body Mass Index, czyli Wskaźnik Masy Ciała. Jest to współczynnik powstały przez podzielenie masy ciała podanej w kilogramach przez kwadrat wysokości podanej w metrach |
| Danie | Potrawa, posiłek, powstały w wyniku przygotowania przy pomocy przepisu |
| Jadłospis | Lista posiłków na dany dzień |
| Kalkulator BMI | Narzędzie pozwalające na obliczenie wskaźnika BMI swojego ciała na podstawie wpisanych wartości: wzrostu oraz wagi |
| Kategoria | Uporządkowany, nazwany zbiór zebranych zasobów odpowiadających konkretnym parametrom |
| Konto Użytkownika | Miejsce Użytkownia w Serwisie pozwalające na gromadzenie i optymalizowanie treści umieszczanych w Serwisie do własnych preferencji | 
| Lista zakupów | Uporządkowana lista produktów, które należy zakupić w celu przygotowania dania |
| Logowanie do serwisu | Czynność, którą musi wykonać Użytkownik, aby otrzymać pełne prawa do korzystania ze wszystkich funkcjonalności Serwisu | 
| Porównywarka | Narzędzie pozwalające na porównanie ze sobą dwóch przepisów |
| Produkt | Wszystko, co jest przeznaczone do spożycia lub przygotowania potraw |
| Przepis | Uporządkowana lista czynności oraz potrzebnych składników pozwalająca na przygotowanie posiłku |
| Serwis | Grupa powiązanych ze sobą interaktywnych stron internetowych o spójnej tematyce (kulinarnej) |
| Rejestracja w serwisie | Inaczej założenie Konta Użytkownika, które przechowuje podane w formularzu rejestracyjnym dane oraz preferencje Użytkownika określone w trakcie korzystania z Serwisu |
| Strona główna serwisu | Startowa strona internetowa pełniąca funkcję reprezentacyjną serwisu. Znajdują się na niej odniesienia do wszystkich funkcjonalności serwisu |
| Wyszukiwarka | Narzędzie pozwalające na przeszukiwanie serwisu pod kątem oczekiwanej treści |

## Skrócone przypadki użycia (Use Cases)
### UC1: Wyszukiwanie przepisu na podstawie wybranych produktów - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję wyszukiwania na podstawie wybranych produktów za pomocą przycisku "Co ugotować". Korzystając z dostępnych kategorii oraz przypisanych do nich produktów Użytkownik zaznacza posiadane produkty oraz zatwierdza swój wybór przyciskiem "Szukaj". Serwis ładuje stronę z wynikami dopasowanymi do wybranych kryteriów. Użytkownik wybiera pożądany przepis lub za pomocą przycisku "Wstecz" wraca do poprzedniego ekranu i zawęża listę wcześniej wybranych produktów celem uzyskania większej ilości wyników wyszukiwania. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC2: Wyszukiwanie przepisu po nazwie - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu zaznacza kursorem okno wyszukiwania i wpisuje za pomocą klawiatury nazwę szukanego przepisu. Następnie zatwierdza wpisany ciąg znaków przyciskiem "Szukaj". Serwis ładuje stronę z wynikami dopasowanymi do wybranych kryteriów. Użytkownik wybiera pożądany przepis lub edytuje wpisany wcześniej ciąg znaków w oknie wyszukiwania widocznym nad zwróconą listą przepisów i ponownie zatwierdza przyciskiem "Szukaj", co skutkuje uzyskaniem nowego wyniku wyszukiwania. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC3: Wyszukiwanie przepisu po kategoriach - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję przeglądania kategorii przepisów za pomocą przycisku "Przepisy". Korzystając z dostępnych kategorii użytkownik zawęża listę przepisów do tych, które oznaczone są wybraną kategorią - robi to za pomocą zaznaczenia odpowiedniej kategorii (oraz ewentualnych podkategorii). Lista zwracanych przepisów generowana jest dynamicznie. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC4: Porównywanie przepisów - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Korzystając z jednej z trzech możliwości wyszukiwania przepisów (UC1/UC2/UC3) użytkownik przechodzi na stronę szczegółowego opisu przygotowania dania. Wybierając przycisk "Dodaj do porównania" użytkownik dodaje przepis do Porównywarki. Następnie Użytkownik może wrócić do wyników wyszukiwania za pomocą przycisku "Wstecz" lub wrócić do strony głównej serwisu i ponownie skorzystać z jednej z trzech możliwości wyszukiwania przepisów (UC1/UC2/UC3) celem znalezienia drugiego pożądanego przepisu. Po przejściu na stronę z jego dokładnym opisem Użytkownik ponownie wybiera przycisk "Dodaj do porównania" i otrzymuje komunikat z odnośnikiem. Klikając w link Użytkownik zostaje przeniesiony do strony z wynikiem porównania przepisów.

### UC5: Obliczanie wartości BMI - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję obliczania wartości BMI za pomocą przycisku "Kalkulator BMI". Użytkownik zostaje przeniesiony na stronę z prostym Kalkulatorem BMI. Użytkownik podaje swoją płeć, wagę oraz wzrost i zatwierdza te dane za pomocą przycisku "Oblicz". Następnie zostaje przeniesiony na stronę z wynikami zwróconymi przez algorytm obliczający wartość BMI oraz z sugerowanymi działaniami, o ile jakiekolwiek są rekomendowane.

### UC8: Dodawanie przepisu - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Z poziomu strony głównej oraz każdej innej podstrony może wybrać opcję "Dodaj przepis". Po wybraniu tej opcji, jeśli Użytkownik jest zalogowany, zostaje przeniesiony do strony dodawania przepisu. Jeśli Użytkownik jest niezalogowany, zostaje przeniesiony do strony logowania. Jeśli Użytkownik nie posiada konta w serwisie, z poziomu strony logowania może wybrać opcję "Rejestracja" po czym zostanie przeniesiony do formularza rejestracji. Po zalogowaniu lub rejestracji Użytkownik zostaje przeniesiony do pożądanej strony dodawania przepisu. Użytkownik wypełnia widoczny formularz dodawania przepisu i zatwierdza wprowadzone dane przyciskiem "Dodaj". Przepis zostaje zapisany w kolejce oczekujących na akceptację i oczekuje na zweryfikowanie przez Administratora.

### UC9: Komentowanie przepisu - Użytkownik
Użytkownik uruchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Korzystając z jednej z trzech możliwości wyszukiwania przepisów (UC1/UC2/UC3) użytkownik przechodzi na stronę szczegółowego opisu przygotowania dania. Pod przepisem znajduje się sekcja komentarzy Użytkowników. Niezalogowany Użytkownik widzi komentarze innych Użytkowników oraz przycisk "Zaloguj, aby dodać opinię". Zalogowany Użytkownik widzi komentarze innych Użytkowników oraz pole do wprowadzenia własnego komentarza i przycisk "Wyślij" do zatwierdzenia go. Po wprowadzeniu komentarza i zatwierdzeniu go strona z przepisem przeładowuje się i Użytkownik może zobaczyć swój komentarz na szczycie listy komentarzy.

### UC10: Tworzenie jadłospisu - Użytkownik

### UC11: Administracja/konserwacja serwisu, naprawa usterek - Administrator

### UC12: Zarządzanie bezpieczeństwem serwisu - Administrator

### UC14: Ocena oczekujących treści - Administrator

## Krótkie historyjki użytkownika (User Stories)

##### US1: Jako Użytkownik chcę wyszukiwać w serwisie przepisy na podstawie nazw posiadanych przeze mnie produktów.
##### US2: Jako Użytkownik chcę wyszukiwać w serwisie przepisy na podstawie nazwy dania.
##### US3: Jako Użytkownik chcę wyszukiwać w serwisie przepisy w oparciu o kategorie dań (śniadanie, obiad, kolacja, itp.)
##### US4: Jako Użytkownik chcę porównywać w serwisie przepisy na podstawie wybranych przeze mnie kryteriów.
##### US5: Jako Użytkownik chcę mieć możliwość obliczać w serwisie wartość BMI mojego ciała.
##### US6: Jako Użytkownik chcę mieć możliwość zarejestrowania swojego konta w serwisie.
##### US7: Jako Użytkownik chcę mieć możliwość zalogowania się do mojego konta w serwisie.
##### US8: Jako Użytkownik chcę dodawać przepisy w serwisie.
##### US9: Jako Użytkownik chcę komentować i oceniać przepisy dostępne w serwisie.
##### US10: Jako Użytkownik chcę móc stworzyć jadłospis na cały dzień z wybranych przeze mnie przepisów.
##### US11: Jako Użytkownik chcę otrzymać stworzony przeze mnie jadłospis na adres e-mail.
##### US12: Jako Administrator chcę mieć możliwość konserwacji, naprawiania usterek oraz utrzymywania prawidłowego działania serwisu.
##### US13: Jako Administrator chcę mieć możliwość zarządzania bezpieczeństwem serwisu.
##### US14: Jako Administrator chcę mieć możliwość oceniania wartości oczekujących na akceptację treści.

## Harmonogram prac nad serwisem z podziałem na semestry

| Semestr | Zadanie do wykonania |
| - | - |
| VI | |
| | Zakres systemu |
| | Business Model Canvas |
| | Zarys architektury systemu |
| | Konfiguracja repozytorium Github |
| | Prototyp systemu |
| | Wdrożenie oprogramowania do śledzenia stanu projektu (JIRA) |
| | Dostosowanie bazy danych do naszych potrzeb |
| | Projekt wizualny strony |
| | Prace nad Front Endem |
| | Dopracowana wyszukiwarka |
| | Refaktoryzacja kodu |
| | Przygotowanie prezentacji na obornę |
| VII | |
| | Dopracowanie Front Endu - poprawienie funkcjonalności, dopracowanie elementów graficznych, itp. |
| | Dołożenie pozostałych funkcjonalności serwisu, m.in.: porównywarka, jadłospisy, lista zakupów, dodawanie przepisów |
| | Możliwość wysyłania listy zakupów, jadłospisów na maila |
| | Panel administracyjny |
| | Rejestracja i logowanie |
| | Komentarze i oceny |
| | Kalkulatory |
| | Refaktoryzacja kodu |
| | Przygotowanie prezentacji na obronę |
