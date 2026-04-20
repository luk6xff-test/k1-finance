# K1 Finance — GitHub Pages

Statyczna strona www przygotowana pod GitHub Pages, bez formularzy, z bezpośrednimi linkami do telefonu, e-maila i social mediów.

## Co jest gotowe

- elegancki, premium layout w kolorach beż / taupe / soft ivory
- menu: Strona główna, O nas, Usługi, Cennik, Kontakt, Bezpłatna konsultacja
- przyciski `tel:` i `mailto:`
- placeholdery do Facebooka i Instagrama
- podstrona `privacy.html`
- workflow GitHub Actions do automatycznego wdrażania po każdym pushu do `main`
- plik `CNAME` dla domeny `k1-finance.pl`

## Jak uruchomić

1. Utwórz nowe repozytorium na GitHubie.
2. Wrzuć do niego wszystkie pliki z tego katalogu.
3. Upewnij się, że główna gałąź nazywa się `main`.
4. Wejdź w `Settings -> Pages`.
5. W sekcji **Build and deployment** wybierz **GitHub Actions**.
6. Po pierwszym pushu workflow automatycznie opublikuje stronę.

## Jak działa automatyczna publikacja

Za każdym razem, gdy zrobisz push do gałęzi `main`, workflow z pliku:

`.github/workflows/deploy.yml`

zdeployuje aktualną wersję strony na GitHub Pages.

## Domena własna

W katalogu głównym jest plik `CNAME`:

`k1-finance.pl`

Dzięki temu GitHub Pages będzie publikować stronę pod tą domeną po poprawnym ustawieniu DNS u operatora.

## Co podmienić po wdrożeniu

### 1. Linki social media
W pliku `index.html` podmień:

- `https://facebook.com/`
- `https://instagram.com/`

na właściwe adresy.

### 2. Zdjęcia
Główne zdjęcie znajduje się w:

`assets/hero-k1.jpg`

Możesz je zastąpić własnym zdjęciem o pionowych proporcjach.

### 3. Teksty i dane firmy
Uzupełnij:

- pełne dane firmy w stopce
- finalne treści sekcji
- politykę prywatności w `privacy.html`

## DNS dla GitHub Pages

Przy domenie apex (`k1-finance.pl`) ustaw rekordy `A` na adresy GitHub Pages oraz opcjonalnie rekord `CNAME` dla `www` na `luk6xff-test.github.io`:
```
k1-finance.pl — A — 185.199.108.153
k1-finance.pl — A — 185.199.109.153
k1-finance.pl — A — 185.199.110.153
k1-finance.pl — A — 185.199.111.153
www.k1-finance.pl — CNAME — luk6xff-test.github.io
```

