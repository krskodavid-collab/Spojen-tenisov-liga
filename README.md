# Spojená tenisová liga

Webová stránka pre správu amatérskej tenisovej ligy s 3 divíziami (A/B/C),
automatickými tabuľkami, rozpisom zápasov, štatistikami, propozíciami a galériou.

## Súbory v priečinku

- `index.html` — celá stránka v jednom súbore (HTML + CSS + JS)
- `logo.svg` — hlavné logo
- `favicon.svg` — ikona do záložky prehliadača
- `propozicie.pdf` — *(nepovinné)* PDF s propozíciami, ktoré sa zobrazí na stránke

## Prihlásenie do administrácie

**Predvolené prihlasovacie údaje:**

- Meno: `admin`
- Heslo: `stl2026`

**Hneď po prvom prihlásení** v záložke **Admin → Prihlasovacie údaje** zmeň
heslo na vlastné. Heslo je uložené v prehliadači — funguje len pre bežných
návštevníkov, takže nezadávaj nič super tajné.

Bez prihlásenia môže každý stránku iba prezerať. **Pridať/zmeniť výsledok,
upravovať hráčov, nahrávať fotky alebo meniť propozície môže iba prihlásený admin.**

---

## Aktualizácia stránky na GitHube (po zmenách)

Keď ti pripravím novú verziu súboru `index.html` (alebo iných), nahraj ju takto:

1. Choď na svoj repozitár na GitHube
2. Klikni na súbor, ktorý chceš nahradiť (napr. `index.html`)
3. Vpravo hore klikni **ikonu ceruzky** (Upraviť) alebo **„Pridať súbor → Nahrať súbory"**
4. Pretiahni nový súbor a klikni **Commit changes**
5. Počkaj 1–2 minúty — stránka sa automaticky aktualizuje

**Dáta zostávajú zachované** (hráči, výsledky, fotky, propozície sú v
prehliadači). Pred väčšími zmenami si ich však pre istotu zálohuj cez
**Admin → Dáta → Export JSON**.

---

## Sekcie stránky

- **Tabuľky** — automaticky prepočítané poradie v každej divízii
- **Rozpis** — všetky zápasy cyklu rozdelené do kôl
- **Výsledky** — chronológia odohraných zápasov
- **Štatistiky** — celkové čísla + lídri kategórií (najviac výhier, najlepšia
  šnúra, najsuverénnejší, najurputnejší...)
- **Propozície** — pravidlá ligy (text + voliteľný PDF na stiahnutie)
- **Galéria** — fotky zo zápasov a udalostí
- **Admin** — správa všetkého (po prihlásení)

## Bodovanie podľa setov

| Výsledok | Víťaz | Porazený |
|---|---|---|
| 2:0 v setoch | **3 body** | 0 bodov |
| 2:1 v setoch | **2 body** | 1 bod |

Pri rovnosti bodov rozhoduje: vzájomný zápas → rozdiel setov → rozdiel gemov → abeceda.

## Postupy / pády po cykle

- **A** → poslední 2 padajú do B
- **B** → prví 2 postupujú do A, poslední 2 padajú do C
- **C** → prví 2 postupujú do B

---

## Ako pridať PDF propozícií

1. Pripravený PDF si pomenuj napr. `propozicie.pdf`
2. Nahraj ho na GitHub do toho istého priečinka ako `index.html`
3. V stránke **Propozície → admin** zadaj presný názov súboru (`propozicie.pdf`)
4. Klikni **Uložiť** — na stránke sa objaví karta s odkazom na PDF

## Zálohovanie

Pred každou väčšou zmenou (napr. ukončenie cyklu) si stiahni zálohu:
**Admin → Dáta → ⬇ Export JSON**

Záloha obsahuje aj fotky, propozície, hráčov a všetky výsledky.
V prípade problému ju vieš znovu nahrať cez **Import JSON**.

## Tipy

- Fotky sa pri nahraní automaticky zmenšia (max šírka 1400px), aby zaberali
  menej miesta. Limit prehliadača je cca 5–10 MB pre všetky fotky spolu.
- Termín cyklu sa zobrazuje v hlavičke aj v rozpise. 7 dní pred koncom sa
  zafarbí oranžovo, po termíne červeno.
- Stránka funguje aj na mobile — celá tabuľka sa zúži a niektoré stĺpce
  sa skryjú pre lepšiu čitateľnosť.
