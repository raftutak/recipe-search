# Zakres systemu

## Krótki opis projektu
Celem projektu jest stworzenie oprogramowania do obsługi biletomatu sprzedającego bilety komunikacji miejskiej, w wersji elektronicznej jak i tradycyjnej. System pozwalać będzie na dostęp do aktualnego rozkładu jazdy tramwajów oraz autobusów oraz do regulaminu korzystania z usług przewoźnika. Oprogramowanie obsługiwać będzie dwie formy płatności – gotówka (banknoty i bilon) oraz forma elektroniczna (karty płatnicze). System udostępniać będzie również opcję wezwania obsługi serwisowej oraz poinformowania o brakach zasobów (papier, toner, monety, banknoty) z poziomu interfejsu użytkownika.

## Aktorzy systemu i ich opis

### Aktorzy podstawowi
Aktor | Opis
--- | ---
Klient | Osoba korzystająca z usług udostępnianych przez biletomat
Serwisant ZTM | Osoba zajmująca się konserwacją i naprawą biletomatu oraz uzupełnianiem zasobów

### Aktorzy wspomagający
Aktor | Opis
--- | ---
System obsługi płatności elektronicznych | System autoryzacji płatności kartą
Bank | Instytucja weryfikująca i księgująca przyjmowane płatności

### Aktorzy zewnętrzni
Aktor | Opis
--- | ---
Zarząd Transportu Miejskiego (ZTM) | Jednostka organizująca, zarządzająca i nadzorująca transport miejski, właściciel biletomatu
Urząd Skarbowy | Podmiot odpowiedzialny za kwestie podatkowe

## Tabela aktor-cel

### Aktorzy podstawowi
Aktor | Cele
--- | ---
Klient | Zakup biletu jednorazowego
 | Zakup biletu okresowego
 | Doładowanie karty miejskiej
 | Sprawdzenie rozkładu jazdy
 | Sprawdzenie regulaminu korzystania z usług przewoźnika
 | Wezwanie serwisu
Serwisant ZTM | Naprawa usterki
 | Uzupełnienie zasobów
 | Zarządzanie i aktualizacja systemu

### Aktorzy wspomagający
Aktor | Cele
--- | ---
System obsługi płatności elektronicznych | Autoryzacja płatności kartą
 | Komunikacja z API banku w celu weryfikacji płatności
Bank | Weryfikacja płatności
 | Księgowanie płatności

### Aktorzy zewnętrzni
Aktor | Cele
--- | ---
Zarząd Transportu Miejskiego (ZTM) | Dystrybucja usług za pośrednictwem biletomatu
 | Udostępnianie usług serwisanta
 | Polityka bezpieczeństwa
 | Udostępnienie rozkładu jazdy
 | Udostępnienie regulaminu korzystania z usług przewoźnika
 | Udostępnianie regulaminu korzystania z biletomatu
Urząd Skarbowy | Kwestie rozliczeniowe oraz podatkowe

## Lista IN-OUT

Kategoria | IN | OUT
--- | --- | ---
Język systemu | Polski | Pozostałe
 | Angielski |
 | Niemiecki | 
 | Ukraiński | 
Formy płatności | Banknoty | Płatności mobilne
 | Bilon | 
 | Karta płatnicza | 
Ulgi | Dla niepełnosprawnych | 
 | Uczniowska |
 | Studencka |
 | Doktorancka |
 | Seniorska |

## Słownik projektowy
Pojęcie | Definicja
--- | ---
Bank | Instytucja weryfikująca i księgująca przyjmowane płatności
Bilet jednorazowy | Dokument jednorazowego użytku upoważniający do przejazdu komunikacją miejską w określonym czasie
Bilet elektroniczny | Cyfrowy dokument jednorazowego użytku upoważniający do przejazdu komunikacją miejską określonej ilości przystanków 
Bilet okresowy | Dokument wielokrotnego użytku upoważniający do przejazdu komunikacją miejską w określonym czasie
Biletomat | Automatyczne urządzenie służące do sprzedaży biletów, umożliwiające sprawdzenie aktualnego rozkładu jazdy oraz regulaminu korzystania z usług przewoźnika
Doładowanie karty miejskiej | Zasilenie środkami karty miejskiej
Forma płatności | Jedna z dostępnych metod płatności - gotówka lub karta płatnicza
Karta miejska | Dokument posiadający możliwość zasilenia środkami, które można wykorzystać do przejazdu komunikacją miejską
Klient | Osoba korzystająca z usług udostępnianych przez biletomat
Oprogramowanie (system) biletomatu | Oprogramowanie zainstalowane w biletomacie umożliwiające korzystanie z jego usług
Płatność | Proces przyjmowania środków określoną formą płatności
Regulamin korzystania z biletomatu | Zbiór zasad dotyczących korzystania z biletomatu
Regulamin korzystania z usług przewoźnika | Zbiór przepisów i zasad dotyczących korzystania z usług przewoźnika
Rozkład jazdy | Element oferty przewozowej obejmujący trasę, przystanki i godziny odjazdów
Serwisant ZTM | Osoba zajmująca się konserwacją i naprawą biletomatu oraz uzupełnianiem zasobów
Strefa obowiązywania biletu | Określony obszar obowiązywania biletu
System obsługi płatności elektronicznych | System autoryzacji płatności kartą
Ulga | Uprawnienie do zmniejszenia kwoty do zapłaty za korzystanie z usług przewoźnika
Urząd Skarbowy | Podmiot odpowiedzialny za kwestie podatkowe
Usterka | Awaria urządzenia utrudniająca lub uniemożliwiająca poprawne działanie
Zarząd Transportu Miejskiego (ZTM) | Jednostka organizująca, zarządzająca i nadzorująca transport miejski, właściciel biletomatu
Zasób | Obiekty materialne niezbędne do poprawnego działania biletomatu (papier, toner)

## Skrócone przypadki użycia (use cases)
### UC1: Zakup biletu jednorazowego - Klient
Klient podchodzi do biletomatu celem zakupu biletu. Na panelu głównym klient wybiera rodzaj biletu - czas ważności biletu oraz opcjonalnie ulgę, którą może poświadczyć. W kolejnym kroku klient wybiera strefę/strefy obowiązywania biletu. System wyświetla kwotę do zapłaty. Następnie klient wybiera formę płatności i płaci określoną kwotę. Płatność jest weryfikowana. Po akceptacji następuje drukowanie biletu oraz potwierdzenia płatności.

### UC2: Zakup biletu okresowego - Klient
Klient podchodzi do biletomatu celem zakupu biletu. Na panelu głównym klient wybiera rodzaj biletu - okres, na który przedłużona zostanie ważność biletu oraz opcjonalnie ulgę, którą może poświadczyć. W kolejnym kroku klient wybiera strefę/strefy obowiązywania biletu. System wyświetla kwotę do zapłaty. Następnie klient wybiera formę płatności i płaci określoną kwotę. Płatność jest weryfikowana. Po akceptacji następuje drukowanie biletu oraz potwierdzenia płatności.

### UC3: Doładowanie karty miejskiej - Klient
Klient podchodzi do biletomatu celem doładowania karty miejskiej. Klient umieszcza kartę miejską w wyznaczonym do tego miejscu na panelu biletomatu. Następnie na panelu głównym wybiera opcję doładowania karty miejskiej. System wyświetla aktualny stan konta klienta i pozwala na wprowadzenie kwoty, którą klient chce zasilić konto. Po zatwierdzeniu klient wybiera formę płatności i płaci określoną kwotę. Płatność jest weryfikowana. Po akceptacji system wyświetla komunikat o doładowaniu oraz drukuje potwierdzenie płatności.

### UC4: Sprawdzenie rozkładu jazdy - Klient
Klient podchodzi do biletomatu celem sprawdzenia rozkładu jazdy. Na panelu głównym klient wybiera opcję sprawdzenia rozkładu jazdy. Następnie wybiera określoną linię autobusową lub tramwajową. Kolejnym krokiem jest wybór kierunku jazdy. Na panelu pojawia się lista poszczególnych przystanków na trasie w wybranym kierunku. Po wybraniu odpowiedniego przystanku pojawia się pełna rozpiska godzinowa przejazdów w danym punkcie.

### UC5: Sprawdzenie regulaminu korzystania z usług przewoźnika - Klient
...

### UC6: Wezwanie serwisu - Klient
...

### UC7: Naprawa usterki - Serwisant ZTM
...

### UC8: Uzupełnienie zasobów - Serwisant ZTM
...

### UC9: Zarządzanie i aktualizacja systemu - Serwisant ZTM
...
