# Chained Together — iPhone / iOS player

Repo zawiera prosty odtwarzacz HLS pod Safari/iOS dla odcinków 1–21.

Każdy odcinek ładuje automatycznie:

- film: `epN_.m3u8`
- polskie napisy: `epN.vtt`

## GitHub Pages

Włącz w repozytorium:

`Settings -> Pages -> Build and deployment -> Deploy from a branch`

Następnie wybierz:

- Branch: `main`
- Folder: `/ (root)`

Po zapisaniu strona będzie dostępna pod:

`https://damian2603.github.io/testfilm/`

Na iPhonie możesz otworzyć ten adres w Safari, a następnie użyć `Udostępnij -> Dodaj do ekranu początkowego`.

## Pliki

- `index.html` — player pod Safari/iOS, wybór EP1–EP21 i automatyczne polskie WebVTT
- `playlist.m3u` — zwykła playlista M3U z URL filmów oraz `#EXTVLCOPT:sub-file=` dla odtwarzaczy, które honorują ten tag

## Uwaga

`#EXTVLCOPT:sub-file=` nie jest standardowym tagiem HLS i nie każdy player iOS go obsłuży. Najpewniejszą opcją w tym repo jest `index.html`, ponieważ przypina WebVTT bezpośrednio jako ścieżkę `<track>` do danego odcinka.
