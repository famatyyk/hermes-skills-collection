# Krótkie posty na inne subreddity (zamiast X/Twitter)

Każdy pod inny sub — żeby nie dublować SideProject. Wklejaj po 1/dzień.

---

## r/PythonProjects2
Tytuł: Made a static audit tool for Python repos — ran it on requests for a sanity check
Treść:
Built Project Doctor — a static scanner for Python/AI repos (structure, tests, CI,
secrets, code risks like pickle/shell=True/HTTP-without-TLS). It doesn't run code
or install deps.

Ran it on `psf/requests` just to test it works. Got 18/100 — mostly because of
pickle usage, potential credential files, and HTTP-without-TLS in tests/examples.

Not a dig at requests (it's great) — just showing what the tool flags. Full
report (results only, no code): https://github.com/famatyyk/project-doctor-samples

If you want an audit of your own repo: https://ctoai-funnel.fly.dev/ (from 19 EUR)

---

## r/learnpython
Tytuł: What static analysis catches in your Python project (I audited requests as a test)
Treść:
Learning Python? Here's something useful: a *static* audit (no running code) of a
repo shows common mistakes even experienced devs make:

- shell=True with user input
- secrets in .env that got committed
- "tests exist" but never run in CI
- no lockfile (works for you, breaks for the client)

I ran a small tool on `requests` as a test — 18/100, mostly from test/example code.
Full report: https://github.com/famatyyk/project-doctor-samples

The tool is paid as a service (from 19 EUR) but the sample shows exactly what it checks.

---

## r/opensource
Tytuł: Audited requests as a smoke test for my static repo scanner — lessons for OSS hygiene
Treść:
Maintaining OSS? A static audit of your repo catches things before contributors
or users do:

- missing CI workflow
- no dependency lockfile
- credential-looking filenames
- HTTP endpoints without TLS

I ran my scanner (Project Doctor) on `psf/requests` — 18/100, almost all from
tests/examples, not production. Point is: the *checklist* matters for every OSS repo.

Sample report: https://github.com/famatyyk/project-doctor-samples
Audit your repo: https://ctoai-funnel.fly.dev/ (from 19 EUR)
