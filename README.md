# testy-oczyszczaczy-dataset

Otwarty zbiór danych o oczyszczaczach powietrza dostępnych na polskim rynku, publikowany przez redakcję [testy-oczyszczaczy.pl](https://testy-oczyszczaczy.pl) — niezależnego serwisu testującego i porównującego oczyszczacze powietrza.

## Co zawiera ten zbiór danych

### `data/measurements.json`

Dane dla 98 modeli oczyszczaczy powietrza: parametry deklarowane przez producentów (CADR, zasięg, cena, filtracja) oraz — dla większości modeli — **realne laboratoryjne pomiary hałasu** wykonane przez redakcję (miernik dźwięku CEM DT-8852, pomieszczenie testowe 20 m², 1 metr od urządzenia). Zawiera też autorski **Wskaźnik Realnej Ciszy (WRC)** — indeks 0–10 liczony liniowo wyłącznie z naszego pomiaru (15 dB → 10 pkt, 45 dB → 0 pkt).

Pełny opis metodologii pomiarowej: [testy-oczyszczaczy.pl/jak-testujemy/](https://testy-oczyszczaczy.pl/jak-testujemy/)

### `data/external-reviews.json`

Ręcznie zebrane i zweryfikowane opinie kupujących z Allegro.pl i Amazon.pl dla wybranych modeli. Każdy wpis zawiera realny link źródłowy, ocenę i liczbę opinii z dnia zbierania, oraz uczciwe podsumowanie napisane przez redakcję na podstawie faktycznie przeczytanych recenzji (włącznie z krytycznymi, jeśli się pojawiły). **Nie jest to zautomatyzowany scraping** — każdy wpis został przeczytany i zweryfikowany przez człowieka.

Pełny opis metodologii zbierania opinii: [testy-oczyszczaczy.pl/jak-zbieramy-opinie/](https://testy-oczyszczaczy.pl/jak-zbieramy-opinie/)

## Czego ten zbiór danych NIE zawiera

- Zdjęć ani materiałów wideo z testów fizycznych.
- Fabrykowanych ani szacowanych wartości — produkty bez realnego pomiaru lub wiarygodnej, dedykowanej oferty z opiniami są pomijane, a nie uzupełniane wymyślonymi danymi.
- Danych osobowych recenzentów.

## Licencja

Dane udostępnione na licencji [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) — możesz je swobodnie wykorzystywać, także komercyjnie, pod warunkiem podania źródła.

## Jak cytować

```
testy-oczyszczaczy.pl (2026). Pomiary hałasu i Wskaźnik Realnej Ciszy (WRC) dla oczyszczaczy powietrza.
https://github.com/BartMar/testy-oczyszczaczy-dataset
```

## Aktualizacje

Ten zbiór danych jest eksportem danych źródłowych z [testy-oczyszczaczy.pl](https://testy-oczyszczaczy.pl) i jest aktualizowany okresowo w miarę dodawania nowych pomiarów i opinii.
