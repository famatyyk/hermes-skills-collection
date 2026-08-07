---
title: "Audytowałem requests — najpopularniejszą bibliotekę HTTP w Pythonie. Wynik: 18/100"
published: false
description: "Co narzędzie do statycznego audytu repo wykryło w requests, i dlaczego to nie oznacza, że biblioteka jest zła."
tags: python, opensource, testing, security, showdev
---

# Audytowałem `requests` — najpopularniejszą bibliotekę HTTP w Pythonie. Wynik: 18/100

Od jakiegoś czasu buduję małe narzędzie — **Project Doctor** — które robi *statyczny* przegląd repozytoriów Python/AI. Nie uruchamia kodu, nie instaluje zależności, nie czyta sekretów. Tylko przegląda strukturę, testy, CI, potencjalne ryzyka w kodzie.

Żeby przetestować, czy w ogóle działa, puściłem je na [`psf/requests`](https://github.com/psf/requests) — bibliotekę, którą pewnie masz w co drugim projekcie.

Wynik: **18/100**.

## Co dokładnie wykryło

| Priorytet | Znalezisko | Gdzie |
| --- | --- | --- |
| HIGH | Odczyt `pickle` | w kodzie |
| HIGH | Pliki mogące zawierać poświadczenia | w katalogu |
| MEDIUM | Adresy HTTP bez TLS | w testach/przykładach |
| LOW | Ogólny `except` utrudniający diagnozę | w kodzie |
| LOW | Brak changelogu / CONTRIBUTING / licencji | w repo |
| LOW | Brak lockfile zależności | w repo |
| LOW | Brak widocznego workflow CI | w repo |

## Zanim napiszesz "to bzdura"

**Zgadzam się.** `requests` to jedna z najlepiej utrzymanych bibliotek w ekosystemie Pythona. Nie oceniam jej bezpieczeństwa ani jakości — to niemożliwe bez uruchamiania i bez kontekstu.

To, co widzisz wyżej, to **co narzędzie zgłasza jako statyczne sygnały**. Większość punktów karnych pochodzi z **testów i przykładów** (np. `http://` w testach, `pickle` użyty w konkretnym, uzasadnionym miejscu). W produkcyjnym użyciu `requests` te rzeczy nie przeszkadzają.

Ale — i tu jest punkt — **gdybyś to był Ty i swoje repo**, te same sygnały to coś, co warto przejrzeć przed wysłaniem do klienta.

## Dlaczego to w ogóle napisałem

Bo większość projektów, które widzę, ma te same błędy — tylko nikt ich nie sprawdzał:

- `shell=True` z danymi od użytkownika
- sekrety w `.env`, które ktoś przypadkiem dodał do gita
- testy, które "są w repo", ale nigdy nie biegną w CI
- brak `lockfile` → u Ciebie działa, u klienta sypie

Project Doctor nie jest konkurentem dla SonarQube czy GitHub Actions. To **gotowy raport w ludzkim języku** dla kogoś, kto chce wiedzieć *co poprawić*, a nie chce konfigurować pipeline.

## Zobacz pełny raport

Cały audyt `requests` (same wyniki, bez kodu):  
👉 https://github.com/famatyyk/project-doctor-samples/blob/main/samples/requests-audit.md

## Chcesz taki audyt dla swojego repo?

🚀 **Zamów: https://ctoai-funnel.fly.dev/**

- **Od 19 EUR**
- Raport Markdown + JSON w 24–48h
- Wynik Project Health 0–100, priorytety naprawy, przegląd testów/CI/sekretów, 5 kroków naprawczych

*Project Doctor nie uruchamia Twojego kodu, nie instaluje zależności i nie czyta plików z nazwami sugerującymi sekrety. Audyt jest w 100% statyczny.*

---

*Znalazłeś w tym poście coś nieścisłego? Napisz w komentarzach — poprawię. (I tak audytuję własne repo narzędzia 😅)*
