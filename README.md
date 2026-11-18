# Dziennik treningowy

Aplikacja do zapisywania treningów na siłowni: wybór ćwiczeń z listy, serie (powtórzenia × kg), notatki, cardio i statystyki progresu oraz regresu. Działa w telefonie i bez internetu. Dane zostają w telefonie.

## Struktura

- `web/` – cała aplikacja (strona, manifest, tryb offline, ikony)
- `.github/workflows/pages.yml` – automatyczna publikacja na GitHub Pages

## Wdrożenie krok po kroku

1. Na GitHubie utwórz nowe repozytorium (np. `dziennik-treningowy`, może być publiczne).
2. Wgraj do niego zawartość tego folderu (przycisk **Add file → Upload files**, przeciągnij wszystkie pliki i foldery razem z `.github`). Gałąź ma nazywać się `main`.
3. Wejdź w **Settings → Pages** i w polu **Source** wybierz **GitHub Actions**.
4. Wejdź w zakładkę **Actions**. Workflow „Publikacja na GitHub Pages” uruchomi się sam (jeśli nie, kliknij **Run workflow**). Po ok. minucie adres strony pojawi się w **Settings → Pages**, w formie `https://TWOJ-LOGIN.github.io/dziennik-treningowy/`.
5. Otwórz ten adres w Chrome na Androidzie, wybierz menu ⋮ → **Zainstaluj aplikację** (lub **Dodaj do ekranu głównego**).
6. Przy pierwszym uruchomieniu naciśnij **Wczytaj moje notatki**, aby załadować treningi z 2, 9 i 16 listopada.

## Aktualizacje

Zmień pliki w `web/` i wgraj je na `main`. Strona opublikuje się sama. Przy zmianach w aplikacji podbij numer `CACHE` w `web/sw.js` (np. `dziennik-v2`), aby telefony pobrały nową wersję.

## Kopia zapasowa

Dane są tylko w telefonie. W zakładce **Ćwiczenia → Dane** użyj **Zapisz kopię zapasową (JSON)**. Ten sam plik wczytasz na nowym telefonie przez **Wczytaj kopię zapasową**.
