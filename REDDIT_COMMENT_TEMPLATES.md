# Szablony komentarzy na Reddit (aktywny zasięg, bez spamu)

Zasada: dajesz wartość → miękkie CTA na końcu. Nie wklejaj tego samego
wszędzie (Reddit to wykrywa). Dobierz szablon do posta.

Linki do wklejenia:
- Sample (requests 18/100): https://github.com/famatyyk/project-doctor-samples
- Funnel (audyt 19 EUR): https://ctoai-funnel.fly.dev/

---

## 1. Pod post "mam błąd w kodzie / nie działa"
Helpful, empatyczny:
> Had the same class of issue last month. Before debugging blind, I ran a
> static scan on my repo — turned out I had `shell=True` with untrusted input
> plus a stray `.env` that almost got committed. Caught it in 2 min.
>
> If you want a free sanity check, here's what my tool flagged in `requests`
> as a test: https://github.com/famatyyk/project-doctor-samples
> (no code runs, just structure/tests/CI/secrets check)

## 2. Pod post "roast my repo / code review please"
Hook na sample:
> Quick tip from auditing repos: most "looks fine" projects fail on the same
> 3 things — no lockfile, tests that never run in CI, `except:` swallowing
> errors. I ran a static tool on `requests` as a smoke test, got 18/100
> (mostly test/example code, not production — requests is great).
> Full report: https://github.com/famatyyk/project-doctor-samples
> Happy to point your repo at the same checker if useful.

## 3. Pod post "how do I improve my Python / repo?"
Edukacja + CTA:
> Static checks catch ~80% of "why does this break for the client" issues:
> - no `lockfile` → works for you, breaks for them
> - tests exist but CI never runs them
> - `print()` instead of `logger`
> - secrets in `.env` that got committed
>
> I built a small tool that reports these as a prioritized list. Sample on
> `requests`: https://github.com/famatyyk/project-doctor-samples
> Full audit for your repo: https://ctoai-funnel.fly.dev/ (from 19 EUR)

## 4. Pod post o security / sekretach / .env
Bezpieczeństwo:
> Reminder that "I'll delete the .env before pushing" fails 100% of the time
> eventually. A static scan for credential-looking filenames + secret patterns
> catches it before the push. I added this to a tool I'm building — sample
> audit of `requests` here: https://github.com/famatyyk/project-doctor-samples
> (no code is read, just filenames + patterns)

## 5. Pod post "showcase mojego projektu"
Miękki, nie reklamowy:
> Nice project! One thing I'd check before showing clients: does your CI
> actually *run* the tests, or just have test files? I audit repos for exactly
> this — ran it on `requests` as a test (18/100, mostly test-code noise).
> Sample: https://github.com/famatyyk/project-doctor-samples

## 6. Czysta wartość (BEZ CTA — buduje karmę)
Tylko się dzielisz znaleziskiem:
> Ran a static analyzer on `requests` for fun — 18/100. The "findings" are
> almost all in tests/examples (pickle, http:// in tests, missing lockfile).
> Not a dig at requests, just interesting what a dumb scanner flags.
> Report if curious: https://github.com/famatyyk/project-doctor-samples

---

# Jak używać (żeby nie dostać bana):
- 1-2 komentarze dziennie, różne subreddity (r/Python, r/learnpython,
  r/PythonProjects2, r/SideProject, r/aws/r/devops jak pasuje)
- Nie wklejaj linku w KAŻDYM komentarzu — co 2-3 użyj szablonu 6 (bez CTA)
- Odpowiadaj na pytania w wątku normalnie (to buduje zasięg Twojego profilu)
- Jak ktoś pyta "jak zrobić audyt mojego?" → wtedy CTA do funnela
