# Zakres systemu

## Krótki opis projektu
Celem projektu jest stworzenie serwisu internetowego **recipe-search** (nazwa robocza) zawierającego bazę przepisów kulinarnych. Główną funkcjonalnością serwisu będzie wyszukiwanie przepisów na podstawie wybranych przez Użytkownika produktów, które w teorii Użytkownik posiada. Zachowana zostanie również standardowa możliwość wyszukiwania przepisów po nazwie oraz selekcja na bazie wyboru wcześniej określonych kategorii.  
  
Z poziomu wyników wyszukiwania oraz z konkretnej strony przepisu Użytkownik będzie miał możliwość skorzystania z porównywarki przepisów. W serwisie dostępny będzie również prosty kalkulator BMI (Body Mass Index).  
  
Dla Użytkowników udostępniony zostanie system rejestracji oraz logowania. Zalogowany Użytkownik będzie mógł komentować przeglądane przepisy oraz dodawać własne (wymagana będzie weryfikacja treści przez Administratora). Użytkownik będzie miał także możliwość stworzenia własnego Jadłospisu z wcześniej dodanych do niego przepisów.

## Aktorzy systemu i ich opis

### Aktorzy podstawowi
| Aktor | Opis |
| - | - |
| Użytkownik | Osoba korzystająca z usług udostępnianych przez serwis |
| Administrator | Osoba zajmująca się utrzymaniem serwisu oraz zapewniająca jego sprawne działanie |

### Aktorzy wspomagający
| Aktor | Opis |
|-------|------|
| Firma hostingowa | Firma udostępniająca usługi hostingowe |

## Tabela aktor-cel

### Aktorzy podstawowi
| Aktor | Cele |
|-------|------|
| Użytkownik | Wyszukanie przepisu | 
| | Porównanie przepisów |
| | Tworzenie jadłospisu (forma koszyku*) |
&nbsp; | Generowanie listy zakupów (forma koszyku*) 
&nbsp; | Dodanie przepisu
Moderator | Ocena oczekujących treści 
Administrator | Administracja serwisem 
&nbsp; | Zarządzanie bezpieczeństwem serwisu 
&nbsp; | Konserwacja serwisu / naprawa usterek 

### Aktorzy wspomagający
Aktor | Cele
--- | ---
Firma hostingowa | Udostępnianie usług hostingowych

### Aktorzy zewnętrzni
Aktor | Cele
--- | ---
Test | Test

## Lista IN-OUT
Kategoria | IN | OUT
--- | --- | ---
Język systemu | Polski | Pozostałe
&nbsp; | Angielski | 
&nbsp; | Niemiecki | 
&nbsp; | Ukraiński | 

## Słownik projektowy
Pojęcie | Definicja
--- | ---
Przepis | 
Serwis | 
Wyszukiwarka | 
Porównywarka | 
Jadłospis | 
Lista zakupów | 

## Skrócone przypadki użycia (use cases)
### UC1: Wyszukiwanie przepisu na podstawie wybranych produktów - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję wyszukiwania na podstawie wybranych produktów za pomocą przycisku "Co ugotować". Korzystając z dostępnych kategorii oraz przypisanych do nich produktów Użytkownik zaznacza posiadane produkty oraz zatwierdza swój wybór przyciskiem "Szukaj". Serwis ładuje stronę z wynikami dopasowanymi do wybranych kryteriów. Użytkownik wybiera pożądany przepis lub za pomocą przycisku "Wstecz" wraca do poprzedniego ekranu i zawęża listę wcześniej wybranych produktów celem uzyskania większej ilości wyników wyszukiwania. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC2: Wyszukanie przepisu po nazwie - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu zaznacza kursorem okno wyszukiwania i wpisuje za pomocą klawiatury nazwę szukanego przepisu. Następnie zatwierdza wpisany ciąg znaków przyciskiem "Szukaj". Serwis ładuje stronę z wynikami dopasowanymi do wybranych kryteriów. Użytkownik wybiera pożądany przepis lub edytuje wpisany wcześniej ciąg znaków w oknie wyszukiwania widocznym nad zwróconą listą przepisów i ponownie zatwierdza przyciskiem "Szukaj", co skutkuje uzyskaniem nowego wyniku wyszukiwania. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC3: Wyszukanie przepisu po kategoriach - Użytkownik
Użytkownik urchamia serwis poprzez podanie poprawnego adresu URL w przeglądarce. Na stronie głównej serwisu wybiera opcję przeglądania kategorii przepisów za pomocą przycisku "Przepisy". Korzystając z dostępnych kategorii użytkownik zawęża listę przepisów do tych, które oznaczone są wybraną kategorią - robi to za pomocą zaznaczenia odpowiedniej kategorii (oraz ewentualnych podkategorii). Lista zwracanych przepisów generowana jest dynamicznie. Po wyborze przepisu Użytkownik zostaje przeniesiony do strony ze szczegółowym opisem przygotowania dania.

### UC4: Porównywanie przepisów - Użytkownik
Klient podchodzi do biletomatu celem zakupu biletu. Na panelu głównym klient wybiera rodzaj biletu - okres, na który przedłużona zostanie ważność biletu oraz opcjonalnie ulgę, którą może poświadczyć. W kolejnym kroku klient wybiera strefę/strefy obowiązywania biletu. System wyświetla kwotę do zapłaty. Następnie klient wybiera formę płatności i płaci określoną kwotę. Płatność jest weryfikowana. Po akceptacji następuje drukowanie biletu oraz potwierdzenia płatności.

### UC3: Tworzenie jadłospisu - Użytkownik
Klient podchodzi do biletomatu celem doładowania karty miejskiej. Klient umieszcza kartę miejską w wyznaczonym do tego miejscu na panelu biletomatu. Następnie na panelu głównym wybiera opcję doładowania karty miejskiej. System wyświetla aktualny stan konta klienta i pozwala na wprowadzenie kwoty, którą klient chce zasilić konto. Po zatwierdzeniu klient wybiera formę płatności i płaci określoną kwotę. Płatność jest weryfikowana. Po akceptacji system wyświetla komunikat o doładowaniu oraz drukuje potwierdzenie płatności.

### UC4: Generowanie listy zakupów - Użytkownik
Klient podchodzi do biletomatu celem sprawdzenia rozkładu jazdy. Na panelu głównym klient wybiera opcję sprawdzenia rozkładu jazdy. Następnie wybiera określoną linię autobusową lub tramwajową. Kolejnym krokiem jest wybór kierunku jazdy. Na panelu pojawia się lista poszczególnych przystanków na trasie w wybranym kierunku. Po wybraniu odpowiedniego przystanku pojawia się pełna rozpiska godzinowa przejazdów w danym punkcie.

### UC5: Dodanie przepisu - Użytkownik
...

### UC6: Ocena oczekujących treści - Moderator
...

### UC7: Administracja serwerem - Administrator
...
