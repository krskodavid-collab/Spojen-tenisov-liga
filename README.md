# Spojená tenisová liga 2026

Webová stránka pre správu amatérskej tenisovej ligy STL — sezóna 2026.

**22 hráčov · 3 ligy · 2 cykly + play-off**

## Súbory v priečinku

- `index.html` — celá stránka v jednom súbore
- `logo.svg` — hlavné logo
- `favicon.svg` — ikona do záložky prehliadača
- `propozicie.pdf` — *(nepovinné)* PDF s propozíciami

## Sezóna 2026 — rozdelenie hráčov

**1. liga (8 hráčov):** Ján Jakubík, Michal Krško, Stanislav Ursíny, Miroslav Mikula, Peter Ondoš, Ivan Krajíček, Andrej Procházka, Anton Kubáň

**2. liga (7 hráčov):** Lukáš Holeša, Ján Zuzík, Marek Meššo, Ján Lokaj, Ludevít Lalík, Dávid Krško, Martin Kočitý

**3. liga (7 hráčov):** Simona Špiriaková, Miroslav Ozimy, Daniel Lokaj, Lucia Papanová, Ľubomír Korista, Peter Ďuroška, Štefan Miksák

## Systém sezóny

- 2 cykly (každý hrá s každým v rámci svojej ligy)
- Hráči zostávajú v rovnakej lige cez celú sezónu
- Body z oboch cyklov sa kumulujú → určujú nasadenie do play-off
- Po skončení 2. cyklu → play-off vo všetkých 3 ligách

### Bodovanie podľa setov

| Výsledok | Víťaz | Porazený |
|---|---|---|
| 2:0 | **3 body** | 0 bodov |
| 2:1 | **2 body** | 1 bod |

### Play-off

- **8 hráčov (1. liga):** štvrťfinále (1v8, 4v5, 3v6, 2v7) → semifinále → finále
- **7 hráčov (2. a 3. liga):** 1. miesto má voľný lístok do semifinále, ŠF (4v5, 3v6, 2v7) → SF → finále
- Víťazi sa automaticky posúvajú do ďalších kôl

## Prihlásenie do administrácie

**Predvolené:** meno `admin` · heslo `stl2026`

Po prvom prihlásení choď do **Admin → Prihlasovacie údaje** a zmeň heslo
na vlastné. Bez prihlásenia môže každý stránku iba prezerať — výsledky
a zmeny môže robiť iba admin.

## Sekcie stránky

- **Tabuľky** — sezónny súčet alebo samostatne za cyklus
- **Rozpis** — zápasy cyklu rozdelené do kôl
- **Výsledky** — chronológia odohraných zápasov
- **Play-off** — bracket s automatickým posúvaním víťazov
- **Štatistiky** — čísla a lídri v 8 kategóriách
- **Propozície** — pravidlá ligy (text + voliteľný PDF)
- **Galéria** — fotky zo zápasov
- **Admin** — všetka správa (po prihlásení)

## Workflow počas sezóny

1. **Cyklus 1** prebieha → admin pridáva výsledky cez záložku **Rozpis**
2. Po dokončení cyklu 1 → admin v **Admin → Cykly a play-off** klikne **„Spustiť cyklus 2"**
3. **Cyklus 2** prebieha rovnako, hráči zostávajú vo svojich ligách
4. Po dokončení cyklu 2 → admin klikne **„🏆 Spustiť play-off"**
5. Bracket sa vygeneruje podľa sezónnej tabuľky (súčet bodov z oboch cyklov)
6. Admin pridáva výsledky play-off zápasov, víťazi sa posúvajú automaticky
7. Po finále stránka vyhlási víťaza zlatým prúžkom

---

## Aktualizácia stránky na GitHube

Keď ti pripravím novú verziu súboru `index.html` (alebo iných), nahraj ju takto:

1. Choď na svoj repozitár
2. Klikni **„Pridať súbor → Nahrať súbory"**
3. Pretiahni nový súbor → **Commit changes**
4. Počkaj 1–2 minúty — stránka sa automaticky aktualizuje

Súbory s rovnakým názvom GitHub automaticky prepíše. Stará verzia zostáva v histórii.

## Migrácia dát po update

Pri prvom otvorení novej verzie sa stará dátová štruktúra (z minulých
verzií) automaticky upgraduje. Ak boli v databáze ešte staré demo mená
(Adam Kováč atď.), automaticky sa nahradia novým STL 2026 zoznamom.

**Ak chceš resetnúť na čistý štart STL 2026:**
Admin → Dáta → **Vynulovať všetko (STL 2026)**

## Zálohovanie

Pred každou väčšou zmenou (ukončenie cyklu, spustenie play-off):
**Admin → Dáta → ⬇ Export JSON**

Záloha obsahuje hráčov, výsledky, propozície, fotky a play-off bracket.
V prípade problému ju vieš znovu nahrať cez **Import JSON**.

## Tipy

- **Tabuľky** — vpravo hore tlačidlo prepína medzi „sezónny súčet" a samostatné cykly
- **Rozpis** — od cyklu 2 sa zobrazí prepínač cyklu 1/2
- **Play-off** — pri 7 hráčoch má 1. miesto voľný lístok (zobrazí sa rovno v semifinále)
- Fotky sa pri nahraní automaticky zmenšia (max šírka 1400px)
- Termín cyklu sa zobrazuje v hlavičke; 7 dní pred koncom oranžovo, po termíne červeno
