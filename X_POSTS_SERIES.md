# Seria postów na X/Twitter — Project Doctor

Gotowe do wklejenia (załóż konto, wklejaj 1/dzień). Styl: wartość → CTA.
Link do funnela na końcu każdego: https://ctoai-funnel.fly.dev/

---

## POST 1 — Demo na znanym repo (hook: kontrowersja)
Zbudowałem narzędzie do audytu repo Python. Puściłem je na `requests`
(najpopularniejszą bibliotekę HTTP). Wynik: 18/100.

Co wykryło:
- HIGH: odczyt pickle
- HIGH: pliki mogące zawierać poświadczenia
- MEDIUM: adresy HTTP bez TLS (w testach/przykładach)
- brak lockfile, brak CI workflow

Zastrzeżenie: to NIE ocena requests. Biblioteka jest świetna.
Narzędzie pokazuje, co warto przejrzeć w TWOIM repo.

Pełny raport (same wyniki): https://github.com/famatyyk/project-doctor-samples

Chcesz taki audyt dla swojego projektu? Od 19 EUR → https://ctoai-funnel.fly.dev/

---

## POST 2 — Edukacja: 5 rzeczy, które narzędzie wyłapało w moim repo
Robiłem audyty 3 projektów Python/AI. Najczęstsze błędy:

1. Brak lockfile (rzeczy działają u Ciebie, sypią u klienta)
2. Testy nie uruchamiane w CI (tylko "są pliki")
3. print() zamiast loggera
4. sekrety w .env commited (nawet puste!)
5. shell=True z danymi od użytkownika

Każdy z tego miał coś. Audyt statyczny wyłapuje to w 2 minuty.

Taki raport dla Ciebie: https://ctoai-funnel.fly.dev/ (od 19 EUR)

---

## POST 3 — Story: "zbudowałem produkt z błędem, którego nie widziałem"
Miałem repo z `subprocess + shell=True`. Działało. Aż klient
zapytał "czy to bezpieczne?". Audyt pokazał: NIE.

Naprawiłem na listę argumentów, dodałem testy, CI.
Teraz mam raport 89/100 zamiast 45/100.

Narzędzie, które mi to pokazało: Project Doctor.
Audyt Twojego repo: https://ctoai-funnel.fly.dev/ (od 19 EUR)

---

## POST 4 — Kontrowersyjne: "Darmowe skanery vs mój audyt"
SonarQube? GitHub Actions? Świetne narzędzia. Ale:
- wymagają konfiguracji pipeline'u
- dają 500 problemów bez priorytetu
- Ty musisz wiedzieć, co naprawić

Project Doctor = gotowy raport w ludzkim języku:
"zrób to, to, to — w tej kolejności".

Dla kogoś kto chce wiedzieć "co poprawić" bez zabawy w CI:
https://ctoai-funnel.fly.dev/ (od 19 EUR)

---

## POST 5 — Lead magnet: darmowy mini-audyt (engaged leads!)
Daję darmowy mini-audyt 3 pierwszym osobom, które:
1. założą repo na GitHubie
2. wkleją link w odpowiedzi
3. napiszą "audyt"

Wygeneruję raport i pokażę publicznie, co wykryłem.
( Potem możesz zamówić pełny za 19 EUR, ale mini jest gratis )

Formularz pełnego audytu: https://ctoai-funnel.fly.dev/

---

# Zasady publikacji (z $100M Leads):
- 1 post / dzień (volume beats perfection)
- każdy = wartość, nie reklama
- CTA tylko na końcu
- jak ktoś odpisze → odpowiedz pomocnie (to engaged lead)
