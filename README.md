# PAB cyfrowa

Program dla Windows do przygotowania kompletnej dokumentacji do pozwolenia na budowę:

* **PZT** – projekt zagospodarowania działki lub terenu (§ 14 rozporządzenia),
* **PAB** – opis architektoniczno-budowlany (§ 20 rozporządzenia),
* **Wniosek** o pozwolenie na budowę (art. 33 Prawa budowlanego),
* **Oświadczenie** o prawie do dysponowania nieruchomością na cele budowlane,
* **Informacja BIOZ** oraz **Plan BIOZ** (art. 21a Prawa budowlanego),
* **Wykaz dokumentów i załączników** wymaganych do uzyskania pozwolenia.

Aplikacja prowadzi użytkownika przez formularz, pilnuje kompletności danych, automatycznie
liczy bilans terenu i wskaźniki zabudowy, a następnie generuje gotowe dokumenty w formatach
**DOCX**, **PDF** oraz **TXT** – ze stroną tytułową, spisem treści, tabelami, numeracją stron,
podpisami projektantów i załącznikami.

Program działa w całości lokalnie. Nie wysyła danych do internetu i nie wymaga połączenia
z siecią. Pierwsze **30 dni** pracy jest bezpłatnym okresem próbnym; po jego upływie
program wymaga klucza licencyjnego (patrz sekcja *Licencja*).

**Autor:** Rami Nassar · 2026 · **BIM architects & consultants** · **Kontakt:** raminassar.arch@gmail.com · **wersja 1.5.2**

---

## Podstawa prawna

* Ustawa z dnia 7 lipca 1994 r. – **Prawo budowlane** (Dz. U. z 2026 r. poz. 524 ze zm.), art. 34.
* **Rozporządzenie Ministra Rozwoju z dnia 11 września 2020 r.** w sprawie szczegółowego
  zakresu i formy projektu budowlanego – tekst jednolity **Dz. U. z 2022 r. poz. 1679**,
  zmieniony **Dz. U. z 2023 r. poz. 2405** oraz **Dz. U. z 2026 r. poz. 597**
  (nowelizacja w mocy od 19 maja 2026 r.).
* Rozporządzenie w sprawie warunków technicznych, jakim powinny odpowiadać budynki
  i ich usytuowanie (Dz. U. z 2022 r. poz. 1225 ze zm.) – w zakresie odesłań.
* Ustawa o ochronie ludności i obronie cywilnej (Dz. U. z 2024 r. poz. 1907 ze zm.).
* Rozporządzenie Ministra Infrastruktury z dnia 23 czerwca 2003 r. w sprawie informacji
  dotyczącej bezpieczeństwa i ochrony zdrowia oraz planu bezpieczeństwa i ochrony zdrowia
  (Dz. U. nr 120 poz. 1126) – dla informacji i planu BIOZ.

Zastosowane jednostki redakcyjne: § 7 (strona tytułowa), § 14 (PZT), § 15 (część rysunkowa),
§ 18 (obszar oddziaływania), § 20 (PAB), § 21 (część rysunkowa PAB), § 23 (załączniki).

Nowelizacja z 2026 r. wnosi w szczególności:

* **§ 14 pkt 6a** – wymagania dotyczące dróg pożarowych oraz zaopatrzenia w wodę do
  zewnętrznego gaszenia pożaru,
* **§ 20 ust. 1 pkt 14** – informacje o ochronie ludności (budowle ochronne, miejsca
  doraźnego schronienia),
* **§ 21 pkt 3** – oznaczenia wyjść ewakuacyjnych, stref zagruzowania i elementów
  budowli ochronnych na rysunkach,
* **§ 15 ust. 3** – wymiary podawane z dokładnością do **0,01 m**.

---

## Wygląd i obsługa

Interfejs utrzymany jest w motywie **głębokiej zieleni ze złotymi akcentami**
(wersja 1.5.2): gradientowy pasek nagłówka ze złotą linią, białe karty formularzy,
złote przyciski akcji głównej i naprzemienne tło tabel. Paleta barw i style ttk
znajdują się w `src/theme.py`.

Wersja 1.5.2 porządkuje pracę w **dziewięć ponumerowanych kroków** widocznych
w lewym pasku bocznym oraz dodaje stronę **O programie**:

| Krok | Sekcja |
|------|--------|
| — | **Pulpit** – stan projektu, postęp i ostatnio otwierane pliki |
| 1 | Dane ogólne |
| 2 | PZT |
| 3 | PAB |
| 4 | BIOZ |
| 5 | Bilans i obiekty |
| 6 | Załączniki |
| 7 | Podgląd |
| 8 | Eksport |
| 9 | Kontrola |
| — | **O programie** – autor, firma, kontakt i zakres programu |

Dodatkowo:

* **Pulpit** pokazuje listę sekcji z postępem wypełnienia, liczbą braków
  i skrótami do każdej z nich oraz listę ostatnich projektów.
* **Pola wymagane** są oznaczone gwiazdką `*`; po najechaniu kursorem na etykietę
  lub pole pojawia się **podpowiedź** z wyjaśnieniem i informacją o wymagalności.
* **Pola zależne** (np. szczegóły rozbiórki, odstępstwa, dostępności) są
  automatycznie włączane i wygaszane zależnie od przełącznika.
* Przyciski **Wstecz / Dalej** oraz klawisze `Alt+←` / `Alt+→` prowadzą po kolei
  przez wszystkie kroki; menu *Widok* pozwala przejść bezpośrednio do sekcji.
* **F1** otwiera okno **Pomoc i szybki start** z tematami krok po kroku.
* **Kopia robocza** jest zapisywana automatycznie co 30 sekund; po nieoczekiwanym
  zamknięciu programu przy następnym uruchomieniu pojawi się propozycja odtworzenia
  danych.
* **Ostatnie projekty** są dostępne w menu *Plik → Ostatnie projekty* oraz na
  Pulpicie.
* **Podgląd** oferuje zmianę rozmiaru czcionki (A− / A+), kopiowanie całego tekstu,
  wyszukiwanie (`Ctrl+F`) oraz przycisk *Otwórz w Wordzie*.
* **Eksport** ma szybki wybór zakresu (*Wszystkie dokumenty*, *Tylko PZT i PAB*,
  *Żaden*) oraz licznik plików do wygenerowania.
* **O programie** (menu *Pomoc → O programie…*) pokazuje nazwę i wersję programu,
  firmę **BIM architects & consultants**, autora **Rami Nassar, 2026** oraz adres
  **raminassar.arch@gmail.com** z przyciskami *Napisz e-mail* i *Kopiuj adres*.
* **Licencja** – pasek stanu i strona *O programie* pokazują stan licencji
  (okres próbny, licencja pełna, wygasła). Okno *Pomoc → Licencja…* pozwala
  sprawdzić stan i aktywować klucz.

---

## Jak korzystać

Pracę rozpoczyna **Pulpit**, który pokazuje postęp wypełnienia danych, listę
braków oraz ostatnio otwierane projekty. Do każdej sekcji można przejść z paska
bocznego, przyciskami *Wstecz / Dalej* albo z menu *Widok*. Sekcje 1–6 są
przeznaczone do wprowadzania danych, sekcje 7–9 do sprawdzenia i wydania
dokumentów.

1. **Dane ogólne** – metryka inwestycji, inwestor, organ administracji
   architektoniczno-budowlanej, wnioskodawca oraz **lista projektantów** (funkcja,
   imię i nazwisko, specjalność, nr uprawnień). Lista trafia na stronę tytułową,
   do metryki dokumentów i do tabel podpisów. Data opracowania trafia do nazw plików
   (`PZT_2026.11.16`).
2. **PZT** – kolejne grupy pól odpowiadają punktom § 14. Puste pola są uzupełniane
   tekstem standardowym, więc dokument zawsze ma pełną strukturę.
3. **PAB** – program użytkowy, forma, parametry, dostępność, środowisko, charakterystyka
   energetyczna, ochrona przeciwpożarowa i ochrona ludności (§ 20 ust. 1).
4. **BIOZ** – zakres i kolejność robót, istniejące zagrożenia, prace szczególnie
   niebezpieczne, instruktaż oraz środki ochrony. Dane zasilają informację i plan BIOZ.
5. **Bilans i obiekty** – pozycje bilansu terenu z automatycznym podsumowaniem
   (powierzchnia zabudowy, drogi, powierzchnia biologicznie czynna, inne) oraz lista
   obiektów wchodzących w zakres zamierzenia. Przycisk *Pow. zabudowy z listy obiektów*
   przenosi sumę powierzchni zabudowy z listy obiektów do bilansu.
6. **Załączniki** – lista dokumentów wymaganych do pozwolenia na budowę ze statusem
   (*Do uzupełnienia / Dołączony / Nie dotyczy*) oraz rejestr załączników projektu
   (nazwa, opis lub ścieżka pliku, status).
7. **Podgląd** – pełna treść dowolnego z siedmiu dokumentów przed eksportem.
   Dostępne są: zmiana rozmiaru czcionki, kopiowanie tekstu, wyszukiwanie
   (`Ctrl+F`) i otwarcie tymczasowej kopii w Wordzie.
8. **Eksport** – wybór folderu, dokumentów (wszystkie siedem) i formatów
   (DOCX/PDF/TXT). Szybki wybór pozwala zaznaczyć wszystko, tylko PZT i PAB
   albo odznaczyć wszystkie pozycje; pod listą widnieje liczba plików do zapisania.
9. **Kontrola** – lista błędów, ostrzeżeń i informacji: brakujące pola, niezgodny bilans,
   przekroczenie limitów z planu miejscowego, niespójna intensywność zabudowy,
   niekompletna lista dokumentów i załączników. Dwukrotne kliknięcie komunikatu
   przenosi do pola, którego dotyczy.

Pola wymagane oznaczono gwiazdką `*`, a podpowiedzi pojawiają się po najechaniu
kursorem. Projekt można zapisać do pliku **JSON** (*Plik → Zapisz*) i wrócić do
niego później. Ostatnio używany folder eksportu, położenie okna i lista ostatnich
projektów są zapamiętywane w `%APPDATA%\PABcyfrowa\config.json`; kopia robocza
niezapisanych zmian trafia do `%APPDATA%\PABcyfrowa\autosave.json`. Przy pierwszym
uruchomieniu programu ustawienia ze starej lokalizacji (`%APPDATA%\OpisPZT`) są
kopiowane automatycznie.

### Wyniki

Dla danych z dnia 16.11.2026 powstają pliki:

```
PZT_2026.11.16.docx          PZT_2026.11.16.pdf          PZT_2026.11.16.txt
PAB_2026.11.16.docx          PAB_2026.11.16.pdf          PAB_2026.11.16.txt
WNIOSEK_2026.11.16.docx      WNIOSEK_2026.11.16.pdf      WNIOSEK_2026.11.16.txt
OSWIADCZENIE_2026.11.16.docx OSWIADCZENIE_2026.11.16.pdf OSWIADCZENIE_2026.11.16.txt
BIOZ_INFO_2026.11.16.docx    BIOZ_INFO_2026.11.16.pdf    BIOZ_INFO_2026.11.16.txt
BIOZ_2026.11.16.docx         BIOZ_2026.11.16.pdf         BIOZ_2026.11.16.txt
ZALACZNIKI_2026.11.16.docx   ZALACZNIKI_2026.11.16.pdf   ZALACZNIKI_2026.11.16.txt
```

Dokumenty DOCX zawierają pole spisu treści – przy pierwszym otwarciu Word zaproponuje
jego zaktualizowanie (albo *Odwołania → Aktualizuj spis treści*). W plikach PDF spis
treści i numeracja stron są wyliczane automatycznie.

---

## Licencja

Program działa **30 dni w trybie próbnym** liczonym od pierwszego uruchomienia.
Po upływie tego terminu dalsza praca wymaga **klucza licencyjnego** otrzymanego
od autora. Klucz jest sprawdzany w całości lokalnie – aktywacja nie wymaga
połączenia z internetem.

## Uwagi

* Program jest narzędziem redakcyjnym – **nie zastępuje wiedzy, doświadczenia
  i odpowiedzialności projektanta**. Ostateczna weryfikacja zakresu i treści
  opracowania należy do osoby posiadającej odpowiednie uprawnienia budowlane.
* Część rysunkowa nie jest generowana – program przygotowuje opis i odwołuje się
  do rysunków; ich wykaz można wpisać w polu *Zestawienie rysunków*.
* Przy pierwszym eksporcie PDF program korzysta z czcionki Arial z katalogu
  `C:\Windows\Fonts` (wbudowanej w system Windows), dzięki czemu polskie znaki
  są odwzorowane poprawnie.

---

## Autor

**Rami Nassar**, 2026 · **BIM architects & consultants**
Kontakt: **raminassar.arch@gmail.com**

© 2026 Rami Nassar. Program udostępniany do własnego użytku; dokumenty wygenerowane
programem należą do osoby, która je opracowała.
