# Hermes Skills Collection

Własna kolekcja skilli dla Hermes Agent, wyciągnięta i zweryfikowana z rejestru
[RA-Skills](https://github.com/Lord1Egypt/RA-Skills) (90k+ community skilli).

## Skąd to się wzięło

Przesiano registry.json (95k skilli) przez filtr: oficjalne (built-in/optional)
LUB kompletne (installCmd + sourceUrl + opis), posortowane po świeżości w git.
Każdy skill przeszedł **skan bezpieczeństwa** (brak subprocess/os.system/eval/
requests.post) przed wgraniem — same metadane i wiedza, bez obcego kodu
wykonywalnego.

## Instalacja

Skopiuj folder z `skills/` do:
```
C:\Users\<user>\AppData\Local\hermes\skills\<nazwa>\
```
Hermes automatycznie wykryje skill przez `skill_view(name="<nazwa>")`.

## Kategorie

- **cpp-*** — C++20/23 expert, code review, support library (AST/CMake/Unity), cheat sheet
- **lua-*** — Lua scripting
- **marketing-*** — leady, growth, promocja (100m-leads, marketing-promotion, growth-record)
- **github-*** — code review, auth, issues, codebase inspection

## Uwaga

Skille pochodzą z community rejestru ClawHub/skills.sh — traktuj jako inspirację
i wiedzę, nie jako audytowane kodem źródłem. Przed użyciem w produkcji przejrzyj
treść SKILL.md.
