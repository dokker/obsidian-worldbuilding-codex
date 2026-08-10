---
type: meta
tags: [meta, konvenció]
---

# Stílus-útmutató — CODEX Codex vault

Ez a dokumentum a vault jegyzeteinek kötelező konvencióit rögzíti. Minden új vagy
frissített jegyzetnek ezt kell követnie. A vault az **igazság forrása** a CODEX világ
kánonjáról — amit ide leírunk, az a hivatkozási alap.

## 1. Mappastruktúra

| Mappa | Tartalom | `type` |
|---|---|---|
| `Atlas/Kontinensek` | földrészek, nagy szárazulatok | `helyszin` |
| `Atlas/Régiók` | országok, tartományok, tájegységek | `helyszin` |
| `Atlas/Települések` | városok, falvak, kolostorvárosok | `helyszin` |
| `Atlas/Helyszínek` | épület, POI, természeti képződmény | `helyszin` |
| `Népek-Kultúrák/Népek` | népek, fajok („Hatalmasságok") | `nep` |
| `Népek-Kultúrák/Kultúrák` | szokások, nyelvek, társadalmi rendek | `kultura` |
| `Vallás-Mágia/Vallások` | vallások, kultuszok, rendek | `vallas` |
| `Vallás-Mágia/Mágia` | mágiarendszerek, misztikus fogalmak | `magia` |
| `Frakciók` | Nemesi Házak, harciskolák, szervezetek | `frakcio` |
| `Szereplők` | nevezetes NJK-k, személyek | `szereplo` |
| `Történelem/Korszakok` | korok, birodalmak | `korszak` |
| `Történelem/Események` | datált események | `esemeny` |
| `Bestiárium` | lények, szörnyek, szellemlények | `leny` |
| `Fogalmak` | egyéb lore-fogalmak, terminusok | `fogalom` |

Nem tartalmi mappák (prefix `_` / `00-`): `_Sablonok`, `_Assets`, `_Meta`, valamint a
`00-Home.md` és a `_*-MOC.md` index-jegyzetek. A `.obsidian/` mappához **soha ne nyúlj**.

## 2. Frontmatter (properties) séma

Minden tartalmi jegyzet kötelező közös mezői:

```yaml
---
type: helyszin | nep | kultura | vallas | magia | frakcio | szereplo | esemeny | korszak | leny | fogalom
aliases: []                # alternatív nevek, OCR-változatok (kereséshez, linkeléshez)
tags: [codex]              # + hierarchikus tag, pl. atlas/regio, vallas/zorawa
status: csonk | vazlat | kesz
kanon: biztos | bizonytalan | kikovetkeztetett
forras: []                 # sorhivatkozás(ok): "full_codex.md#L1990-L2001"
ocr_bizonytalan: false     # true, ha a szöveg OCR-zaj miatt kétséges
kapcsolodo: []             # [[wikilinkek]] a kapcsolódó jegyzetekre
---
```

Típus-specifikus mezők (a közösek után, opcionálisak):
- **helyszin**: `kontinens`, `regio`, `szulo_hely` (magasabb szintű hely), `nepek`, `birodalom`
- **nep**: `elohely` (jellemző terület), `rokon_nepek`, `nyelv`
- **kultura**: `nep`, `regio`
- **vallas**: `pantheon`, `szenthely`, `rendek`
- **magia**: `forras` (isteni/misztikus/démoni), `iskola`
- **frakcio**: `tipus` (nemesi ház / harciskola / rend), `szekhely`, `vezeto`
- **szereplo**: `nep`, `frakcio`, `helyszin`, `allapot` (él/halott/ismeretlen), `cim`
- **esemeny**: `datum`, `korszak`, `helyszin`
- **korszak**: `kezdet`, `veg`
- **leny**: `elohely`, `veszelyesseg`
- **fogalom**: `kategoria`

## 3. Elnevezés

- A fájlnév a kanonikus magyar név, ékezetekkel és a világ speciális betűivel
  (pl. `Abrýss.md`, `Sárkánygerinc Hegység.md`, `Zorawa Miszticizmus.md`).
- Az OCR-variánsokat és rövidebb alakokat `aliases`-be tesszük, hogy a `[[linkelés]]`
  és a keresés megtalálja őket.

## 4. Linkelés

- Bőségesen linkelj `[[wikilink]]`-kel a törzsszövegben minden entitásra, amelynek van
  (vagy lehet) saját jegyzete. A még meg nem írt célpont (piros link) **elfogadott** —
  jelzi a jövőbeli teendőt.
- Kétirányú kapcsolatnál a `kapcsolodo` frontmatter-mezőbe is vedd fel a fontosabb linkeket.

## 5. Forráshivatkozás és kánon-bizalom

- Minden állítás mögött ott a `forras` sorhivatkozás a `source/full_codex.md`-be
  (`fájl#Lkezdet-Lvég`). A forrás sorai változhatnak — a hivatkozás tájékozódási pont,
  nem abszolút.
- `kanon`: `biztos` (a forrás egyértelműen kimondja), `bizonytalan` (OCR-zaj vagy
  homályos szöveg), `kikovetkeztetett` (mi vezettük le, nincs szó szerint a forrásban).
- OCR-zaj esetén `ocr_bizonytalan: true`, és a kétes szövegrész mellé `> [!warning] OCR`
  callout kerül.

## 6. Jegyzet-testtörzs ajánlott felépítése

```
# Cím
> [!info] Egymondatos összefoglaló

## Áttekintés
## Földrajz / Történet / Tanítások (típus szerint)
## Kapcsolatok
## Nyitott kérdések / OCR-bizonytalanságok
## Források
```
