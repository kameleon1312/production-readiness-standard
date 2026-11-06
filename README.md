# Production Readiness & Security Standard

Uniwersalny, technologicznie neutralny standard audytowy do sprawdzania, czy **strona internetowa, aplikacja webowa, SaaS, sklep internetowy lub system z panelem użytkownika** jest gotowy do publikacji i bezpiecznego utrzymania na produkcji.

Obejmuje: architekturę i jakość kodu, application security (OWASP Top 10:2025, ASVS 5.0), uwierzytelnianie i autoryzację, API, bazy danych (w tym Supabase i Firebase), infrastrukturę i nagłówki HTTP, frontend, wydajność (Core Web Vitals), testy, dostępność (WCAG 2.2, EAA), SEO, prywatność i prawo (RODO, PKE, prawo konsumenckie PL/UE), płatności (PCI DSS 4.0.1), upload plików, logowanie i reagowanie na incydenty, backup i DR, supply chain, PWA oraz checklisty dla Next.js, React + Vite, Node.js, Supabase, Firebase, Shopify i WordPress.

## Zawartość

Cały zestaw znajduje się w katalogu [`docs/`](docs/) — zacznij od [docs/README.md](docs/README.md).

| Dokument | Opis |
|---|---|
| [Master Checklist](docs/PRODUCTION-READINESS-MASTER-CHECKLIST.md) | 26 części, 526 punktów kontrolnych z ID, priorytety P0–P3, wymagania warunkowe, statusy i dowody |
| [Security Testing Playbook](docs/SECURITY-TESTING-PLAYBOOK.md) | Procedury testów i polecenia CLI z interpretacją wyników i ograniczeniami |
| [Go / No-Go](docs/PRODUCTION-RELEASE-GO-NO-GO.md) | Formularz decyzji o publikacji i akceptacji ryzyka |
| [Incident Response Plan](docs/INCIDENT-RESPONSE-PLAN.md) | Reagowanie na incydenty, w tym naruszenia ochrony danych |
| [Risk Register](docs/RISK-REGISTER-TEMPLATE.md) | Szablon rejestru ryzyk |
| [Audit Report](docs/AUDIT-REPORT-TEMPLATE.md) | Szablon raportu z audytu |
| [Maintenance Calendar](docs/PRODUCTION-MAINTENANCE-CALENDAR.md) | Obowiązki po publikacji |
| [Standards & References](docs/STANDARDS-AND-REFERENCES.md) | Wersje standardów, oficjalne źródła, status weryfikacji |

## Jak zastosować w projekcie

**Opcja A — kopia katalogu (najprościej):**

```bash
# w katalogu głównym projektu
git clone --depth 1 https://github.com/kameleon1312/production-readiness-standard /tmp/prs
mkdir -p docs/production-readiness
cp /tmp/prs/docs/*.md docs/production-readiness/
rm -rf /tmp/prs
```

**Opcja B — nowy projekt z szablonu:** jeżeli w ustawieniach tego repozytorium zaznaczono *Template repository*, użyj przycisku **Use this template** na GitHubie.

Następnie postępuj wg [docs/README.md](docs/README.md): wypełniane egzemplarze trzymaj w `docs/audit/<data>/`, nie modyfikuj szablonów.

> 🔒 Wypełnione audyty mogą opisywać niezałatane podatności — nie publikuj ich w repozytoriach publicznych.

## Wersjonowanie

Standard jest wersjonowany zgodnie z [SemVer](https://semver.org/lang/pl/) — zmiany opisuje [CHANGELOG.md](CHANGELOG.md). Wersja i data weryfikacji standardów znajdują się w nagłówku głównej checklisty. Przegląd standardu: co najmniej raz w roku oraz po wydaniu nowej wersji kluczowego standardu (OWASP, NIST, WCAG, PCI DSS).

## Zastrzeżenie

Dokumenty nie stanowią porady prawnej i nie zastępują profesjonalnego testu penetracyjnego, audytu prawnego ani audytu infrastruktury. Szczegóły: sekcja *Known Limitations & Audit Boundaries* w głównej checkliście.
