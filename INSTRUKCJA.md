# Sternik – instrukcja

*Trzyma kurs Twojego planu – decyzje zostają przy Tobie.*

Sternik pilnuje Twojego długoterminowego planu inwestycyjnego (IKE, IKZE, rachunek zwykły w XTB) i oszczędności (lokaty, konta, obligacje): liczy proporcje, przypomina o terminach, wpłatach i przeglądach, prowadzi księgę transakcji i pomaga porównać PIT-38 z PIT-8C. **Nie daje rekomendacji inwestycyjnych** – pilnuje zasad, które sam ustalisz.

## Instalacja (Windows 10/11)
1. Pobierz plik `Sternik-…-instalator.exe` (link od osoby, która Ci go poleciła, albo strona wydań).
2. Uruchom go. Windows może pokazać okno **„System Windows ochronił ten komputer”** (program nie ma płatnego podpisu cyfrowego) – kliknij **„Więcej informacji” → „Uruchom mimo to”**.
3. Instalacja trwa kilka sekund, nie wymaga hasła administratora. Na pulpicie i w menu Start pojawi się **Sternik**.

## Pierwsze uruchomienie
Zobaczysz ekran powitalny z trzema drogami:
- **Zacznij od pustego planu** – wpisz miesięczną wpłatę, miesiąc startu i limit IKE (podpowiedziany ustawowy). Resztę zasad zmienisz w *Ustawienia → Plan i zasady*.
- **Wczytaj kopię (.json)** – jeśli masz kopię danych z Sternika (np. z innego komputera).
- **Zaimportuj historię z XTB** – w xStation wygeneruj historię konta do pliku .xlsx (osobno dla każdego konta, okres od założenia konta) i wskaż pliki. Później wystarczą krótsze raporty: od dnia poprzedniego importu (albo wcześniej) do dziś – Sternik doliczy nowe operacje do zapamiętanego salda gotówki. Gdy raport zaczyna się za późno, import się wstrzyma i Sternik poda, od kiedy wygenerować raport. Po aktualizacji do 1.5.1 zaimportuj raz raporty od założenia konta, żeby Sternik zapamiętał salda. Przelew z rachunku zwykłego na IKE/IKZE widać na liście wpłat jako ujemną wpłatę rachunku zwykłego – te pieniądze liczą się tylko jako wpłata na IKE.

## Codzienne używanie
- **Pulpit** – majątek razem, struktura kont, „Do zrobienia” (kliknięcie prowadzi tam, gdzie sprawę się załatwia), podpowiedź wpłaty dla wybranego konta (IKE, IKZE albo rachunek zwykły – tu według docelowych udziałów, które ustawisz przy pozycjach), **Zadania** (Twoja lista spraw z terminami: kliknięcie treści otwiera okno – można ustawić powtarzanie co miesiąc, kwartał lub rok, obszar i notatkę; zrobione dawniej niż 90 dni temu trafiają do archiwum) i terminy oszczędności. Plany miesięcznych wpłat każdego konta ustawisz w *Ustawienia → Plan i zasady*.
- **Portfel** – pozycje IKE/IKZE i rachunku zwykłego (w oknie pozycji możesz wpisać planowaną kwotę zakupu albo dokupu – pod paskiem struktury zobaczysz stan po planowanych zakupach), wpłaty (na IKE, IKZE i rachunek zwykły, z kalendarzem planu każdego konta), tezy satelitów i pozycji rachunku zwykłego (z przypomnieniem o przeglądzie), historia każdego rachunku i całego majątku. Kliknij pozycję, żeby wpisać wartość z XTB albo zmienić dane.
- **Transakcje** – księga operacji, średnie ceny i zamknięte pozycje, zestawienie PIT-38.
- **Oszczędności** – lokaty, konta oszczędnościowe, obligacje skarbowe. Gdy lokata się kończy (albo ją zrywasz), kliknij **„Zakończ”** i wskaż, gdzie trafiły pieniądze – na konto oszczędnościowe, nową lokatę, IKE/IKZE (zapisze się wpłata), rachunek zwykły albo poza program; możesz rozdzielić kwotę na kilka miejsc. Zakończone lokaty i ich wynik są w podzakładce **Historia** (tam też „Cofnij”).
- **Ustawienia** – zasady planu, źródła cen, import z XTB, kopia zapasowa.

**Reguły wyjścia (tygodniowe zamknięcie):** w oknie satelity albo pozycji rachunku zwykłego ustaw *poziom wyjścia*, *potwierdzenie trendu* i *punkt kontrolny tezy* (data i co sprawdzić). Sternik pobiera z Arkusza Google (a gdy arkusz nie zna symbolu – z Xetry) oficjalne zamknięcia sesji i po piątkowej sesji (dla giełd w USA ok. 22:15 naszego czasu) zapisuje zamknięcie tygodnia; przy święcie liczy się ostatnia sesja tygodnia. Zamknięcie poniżej poziomu wyjścia daje alert **„SPRZEDAJ”** – zostaje, dopóki nie sprzedasz, nie zmienisz poziomu albo nie wybierzesz w *Portfel → Tezy* **„Trzymam mimo sygnału”**. Zamknięcie powyżej potwierdzenia podpowiada podniesienie poziomu (**„Zostawiam poziom”** je wycisza). W ciągu tygodnia spadek poniżej poziomu to tylko informacja. Od daty punktu kontrolnego przypomnienie wisi do „Przejrzane dziś”. W tym samym oknie ustawisz **realizację zysku**: do trzech progów wzrostu od ceny bazowej (domyślnie średnia cena zakupu z księgi), np. +100% → sprzedaj 50%. Zamknięcie tygodnia na progu lub wyżej daje alert **„SPRZEDAJ CZĘŚĆ”** z ilością do sprzedania; znika sam po sprzedaży w księdze (np. po imporcie z XTB) albo po „Zrealizowane” / „Pomijam ten próg” w *Tezach*. Zamknięcia spółek i ETF-ów z GPW pochodzą z oficjalnego archiwum notowań GPW (od 1.6.0) – nazwa spółki w archiwum (np. CDPROJEKT) dobiera się sama, a gdy się nie da, wybierzesz ją w oknie notowań (*Ustawienia → Źródła cen* → pozycja → „GPW – nazwa w archiwum”). Na karcie pozycji w *Tezach* są też linki do wykresów z pełną historią (TradingView, Stooq) – tam wygodnie sprawdzisz wsparcia i opory, bo wykres w XTB pokazuje tylko część historii. Historia zamknięć jest na karcie pozycji w *Tezach*; gdy arkusz nie poda danych, zamknięcie wpiszesz ręcznie w oknie pozycji. Przy pierwszym użyciu trzeba zaktualizować skrypt w arkuszu – instrukcja pojawi się w *Ustawienia → Źródła cen*.

Ceny instrumentów: kursy walut NBP pobierają się same; ceny ETF-ów i akcji z Xetry (w EUR) podaje od razu bezpłatny dostawca **Xetra (Deutsche Börse)**, a pozostałe (Warszawa, USA, inne giełdy) – **Arkusz Google**, który ustawisz raz w *Ustawienia → Źródła cen* (instrukcja krok po kroku jest w oknie „Ustaw”). Dla pozycji w EUR z innej giełdy niż Xetra (np. ETC na złoto z Londynu) wpisz w oknie notowań jej ISIN – znajdziesz go w karcie instrumentu w XTB. Xetra udostępnia transakcje tylko z ostatniej doby, więc piątkowe zamknięcie z Xetry Sternik zapisze, jeśli uruchomisz go najpóźniej w poniedziałek. Serwis giełdy ogranicza też liczbę pobrań – przy komunikacie „chwilowo ogranicza liczbę pobrań” odśwież ceny po kilku minutach.

## Twoje dane
- Dane są **tylko na Twoim komputerze**, w folderze `%APPDATA%\Sternik` (menu *Plik → Otwórz folder z danymi*). Sternik nie wysyła ich nigdzie.
- Kopia zapasowa robi się sama raz dziennie (folder `kopie`, ostatnie 30 dni). Ręcznie: *Ustawienia → Kopia zapasowa → Pobierz plik .json*.
- Przeniesienie na inny komputer: pobierz kopię .json i wczytaj ją na nowym komputerze (ekran powitalny albo *Ustawienia → Kopia zapasowa*).
- Odinstalowanie programu **nie usuwa** danych.

## Aktualizacje
Gdy pojawi się nowa wersja, w nagłówku zobaczysz przycisk **„Dostępna wersja … – pobierz”**. Pobierz instalator i uruchom go – zainstaluje się na poprzedniej wersji, dane zostają. Ręcznie: *Pomoc → Sprawdź aktualizacje*.

## Pomoc
*Pomoc → O programie* pokazuje wersję i miejsce danych. Zestawienia podatkowe są pomocą do porównania z PIT-8C, nie poradą podatkową.
