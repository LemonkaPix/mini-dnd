# Zasady generowania kart postaci (PDF) — DIET CYBERPUNK

Instrukcja dla agentów przygotowujących gotowe do druku karty postaci (Character Sheet) w formacie PDF na podstawie plików z folderu `Rules-DNDxCyberpunk/Classes/`.

---

## 1. Pliki źródłowe i nazewnictwo
* **Źródło danych klasy:** `Rules-DNDxCyberpunk/Classes/<NazwaKlasy>.md`
* **Kontekst mechaniki i pojęć:** `Rules-DNDxCyberpunk/Ogólne zasady DIET CYBERPUNK.md`
* **Plik wynikowy:** `Rules-DNDxCyberpunk/Classes/<NazwaKlasy>-Karta-Postaci.pdf` (np. `Netrunner-Karta-Postaci.pdf`).
* **Wzór referencyjny:** `Rules-DNDxCyberpunk/Classes/Netrunner-Karta-Postaci.pdf`.

---

## 2. Wymagania obowiązkowe (układ i treść)

1. **Format i liczba stron:**
   * Ściśle **1 strona A4 w orientacji poziomej (Landscape)**: `@page { size: A4 landscape; margin: 7mm; }`.
   * Kontener `body` ma stałe wymiary obszaru roboczego `283mm × 196mm` i `overflow: hidden` — treść **nie może** przelewać się na 2. stronę ani być przycięta.
2. **Brak charakterystyki roleplayowej i pola na wygląd:**
   * **Nie dodawaj** opisów fabularnych, historii postaci, cech charakteru, ideałów, więzi, wad ani okienka na szkic/opis wyglądu.
   * Z części opisowej pozostaw **wyłącznie** białe pole na **Nazwę postaci / Pseudonim** oraz białe, puste pole na **Poziom** w nagłówku (do wpisania ołówkiem).
3. **Przyjazność dla druku i brak zhardcodowanych statystyk:**
   * Białe tło karty (`#ffffff`) i białe pola do wpisywania ołówkiem (nazwa, poziom, cechy, PŻ, AC, inicjatywa) z wysokim kontrastem tekstu (`#111827`) oraz akcentami cyberpunkowymi (ciemny granat `#0f172a`, cyjan `#007ea7` / `#06b6d4`, magenta `#b81d65` / `#ec4899`).
   * **Nie wpisuj na sztywno liczb** dla: 6 cech (`SIŁ`, `ZRĘ`, `KON`, `INT`, `MĄD`, `CHA`), `max PŻ`, `AC` oraz `Inicjatywy` — zostaw puste pola do uzupełnienia ołówkiem (możesz podać jedynie wzór pomocniczy pod spodem, np. `Kurtka balist.: 11 + ZRĘ`, `k20 + ZRĘ`).
   * Wszelkie zasoby zużywalne podczas sesji (Sloty RAM, ładunki *Sandevistanu*, *Kości Taktyczne*, użycia *1x na sesję*) muszą mieć wyraźne **checkboxy** (`□`) do odhaczania ołówkiem.
   * Pole **PŻ** musi mieć dwie puste linie (`_____ / _____`) na bieżącą i maksymalną wartość.
4. **Sloty RAM bez tabelki poziomów:**
   * Dla klas korzystających z RAM nie twórz tabelki progresji poziomów — zamiast tego umieść **3 wiersze** z checkboxami (w każdym wierszu cyfry rzymskie malejąco od lewej do prawej):
     * **RAM 1:** 4 sloty z małymi cyframi rzymskimi nad każdym slotem oznaczającymi poziom odblokowania (`III`, `II`, `I`, `I`),
     * **RAM 2:** 3 sloty (`IV`, `III`, `III`),
     * **RAM 3:** 2 sloty (`V`, `V`).
5. **Zgodność z plikiem klasy:**
   * Przepisz dokładnie Prędkość (z przeliczeniem na kratki: `5 ft = 1 kratka`), ataki bronią, zdolności pasywne, aktywne i reakcje z pliku `.md` danej klasy.
   * Jeśli jakaś zdolność nie występuje w pliku klasy (np. brak broni białej u Netrunnera), nie wymyślaj jej na własną rękę.

---

## 3. Struktura 3-kolumnowego layoutu

* **Nagłówek (Header):**
  * Lewa strona: Nazwa klasy (duże litery), podtytuł z klasą bazową D&D (np. `KLASA BAZOWA: CZARODZIEJ • DIET CYBERPUNK`) oraz **białe, puste pole** `Poziom` do wpisania ołówkiem.
  * Prawa strona: Rozciągnięte **białe pole** `Nazwa postaci / Pseudonim` do wpisania ołówkiem.
* **Kolumna 1 (`88mm`) — Cechy, Statystyki, Ściągawka, Ekwipunek:**
  * Panel **Cechy (Modyfikatory)** w siatce 3×2 (`SIŁ`, `ZRĘ`, `KON`, `INT`, `MĄD`, `CHA`) z pustym miejscem na wpisanie modyfikatora. Główną cechę lub główne cechy klasy wyróżnij ramką w kolorze magenty i symbolem `★`.
  * Panel **Statystyki bojowe**: `PŻ` (`___ / ___`), `AC` (puste pole + wzór pancerza), `Prędkość` (`ft / m / kr.`), `Inicjatywa` (puste pole + `k20 + ZRĘ`).
  * **Ściągawka tury** (skrót: Ruch + Akcja + Akcja Dodatkowa + Reakcja, lista podstawowych akcji dostępnych dla każdego jak Unik/Sprint/Wycofanie/Pomoc/Ukrycie/Rozbrojenie/Przygotowanie akcji, zasada Krytyka `20`).
  * **Ekwipunek, Kredyty i Notatki** (`flex: 1`, linie do ręcznych zapisków).
* **Kolumna 2 (`96mm`) — Zasoby klasowe, Zdolności i Akcje podstawowe:**
  * *Dla klas sieciowych/modułowych:* **Sloty Pamięci RAM** (3 wiersze z cyframi rzymskimi nad slotami) oraz **Podstawowe Skrypty / Mikromoduły**.
  * *Dla klas bojowych:* **Ataki (Broń)** + tracker **Zasobów klasowych** (checkboxy dla ładunków, kości taktycznych, punktów przeciążenia, szału itp.).
  * **Zdolności specjalne** (pasywne, reakcje, akcje `1x na sesję` z checkboxem).
* **Kolumna 3 (`1fr`) — Zdolności zaawansowane i Programy:**
  * Pozostałe zdolności / **Programy 1. poziomu** / manewry (każda karta zdolności ma wyraźny badge typu akcji: `AKCJA`, `AKCJA DODATKOWA`, `REAKCJA` oraz koszt zasobów).
  * Panel na dodatkowe/późniejsze programy lub zdolności z wyższych poziomów (`flex: 1`, linie do uzupełnienia podczas kampanii).

---

## 4. Pipeline generowania i obowiązkowa weryfikacja (macOS)

1. Zapisz roboczy plik HTML w katalogu `scratch/` (w folderze artefaktów konwersacji, nie w repozytorium).
2. Wygeneruj PDF przez Brave Browser w trybie headless:
   ```bash
   "/Applications/Brave Browser.app/Contents/MacOS/Brave Browser" \
     --headless --disable-gpu --no-pdf-header-footer \
     --print-to-pdf="/Users/maciej/Desktop/Foldery/Notes/Mini DnD/Rules-DNDxCyberpunk/Classes/<NazwaKlasy>-Karta-Postaci.pdf" \
     "file://<ścieżka_do_scratch>/<klasa>_sheet.html"
   ```
3. Wyrenderuj podgląd PNG wszystkich stron przez Ghostscript (`gs`):
   ```bash
   gs -q -dNOPAUSE -dBATCH -sDEVICE=png16m -r150 \
     -sOutputFile="<ścieżka_do_scratch>/preview-%d.png" \
     "/Users/maciej/Desktop/Foldery/Notes/Mini DnD/Rules-DNDxCyberpunk/Classes/<NazwaKlasy>-Karta-Postaci.pdf"
   ```
4. **Sprawdź wynik:**
   * Upewnij się, że wygenerował się **tylko jeden plik** `preview-1.png` (brak `preview-2.png`).
   * Otwórz `preview-1.png` narzędziem `read_file` i wizualnie zweryfikuj: brak uciętego tekstu, brak niezgrabnego zawijania krótkich wartości (w razie potrzeby użyj `white-space: nowrap` lub lekko skoryguj szerokość kolumn w `.vitals-row`), równe marginesy i czytelność wszystkich ramek.

---

## 5. Bazowy szablon CSS (referencja z karty Netrunnera)

```css
@page {
  size: A4 landscape;
  margin: 7mm;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --ink: #111827;
  --muted: #4b5563;
  --cyan: #007ea7;
  --cyan-bg: #eef9fc;
  --magenta: #b81d65;
  --magenta-bg: #fdf1f7;
  --dark: #0f172a;
  --border: #94a3b8;
  --light-bg: #f8fafc;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  color: var(--ink);
  background: #ffffff;
  font-size: 8.4pt;
  line-height: 1.3;
  width: 283mm;
  height: 196mm;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  gap: 3mm;
}

.grid {
  display: grid;
  grid-template-columns: 88mm 96mm 1fr;
  gap: 3mm;
  flex: 1;
  min-height: 0;
}

/* Białe pola w nagłówku (do wypełnienia ołówkiem) */
.level-box {
  background: #ffffff;
  color: var(--dark);
  border: 1.5px solid #22d3ee;
  padding: 1mm 3mm;
  border-radius: 3px;
  text-align: center;
  min-width: 17mm;
}

.name-field {
  flex: 1;
  background: #ffffff;
  color: var(--dark);
  border: 1.5px solid #cbd5e1;
  border-left: 3.5px solid #ec4899;
  padding: 1.2mm 3.5mm;
  border-radius: 2px;
}

/* 3 wiersze slotów RAM z cyframi rzymskimi nad checkboxem */
.ram-rows { display: flex; flex-direction: column; gap: 1.6mm; }
.ram-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: var(--light-bg);
  border: 1px solid #cbd5e1;
  border-left: 3px solid var(--magenta);
  border-radius: 3px;
  padding: 1.2mm 2.5mm;
}
.slot-group { display: flex; align-items: flex-end; gap: 2.5mm; }
.slot-item { display: flex; flex-direction: column; align-items: center; gap: 0.5mm; }
.slot-lvl { font-size: 6.2pt; font-weight: 800; color: var(--magenta); line-height: 1; }
```
