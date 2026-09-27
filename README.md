# testy-oczyszczaczy-dataset

Otwarty zbiór danych o oczyszczaczach powietrza dostępnych na polskim rynku,
publikowany przez redakcję [testy-oczyszczaczy.pl](https://testy-oczyszczaczy.pl) -
niezależnego serwisu testującego i porównującego oczyszczacze powietrza.

## Co zawiera ten zbiór danych

### `data/measurements.json`

Dane dla **102 modeli** oczyszczaczy powietrza: parametry deklarowane przez producentów
(CADR, zasięg, cena, filtracja) oraz - dla **90 z nich** - **własne pomiary hałasu**
wykonane przez redakcję.

Zawiera też autorski **Wskaźnik Realnej Ciszy (WRC)**: indeks 0-10 liczony liniowo
wyłącznie z naszego pomiaru, nigdy z deklaracji producenta (15 dB = 10 pkt,
45 dB = 0 pkt).

**Tor pomiarowy:** mikrofon pomiarowy Røde NT1 5. generacji w systemie Room EQ Wizard
(REW), kalibracja plikiem kalibracyjnym mikrofonu, pomieszczenie testowe 20 m²,
tło 15 dB, mikrofon 1 metr od urządzenia. 79 z 90 pomiarów pochodzi z tego toru.
Pozostałych 11 zmierzono ręcznym miernikiem CEM DT-8852, **wyłącznie powyżej 30 dB**,
bo tam zaczyna się jego zakres pomiarowy.

### Ograniczenie, o którym mówimy wprost

**23 z 90 pomiarów leży mniej niż 3 dB nad tłem** (najniższy to 15,26 dB, zaledwie
0,26 dB nad tłem). Przy tak małej różnicy wyniku nie da się przypisać samemu
urządzeniu, bo dominuje akustyka pomieszczenia. **Takie wartości traktuj jako górne
ograniczenie:** urządzenie nie jest głośniejsze niż podana liczba, ale może być
cichsze, niż potrafimy zmierzyć.

Podajemy to, bo zbiór ma służyć do cytowania, a liczba bez znanej granicy błędu
jest do tego nieprzydatna.

### `data/external-reviews.json`

Ręcznie zebrane i zweryfikowane opinie kupujących z **Allegro.pl, MediaExpert.pl
i Amazon.pl** dla wybranych modeli. Każdy wpis zawiera realny link źródłowy, ocenę
i liczbę opinii z dnia zbierania oraz podsumowanie napisane przez redakcję na podstawie
faktycznie przeczytanych recenzji, włącznie z krytycznymi, jeśli się pojawiły.
**Nie jest to zautomatyzowany scraping** - każdy wpis przeczytał i zweryfikował człowiek.

Pełny opis metodologii:
[jak testujemy](https://testy-oczyszczaczy.pl/jak-testujemy/) i
[jak zbieramy opinie](https://testy-oczyszczaczy.pl/jak-zbieramy-opinie/).

## Czego ten zbiór danych NIE zawiera

- Zdjęć ani materiałów wideo z testów fizycznych.
- Fabrykowanych ani szacowanych wartości. Produkty bez realnego pomiaru lub bez
  wiarygodnej, dedykowanej oferty z opiniami są pomijane, a nie uzupełniane
  wymyślonymi danymi.
- **Pomiarów wycofanych.** Dwa wyniki dla modeli Philips (AC2220/10 i AC3737/10)
  zostały wycofane po weryfikacji jako błąd pomiaru - w tym zbiorze mają
  `measuredNoiseDb: null`, a nie starą wartość.
- Danych osobowych recenzentów.

## Licencja

**Creative Commons Attribution 4.0 International (CC BY 4.0).**
Wiążący jest pełny tekst w pliku [`LICENSE`](LICENSE); skrót po polsku
znajdziesz w [`LICENSE.md`](LICENSE.md).

Możesz te dane swobodnie wykorzystywać, także komercyjnie, pod warunkiem podania
źródła i zaznaczenia, czy wprowadzono zmiany.

## Jak cytować

```
testy-oczyszczaczy.pl (2026). Pomiary hałasu i Wskaźnik Realnej Ciszy (WRC)
dla oczyszczaczy powietrza. CC BY 4.0.
https://github.com/BartMar/testy-oczyszczaczy-dataset
```

## Aktualizacje

Zbiór jest eksportem danych źródłowych z [testy-oczyszczaczy.pl](https://testy-oczyszczaczy.pl),
generowanym skryptem i aktualizowanym w miarę dodawania nowych pomiarów i opinii.
Data ostatniego eksportu znajduje się w polu `updated` w `data/measurements.json`.
