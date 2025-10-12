
# Dokumentace – Klinika cirkadiánní medicíny (studentský projekt)

*Datum:* 2025-10-12  
*Autoři:* Jméno 1, Jméno 2, Jméno 3, Jméno 4  
*Poznámka:* Všechny texty a obrázky jsou generované AI. Patička to zřetelně uvádí.

---

## 1. Specifikace webu

### 1.1 Představení řešeného webu
- **Název:** Klinika cirkadiánní medicíny
- **Popis:** Specializované pracoviště pro spánek, světelnou hygienu, chronoterapii (načasování léčby), programy pro směnný provoz a jet‑lag.
- **Cílové skupiny:** 
  - Pacienti s poruchami spánku a bdělosti
  - Pracující na směny (zdravotníci, hasiči, IT)
  - Cestovatelé (jet‑lag)
  - Pacienti s migrénou a dalšími stavy citlivými na cirkadiánní rytmy
- **Cíl webu:** Umožnit informovanou volbu vyšetření/programu a pohodlnou on‑line rezervaci.

### 1.2 Struktura a stručný popis stránek
- **Homepage (index.html):** Hrdinský přehled služeb (CSS Grid ≥ 8 prvků, 2 prvky přes více buněk), novinky, CTA.
- **Seznam vyšetření (seznam.html):** Karty vyšetření/programů (Flexbox), odkazy na detail.
- **Detail vyšetření (detail.html):** Obsah + sticky aside (cena, doba, CTA), tabulka termínů, použití `article`, `section`, `aside`, `time`, `table`.
- **Rezervace (rezervace.html):** Vícekrokový formulář (fieldset/legend), přístupné popisky.
- **Kontakt (kontakt.html):** Adresa, otevírací doba (tabulka s `time`), mapa, dopravní info.
- **Navigace:** Hlavní menu + vyhledávací box na všech stránkách, drobečková navigace.

### 1.3 Požadavky na implementaci
- Mobile‑first, responzivně.  
- Semantické elementy: `article`, `section`, `header`, `footer`, `aside`, `time`, `table`, `p`, `img`, `h1`–`h3`.  
- Bez frameworků. 1× vlastní `style.css` (> 400 řádků, proměnné, Grid, Flexbox).  
- Přístupnost: kontrasty, focus styly, `sr-only`, popisky formulářů, WCAG 2.1 AA snaha.  
- Vždy relativní adresace.

### 1.4 Návrh technologií (frontend + backend)
- **Frontend:** HTML5 + CSS3, bez JS (pro ukázku). Lze rozšířit o JS validaci a ARIA live‑regiony.
- **Backend (doporučení):** Statická verze pro odevzdání. Případné rozšíření: Node/Express, Python/Flask nebo PHP pro zpracování rezervací.
- **Zdůvodnění:** Pro účely kurzu postačí statika; případný backend by obsloužil kalendáře, e‑maily a přihlášení.

### 1.5 Nasazení – hosting, údržba, analytika, marketing, kontinuální UX
- **Hosting:** GitHub Pages / Netlify (snadné CI/CD).  
- **Údržba:** Semver pro verze; pull requesty a code review.  
- **Analytika:** Plausible / Matomo (privacy‑friendly).  
- **Marketing:** SEO základ (title, description), strukturovaná data `Organization`, `LocalBusiness`.  
- **UX výzkum:** Jednoduché testy s 5 uživateli, sledování vyhledávání, heatmapy (pokud eticky v pořádku).

---

## 2. Metodika projektu

### 2.1 Postup
1. **Research & UX cíl** → definice person (pacient na směny, cestovatel, migrenik).
2. **Informační architektura** → mapy stránek, názvosloví.
3. **Klikatelný prototyp (Hi‑Fi)** → Figma/Axure, mobil/desktop.
4. **UI Kit / Design tokens** → barvy, typografie, komponenty.
5. **HTML + CSS** → mobile‑first, přístupnost.
6. **Interní testování** → checklist WCAG, validátor W3C.
7. **Odevzdání** → ZIP se strukturou (viz níže).

### 2.2 Software, nástroje, IDE
- VS Code, Axure/Figma, W3C validator, kontrastní nástroje (TPGi).

### 2.3 Využití AI nástrojů
- **Texty:** prompt „Napiš srozumitelný popis světelné terapie pro veřejnost, 120–150 slov, věcně, bez diagnóz.“
- **Obrázky:** prompt „Isometrická ilustrace: moderní světelná terapie v klinice, jemné světlo svítání, čisté linie, plochý vektor.“
- **UX content:** prompt „Navrhni mikrotexty pro tlačítka a prázdné stavy v češtině.“
- **Kritické zhodnocení:** AI zrychluje obsah, nutná kontrola faktů a jazyková korektura.

---

## 3. Splnění požadavků (mapování)
- **Téma poskytovatele zdravotních služeb:** Ano – klinika cirkadiánní medicíny.
- **Stránky povinné:** Homepage, Seznam, Detail, Výsledky vyhledávání, Kontakt, Rezervace – vše přítomno.
- **Vyhledávání:** Box ve všech stránkách; ukázkové výsledky existují.
- **Rezervace:** Kompletní proces (demonstrace kroků).
- **Patička:** Rozšířená + autoři + poznámka „studentský projekt“.
- **Klikatelný prototyp:** V této verzi nahrazeno funkční statikou; prototyp lze vytvořit v Axure a exportovat do složky `Prototyp`.
- **HTML5 + CSS:** 1× `style.css` (> 400 řádků), Grid (≥ 8 prvků, 2× span), Flexbox, proměnné.
- **Přístupnost:** WCAG‑friendly styly, `sr-only`, focus, kontrasty.
- **Relativní adresy:** Ano (vše lokální).

---

## 4. Odevzdání (ZIP struktura)

```
CircadianClinicProject/
├─ Web/
│  ├─ index.html
│  ├─ seznam.html
│  ├─ detail.html
│  ├─ rezervace.html
│  ├─ kontakt.html
│  ├─ style.css
│  └─ images/
│     ├─ logo.svg
│     └─ placeholder.svg
├─ Prototyp/
│  └─ README.txt (jak exportovat z Axure/Figma)
└─ dokumentace.md
```

---

## 5. Rozdělení práce (tým 3–4 osoby)
- **UX/IA (Osoba A):** sitemap, prototyp, flow rezervace, přístupnost.
- **UI/Frontend (Osoba B):** komponenty, Grid/Flexbox, responzivita.
- **Obsah/AI (Osoba C):** texty, ilustrace, kontrola konzistence.
- **QA/Deployment (Osoba D):** validace, WCAG checklist, ZIP, Moodle.

---

## 6. Plán konzultace (10 bodů)
- Připravte konkrétní otázky: „Je flow rezervace srozumitelný?“, „Je breadcrumb smysluplný?“, „Splňuje hrdinský Grid zadání?“
