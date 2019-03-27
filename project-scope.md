# Zakres systemu

## Krótki opis projektu
Celem projektu jest stworzenie serwisu internetowego **recipe-search** (nazwa robocza) zawierającego bazę przepisów kulinarnych. Główną funkcjonalnością serwisu będzie wyszukiwanie przepisów na podstawie wybranych przez Użytkownika produktów, które w teorii Użytkownik posiada. Zachowana zostanie również standardowa możliwość wyszukiwania przepisów po nazwie oraz selekcja na bazie wyboru wcześniej określonych kategorii.  
  
Z poziomu strony ze szczegółowym opisem przygotowania dania Użytkownik będzie miał możliwość skorzystania z porównywarki przepisów. W serwisie dostępny będzie również prosty kalkulator BMI (Body Mass Index).  
  
Dla Użytkowników udostępniony zostanie system rejestracji oraz logowania. Zalogowany Użytkownik będzie mógł komentować przeglądane przepisy oraz dodawać własne (wymagana będzie weryfikacja treści przez Administratora). Użytkownik będzie miał także możliwość stworzenia własnego Jadłospisu z wcześniej dodanych do niego przepisów.

## Aktorzy systemu i ich opis

### Aktorzy podstawowi
| Aktor | Opis |
| - | - |
| Użytkownik | Osoba korzystająca z usług udostępnianych przez serwis |
| Administrator | Osoba zajmująca się utrzymaniem serwisu oraz zapewniająca jego sprawne działanie |

### Aktorzy wspomagający
| Aktor | Opis |
| - | - |
| Firma hostingowa | Firma udostępniająca usługi hostingowe |

## Tabela aktor-cel

### Aktorzy podstawowi
| Aktor | Cele |
| - | - |
| Użytkownik | Wyszukiwanie przepisu na podstawie wybranych produktów | 
| | Wyszukiwanie przepisu po nazwie |
| | Wyszukiwanie przepisu po kategoriach |
| | Porównywanie przepisów |
| | Obliczanie wartości BMI |
| | Rejestracja w serwisie |
| | Logowanie do serwisu |
| | Dodawanie przepisu |
| | Komentowanie przepisu |
| | Tworzenie jadłospisu |
| Administrator | Administracja serwisem |
|| Zarządzanie bezpieczeństem serwisu ||
|| Konserwacja serwisu / naprawa usterek ||
|| Ocena oczekujących treści ||

### Aktorzy wspomagający
| Aktor | Cele |
| - | - |
| Firma hostingowa | Udostępnianie usług hostingowych |

## Lista IN-OUT
| Kategoria | IN | OUT |
| - | - | - |
| Język systemu | Polski | Pozostałe |
| | Angielski | |
| | Niemiecki | |
| | Ukraiński | |

## Słownik projektowy
| Pojęcie | Definicja |
| - | - |
| Przepis | |
| Serwis | |
| Wyszukiwarka | |
| Porównywarka | |
| Jadłospis | |
| Lista zakupów | |

## Skrócone przypadki użycia (use cases)
### UC1: Wyszukiwanie przepisu na podstawie wybranych produktów - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję wyszukiwania na podstawie wybranych produktów za pomocą przycisku "Co ugotować". Korzystając z dostępnych kategorii oraz przypisanych do nich produktów Użytkownik zaznacza posiadane produkty oraz zatwierdza swój wybór przyciskiem "Szukaj". Serwis ładuje stronę z wynikami dopasowanymi do wybranych kryteriów. Użytkownik wybiera pożądany przepis lub za pomocą przycisku "Wstecz" wraca do poprzedniego ekranu i zawęża listę wcześniej wybranych produktów celem uzyskania większej ilości wyników wyszukiwania. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC2: Wyszukiwanie przepisu po nazwie - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu zaznacza kursorem okno wyszukiwania i wpisuje za pomocą klawiatury nazwę szukanego przepisu. Następnie zatwierdza wpisany ciąg znaków przyciskiem "Szukaj". Serwis ładuje stronę z wynikami dopasowanymi do wybranych kryteriów. Użytkownik wybiera pożądany przepis lub edytuje wpisany wcześniej ciąg znaków w oknie wyszukiwania widocznym nad zwróconą listą przepisów i ponownie zatwierdza przyciskiem "Szukaj", co skutkuje uzyskaniem nowego wyniku wyszukiwania. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC3: Wyszukiwanie przepisu po kategoriach - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję przeglądania kategorii przepisów za pomocą przycisku "Przepisy". Korzystając z dostępnych kategorii użytkownik zawęża listę przepisów do tych, które oznaczone są wybraną kategorią - robi to za pomocą zaznaczenia odpowiedniej kategorii (oraz ewentualnych podkategorii). Lista zwracanych przepisów generowana jest dynamicznie. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC4: Porównywanie przepisów - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Korzystając z jednej z trzech możliwości wyszukiwania przepisów (UC1/UC2/UC3) użytkownik przechodzi na stronę szczegółowego opisu przygotowania dania. Wybierając przycisk "Dodaj do porównania" użytkownik dodaje przepis do Porównywarki. Następnie Użytkownik może wrócić do wyników wyszukiwania za pomocą przycisku "Wstecz" lub wrócić do strony głównej serwisu i ponownie skorzystać z jednej z trzech możliwości wyszukiwania przepisów (UC1/UC2/UC3) celem znalezienia drugiego pożądanego przepisu. Po przejściu na stronę z jego dokładnym opisem Użytkownik ponownie wybiera przycisk "Dodaj do porównania" i otrzymuje komunikat z odnośnikiem. Klikając w link Użytkownik zostaje przeniesiony do strony z wynikiem porównania przepisów.

### UC5: Obliczanie wartości BMI - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję obliczania wartości BMI za pomocą przycisku "Kalkulator BMI". Użytkownik zostaje przeniesiony na stronę z prostym Kalkulatorem BMI. Użytkownik podaje swoją płeć, wagę oraz wzrost i zatwierdza te dane za pomocą przycisku "Oblicz". Następnie zostaje przeniesiony na stronę z wynikami zwróconymi przez algorytm obliczający wartość BMI oraz z sugerowanymi działaniami, o ile jakiekolwiek są rekomendowane.

### UC6: Rejestracja w serwisie - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Z poziomu strony głównej oraz każdej innej podstrony może wybrać opcję "Rejestracja". Po wybraniu tej opcji zostaje przeniesiony do ekranu z formularzem rejestracyjnym, który musi uzupełnić uwzględniając wymagane pola (imię, adres email, hasło, potwierdzenie hasła, checkbox potwierdzający akceptację warunków użytkowania serwisu). Użytkownik zatwierdza podane dane za pomocą przycisku "Zarejestruj". Po rejestracji Użytkownik jest automatycznie zalogowany i przeniesiony do strony głównej serwisu. Zalogowany Użytkownik może korzystać z pełnej funkcjonalności serwisu lub też wylogować się z niego za pomocą przycisku "Wyloguj" dostępnego z poziomu strony głównej oraz każdej innej podstrony.

### UC7: Logowanie do serwisu - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Z poziomu strony głównej oraz każdej innej podstrony może wybrać opcję "Logowanie". Po wybraniu tej opcji zostaje przeniesiony do ekranu z formularzem logowania, który musi uzupełnić uwzględniając wymagane pola (adres email, hasło). Użytkownik zatwierdza podane dane za pomocą przycisku "Zaloguj". Po zalogowaniu Użytkownik jest automatycznie przeniesiony do strony głównej serwisu. Zalogowany Użytkownik może korzystać z pełnej funkcjonalności serwisu lub też wylogować się z niego za pomocą przycisku "Wyloguj" dostępnego z poziomu strony głównej oraz każdej innej podstrony.

### UC8: Dodawanie przepisu - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Z poziomu strony głównej oraz każdej innej podstrony może wybrać opcję "Dodaj przepis". Po wybraniu tej opcji, jeśli Użytkownik jest zalogowany, zostaje przeniesiony do strony dodawania przepisu. Jeśli Użytkownik jest niezalogowany, zostaje przeniesiony do strony logowania. Jeśli Użytkownik nie posiada konta w serwisie, z poziomu strony logowania może wybrać opcję "Rejestracja" po czym zostanie przeniesiony do formularza rejestracji. Po zalogowaniu lub rejestracji Użytkownik zostaje przeniesiony do pożądanej strony dodawania przepisu. Użytkownik wypełnia widoczny formularz dodawania przepisu i zatwierdza wprowadzone dane przyciskiem "Dodaj". Przepis zostaje zapisany w kolejce oczekujących na akceptację i oczekuje na zweryfikowanie przez Administratora.

### UC9: Komentowanie przepisu - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Korzystając z jednej z trzech możliwości wyszukiwania przepisów (UC1/UC2/UC3) użytkownik przechodzi na stronę szczegółowego opisu przygotowania dania. Pod przepisem znajduje się sekcja komentarzy Użytkowników. Niezalogowany Użytkownik widzi komentarze innych Użytkowników oraz przycisk "Zaloguj, aby dodać opinię". Zalogowany Użytkownik widzi komentarze innych Użytkowników oraz pole do wprowadzenia własnego komentarza i przycisk "Wyślij" do zatwierdzenia go. Po wprowadzeniu komentarza i zatwierdzeniu go strona z przepisem przeładowuje się i Użytkownik może zobaczyć swój komentarz na szczycie listy komentarzy.

### UC10: Tworzenie jadłospisu

### UC11: Ocena oczekujących treści - Administrator
