# Zakres systemu

## Krótki opis projektu
Celem projektu jest serwis internetowy z przepisami kulinarnymi, który pozwalać będzie na wyszukanie przepisów kulinarnych na podstawie podanych przez użytkownika produktów. System udostępniać będzie możliwość porównania wyszukanych przepisów po ich cechach (na zimno czy ciepło, wartości odżywcze, czas przygotowania etc.) i z wybranych przepisów utworzyć jadłospis na podany dzień. Następnie, system generuje listę zakupów oraz pozwala wysłać tę listę na maila, SMS lub wydrukować. 

## Aktorzy systemu i ich opis

### Aktorzy podstawowi
Aktor | Opis
--- | ---
Użytkownik | Osoba korzystająca z usług udostępnianych przez serwis
Moderator | Osoba zajmująca się akceptowaniem dodawanych treści przez użytkowników
Administrator | Osoba zajmująca się administracją, konserwacją i opieką techniczną serwisu

### Aktorzy wspomagający
Aktor | Opis
--- | ---
Firma hostingowa | Udostępnianie usług hostingowych

### Aktorzy zewnętrzni
Aktor | Opis
--- | ---
Test | Test

## Tabela aktor-cel

### Aktorzy podstawowi
Aktor | Cele
--- | ---
Użytkownik | Wyszukanie przepisu 
&nbsp; |Porównanie przepisów 
&nbsp; |Tworzenie jadłospisu (forma koszyku*) 
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
### UC1: Wyszukanie przepisu - Użytkownik
Klient podchodzi do biletomatu celem zakupu biletu. Na panelu głównym klient wybiera rodzaj biletu - czas ważności biletu oraz opcjonalnie ulgę, którą może poświadczyć. W kolejnym kroku klient wybiera strefę/strefy obowiązywania biletu. System wyświetla kwotę do zapłaty. Następnie klient wybiera formę płatności i płaci określoną kwotę. Płatność jest weryfikowana. Po akceptacji następuje drukowanie biletu oraz potwierdzenia płatności.

### UC2: Porównanie przepisu - Użytkownik
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
